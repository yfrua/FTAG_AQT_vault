# TODO
- [x] Check out the Common Ntuple Framework
	- From Teresa: toptoolkit-ntuples v14.0.0, TopCPToolkit v2.22.0, AthAnalysis 25.2.66
	- Use latest version: toptoolkit-ntuples v15.0.0 TopCPToolkit v2.23.0 AthAnalysis 25.2.74
- [ ] Get Teresa's unfiltered di-jet samples, [[DAOD list]].
	- [x] download one MC DAOD file for every JZx slice for all champaigns
		- mc23a, mc23d, mc23e.
	- [ ] data and trigger
		- data22, data23, data24
		- one file for each data taking year
	- [ ] separate data by pT #Question
		- do pT binning in fitting procedure?
		- separate into different files, instead of a whole?
- [ ] Study [[Ellen's presentations]] to understand which [[Event selection|event selection]] you want to apply.
	- [ ] locally make sure selection code works fine
	- selection will be adapted to the current recommendations.
	- investigate how low in pT the selection can be expanded to have maximum overlap with the Z+jets calibration.
- [ ] submit job to the Grid, produce a first set of nominal only ntuples.
- [ ] make control plot
- [ ] Do [[SV Mass Fitting Methodology|template fit]] on secondary mass distribution, get SF 
	- Use both direct tag and negative tag methods
	- [ ] calculate [[SF Uncertainty]]
- [ ] Study whether effect of the quark/gluon composition of the sample on the Scale Factor can be estimated.

# Resources
- repo for this vault: [github](https://github.com/yfrua/FTAG_AQT_vault)
- AQT jira (AFT-840): [[jira page]], [jira url](https://its.cern.ch/jira/browse/AFT-840)
- Common Ntuple Framework: [gitlab](https://gitlab.cern.ch/atlas-ftag-calibration/toptoolkit-ntuples) 
- TopCPToolkit documentation: [url](https://topcptoolkit.docs.cern.ch/latest/)

