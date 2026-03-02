Feirui will derive the light jet mistag calibration of the taggers GN3PlowMuons or GN3EPCLV01 at high jet pT. The conventional light mistag calibration is done with the negative tag method on a Z+jets selection. However, this selection yields jets with a rapidity falling jet pT spectrum, calibrations can only be done for jets up to pT=300 GeV. A [[Ellen's presentations|previous AQP task]] applied for the first time the current light jet mistag calibration strategy on a high pT jet sample in Rel.21 using a di-jet selection. This calibration uses a similar strategy for the scale factor extraction but a different selection. 

For the training of the recent GN3 tagger, the light jet label is split in gluon, u/d quark and strange quark labels, though for analyses the calibration for light jets is provided only inclusively over gluons and light quarks. The separate training of the different light jet components might affect efficiencies and scale factors of the light jet mistag and the validity of the light mistag calibration needs to be checked for different selections and phase spaces.   
The previous di-jet calibration started from a jet pT=150 GeV and therefore has an overlapping range of 150 < pT < 300 GeV with the standard Z+jets light calibration. Consistency of scale factors between two selections with different gluon/quark composition (Z+jets, dijet) can be checked in this pT range.   
For the standard calibrations, the SFs for pT > 300 GeV are estimated using a MC-based extrapolation, by estimating the impact of different data-driven corrections on the SFs and MC modeling effects at high pT. The dijet light calibration will help to estimate whether the effects of quark/gluon composition are covered by the MC-based high-pT extrapolation.

- The existing light mistag calibration on dijet events in Rel.21 will be ported to **Rel.25** and the selection will be adapted to the current recommendations. Especially, it should be investigated ==how low in pT the selection can be expanded== to have maximum overlap with the Z+jets calibration
- The composition in quarks and gluons of the selected sample will be studied, as well the composition in $g\to bb$, $g\to cc$ which are counted as b- and c-jets, respectively, and which might have an impact on the calibration according to previous studies.
- ==Using both direct tag and negative tag methods==, light mistag efficiency scale factors will be extracted as a function of the jet pT and the uncertainties should be estimated, similarly to the standard light mistag calibration
- Compare the SFs obtained with 150 < pT < 300 GeV with those obtained with the standard Z+jets calibration **using Run3 data up to 2024**
- Study whether effect of the quark/gluon composition of the sample on the Scale Factor can be estimated.
- [if time allows] extend the calibration to the 2025 and 2026 datasets

Some additional responsibilities are found below:

- The project should be well documented via regular updates in meetings and (if applicable) in the central [ftag-docs](https://ftag.docs.cern.ch/) page. Documentation should be of sufficient detail and quality to replicate the studies.
- The qualifier should maintain this JIRA ticket with a list of links to presentations in FTAG meetings, and links to relevant code/documentation produced during the project. Please update this ticket any time you give a talk in a meeting, or otherwise every two weeks with short update on progress.
- The local supervisor will give an overview presenting the project, 4 months after the start date. This update will summarize the progress so far and any interventions that would be needed to make sure the goals are met.
- Please read the [ftag guidance](https://ftag.docs.cern.ch/getting_involved/aqp/) for new AQPs for additional guidance

Expected start date: 05.01.26  
Glance codes:  
Qualifying student:  [Feirui Ye](https://its.cern.ch/jira/secure/ViewProfile.jspa?name=fye)   
Technical supervisor(s): [Lorenzo Santi](https://its.cern.ch/jira/secure/ViewProfile.jspa?name=losanti)   
Local supervisor(s): [Yanwen Liu](https://its.cern.ch/jira/secure/ViewProfile.jspa?name=yliu)   
Tagging: [Valentina Vecchio](https://its.cern.ch/jira/secure/ViewProfile.jspa?name=vvecchio) [Angela Maria Burger](https://its.cern.ch/jira/secure/ViewProfile.jspa?name=anburger) [Martino Tanasini](https://its.cern.ch/jira/secure/ViewProfile.jspa?name=mtanasin) [Lorenzo Santi](https://its.cern.ch/jira/secure/ViewProfile.jspa?name=losanti)