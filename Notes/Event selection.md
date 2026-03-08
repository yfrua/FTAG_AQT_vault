# Current
- GRL
- Trigger
- Baseline Jvt Jet
	- At least two jets with pT > 20 GeV
	- Leading jet pT > 110 GeV
	- (not implemented) <= 1 b-tagged jet
	- (not implemented) jet cleaning
- No electrons or muons in event
- 
# In Ellen's case
- Recommended basic selection  
	- GRL: Select events only on the specified good runs list 
	- GOODCALO: Ensure that the LAr and Tile are working properly for the event (no noise bursts) 
	- PRIVTX: Ensure that at least one primary vertex exists in the event 
	- RECO_LEVEL: Allows to define a reco-level-only selection: particle-level events do not pass
- Leading jet pT > 110 GeV
- No electrons or muons in event
- select jets with $|\eta|<2.5$
- No subleading b-tagged jets
	- reduce the number of leading jets being truth b-jets since b-jets might be coming from gluon splitting

![[Pasted image 20260226181049.png|300]]