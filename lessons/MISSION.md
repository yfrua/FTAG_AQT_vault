# Mission: ATLAS light-jet (dijet) flavor-tagging calibration pipeline

## Why
Working daily in the `light-jet-calib-dijet` codebase (C++/ROOT/RooFit under AnalysisBase 25.2.1). Goal: confidently modify, diagnose, and validate the calibration chain — knowing what every fit input, parameter, and plot element actually is — rather than treating it as a black box.

## Success looks like
- Can explain what any element of a DoFit post-fit plot is made of and spot pathological fits from the plots alone (e.g. runaway SFs, gamma pulls)
- Can trace any workspace object back to the code that created it (BuildWS → DoFit → DoResults) and predict the effect of changing it
- Can run and re-verify the full pipeline (Plot → ProcessInputs → BuildWS → DoFit → DoResults) after a change, and judge whether results are trustworthy

## Constraints
- Learning happens on the real codebase and real data (period ADE, GN2/GN3 taggers); no sandbox reproductions
- Production outputs must never be overwritten carelessly (unique NameString per fit)
- Physics-model changes (what floats, what's fixed) are the user's/FTAG's decision, not the agent's

## Out of scope
- Re-deriving the b-jet and c-jet calibrations themselves (they are inputs, read from CDI/files)
- Reimplementing FastFrames histogram production (external repo `fye/FTAG_ljetcali_FastFrames`)
- Formal statistics theory beyond what the pipeline uses (likelihoods, constraint terms)
