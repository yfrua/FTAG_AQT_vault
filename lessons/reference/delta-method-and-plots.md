---
topic: Delta method wiring & DoFit plot element quick reference
status: active
prerequisites:
  - "[[0004-delta-method]]"
  - "[[0003-stack-vs-fit-result-mismatch]]"
---

# Reference: Delta Method Map & Plot Elements

Quick lookup for the extrapolation bin wiring and DoFit plot composition. Terminology follows [[GLOSSARY]].

## Delta method wiring (SF_*_l only)

| Scheme | Fixed in fit (alpha) | Reported as | Uncertainties from |
|---|---|---|---|
| Continuous (6 q.) | `SF_Neg_TagBin6_l` = 1 | SF6 = α·SF5 = SF(70–65%) | TagBin5 (all components) |
| Continuous2D, b side | `SF_Neg_TagBin7_l` = 1 | SF7 = α·SF6 = SF(70–65%) | TagBin6 |
| Continuous2D, c side | `SF_Neg_TagBin4_l` = 1 | SF4 = β·SF3 = SF(30–10%) | TagBin3 |

Fit-side: `DoFit.cxx` NP loop (`extrapolate_SF`). Result-side: `DoResults.cxx` (CentVal + uncertainty blocks). Only the light SF; b/c SFs follow `fixBSF`/fixed-at-1 logic.

> [!warning] Open gap
> The **b SF in the tightest bin still floats** (range [0, 10], unconstrained) — the runaway seen in [[0003-stack-vs-fit-result-mismatch]]. Extending the delta method to b is a physics decision (user/FTAG).

## DoFit plot elements

| Element | Built from | Parameters used |
|---|---|---|
| Stacked l/c/b fills | `GetHistogram()`: shape (renormalized) × coef | post-fit; gammas stripped |
| Red line | `GetTotal()` (mSV plot) / `GetYieldTotal()` (TagBin plot) | post-fit, gammas included |
| Grey band | `GetYieldTotalBin()`: integral + `getPropagatedError(FitRes)` | post-fit ± σ |
| Blue dashed | `GetTotalPrefit()` captured before the fit | pre-fit (= raw MC) |
| Data points | `obsData` + SumW2 errors from `ContNegTagInputs` | observed |

## Diagnostic flow: stack vs red line

```mermaid
flowchart TD
    A[Stack top ≠ red line] --> B{Data/Fit panel flat at 1.0?}
    B -- yes --> C[Gap = gamma pull<br>size of gap ≈ gamma activity]
    B -- yes, huge gap --> D[Check floated SFs against<br>physics priors e.g. SF_Neg_TagBin6_b]
    B -- no --> E[Plot bug or stale workspace<br>check post-fit values loaded]
    F[Prefit ≠ raw MC] --> G[Flavor fraction init wrong<br>fixed 2026-09-18, see LR 0003]
```

## Diagnostic shortcuts

- **Stack top ≠ red line** ⇒ gammas active in that category; size of gap = gamma pull.
- **Huge gap + Data/Fit flat at 1.0** ⇒ check floated SFs against physics priors (e.g. `SF_Neg_TagBin6_b`).
- **Fit status**: 0 = converged; 4 = error matrix not pos-def (can still be at the minimum); the retry loop re-fits up to 800×.
- **Prefit ≠ raw MC** ⇒ flavor fraction init wrong (see learning record 0003; fixed 2026-09-18).

> [!question]- Self-check: which two plot quantities differ only by gammas?
>
> > [!success]- Answer
> > The stack top (Σ coef, gammas stripped by renormalization) and the red line (gamma-included PDF integral). Identical when all γ = 1.

---
**Sources:** `DoCalibration/src/DoFit.cxx` (Plot, NP loop), `DoCalibration/src/ModelTool.cxx` (GetHistogram, GetTotal*), `DoCalibration/src/DoResults.cxx` (delta-method reporting).

Created 2026-09-18 · Converted to Obsidian Markdown 2026-09-23
