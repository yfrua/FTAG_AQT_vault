# List of all kinds of unc.
1. systematic unc.
2. MC modelling unc.
3. flip-to-nominal extrapolation unc.
4. c-jet SF unc.
5. fit unc.
	- Uncertainty obtained in the nominal fit.
6. (fit) MC stat. unc.
7. (fit) data stat. unc.
8. impact parameter uncertainty

# 2. MC modelling uncertainty
Accounts for differences between MC generators in the  templates. Fits using Z+jets events simulated Sherpa and MadGraph+Py8 samples are  performed and the absolute difference between the two scale factors is used as an  uncertainty. (From now on we plan to use the difference between PowhegPy8 and Sherpa  instead).

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

# 3. Extrapolation Uncertainty 
- An extrapolation uncertainty is estimated to cover any differences between nominal and flip taggers.
	- $unc(\text{extrapolation})=1-\hat{SF}/SF$, where hat stands for flip-tagger.
- 5-8% for DL1 and 4-18% for DL1r (depending on the tagger and working point).

# 4. c-jet SF uncertainty
The c-jet SF is obtained from the calibration on ttbar events with  one lepton. The SF for the flipped taggers is fixed to SFc = 1+/-0.3. The estimate for the  charm SF uncertainty is derived by comparing the results obtained from the calibration  with the nominal configuration (SFc = 1) to the results obtained from calibrations that use  variations (SFc = 0.7 and SFc = 1.3) and use fixed NP for the MC statistics.

# 6. Fit MC uncertainty
Accounts for the impact of the statistical uncertainty of the fit  templates. The fit is performed with all NP let floating free (“nom”) and once with all NP  free except the NP for the MC statistics (“fixgamma”). The impact of the MC template  statistics ΔMCstat is obtained by comparing the uncertainties on the POI of both fits.
$$\Delta_{MC,stat} = \sqrt{\Delta^2_{Nom} - \Delta^2_{fixgamma}}$$

# 7. Fit data uncertainty
The effect of the data statistical uncertainties on the POI (SFl,i) is  evaluated by fixing all NPs except the POIs to their best-fit values. The resulting  uncertainties from that fit is an estimate of the uncertainty due to the limited statistics of  the data sample.

# 8. Impact parameter uncertainty
Accounts for mismodeling of the transverse (d0) and  longitudinal (z0) track impact parameters in the detector simulation. Systematic templates  are created with data-driven corrections via the adjusted MC method and these are used  to in a systematic fit with fixed MC statistical NPs (“fixgamma”). The difference in the  systematic and the nominal fit is taken as the impact parameter uncertainty.