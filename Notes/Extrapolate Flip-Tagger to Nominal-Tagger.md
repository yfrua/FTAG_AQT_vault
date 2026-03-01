From "Systematic uncertainty on the negative tag method: update on the extrapolation uncertainty", "Calibration of the light-flavour jet mistagging efficiency of the b-tagging algorithms with Z+jets events using 139 \mathrmfb^-1 of ATLAS proton-proton collision data at \sqrts = 13 TeV"
# Nominal Tagger Uncertainty
## MC-based adjusted MC method
- Data are replaced by MC with data-driven corrections applied.
- $SF =\epsilon(mistag)_{data} / \epsilon(mistag)_{MC}$, 
	- MC is here MC without any correction applied, 
	- data is the MC with corrections applied.
	- use Powheg+Pythia8 generator
- Corrections applied:
	- Data-driven correction on d0/z0 track impact parameter
		- Impact parameters are smeared using maps from the tracking group.
	- Fake track rate variation
		- MC underestimates number of fake tracks in data, MC have fewer number of fake tracks than data.
		- Randomly, drop 10% of fake tracks
		- Dropping tracks is workaround: cannot add tracks, so ==drop tracks and symmetrize SF around 1==
## Shower Modelling
- use Powheg + Herwig

# Extrapolation Uncertainty 
- An extrapolation uncertainty is estimated to cover any differences between nominal and flip taggers.
	- $unc(\text{extrapolation})=1-\hat{SF}/SF$, where hat stands for flip-tagger.
- 5-8% for DL1 and 4-18% for DL1r (depending on the tagger and working point).