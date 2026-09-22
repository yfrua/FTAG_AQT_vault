---
topic: Stack vs fit-result mismatch, (SF_b, gamma) flat direction
status: completed
prerequisites:
  - "[[0001-post-fit-plot-extraction]]"
  - "[[0002-workspace-contents]]"
---

# 0003 — When the Stack Doesn't Touch the Red Line

*A diagnostic story: post-fit stacks, gamma factors, and a scale factor that ran away.*

**Mission:** [[MISSION]] · **Prev:** [[0002-workspace-contents]] · **Next:** [[0004-delta-method]] · **Reference:** [[delta-method-and-plots]] · **Glossary:** [[GLOSSARY]]

---

## The observation

In a GN2-rebin fit (80–120 GeV, fit status 0 = converged), the TagBin plot showed the stacked fills up to **6× above** the red "Fit Result" line in the tightest quantile (65–0%) — yet the Data/Fit panel was flat at 1.0. How can the fit "succeed" while its own components disagree with it?

## Recap: what each element is made of

| Element | Formula |
|---|---|
| Stack component *i* | `GetHistogram()`: shape × coefᵢ, **renormalized** to unit integral |
| Stack top | Σᵢ coefᵢ — gammas **stripped** by the renormalization |
| Red line | `GetYieldTotal()`: Σᵢ coefᵢ × ∫funcᵢ — gammas **included** (they multiply the shapes) |
| Blue dashed | Same machinery at pre-fit parameter values |

**When all gammas = 1, stack top ≡ red line exactly.** Any gap is the fit's gamma pull. A *huge* gap means weakly-constrained gammas or something pathological in the coefficients themselves.

> [!warning] This recap is the **TagBin plot** wiring
> The mSV plot (`Plot()`) is wired differently: its red line is `GetTotal()` — the sum of the *same* gamma-stripped components as the stack (`DoFit.cxx:1205`), so red ≡ stack top there **by construction**. In mSV plots the gammas surface only in the grey band (`GetYieldTotalBin`, gamma-included, `DoFit.cxx:1135`) and the Data/Fit panel divides by the gamma-**stripped** total (`DoFit.cxx:1416`) — so in a pathological category the mSV panel goes empty (points at ≈0.17 fall below the 0.9–1.1 pad) while the TagBin panel stays flat at 1.0.

## The cast: coefᵢ, funcᵢ, shape, γ

All four live in one object: the category model `<Cat>_model`, a RooRealSumPdf over the three flavors, `<Cat>_model = Σᵢ coefᵢ · funcᵢ`, i ∈ {l, c, b}. ModelTool reads both lists straight from the workspace (`funcList()`, `coefList()`, `ModelTool.cxx:94–142`), and every DoFit log prints them. From the log, TagBin6:

| Ingredient | Workspace object | What it is |
|---|---|---|
| funcᵢ | RooProduct `l_Chan_TagBin6_shapes` = `l_Chan_TagBin6_Hist_alphanominal × mc_stat_Chan_TagBin6 × Chan_TagBin6_model_binWidth` | Flavor i's mSV shape as a function of mSV: nominal MC template × MC-stat factor × bin-width normalisation |
| γ | `gamma_stat_Chan_TagBin6_bin_{0,1,2}`, Gaussian-constrained around global observables `nom_gamma_stat_...` = 1 | Per (tag bin × mSV bin) MC-statistics multipliers, width = that bin's relative MC stat error. They sit inside `mc_stat_<Cat>`, which multiplies **all three flavors alike** |
| coefᵢ | RooProduct `b_Chan_TagBin6_scaleFactors` = `b_Chan_TagBin6_epsilon × N_TagBin6_b × Lumi` | Flavor i's expected yield in the category: efficiency × normalization equation (carries `Scale`, `f`, and the `SF_Neg_*` POIs). Pre-fit in TagBin6: l 1.8e7, c 1.6e7, b 1.4e8 |
| shape | — | funcᵢ **renormalized to unit integral** inside `GetHistogram()` (`ModelTool.cxx:209`), then scaled by coefᵢ |

Two consequences do all the work in this lesson:

**Renormalization strips any overall scale in funcᵢ — including the γ level.** Stack component *i* is `coefᵢ × funcᵢ(center_b) / Σ_b funcᵢ(center_b)`: the sum over mSV bins equals coefᵢ no matter what the gammas do — a global γ level, the bin-width factor, all cancel in the ratio. That is what "gammas stripped" means: ==the stack top is Σᵢ coefᵢ by construction; γ can only redistribute relative heights *between* mSV bins, never change a component's total.== The PDF-side quantities (`GetYieldTotal(Bin)`) integrate funcᵢ as-is, so they keep the γ level linearly — γ ≈ 0.17 drags them to 0.17× while Σᵢ coefᵢ stays put. The stack-vs-red gap *is* the γ pull, made visible.

