# Stack vs red line: the (SF_b, gamma) flat direction

Diagnosed a 6x stack-vs-fit-result gap in the tightest quantile of a GN2-rebin fit: `SF_Neg_TagBin6_b` floated to 7.46 while per-bin gammas compensated at ~0.17 (near-flat likelihood direction, made cheap by the rebin's thinner mSV bins). The user learned to separate the gamma-stripped stack from the gamma-included PDF integral, and that "status 0 + flat Data/Fit panel" does not preclude pathological coefficients.

**Evidence:** followed the numeric decomposition (Σcoef = 1.14e9 vs data 1.98e8) and connected it to the delta method's protection of the light SF only.

**Implications:** candidate remediations (fix SF_Neg_TagBin6_b, tighten SF range, fixBSF) are recorded but are physics decisions for the user/FTAG, not the agent.
