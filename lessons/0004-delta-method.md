---
topic: Delta method — extrapolating the tightest-bin light SF
status: completed
prerequisites:
  - "[[0003-stack-vs-fit-result-mismatch]]"
---

# 0004 — The Delta Method: Extrapolating the Tightest-Bin SF

*Why the last quantile's scale factor is not fitted — and how it is produced anyway.*

**Mission:** [[MISSION]] · **Prev:** [[0003-stack-vs-fit-result-mismatch]] · **Reference:** [[delta-method-and-plots]] · **Glossary:** [[GLOSSARY]]

---

## The problem

In the negative-tag (Flip) calibration, light jets pile up in the *loosest* quantile bins. By the tightest quantile (65–0%) the sample is overwhelmingly b-jet dominated and the light-flavor contribution is vanishingly small. The fit has **essentially no sensitivity to the light SF there** — leaving it floating creates an unconstrained parameter and a flat direction for the minimizer (the light analogue of the pathology in [[0003-stack-vs-fit-result-mismatch]]).

**The idea:** don't fit the tightest-bin light SF. Fix it during the fit, then afterwards *define* it as the adjacent bin's SF: SF(tightest) = α · SF(adjacent), with α = 1. ==The tightest bin is an extrapolation, not a measurement.==

## Stage 1: in the fit (DoFit.cxx)

While configuring parameters before `fitTo()` (`DoFit.cxx:758-767`):

```cpp
bool extrapolate_SF = (deltaMethod &&
    (((ParName.Contains("SF_Neg_TagBin4_l") || ParName.Contains("SF_Neg_TagBin7_l"))
        && Tagger.Contains("Continuous2D"))) ||
    (ParName.Contains("SF_Neg_TagBin6_l") && Tagger.Contains("Continuous")
        && !Tagger.Contains("Continuous2D")));

if (extrapolate_SF) var->setConstant(kTRUE);
```

The tightest-bin **light** SF — the *alpha parameter* — is held at its initial value (1.0 for Flip fits). Note the guard `Contains("Continuous") && !Contains("Continuous2D")`: string matching is order-sensitive, so the 2D exclusion must come first.

## Stage 2: in the results (DoResults.cxx)

The reported central value for the tightest bin is reconstructed (`DoResults.cxx:621-657`):

```cpp
// SF6 = alpha*SF5
CentVal = h_Fit_NOM->GetBinContent(x)              // alpha (fixed = 1)
        * h_Result_Total[Key_Bin5]->GetBinContent(x); // fitted SF of adjacent bin
```

With α ≡ 1 the delta method reduces to **SF(65–0%) := SF(70–65%)**. The α parameterization is deliberate scaffolding: code comments mention a Gaussian-constrained floating α/"beta" as the general scheme, but here it is pinned to 1.

**Uncertainty propagation:** the tightest bin **inherits the adjacent bin's uncertainties** component by component (`DoResults.cxx:698-760`) — fit uncertainty, data stat, MC stat, and each systematic variation. The tightest bin never has an uncertainty of its own.

## Which bins, for which tagger

| Tagger scheme | Extrapolated bin (fixed in fit) | Source bin (measured) | Parameter |
|---|---|---|---|
| Continuous (6 quantiles, e.g. GN2v01Flip) | TagBin6 (65–0%) | TagBin5 (70–65%) | α |
| Continuous2D — b side | TagBin7 (65–0%) | TagBin6 (70–65%) | α |
| Continuous2D — c side | TagBin4 (10–0%) | TagBin3 (30–10%) | β |

Only the **light-flavor** SF (`_l`) is extrapolated in all cases.

## The gap this leaves open

The delta method protects the *light* SF in the tightest bin — but the **b SF in the same bin still floats** (range [0, 10], no constraint). In the GN2-rebin fit it drifted to 7.46 while per-bin gammas compensated at ≈0.17 — the near-flat (SF_b, γ) direction of [[0003-stack-vs-fit-result-mismatch]]. Extending the extrapolation logic to `SF_Neg_TagBin6_b` is the natural closure (a physics decision).

## Why "delta"?

The name refers to the bin-to-bin *difference* parameterization: rather than measuring each quantile's SF independently, the tightest bin is tied to its neighbor by a delta (here δ = 0, i.e. α = 1). It converts an unconstrained measurement into a constrained extrapolation — the standard FTAG treatment for the last PCBT/PCFT interval, where "CTight" and "BTight" label the tightest c and b intervals in the PCFT (2D) scheme.

## Check your understanding

> [!question] The reported SF for the 65–0% bin equals the 70–65% bin's SF, with identical uncertainties. What fit information is therefore *deliberately discarded* for that bin, and why is that the right call?
> Answer from memory first, then unfold to check.
>
> > [!success]- Answer
> > The fit's own (meaningless) estimate and error for that bin's light SF. Floating it would produce a value with a huge, likelihood-flat uncertainty — no measurement, just a direction the minimizer drifted. Discarding it in favour of the adjacent bin's measurement converts noise into a defined extrapolation, at the cost of assuming the SF varies smoothly (δ = 0) across the quantile boundary.

---

**Primary sources:** `DoCalibration/src/DoFit.cxx` lines 758–767 (fixing alpha), `DoCalibration/src/DoResults.cxx` lines 619–760 (central value + uncertainty inheritance). Background: [HistFactory paper (CERN-OPEN-2012-016)](https://cds.cern.ch/record/1376755).

*Ask follow-up questions to your agent — anything unclear, dig in together.*
