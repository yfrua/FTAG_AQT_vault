- unprescaled trigger: [Twiki](https://twiki.cern.ch/twiki/bin/viewauth/Atlas/LowestUnprescaled#Triggers_in_2023)
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
- L1jJ trigger? #Question 

## data22_13p6TeV

| trigger name                                                                                                                                                                                 | PS Corr Ready Lumi ($\text{nb}^{-1}$) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| [HLT_j45_L1J15](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j45_L1J15 "link to COMA Chain/Item Report for HLT_j45_L1J15")          | 442                                   |
| [HLT_j60_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j60_L1J20 "link to COMA Chain/Item Report for HLT_j60_L1J20")          | 4,882                                 |
| [HLT_j85_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j85_L1J20 "link to COMA Chain/Item Report for HLT_j85_L1J20")          | 11,672                                |
| [HLT_j110_L1J30](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j110_L1J30 "link to COMA Chain/Item Report for HLT_j110_L1J30")       | 34,827                                |
| [HLT_j175_L1J50](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j175_L1J50 "link to COMA Chain/Item Report for HLT_j175_L1J50")       | 172,445                               |
| [HLT_j260_L1J75](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j260_L1J75 "link to COMA Chain/Item Report for HLT_j260_L1J75")       | 1,154,264                             |
| [HLT_j360_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j360_L1J100 "link to COMA Chain/Item Report for HLT_j360_L1J100")    | 6,515,200                             |
| [HLT_j420_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1J100 "link to COMA Chain/Item Report for HLT_j420_L1J100")    | 21,543,778                            |
| [HLT_j420_L1J120](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1J120 "link to COMA Chain/Item Report for HLT_j420_L1J120")    | 21,541,378                            |
| [HLT_j420_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1jJ160 "link to COMA Chain/Item Report for HLT_j420_L1jJ160") | 514,758                               |
| [HLT_j440_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j440_L1J100 "link to COMA Chain/Item Report for HLT_j440_L1J100")    | 21,541,378                            |
| [HLT_j450_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j450_L1J100 "link to COMA Chain/Item Report for HLT_j450_L1J100")    | 21,541,378                            |
| [HLT_j460_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j460_L1J100 "link to COMA Chain/Item Report for HLT_j460_L1J100")    | 21,541,378                            |
| [HLT_j480_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j480_L1J100 "link to COMA Chain/Item Report for HLT_j480_L1J100")    | 40,022,750                            |
| [HLT_j500_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j500_L1J100 "link to COMA Chain/Item Report for HLT_j500_L1J100")    | 40,022,750                            |
| [HLT_j520_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j520_L1J100 "link to COMA Chain/Item Report for HLT_j520_L1J100")    | 40,022,750                            |
## data23_13p6TeV

| trigger name                                                                                                                                                                                 | PS Corr Ready Lumi ($\text{nb}^{-1}$) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| [HLT_j20_L1J12](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j20_L1J12 "link to COMA Chain/Item Report for HLT_j20_L1J12")          | 150                                   |
| [HLT_j45_L1J15](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j45_L1J15 "link to COMA Chain/Item Report for HLT_j45_L1J15")          | 10.7                                  |
| [HLT_j60_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j60_L1J20 "link to COMA Chain/Item Report for HLT_j60_L1J20")          | 439                                   |
| [HLT_j85_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j85_L1J20 "link to COMA Chain/Item Report for HLT_j85_L1J20")          | 1,230                                 |
| [HLT_j110_L1J30](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j110_L1J30 "link to COMA Chain/Item Report for HLT_j110_L1J30")       | 3,797                                 |
| [HLT_j175_L1J50](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j175_L1J50 "link to COMA Chain/Item Report for HLT_j175_L1J50")       | 29,310                                |
| [HLT_j260_L1J75](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j260_L1J75 "link to COMA Chain/Item Report for HLT_j260_L1J75")       | 184,754                               |
| [HLT_j360_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j360_L1J100 "link to COMA Chain/Item Report for HLT_j360_L1J100")    | 943,674                               |
| [HLT_j420_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1J100 "link to COMA Chain/Item Report for HLT_j420_L1J100")    | 15,454,626                            |
| [HLT_j420_L1J120](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1J120 "link to COMA Chain/Item Report for HLT_j420_L1J120")    | 15,454,626                            |
| [HLT_j420_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1jJ160 "link to COMA Chain/Item Report for HLT_j420_L1jJ160") | 246,166                               |
| [HLT_j440_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j440_L1J100 "link to COMA Chain/Item Report for HLT_j440_L1J100")    | 15,454,626                            |
| [HLT_j450_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j450_L1J100 "link to COMA Chain/Item Report for HLT_j450_L1J100")    | 15,454,626                            |
| [HLT_j460_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j460_L1J100 "link to COMA Chain/Item Report for HLT_j460_L1J100")    | 15,454,626                            |
| [HLT_j480_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j480_L1J100 "link to COMA Chain/Item Report for HLT_j480_L1J100")    | 31,212,704                            |
| [HLT_j500_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j500_L1J100 "link to COMA Chain/Item Report for HLT_j500_L1J100")    | 31,212,704                            |
| [HLT_j520_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j520_L1J100 "link to COMA Chain/Item Report for HLT_j520_L1J100")    | 31,212,704                            |
## data24_13p6TeV

| trigger name                                                                                                                                                                                 | PS Corr Ready Lumi ($\text{nb}^{-1}$) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| [HLT_j20_L1jJ20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j20_L1jJ20 "link to COMA Chain/Item Report for HLT_j20_L1jJ20")       | 1,943                                 |
| [HLT_j20_L1jJ30](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j20_L1jJ30 "link to COMA Chain/Item Report for HLT_j20_L1jJ30")       | 9.96                                  |
| [HLT_j45_L1J15](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j45_L1J15 "link to COMA Chain/Item Report for HLT_j45_L1J15")          | 62.9                                  |
| [HLT_j60_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j60_L1J20 "link to COMA Chain/Item Report for HLT_j60_L1J20")          | 840                                   |
| [HLT_j60_L1jJ50](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j60_L1jJ50 "link to COMA Chain/Item Report for HLT_j60_L1jJ50")       | 1,558                                 |
| [HLT_j85_L1J20](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j85_L1J20 "link to COMA Chain/Item Report for HLT_j85_L1J20")          | 2,339                                 |
| [HLT_j85_L1jJ50](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j85_L1jJ50 "link to COMA Chain/Item Report for HLT_j85_L1jJ50")       | 4,292                                 |
| [HLT_j110_L1jJ60](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j110_L1jJ60 "link to COMA Chain/Item Report for HLT_j110_L1jJ60")    | 13,914                                |
| [HLT_j175_L1J50](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j175_L1J50 "link to COMA Chain/Item Report for HLT_j175_L1J50")       | 55,135                                |
| [HLT_j175_L1jJ90](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j175_L1jJ90 "link to COMA Chain/Item Report for HLT_j175_L1jJ90")    | 101,780                               |
| [HLT_j260_L1jJ125](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j260_L1jJ125 "link to COMA Chain/Item Report for HLT_j260_L1jJ125") | 641,623                               |
| [HLT_j360_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j360_L1J100 "link to COMA Chain/Item Report for HLT_j360_L1J100")    | 799,906                               |
| [HLT_j360_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j360_L1jJ160 "link to COMA Chain/Item Report for HLT_j360_L1jJ160") | 3,222,432                             |
| [HLT_j420_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1J100 "link to COMA Chain/Item Report for HLT_j420_L1J100")    | 12,616,139                            |
| [HLT_j420_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1jJ160 "link to COMA Chain/Item Report for HLT_j420_L1jJ160") | 60,828,012                            |
| [HLT_j420_L1jJ180](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j420_L1jJ180 "link to COMA Chain/Item Report for HLT_j420_L1jJ180") | 60,792,306                            |
| [HLT_j440_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j440_L1J100 "link to COMA Chain/Item Report for HLT_j440_L1J100")    | 12,616,139                            |
| [HLT_j440_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j440_L1jJ160 "link to COMA Chain/Item Report for HLT_j440_L1jJ160") | 60,792,305                            |
| [HLT_j450_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j450_L1J100 "link to COMA Chain/Item Report for HLT_j450_L1J100")    | 12,616,139                            |
| [HLT_j450_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j450_L1jJ160 "link to COMA Chain/Item Report for HLT_j450_L1jJ160") | 60,792,305                            |
| [HLT_j460_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j460_L1J100 "link to COMA Chain/Item Report for HLT_j460_L1J100")    | 12,616,139                            |
| [HLT_j460_L1jJ160](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j460_L1jJ160 "link to COMA Chain/Item Report for HLT_j460_L1jJ160") | 60,792,305                            |
| [HLT_j480_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j480_L1J100 "link to COMA Chain/Item Report for HLT_j480_L1J100")    | 25,232,278                            |
| [HLT_j500_L1J100](https://atlas-tagservices.cern.ch/tagservices/RunBrowser/runBrowserReport/runBrowserReport.php?cn=HLT_j500_L1J100 "link to COMA Chain/Item Report for HLT_j500_L1J100")    | 25,232,278                            |

# Leading jet pT binning and triggers
#TODO Find trigger efficiency plots?

| bin | pT range [GeV] | 2022            | 2023            | 2024             |
| --- | -------------- | --------------- | --------------- | ---------------- |
| 1   | 110 - 150      | HLT_j85_L1J20   | HLT_j85_L1J20   | HLT_j85_L1jJ50   |
| 2   | 150 - 300      | HLT_j110_L1J30  | HLT_j110_L1J30  | HLT_j110_L1jJ60  |
| 3   | 300 - 400      | HLT_j260_L1J75  | HLT_j260_L1J75  | HLT_j260_L1jJ125 |
| 4   | 400 - 500      | HLT_j360_L1J100 | HLT_j360_L1J100 | HLT_j360_L1jJ160 |
| 5   | 500 - 700      | HLT_j480_L1J100 | HLT_j480_L1J100 | HLT_j480_L1J100  |
| 6   | 700 - 900      | HLT_j520_L1J100 | HLT_j520_L1J100 | HLT_j500_L1J100  |
| 7   | 900 - 1200     | same as above   | same as above   | same as above    |
| 8   | 1200 - 1500    | same as above   | same as above   | same as above    |
| 9   | 1500 - 3000    | same as above   | same as above   | same as above    |


# Ellen's case
- latest
![[Pasted image 20260227181700.png|697]]
- before
![[Pasted image 20260226182439.png]]
