# ATLAS Light-Jet Calibration Glossary

Canonical language for this teaching workspace. Every lesson, reference, and learning record uses these terms. A term appears here only once the user has demonstrated they can use it correctly (see learning records).

## Fit model

**RooWorkspace**:
Self-contained ROOT container holding the complete statistical model: simultaneous PDF, observed data, parameters, and snapshots. One file per (PtBin × Tagger): `NegTagContWS.*.root`.
_Avoid_: root file, ws

**HistFactory model**:
Parametric template model built from MC shape templates whose normalizations are physics equations with constraint terms attached. The structure BuildWS produces.
_Avoid_: likelihood (it is one ingredient of the likelihood)

**RooSimultaneous (simPdf)**:
Top-level PDF spanning all tag-bin categories, sharing parameters across them.
_Avoid_: combined PDF

**Scale factor (SF)**:
Parameter of interest `SF_Neg_TagBin{2-6}_{l,c,b}` scaling the MC tagging efficiency so predicted yields match data per tag bin and flavor. _In this workspace, always name bin and flavor._
_Avoid_: calibration constant, correction factor

**MC efficiency (Eff_MC)**:
Fraction of pre-tag jets of a flavor landing in tag bin *i*, measured from MC and fixed during the fit.
_Avoid_: efficiency alone

**Flavor fraction (f_b, f_c)**:
Pre-tag b/c flavor composition entering every normalization equation; `f_l = 1 − f_c − f_b`. Floats in the fit (post-fit results insensitive to their init).
_Avoid_: purity

**Gamma (γ)**:
Per-bin MC-statistics nuisance parameter multiplying a template bin, Gaussian-constrained around 1. Its constraint width scales with per-bin MC statistics.
_Avoid_: MC uncertainty (that's its cause, not the parameter)

**Flat direction**:
Parameter combination that leaves the likelihood nearly unchanged, letting the minimizer wander (e.g. SF_b ↑ traded against γ ↓).
_Avoid_: degeneracy (reserved for exact invariance)

**Snapshot (NominalParamValues)**:
Stored pre-fit parameter vector used to reset the model to a defined state before each fit variation.

**SumW2**:
Sum of squared event weights stored alongside a weighted histogram; the correct error bar for weighted data. RooFit's `plotOn` loses it on HistFactory datasets, hence the explicit overwrite in DoFit.

## Plot elements

**Post-fit plot**:
The RooFit PDF re-evaluated bin-by-bin at post-fit parameter values — not a histogram readout.
_Avoid_: fit histogram

**Post-fit / pre-fit**:
Model evaluated at fitted vs initial parameter values. The pre-fit equals the raw MC templates only when initial values are physically correct.

**Stack**:
Sum of per-flavor components from `GetHistogram()`. **Plot-type dependent since 2026-09-28**: mSV plot passes `IntegralNorm = true` — per-bin γ-**included** integral × coef; TagBin plot keeps the default renormalized shape × coef, which **strips** γ.
_Avoid_: total

**Fit-result line (red)**:
Plot-type dependent. mSV plot: `GetTotal(..., true)` — sum of the same γ-included components as the stack, so it hugs the stack top **by construction**. TagBin plot: `GetYieldTotal()` — γ-included full-PDF integral; its gap to the γ-stripped stack is the γ pull.
_Avoid_: one definition for both plot types

**Fit band (grey)**:
γ-included per-bin PDF integral ± `getPropagatedError(FitRes)` in the mSV plot; since 2026-09-28 its center coincides with the red line. Never drawn in TagBin plots — the band histogram is cloned but never filled there.

**TagBin1 (complement bin)**:
Loosest quantile: yield = pre-tag total minus all tagged contributions, `N_Inc_Pretag × f × (1 − Σ Eff·SF)`. Makes the fit self-normalizing.
_Avoid_: loosest bin (ambiguous with TagBin2)

## Calibration scheme

**Delta method**:
Tightest-bin light SF is fixed during the fit, then reported afterwards as α × adjacent-bin SF (α = 1 here), inheriting all of the adjacent bin's uncertainties. The tightest bin is an extrapolation, not a measurement.

**Continuous / Continuous2D**:
Tagger quantile schemes. Continuous: 6 bins, TagBin6 light SF extrapolated. Continuous2D: b side extrapolates TagBin7 (α), c side TagBin4 (β).

**Negative-tag (Flip) calibration**:
Light-jet SF calibration using the negative tagger-weight sideband; workspace `NegTagContWS`, parameters `SF_Neg_*`. Method conventions live in code and FTAG internal notes (see [[RESOURCES]] Gaps).

**PCBT / PCFT**:
Pseudo-continuous b-tagging / c-tagging quantile schemes; CTight and BTight label the tightest c and b intervals in the 2D (PCFT) scheme, where the delta method applies.

## Conventions in this workspace

- "Stack" is plot-type dependent since 2026-09-28: γ-included (per-bin integral × coef, `IntegralNorm`) in mSV plots, γ-stripped (renormalized shape × coef) in TagBin plots. The TagBin stack-vs-red gap remains the γ-activity diagnostic.
- Example fits: GN2v01 Flip, period ADE (163 fb⁻¹), unless stated otherwise.
