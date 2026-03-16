# Basic Info
- unprescaled trigger: [TWiki](https://twiki.cern.ch/twiki/bin/viewauth/Atlas/LowestUnprescaled#Triggers_in_2023)
- Run 3 trigger naming convention: [TWiki](https://twiki.cern.ch/twiki/bin/view/Atlas/TriggerNamingRun3)
- search for prescaled trigger: [COMA](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.html)
- ATLAS Luminosity Calculator: [lumicalc](https://atlas-lumicalc.cern.ch/), [tutorial](https://twiki.cern.ch/twiki/bin/view/AtlasComputing/CoolLumiCalcTutorial)
- why do we need trigger for event selection?
	- It is necessary for data taking
	- To make sure all selected events come from expected physics process.
- Luminosity stuff naming: [COMA help](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserLib/helpme.php?inname=Luminosity)
	- **LB**: Luminosity Block, about 1 minute of data taking, have ~100K events.
	- **Stable Lumi:** integrated luminosity over all Stable Beam LBs for the LB Range, Run, or Period (as indicated in the report).
	- **Ready Lumi:** integrated luminosity over all Stable Beam LBs when the ATLAS Ready flag was true.
	- **PS Corr Stable Lumi:** Prescale corrected integrated luminosity, which may be at the LB level or integrated over ranges of LBs, Runs, or Periods (or over all Runs in the user temporal selection).
	- **PS Corr Ready Lumi:** is the PS Corr Stable Lumi, but only during LB Ranges when the ATLAS Ready flag was true.
 
# Available triggers
- L1jJ trigger:
	- Small-R jets are denoted jJ and gJ, for gFEX and jFEX, respectively
		- FEX: Feature EXtractor
		- The jFEX is intended to receive high granularity data from the calorimeters (0.1×0.1 in η × φ for the central calorimeter, larger in the forward regions) and identify jets and large-area taus. It also calculates global variables like the total transverse energy and the missing transverse energy. [ref](https://cds.cern.ch/record/2289210/files/ATL-DAQ-PROC-2017-032.pdf)
	- by default, jJ jets are defined in |eta|<3.1
-  New naming for Calo items (w.r.t. Run 2)
![[Pasted image 20260313192534.png]]
- in the following table, 2nd column comes from COMA, 3rd comes from lumicalc with link to the calculation result.

## data22_13p6TeV
- Live fraction trigger: L1_EM22VHI
- unprescaled trigger total lumi
	- 75 bunches only
		- HLT_j175f_L1J50p31ETA49: [1,585.42 pb-1](https://atlas-lumicalc.cern.ch/results/cc5f47/result.html)
	- 75, 300 bunches
		- HLT_j420_L1J100: [14,647.2 pb-1](https://atlas-lumicalc.cern.ch/results/348ff0/result.html)
		- HLT_2j250c_j120c_ftf_presel2j180XXj80_L1J100: [14,647.2 pb-1](https://atlas-lumicalc.cern.ch/results/6a9550/result.html)
	- From 400 bunches:
		- HLT_j420_pf_ftf_preselj225_L1J100: 
		- HLT_2j250c_j120c_pf_ftf_presel2j180XXj80_L1J100: 

| trigger name                                                                                                                                                                                 | PS Corr Ready Lumi ($\text{nb}^{-1}$) | Total Lumi in GRL ($\text{nb}^{-1}$)                                    | ratio |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- | ----------------------------------------------------------------------- | ----- |
| [HLT_j45_L1J15](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j45_L1J15 "link to COMA Chain/Item Report for HLT_j45_L1J15")          | 442                                   | [11.327](https://atlas-lumicalc.cern.ch/results/4cc34/result.html)      | 39.0  |
| [HLT_j60_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j60_L1J20 "link to COMA Chain/Item Report for HLT_j60_L1J20")          | 4,882                                 | [2,911.19](https://atlas-lumicalc.cern.ch/results/a4b48c/result.html)   | 1.68  |
| [HLT_j85_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j85_L1J20 "link to COMA Chain/Item Report for HLT_j85_L1J20")          | 11,672                                | [6,245.94](https://atlas-lumicalc.cern.ch/results/eeaaa8/result.html)   | 1.87  |
| [HLT_j110_L1J30](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j110_L1J30 "link to COMA Chain/Item Report for HLT_j110_L1J30")       | 34,827                                | [18,667.1](https://atlas-lumicalc.cern.ch/results/1908f7/result.html)   | 1.86  |
| [HLT_j175_L1J50](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j175_L1J50 "link to COMA Chain/Item Report for HLT_j175_L1J50")       | 172,445                               | [104,402](https://atlas-lumicalc.cern.ch/results/83ce6c/result.html)    | 1.65  |
| [HLT_j260_L1J75](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j260_L1J75 "link to COMA Chain/Item Report for HLT_j260_L1J75")       | 1,154,264                             | [709,172](https://atlas-lumicalc.cern.ch/results/9ac815/result.html)    | 1.63  |
| [HLT_j360_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j360_L1J100 "link to COMA Chain/Item Report for HLT_j360_L1J100")    | 6,515,200                             | [4,525,930](https://atlas-lumicalc.cern.ch/results/5e4686/result.html)  | 1.44  |
| [HLT_j420_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1J100 "link to COMA Chain/Item Report for HLT_j420_L1J100")    | 21,543,778                            | [14,647,200](https://atlas-lumicalc.cern.ch/results/52fc64/result.html) | 1.47  |
| [HLT_j420_L1J120](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1J120 "link to COMA Chain/Item Report for HLT_j420_L1J120")    | 21,541,378                            | [14,647,200](https://atlas-lumicalc.cern.ch/results/ca62f4/result.html) | 1.47  |
| [HLT_j420_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1jJ160 "link to COMA Chain/Item Report for HLT_j420_L1jJ160") | 514,758                               | [244,434](https://atlas-lumicalc.cern.ch/results/ff6fce/result.html)    | 2.10  |
| [HLT_j440_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j440_L1J100 "link to COMA Chain/Item Report for HLT_j440_L1J100")    | 21,541,378                            | [14,647,200](https://atlas-lumicalc.cern.ch/results/7d5dd9/result.html) | 1.47  |
| [HLT_j450_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j450_L1J100 "link to COMA Chain/Item Report for HLT_j450_L1J100")    | 21,541,378                            | [14,647,200](https://atlas-lumicalc.cern.ch/results/49be5e/result.html) | 1.47  |
| [HLT_j460_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j460_L1J100 "link to COMA Chain/Item Report for HLT_j460_L1J100")    | 21,541,378                            | [14,647,200](https://atlas-lumicalc.cern.ch/results/ab030a/result.html) | 1.47  |
| [HLT_j480_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j480_L1J100 "link to COMA Chain/Item Report for HLT_j480_L1J100")    | 40,022,750                            | [29.294,400](https://atlas-lumicalc.cern.ch/results/988793/result.html) | 1.37  |
| [HLT_j500_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j500_L1J100 "link to COMA Chain/Item Report for HLT_j500_L1J100")    | 40,022,750                            | [29.294,400](https://atlas-lumicalc.cern.ch/results/8228d/result.html)  | 1.37  |
| [HLT_j520_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j520_L1J100 "link to COMA Chain/Item Report for HLT_j520_L1J100")    | 40,022,750                            | [29.294,400](https://atlas-lumicalc.cern.ch/results/634bdb/result.html) | 1.37  |
## data23_13p6TeV
- Live fraction trigger: L1_eEM26M
- unprescaled trigger total lumi
	- 75 bunches only
		- HLT_j175f_L1J50p31ETA49: [899.334 pb-1](https://atlas-lumicalc.cern.ch/results/3f5c03/result.html)
	- 75, 400 bunches
		- HLT_j420_L1J100: [13,323.6 pb-1](https://atlas-lumicalc.cern.ch/results/7c8a9e/result.html)
		- HLT_2j250c_j120c_ftf_presel2j180XXj80_L1J100: [13,323.6 pb-1](https://atlas-lumicalc.cern.ch/results/fcf2ba/result.html)
	- From 400 bunches
		- HLT_j420_pf_ftf_preselj225_L1J100: [26,647.1 pb-1](https://atlas-lumicalc.cern.ch/results/8395ca/result.html)
		- HLT_2j250c_j120c_pf_ftf_presel2j180XXj80_L1J100: [26,647.1 pb-1](https://atlas-lumicalc.cern.ch/results/91ec45/result.html)

| trigger name                                                                                                                                                                                 | PS Corr Ready Lumi ($\text{nb}^{-1}$) | Total Lumi in GRL ($\text{nb}^{-1}$)                                    | ratio |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- | ----------------------------------------------------------------------- | ----- |
| [HLT_j20_L1J12](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j20_L1J12 "link to COMA Chain/Item Report for HLT_j20_L1J12")          | 150                                   | [0](https://atlas-lumicalc.cern.ch/results/ba3821/result.html)          | \     |
| [HLT_j45_L1J15](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j45_L1J15 "link to COMA Chain/Item Report for HLT_j45_L1J15")          | 10.7                                  | [8.44288](https://atlas-lumicalc.cern.ch/results/6765c4/result.html)    | 1.27  |
| [HLT_j60_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j60_L1J20 "link to COMA Chain/Item Report for HLT_j60_L1J20")          | 439                                   | [376.265](https://atlas-lumicalc.cern.ch/results/c73534/result.html)    | 1.17  |
| [HLT_j85_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j85_L1J20 "link to COMA Chain/Item Report for HLT_j85_L1J20")          | 1,230                                 | [1,053.49](https://atlas-lumicalc.cern.ch/results/c13258/result.html)   | 1.17  |
| [HLT_j110_L1J30](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j110_L1J30 "link to COMA Chain/Item Report for HLT_j110_L1J30")       | 3,797                                 | [3,252.29](https://atlas-lumicalc.cern.ch/results/110405/result.html)   | 1.17  |
| [HLT_j175_L1J50](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j175_L1J50 "link to COMA Chain/Item Report for HLT_j175_L1J50")       | 29,310                                | [25,106.8](https://atlas-lumicalc.cern.ch/results/31dbd9/result.html)   | 1.17  |
| [HLT_j260_L1J75](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j260_L1J75 "link to COMA Chain/Item Report for HLT_j260_L1J75")       | 184,754                               | [158,262](https://atlas-lumicalc.cern.ch/results/3b28b5/result.html)    | 1.17  |
| [HLT_j360_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j360_L1J100 "link to COMA Chain/Item Report for HLT_j360_L1J100")    | 943,674                               | [808,378](https://atlas-lumicalc.cern.ch/results/7d0b78/result.html)    | 1.17  |
| [HLT_j420_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1J100 "link to COMA Chain/Item Report for HLT_j420_L1J100")    | 15,454,626                            | [13,323,600](https://atlas-lumicalc.cern.ch/results/bf3168/result.html) | 1.16  |
| [HLT_j420_L1J120](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1J120 "link to COMA Chain/Item Report for HLT_j420_L1J120")    | 15,454,626                            | [13,323,600](https://atlas-lumicalc.cern.ch/results/fc8180/result.html) | 1.16  |
| [HLT_j420_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1jJ160 "link to COMA Chain/Item Report for HLT_j420_L1jJ160") | 246,166                               | [227,509](https://atlas-lumicalc.cern.ch/results/4d079b/result.html)    | 1.08  |
| [HLT_j440_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j440_L1J100 "link to COMA Chain/Item Report for HLT_j440_L1J100")    | 15,454,626                            | [13,323,600](https://atlas-lumicalc.cern.ch/results/da8996/result.html) | 1.16  |
| [HLT_j450_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j450_L1J100 "link to COMA Chain/Item Report for HLT_j450_L1J100")    | 15,454,626                            | [13,323,600](https://atlas-lumicalc.cern.ch/results/a8c32d/result.html) | 1.16  |
| [HLT_j460_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j460_L1J100 "link to COMA Chain/Item Report for HLT_j460_L1J100")    | 15,454,626                            | [13,323,600](https://atlas-lumicalc.cern.ch/results/980a73/result.html) | 1.16  |
| [HLT_j480_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j480_L1J100 "link to COMA Chain/Item Report for HLT_j480_L1J100")    | 31,212,704                            | [26,647,100](https://atlas-lumicalc.cern.ch/results/85b17/result.html)  | 1.17  |
| [HLT_j500_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j500_L1J100 "link to COMA Chain/Item Report for HLT_j500_L1J100")    | 31,212,704                            | [26,647,100](https://atlas-lumicalc.cern.ch/results/556f6f/result.html) | 1.17  |
| [HLT_j520_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j520_L1J100 "link to COMA Chain/Item Report for HLT_j520_L1J100")    | 31,212,704                            | [26,647,100](https://atlas-lumicalc.cern.ch/results/556f6f/result.html) | 1.17  |

## data24_13p6TeV
- Live fraction trigger: L1_eEM26M
- unprescaled trigger total lumi
	- 75 bunches only
		- HLT_j175f_L1jJ90p30ETA49: [5,796.11 pb-1](https://atlas-lumicalc.cern.ch/results/2bbfa3/result.html)
	- 75, 400 bunches
		- HLT_j420_L1jJ160: [53,945.1 pb-1](https://atlas-lumicalc.cern.ch/results/7eef32/result.html)
		- HLT_2j250c_j120c_ftf_presel2j180XXj80_L1jJ160: [53,945.1 pb-1](https://atlas-lumicalc.cern.ch/results/5c3a6e/result.html)
	- From 400 bunches
		- HLT_j400_pf_ftf_preselj225_L1jJ160: [107,377.0 pb-1](https://atlas-lumicalc.cern.ch/results/cc42b8/result.html)
		- HLT_2j235c_j115c_pf_ftf_presel2j180XXj80_L1jJ160: [107,890.0 pb-1](https://atlas-lumicalc.cern.ch/results/c5432f/result.html)

| trigger name                                                                                                                                                                                 | PS Corr Ready Lumi ($\text{nb}^{-1}$) | Total Lumi in GRL ($\text{nb}^{-1}$)                                    | ratio |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- | ----------------------------------------------------------------------- | ----- |
| [HLT_j20_L1jJ20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j20_L1jJ20 "link to COMA Chain/Item Report for HLT_j20_L1jJ20")       | 1,943                                 | [0](https://atlas-lumicalc.cern.ch/results/42447c/result.html)          | \     |
| [HLT_j20_L1jJ30](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j20_L1jJ30 "link to COMA Chain/Item Report for HLT_j20_L1jJ30")       | 9.96                                  | [0](https://atlas-lumicalc.cern.ch/results/2b0f32/result.html)          | \     |
| [HLT_j45_L1J15](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j45_L1J15 "link to COMA Chain/Item Report for HLT_j45_L1J15")          | 62.9                                  | [17.7199](https://atlas-lumicalc.cern.ch/results/2e9227/result.html)    | 3.55  |
| [HLT_j60_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j60_L1J20 "link to COMA Chain/Item Report for HLT_j60_L1J20")          | 840                                   | [706.561](https://atlas-lumicalc.cern.ch/results/5de92d/result.html)    | 1.19  |
| [HLT_j60_L1jJ50](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j60_L1jJ50 "link to COMA Chain/Item Report for HLT_j60_L1jJ50")       | 1,558                                 | [1,348.92](https://atlas-lumicalc.cern.ch/results/983663/result.html)   | 1.15  |
| [HLT_j85_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j85_L1J20 "link to COMA Chain/Item Report for HLT_j85_L1J20")          | 2,339                                 | [1,966.06](https://atlas-lumicalc.cern.ch/results/337a88/result.html)   | 1.19  |
| [HLT_j85_L1jJ50](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j85_L1jJ50 "link to COMA Chain/Item Report for HLT_j85_L1jJ50")       | 4,292                                 | [3,708.03](https://atlas-lumicalc.cern.ch/results/d3053c/result.html)   | 1.16  |
| [HLT_j110_L1jJ60](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j110_L1jJ60 "link to COMA Chain/Item Report for HLT_j110_L1jJ60")    | 13,914                                | [12,091.9](https://atlas-lumicalc.cern.ch/results/fd1a48/result.html)   | 1.15  |
| [HLT_j175_L1J50](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j175_L1J50 "link to COMA Chain/Item Report for HLT_j175_L1J50")       | 55,135                                | [46,608.5](https://atlas-lumicalc.cern.ch/results/fa281f/result.html)   | 1.18  |
| [HLT_j175_L1jJ90](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j175_L1jJ90 "link to COMA Chain/Item Report for HLT_j175_L1jJ90")    | 101,780                               | [88,415](https://atlas-lumicalc.cern.ch/results/5f8f82/result.html)     | 1.15  |
| [HLT_j260_L1jJ125](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j260_L1jJ125 "link to COMA Chain/Item Report for HLT_j260_L1jJ125") | 641,623                               | [560,656](https://atlas-lumicalc.cern.ch/results/208da3/result.html)    | 1.14  |
| [HLT_j360_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j360_L1J100 "link to COMA Chain/Item Report for HLT_j360_L1J100")    | 799,906                               | [675,557](https://atlas-lumicalc.cern.ch/results/a854c8/result.html)    | 1.18  |
| [HLT_j360_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j360_L1jJ160 "link to COMA Chain/Item Report for HLT_j360_L1jJ160") | 3,222,432                             | [2,818,510](https://atlas-lumicalc.cern.ch/results/f0e6b/result.html)   | 1.14  |
| [HLT_j420_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1J100 "link to COMA Chain/Item Report for HLT_j420_L1J100")    | 12,616,139                            | [11,266,700](https://atlas-lumicalc.cern.ch/results/cc5e40/result.html) | 1.12  |
| [HLT_j420_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1jJ160 "link to COMA Chain/Item Report for HLT_j420_L1jJ160") | 60,828,012                            | [53,945,100](https://atlas-lumicalc.cern.ch/results/3438b0/result.html) | 1.13  |
| [HLT_j420_L1jJ180](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1jJ180 "link to COMA Chain/Item Report for HLT_j420_L1jJ180") | 60,792,306                            | [53,945,100](https://atlas-lumicalc.cern.ch/results/4435a5/result.html) | 1.13  |
| [HLT_j440_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j440_L1J100 "link to COMA Chain/Item Report for HLT_j440_L1J100")    | 12,616,139                            | [11,266,700](https://atlas-lumicalc.cern.ch/results/cc5e40/result.html) | 1.12  |
| [HLT_j440_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j440_L1jJ160 "link to COMA Chain/Item Report for HLT_j440_L1jJ160") | 60,792,305                            | [53,945,100](https://atlas-lumicalc.cern.ch/results/4435a5/result.html) | 1.13  |
| [HLT_j450_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j450_L1J100 "link to COMA Chain/Item Report for HLT_j450_L1J100")    | 12,616,139                            | [11,266,700](https://atlas-lumicalc.cern.ch/results/cc5e40/result.html) | 1.12  |
| [HLT_j450_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j450_L1jJ160 "link to COMA Chain/Item Report for HLT_j450_L1jJ160") | 60,792,305                            | [53,945,100](https://atlas-lumicalc.cern.ch/results/4435a5/result.html) | 1.13  |
| [HLT_j460_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j460_L1J100 "link to COMA Chain/Item Report for HLT_j460_L1J100")    | 12,616,139                            | [11,266,700](https://atlas-lumicalc.cern.ch/results/cc5e40/result.html) | 1.12  |
| [HLT_j460_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j460_L1jJ160 "link to COMA Chain/Item Report for HLT_j460_L1jJ160") | 60,792,305                            | [53,945,100](https://atlas-lumicalc.cern.ch/results/4435a5/result.html) | 1.13  |
| [HLT_j480_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j480_L1J100 "link to COMA Chain/Item Report for HLT_j480_L1J100")    | 25,232,278                            | [22,533,400](https://atlas-lumicalc.cern.ch/results/d0c0d2/result.html) | 1.12  |
| [HLT_j500_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j500_L1J100 "link to COMA Chain/Item Report for HLT_j500_L1J100")    | 25,232,278                            | [22,533,400](https://atlas-lumicalc.cern.ch/results/d0c0d2/result.html) | 1.12  |

# Leading jet pT binning and triggers
#TODO Find trigger efficiency plots?
## trigger

| bin | pT range [GeV] | 2022            | 2023            | 2024             |
| --- | -------------- | --------------- | --------------- | ---------------- |
| 1   | 50 - 100       | HLT_j45_L1J15   | HLT_j45_L1J15   | HLT_j45_L1J15    |
| 2   | 100 - 150      | HLT_j85_L1J20   | HLT_j85_L1J20   | HLT_j85_L1jJ50   |
| 3   | 150 - 300      | HLT_j110_L1J30  | HLT_j110_L1J30  | HLT_j110_L1jJ60  |
| 4   | 300 - 400      | HLT_j260_L1J75  | HLT_j260_L1J75  | HLT_j260_L1jJ125 |
| 5   | 400 - 500      | HLT_j360_L1J100 | HLT_j360_L1J100 | HLT_j360_L1jJ160 |
| 6   | 500 - 700      | HLT_j480_L1J100 | HLT_j480_L1J100 | HLT_j480_L1J100  |
| 7   | 700 - 900      | HLT_j520_L1J100 | HLT_j520_L1J100 | HLT_j500_L1J100  |
| 8   | 900 - 1200     | same as above   | same as above   | same as above    |
| 9   | 1200 - 1500    | same as above   | same as above   | same as above    |
| 10  | 1500 - 3000    | same as above   | same as above   | same as above    |
## total luminosity in GRL
- in the unit of $\text{nb}^{-1}$

| bin | pT range [GeV] | 2022          | 2023          | 2024          |
| --- | -------------- | ------------- | ------------- | ------------- |
| 1   | 50 - 100       | 11.327        | 8.44288       | 17.7199       |
| 2   | 100 - 150      | 6,245         | 1,053.49      | 3,708.03      |
| 3   | 150 - 300      | 18,667.1      | 3,252.29      | 12,091.9      |
| 4   | 300 - 400      | 709,172       | 158,262       | 560,656       |
| 5   | 400 - 500      | 4,525,930     | 808,378       | 2,818,510     |
| 6   | 500 - 700      | 29.294,400    | 26,647,100    | 22,533,400    |
| 7   | 700 - 900      | same as above | same as above | same as above |
| 8   | 900 - 1200     | same as above | same as above | same as above |
| 9   | 1200 - 1500    | same as above | same as above | same as above |
| 10  | 1500 - 3000    | same as above | same as above | same as above |

# Good Run List
- base path to GRL file: `/cvmfs/atlas.cern.ch/repo/sw/database/GroupData/`
- recommended lumi tag: OflLumi-Run3-008 (OflLumi-Run3-003 or later)
- get run number after opening a root file by root: 
```
CollectionTree->Scan("EventInfoAuxDyn.runNumber", "", "", 1)
```
- get number of events:
```
CollectionTree->GetEntries()
```

## data22_13p6TeV
- from `GoodRunsLists/data22_13p6TeV/20250321/data22_13p6TeV.periodAllYear_DetStatus-v134-pro28-10_MERGED_PHYS_StandardGRL_All_Good_25ns_ignore_TRIGLAR.xml`
```
430536,430542,430580,430648,430896,431037,431178,431179,431215,431228,
431241,431341,431493,431810,431812,431850,431885,431894,431906,431914,
432180,435816,435831,435854,435931,435946,436041,436169,436354,436377,
436422,436496,436550,436582,436584,436602,436656,436799,436863,436983,
437010,437034,437062,437065,437079,437124,437484,437548,437580,437711,
437744,437756,437898,437991,438181,438219,438234,438252,438266,438277,
438298,438323,438364,438411,438446,438481,438502,438532,438638,438737,
438786,439529,439607,439676,439798,439830,439859,439911,439927,440407,
440447,440499,440543,440570,440613
```
- downloaded run: 
	- [p] DAOD_PHYS.43636795: 436496, 103508 events
	- [c] DAOD_PHYS.43636728: 430897, 152071 events

## data23_13p6TeV
- from `GoodRunsLists/data23_13p6TeV/20250321/data23_13p6TeV.periodAllYear_DetStatus-v133-pro31-11_MERGED_PHYS_StandardGRL_All_Good_25ns_ignoreTRIG_JETCTPIN.xml`
```
451587,451595,451611,451618,451735,451794,451804,451866,451896,452028,
452163,452202,452241,452463,452533,452573,452624,452640,452669,452696,
452726,452785,452787,452799,452843,452872,453353,453530,453556,453617,
453644,453657,453713,453733,453754,453795,453816,453858,453981,454054,
454083,454129,454163,454188,454222,454322,455857,455870,455924,455975,
456016,456110,456118,456126,456151,456164,456225,456273,456303,456314,
456316,456346,456386,456409,456522,456665,456685,456714,456729,456749
```
- downloaded run:
	- [p] 451896
## data24_13p6TeV
- from `GoodRunsLists/data24_13p6TeV/20260127/data24_13p6TeV.periodsEtoO_DetStatus-v140-pro36-13_MERGED_PHYS_StandardGRL_All_Good_25ns.xml`
	- periods E to O is actually all year for 2024.
```
473235,473255,473317,473323,473329,473334,473382,473400,473617,473747,
473796,473915,473959,473968,474271,474441,474448,474462,474509,474533,
474562,474600,474602,474657,474679,474770,474813,474926,474991,475008,
475035,475052,475066,475168,475192,475234,475321,475341,475369,475474,
475522,476060,476218,476265,476276,476301,476348,476384,476396,476428,
476476,476505,476589,476634,476718,476730,476760,476785,476875,476929,
476991,477002,477023,477037,477048,479103,479213,479239,479269,479279,
479327,479345,479374,479439,479449,479507,479519,479553,479563,479598,
479615,479633,479666,479680,479710,479720,479885,479913,479929,479955,
480022,480032,480188,480197,480219,480277,480283,480307,480407,480481,
480496,480657,480674,480741,480774,480794,480828,480957,481013,481032,
481042,481079,481108,481138,481166,481182,481207,481268,481277,481318,
481375,481398,481510,481553,481591,481603,481616,481638,481749,481865,
481893,481968,482028,482084,482129,482153,482212,482221,482374,482400,
482427,482448,482471,482485,482596,482727,482747,482768,482778,482798,
482819,483370,483398,483409,483440,483515,483532,483685,483725,483767,
483782,483833,483852,483869,483888,484016,484074,484097,484126,484146,
484191,484203,484220,484222,484249,484258,484296,484313,484336,484354,
484426,484442,484466,484568,484573,484583,484597,484610,484616,484653,
484710,484715,484754,484780,484799,484909,484953,484979,485051,485090,
485416,485431,485481,485492,485506,485886,485887,485950,486026,486131,
486179,486205,486211,486224,486253,486262,486273,486295,486310,486315,
486376,486384,486475,486640,486658,486689,486706
```
- downloaded run:
	- [p] 473235

# Ellen's case
- latest
![[Pasted image 20260227181700.png|697]]
- before
![[Pasted image 20260226182439.png]]
