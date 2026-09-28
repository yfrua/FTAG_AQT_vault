# mSV stack switched to γ-included (`IntegralNorm`)

The user approved changing the plots so stacks and the red "Fit Result" lines are γ-**included**: `ModelTool::GetHistogram`/`GetTotal` gained `const bool IntegralNorm = false` (`ModelTool.h:51,53`). When true, `GetHistogram` builds each component from a per-bin `createIntegral` (named ranges `Range_<HistName>_<CompName>_<n>`) instead of center-evaluation + renormalization, so the γ level survives; both paths end with `Scale(coef)`. The mSV plot passes `true` (`DoFit.cxx:1205,1225`); the same day the user also opted the **TagBin summary plot in** (`DoFit.cxx:1609`), so ==every stack is now γ-included and the stack-vs-red γ diagnostic is retired in both plot types==.

Verified on GN2_rebin period ADE (163 fb⁻¹): TagBin6 mSV plots for PtBin2 (80–120 GeV — the original 6×-overshoot case) and PtBin4 (200–300 GeV) now show stack = red = data with Data/Fit ≈ 1.0 in all three mSV bins, and the band center on the red line. TagBin summary plot unchanged.

**Evidence:** requested after understanding the two wirings in [[0003-stack-vs-fit-result-mismatch]]; verified by rerunning `run/run_do_fit.sh GN2_rebin` and inspecting the regenerated plots and `FitStatus.tex`.

**Implications:**
- With γ-included stacks everywhere, ==γ activity is no longer visible as a stack-vs-red gap==; it shows as prefit-dashed-vs-postfit differences and in fit uncertainties/pulls. The old diagnostic is one flag away (`IntegralNorm = false`).
- FitStatus.tex flags: `PtBin3_NOM` status 4 (fit failed to converge — pre-existing) and `PtBin2_CSF_UP` status 4; the many "FAILED ... PtBin: 2" lines in `logs/04_do_fit.log` belong to the non-Flip channel.
- `run/run_do_fit.sh` removes the old log before running — keep copies of logs worth comparing.