**The runaway and the compensation live on opposite sides of the product.** `SF_Neg_TagBin6_b` enters only through coef_b (inside `N_TagBin6_b`); the gammas enter only through funcᵢ (inside `mc_stat`). (SF_b × 7.46, γ × 0.17) is a pure product trade — coef_b inflated while every func is crushed — a near-flat direction of the likelihood, and exactly the valley the minimizer settled into below.

> [!tip] Not all gammas float
> HistFactory keeps a γ floating only where the bin's relative MC stat error exceeds the configured threshold (`SetStatErrorConfig`, `BuildWS.cxx:432`; `ActivateStatError`, `BuildWS.cxx:472`). In this build only `gamma_stat_Chan_TagBin5/6_bin_*` appear in the fit's Nuisance Parameters (DoFit log) — the TagBins 1–4 gammas exist but are pinned at 1. A second, config-level reason the stack-vs-red gap can only light up in the tightest bins. `FitOption = "MC_STAT"` fixes even those (`DoFit.cxx:4,770`) — a built-in cross-check.

> [!question] γ is shared by all flavors (one `mc_stat` per category). What does γ ≈ 0.17 therefore do to (a) the stack top, (b) the TagBin red line, (c) the l:c:b composition *within* one mSV bin?
> Answer from memory first, then unfold to check.
>
> > [!success]- Answer
> > (a) Nothing — component totals stay Σᵢ coefᵢ. (b) Suppresses it ≈0.17×, since the integral keeps the γ level. (c) Nothing — γ_b multiplies l, c and b equally inside a bin, so the per-bin flavor composition is γ-invariant; only the relative weight of *different* mSV bins (SV bins vs no-SV) is distorted.

## The diagnosis, step by step

### 1. Decompose the two quantities

Open the workspace and the `FitResult.root` histograms (Scale, f_c, f_b, SFs), set post-fit values, compute both sums for the problem category:

```
sum(coef)          = 1.14e9   // what the stack shows
raw PDF integral   = 1.14e9   // with gammas = 1 (identical!)
data in category   = 1.98e8   // what the red line matches
```

The *coefficients themselves* overshoot data by 6×. The red line only matches because the fitted gammas crush the shape functions by ~0.17.

### 2. Find the guilty coefficient

Post-fit parameters show `SF_Neg_TagBin6_b = 7.46` — the b-jet SF in the tightest quantile floated to 7.5 (range [0, 10], no constraint). It alone explains the overshoot.

### 3. Recognize the flat direction

SF_b scales the whole b component in the category; gammas scale every component bin-by-bin. With b dominant, the pair (SF_b ↑, γ ↓) leaves the PDF almost unchanged: 7.46 × 0.17 ≈ 1.27 — the same net prediction as SF_b = 1.27 with γ = 1. The rebin's finer mSV binning lowers MC statistics per bin, which *widens* the gamma constraints and makes this valley cheap. The minimizer converged happily (status 0) — to a physically absurd corner.

### 4. Why the Data/Fit panel looked healthy

The panel divides data by the **red line** (gamma-included PDF). It checks the fit's prediction, never the raw stack.

## The fix direction

The delta method already fixes the *light* SF in the tightest bin (`SF_Neg_TagBin6_l`) — see [[0004-delta-method]]. The b SF in the same bin floats unconstrained, which is what ran away. Options:

1. Fix `SF_Neg_TagBin6_b` = 1 (extend delta-method logic to b)
2. Tighten the SF range from [0, 10] to a physical window
3. `fixBSF = true` — note: for Flip taggers no BSF file is read, so they'd be fixed at 1.0

## General lessons

- ==**Converged ≠ healthy.**== Status 0 means a stationary point, not the one you want. Check parameter values against physics priors.
- **Near-flat directions are the enemy.** Parameters multiplying the same bins (SF, γ) can trade off; constraint widths set the excursion scale.
- **Plot artifacts carry information.** The stack-vs-red gap is a free gamma-activity diagnostic; the flavor decomposition stays meaningful even when the absolute height doesn't.
- **Bin more ⇒ constrain less.** Rebinning improves shape resolution but thins per-bin MC statistics, loosening every gamma constraint.

## Check your understanding

> [!question] If the b component dominated the category *and* the gamma constraints were very tight (tiny MC stat errors), could the same runaway happen?
> Answer from memory first, then unfold to check.
>
> > [!success]- Answer
> > No. The gamma constraint Gaussian(1, σ) with tiny σ makes γ = 0.17 cost ~((1−0.17)/σ)²/2 — an enormous penalty. The flat direction only becomes attractive when the constraint is loose, i.e. when per-bin MC statistics are poor. That's why the rebin (thinner bins, fewer MC events per bin) unlocked it.

---

**Primary sources:** `DoCalibration/src/DoFit.cxx` (which parameters float), `DoCalibration/src/ModelTool.cxx` `GetHistogram` (the renormalization), `DoCalibration/src/DoResults.cxx` (how results recombine SFs). Background: [ROOT RooFit manual](https://root.cern/manual/roofit/).

*Ask follow-up questions to your agent — anything unclear, dig in together.*
