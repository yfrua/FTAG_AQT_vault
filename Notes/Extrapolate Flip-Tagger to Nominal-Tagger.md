From "Systematic uncertainty on the negative tag method: update on the extrapolation uncertainty"

- MC-based Adjusted MC method
	- Data are replaced by MC with data-driven corrections applied.
	- $SF = Eff(mistag)_{data} / Eff(mistag)_{MC}$, MC is here MC without any correction applied, data is the MC with corrections applied
- Corrections applied:
	- Data-driven correction on d0/z0 track impact parameter
		- Impact parameters are smeared using maps from the tracking group.
	- Fake track rate variation
		- MC underestimates number of fake tracks in data, MC have fewer number of fake tracks than data.
		- Randomly, drop 10% of fake tracks
		- Dropping tracks is workaround: cannot add tracks, so ==drop tracks and symmetrize SF around 1==
		- 