# ATLAS FTAG light-jet calibration Resources

## Knowledge

- [ROOT RooFit manual](https://root.cern/manual/roofit/)
  Official RooFit guide. Use for: PDFs, `RooRealSumPdf`, `fitTo`, snapshots, workspaces, plotting.
- [HistFactory paper — CERN-OPEN-2012-016](https://cds.cern.ch/record/1376755)
  The HistFactory template: channels, samples, norm factors, stat-error gammas, constraint terms. Use for: understanding the workspace structure BuildWS produces.
- [ATLAS FTAG public results twiki](https://twiki.cern.ch/twiki/bin/view/AtlasPublic/FlavourTaggingPublicResults)
  Public flavor-tagging results and calibration notes. Use for: context on how this calibration fits into FTAG releases.
- Codebase primaries (highest trust for anything implementation-specific):
  `DoCalibration/src/{BuildWS,DoFit,DoResults,ProcessInputs}.cxx`, `DoCalibration/src/ModelTool.cxx`, `DoCalibration/inifiles/*.ini`.

## Wisdom (Communities)

- ATLAS FTAG internal working meetings / hypernews (via CERN account)
  Use for: physics decisions on what floats vs what's fixed (e.g. extending the delta method to the b SF), and calibration review conventions.

## Gaps

- No good public reference found yet for the negative-tag (Flip tagger) light-jet method conventions used by this code — in-code comments and the user's collaborators are the source of truth for now.
