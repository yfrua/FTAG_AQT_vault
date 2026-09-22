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
