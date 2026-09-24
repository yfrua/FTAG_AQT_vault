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

## 2. MC modelling uncertainty
Accounts for differences between MC generators in the  templates. Fits using Z+jets events simulated Sherpa and MadGraph+Py8 samples are  performed and the absolute difference between the two scale factors is used as an  uncertainty. (From now on we plan to use the difference between PowhegPy8 and Sherpa  instead).

## Nominal Tagger Uncertainty
### MC-based adjusted MC method
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
### Shower Modelling
- use Powheg + Herwig

## 3. Extrapolation Uncertainty 
- An extrapolation uncertainty is estimated to cover any differences between nominal and flip taggers.
	- $unc(\text{extrapolation})=1-\hat{SF}/SF$, where hat stands for flip-tagger.
- 5-8% for DL1 and 4-18% for DL1r (depending on the tagger and working point).

## 4. c-jet SF uncertainty
The c-jet SF is obtained from the calibration on ttbar events with  one lepton. The SF for the flipped taggers is fixed to SFc = 1+/-0.3. The estimate for the  charm SF uncertainty is derived by comparing the results obtained from the calibration  with the nominal configuration (SFc = 1) to the results obtained from calibrations that use  variations (SFc = 0.7 and SFc = 1.3) and use fixed NP for the MC statistics.

## 6. Fit MC uncertainty
Accounts for the impact of the statistical uncertainty of the fit  templates. The fit is performed with all NP let floating free (“nom”) and once with all NP  free except the NP for the MC statistics (“fixgamma”). The impact of the MC template  statistics ΔMCstat is obtained by comparing the uncertainties on the POI of both fits.
$$\Delta_{MC,stat} = \sqrt{\Delta^2_{Nom} - \Delta^2_{fixgamma}}$$

## 7. Fit data uncertainty
The effect of the data statistical uncertainties on the POI (SFl,i) is  evaluated by fixing all NPs except the POIs to their best-fit values. The resulting  uncertainties from that fit is an estimate of the uncertainty due to the limited statistics of  the data sample.

## 8. Impact parameter uncertainty
Accounts for mismodeling of the transverse (d0) and  longitudinal (z0) track impact parameters in the detector simulation. Systematic templates  are created with data-driven corrections via the adjusted MC method and these are used  to in a systematic fit with fixed MC statistical NPs (“fixgamma”). The difference in the  systematic and the nominal fit is taken as the impact parameter uncertainty.

# Systematic Uncertainty from NTuples

- At the ntuple-processing stage (`AnalyseNtuple/util/Process.cxx:5-7`), there are three preprocessor flags for reweighting-based systematics derived from ntuple generator weights:
	- `DO_WEIGHT_SYS = 1` — master switch (enabled)
	- `DO_PDF = 0` — PDF weight systematics (disabled)
	- `DO_QCD = 0` — QCD scale weight systematics (disabled)
So PDF (100 Hessian variations) and QCD (MUR/MUF/PS scales) ntuple-level systematics are both turned off.
- At the calibration stage (`DoCalibration/`), systematics are applied at the template level using pre-computed variation ROOT files from `mc_uncertainty_inputs/templates/`, not directly from ntuples. These are tracking systematics (`TRK_RES_D0Z0_MEAS, s4415, s4416, s4417`) derived from ttbar variation samples. The code also has generator, charm, BSF, and MC-efficiency systematics handled post-fit.
In short: all systematic uncertainties in use (tracking, generator alternative, charm/BSF, MC efficiency, flip extrapolation) are injected at the template/fit/post-fit levels, not read from ntuple event weights.

