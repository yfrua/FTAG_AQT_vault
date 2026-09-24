# Prefit plot root cause: off-by-one flavor fraction init

Misconception corrected: the stale DoFit comment blamed the RooRealSumPdf coefficients, but the real cause of the broken prefit was `BuildWS.cxx` initializing f_c to the light fraction (at(1)) and f_b to the charm fraction (at(2)) — fixed to at(2)/at(3) on 2026-09-18, after which all 18 coefficients match raw MC templates to ~1e-5 and the prefit line was enabled.

**Evidence:** fix verified numerically (coefficient-vs-template match) and visually (PtBin4 prefit curve above postfit in SV bins, fit through data).

**Implications:** existing output dirs predate the fix — prefit curves there remain wrong; postfit results unaffected (f_c/f_b float). Physics-model decisions stay with the user/FTAG.
