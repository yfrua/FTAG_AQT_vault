From "Systematic uncertainty on the negative tag method: update on the extrapolation uncertainty", "Calibration of the light-flavour jet mistagging efficiency of the b-tagging algorithms with Z+jets events using 139 \mathrmfb^-1 of ATLAS proton-proton collision data at \sqrts = 13 TeV"

# MC-based Adjusted MC method
- Data are replaced by MC with data-driven corrections applied.
- $SF = Eff(mistag)_{data} / Eff(mistag)_{MC}$, MC is here MC without any correction applied, data is the MC with corrections applied.
- Corrections applied:
	- Data-driven correction on d0/z0 track impact parameter
		- Impact parameters are smeared using maps from the tracking group.
	- Fake track rate variation
		- MC underestimates number of fake tracks in data, MC have fewer number of fake tracks than data.
		- Randomly, drop 10% of fake tracks
		- Dropping tracks is workaround: cannot add tracks, so ==drop tracks and symmetrize SF around 1==
		- 