## List of Systematics
- data
```
NOSYS
JET_JERUnc_Noise_PreRec__1up
JET_JERUnc_Noise_PreRec__1down
JET_JER_DataVsMC_MC16__1up
JET_JER_DataVsMC_MC16__1down
JET_JER_EffectiveNP_1__1up
JET_JER_EffectiveNP_1__1down
JET_JER_EffectiveNP_10__1up
JET_JER_EffectiveNP_10__1down
JET_JER_EffectiveNP_11__1up
JET_JER_EffectiveNP_11__1down
JET_JER_EffectiveNP_12restTerm__1up
JET_JER_EffectiveNP_12restTerm__1down
JET_JER_EffectiveNP_2__1up
JET_JER_EffectiveNP_2__1down
JET_JER_EffectiveNP_3__1up
JET_JER_EffectiveNP_3__1down
JET_JER_EffectiveNP_4__1up
JET_JER_EffectiveNP_4__1down
JET_JER_EffectiveNP_5__1up
JET_JER_EffectiveNP_5__1down
JET_JER_EffectiveNP_6__1up
JET_JER_EffectiveNP_6__1down
JET_JER_EffectiveNP_7__1up
JET_JER_EffectiveNP_7__1down
JET_JER_EffectiveNP_8__1up
JET_JER_EffectiveNP_8__1down
JET_JER_EffectiveNP_9__1up
JET_JER_EffectiveNP_9__1down
```
- MC
```
NOSYS
JET_BJES_Response__1up
JET_BJES_Response__1down
JET_EffectiveNP_Detector1__1up
JET_EffectiveNP_Detector1__1down
JET_EffectiveNP_Detector2__1up
JET_EffectiveNP_Detector2__1down
JET_EffectiveNP_Mixed1__1up
JET_EffectiveNP_Mixed1__1down
JET_EffectiveNP_Mixed2__1up
JET_EffectiveNP_Mixed2__1down
JET_EffectiveNP_Mixed3__1up
JET_EffectiveNP_Mixed3__1down
JET_EffectiveNP_Modelling1__1up
JET_EffectiveNP_Modelling1__1down
JET_EffectiveNP_Modelling2__1up
JET_EffectiveNP_Modelling2__1down
JET_EffectiveNP_Modelling3__1up
JET_EffectiveNP_Modelling3__1down
JET_EffectiveNP_Modelling4__1up
JET_EffectiveNP_Modelling4__1down
JET_EffectiveNP_Statistical1__1up
JET_EffectiveNP_Statistical1__1down
JET_EffectiveNP_Statistical2__1up
JET_EffectiveNP_Statistical2__1down
JET_EffectiveNP_Statistical3__1up
JET_EffectiveNP_Statistical3__1down
JET_EffectiveNP_Statistical4__1up
JET_EffectiveNP_Statistical4__1down
JET_EffectiveNP_Statistical5__1up
JET_EffectiveNP_Statistical5__1down
JET_EffectiveNP_Statistical6__1up
JET_EffectiveNP_Statistical6__1down
JET_EtaIntercalibration_Modelling__1up
JET_EtaIntercalibration_Modelling__1down
JET_EtaIntercalibration_NonClosure_0p2_PreRec__1up
JET_EtaIntercalibration_NonClosure_0p2_PreRec__1down
JET_EtaIntercalibration_TotalStat__1up
JET_EtaIntercalibration_TotalStat__1down
JET_FCal_MC23_NonClosure_PreRec__1up
JET_FCal_MC23_NonClosure_PreRec__1down
JET_Flavor_Composition__1up
JET_Flavor_Composition__1down
JET_Flavor_Response__1up
JET_Flavor_Response__1down
JET_InSitu_NonClosure_PreRec__1up
JET_InSitu_NonClosure_PreRec__1down
JET_JERUnc_Noise_PreRec__1up
JET_JERUnc_Noise_PreRec__1down
JET_JERUnc_Noise_PreRec_PseudoData__1up
JET_JERUnc_Noise_PreRec_PseudoData__1down
JET_JER_DataVsMC_MC16__1up
JET_JER_DataVsMC_MC16__1down
JET_JER_DataVsMC_MC16_PseudoData__1up
JET_JER_DataVsMC_MC16_PseudoData__1down
JET_JER_EffectiveNP_1__1up
JET_JER_EffectiveNP_1__1down
JET_JER_EffectiveNP_10__1up
JET_JER_EffectiveNP_10__1down
JET_JER_EffectiveNP_10_PseudoData__1up
JET_JER_EffectiveNP_10_PseudoData__1down
JET_JER_EffectiveNP_11__1up
JET_JER_EffectiveNP_11__1down
JET_JER_EffectiveNP_11_PseudoData__1up
JET_JER_EffectiveNP_11_PseudoData__1down
JET_JER_EffectiveNP_12restTerm__1up
JET_JER_EffectiveNP_12restTerm__1down
JET_JER_EffectiveNP_12restTerm_PseudoData__1up
JET_JER_EffectiveNP_12restTerm_PseudoData__1down
JET_JER_EffectiveNP_1_PseudoData__1up
JET_JER_EffectiveNP_1_PseudoData__1down
JET_JER_EffectiveNP_2__1up
JET_JER_EffectiveNP_2__1down
JET_JER_EffectiveNP_2_PseudoData__1up
JET_JER_EffectiveNP_2_PseudoData__1down
JET_JER_EffectiveNP_3__1up
JET_JER_EffectiveNP_3__1down
JET_JER_EffectiveNP_3_PseudoData__1up
JET_JER_EffectiveNP_3_PseudoData__1down
JET_JER_EffectiveNP_4__1up
JET_JER_EffectiveNP_4__1down
JET_JER_EffectiveNP_4_PseudoData__1up
JET_JER_EffectiveNP_4_PseudoData__1down
JET_JER_EffectiveNP_5__1up
JET_JER_EffectiveNP_5__1down
JET_JER_EffectiveNP_5_PseudoData__1up
JET_JER_EffectiveNP_5_PseudoData__1down
JET_JER_EffectiveNP_6__1up
JET_JER_EffectiveNP_6__1down
JET_JER_EffectiveNP_6_PseudoData__1up
JET_JER_EffectiveNP_6_PseudoData__1down
JET_JER_EffectiveNP_7__1up
JET_JER_EffectiveNP_7__1down
JET_JER_EffectiveNP_7_PseudoData__1up
JET_JER_EffectiveNP_7_PseudoData__1down
JET_JER_EffectiveNP_8__1up
JET_JER_EffectiveNP_8__1down
JET_JER_EffectiveNP_8_PseudoData__1up
JET_JER_EffectiveNP_8_PseudoData__1down
JET_JER_EffectiveNP_9__1up
JET_JER_EffectiveNP_9__1down
JET_JER_EffectiveNP_9_PseudoData__1up
JET_JER_EffectiveNP_9_PseudoData__1down
JET_JESUnc_Noise_PreRec__1up
JET_JESUnc_Noise_PreRec__1down
JET_JESUnc_VertexingAlg_PreRec__1up
JET_JESUnc_VertexingAlg_PreRec__1down
JET_NNJvtEfficiency__1down
JET_NNJvtEfficiency__1up
JET_Pileup_OffsetMu__1up
JET_Pileup_OffsetMu__1down
JET_Pileup_OffsetNPV__1up
JET_Pileup_OffsetNPV__1down
JET_Pileup_PtTerm__1up
JET_Pileup_PtTerm__1down
JET_Pileup_RhoTopology__1up
JET_Pileup_RhoTopology__1down
JET_SingleParticle_HighPt__1up
JET_SingleParticle_HighPt__1down
```