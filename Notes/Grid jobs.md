- grid job monitor: [PanDA](https://bigpanda.cern.ch/)
- kill grid jobs:
	- setupATLAS, lsetup panda, pbook
	- kill(`jedTaskID`), python syntax which `jedTaskID` can be a scalar or list.
- check container file size:
	- lsetup rucio, voms-proxy-init -voms atlas
	- rucio list-files `<DSID>` | grep Total
- rucio Web UI: https://atlas-rucio-webui.cern.ch/
- rucio UI: https://rucio-ui.cern.ch/
- requested RSE: BEIJING-LCG2-EOS_LOCALGROUPDISK

# data
| name   | task id                                             | N_files | size | output DID                                                                               |
| ------ | --------------------------------------------------- | ------- | ---- | ---------------------------------------------------------------------------------------- |
| data22 | [51006534](https://bigpanda.cern.ch/task/51006534/) |         |      | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp22_v01_p7019.CNF_2J_L2J_ab6d1b1_output/ |

# mc23a
- without systematics.
## dijet

| name    | task id                                             | N_files | size     | output DID                                                                          |
| ------- | --------------------------------------------------- | ------- | -------- | ----------------------------------------------------------------------------------- |
| JZ2     | [51006630](https://bigpanda.cern.ch/task/51006630/) | 84      | 6.54 GB  | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_50846f3_output/ |
| JZ3     | [51006632](https://bigpanda.cern.ch/task/51006632/) | 165     | 25.16 GB | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_50846f3_output/ |
| JZ4     | [51006634](https://bigpanda.cern.ch/task/51006634/) | 225     | 32.15 GB | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_50846f3_output/ |
| JZ5     | [51006636](https://bigpanda.cern.ch/task/51006636/) | 86      | 16.55 GB | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_50846f3_output/ |
| JZ6     | [51006638](https://bigpanda.cern.ch/task/51006638/) | 83      | 10.06 GB | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_50846f3_output/ |
| JZ7     | [51006641](https://bigpanda.cern.ch/task/51006641/) | 55      | 6.36 GB  | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_50846f3_output/ |
| JZ8     | [51006645](https://bigpanda.cern.ch/task/51006645/) | 48      | 6.45 GB  | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_50846f3_output/ |
| JZ9incl | [51006647](https://bigpanda.cern.ch/task/51006647/) | 42      | 5.03 GB  | user.fye.801174.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_50846f3_output/ |

## ttbar

| name      | task id                                             | N_files | size    | output DID                                                                            |
| --------- | --------------------------------------------------- | ------- | ------- | ------------------------------------------------------------------------------------- |
| SingleLep | [51006572](https://bigpanda.cern.ch/task/51006572/) | 177     | 6.69 GB | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| DiLep     | [51006574](https://bigpanda.cern.ch/task/51006574/) | 150     | 2.73 GB | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |


## Wjets

| name                          | task id                                             | N_files | size     | output DID                                                                       |
| ----------------------------- | --------------------------------------------------- | ------- | -------- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        | [51006578](https://bigpanda.cern.ch/task/51006578/) | 35      | 2.04 GB  | user.fye.700777.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   | [51006580](https://bigpanda.cern.ch/task/51006580/) | 161     | 11.24 GB | user.fye.700778.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     | [51006583](https://bigpanda.cern.ch/task/51006583/) | 788     | 35.42 GB | user.fye.700779.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Wmunu_maxHTpTV2_BFilter       | [51006586](https://bigpanda.cern.ch/task/51006586/) | 30      | 1.53 GB  | user.fye.700780.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  | [51006590](https://bigpanda.cern.ch/task/51006590/) | 233     | 7.93 GB  | user.fye.700781.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Wmunu_maxHTpTV2_CVetoBVeto    | [51006593](https://bigpanda.cern.ch/task/51006593/) | 650     | 24.52 GB | user.fye.700782.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Wtaunu_maxHTpTV2_BFilter      | [51006597](https://bigpanda.cern.ch/task/51006597/) | 45      | 2.27 GB  | user.fye.700783.Sh.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_50846f3_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto | [51006599](https://bigpanda.cern.ch/task/51006599/) | 163     | 20.6 GB  | user.fye.700784.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   | [51006601](https://bigpanda.cern.ch/task/51006601/) | 815     | 61.93 GB | user.fye.700785.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |

## Zjets

| name                           | task id                                             | N_files | size     | output DID                                                                       |
| ------------------------------ | --------------------------------------------------- | ------- | -------- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          | [51006603](https://bigpanda.cern.ch/task/51006603/) | 59      | 1.69 GB  | user.fye.700786.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Zee_maxHTpTV2_CFilterBVeto     | [51006606](https://bigpanda.cern.ch/task/51006606/) | 67      | 3.59 GB  | user.fye.700787.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Zee_maxHTpTV2_CVetoBVeto       | [51006608](https://bigpanda.cern.ch/task/51006608/) | 982     | 23.03 GB | user.fye.700788.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Zmumu_maxHTpTV2_BFilter        | [51006610](https://bigpanda.cern.ch/task/51006610/) | 59      | 1.06 GB  | user.fye.700789.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   | [51006612](https://bigpanda.cern.ch/task/51006612/) | 74      | 1.93 GB  | user.fye.700790.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     | [51006614](https://bigpanda.cern.ch/task/51006614/) | 810     | 11.7 GB  | user.fye.700791.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Ztautau_maxHTpTV2_BFilter      | [51006617](https://bigpanda.cern.ch/task/51006617/) | 73      | 5.62 GB  | user.fye.700792.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto | [51006619](https://bigpanda.cern.ch/task/51006619/) | 138     | 11.38 GB | user.fye.700793.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   | [51006621](https://bigpanda.cern.ch/task/51006621/) | 994     | 70.53 GB | user.fye.700794.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Znunu_pTV2_BFilter             | [51006623](https://bigpanda.cern.ch/task/51006623/) | 47      | 4.45 GB  | user.fye.700795.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Znunu_pTV2_CFilterBVeto        | [51006626](https://bigpanda.cern.ch/task/51006626/) | 80      | 11.83 GB | user.fye.700796.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |
| Znunu_pTV2_CVetoBVeto          | [51006628](https://bigpanda.cern.ch/task/51006628/) | 871     | 59.59 GB | user.fye.700797.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_50846f3_output/ |


---
==obsolete p-tag used!!==
# data

| name              | task id                                             | N_files | size      | output DID                                                                               |
| ----------------- | --------------------------------------------------- | ------- | --------- | ---------------------------------------------------------------------------------------- |
| data22            | [49888309](https://bigpanda.cern.ch/task/49888309/) | 1240    | 45.400 GB | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp22_v02_p6700.CNF_2J_L2J_0ad54d4_output/ |
| data22_unprescale | [50682356](https://bigpanda.cern.ch/task/50682356/) | 397     | 45.95 GB  | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp22_v02_p6700.CNF_2J_L2J_a5aa9f7_output/ |



# mc23a
- Total number of files: 11,954
- Total size: 9.776 TB
## dijet

| name    | task id                                             | N_files | size       | output DID                                                                          |
| ------- | --------------------------------------------------- | ------- | ---------- | ----------------------------------------------------------------------------------- |
| JZ2     | [49888325](https://bigpanda.cern.ch/task/49888325/) | 92      | 121.732 GB | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_9fa9dd6_output/ |
| JZ3     | [49888328](https://bigpanda.cern.ch/task/49888328/) | 204     | 416.696 GB | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_9fa9dd6_output/ |
| JZ4     | [49888332](https://bigpanda.cern.ch/task/49888332/) | 253     | 509.987 GB | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_9fa9dd6_output/ |
| JZ5     | [49888335](https://bigpanda.cern.ch/task/49888335/) | 132     | 261.260 GB | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_9fa9dd6_output/ |
| JZ6     | [49888337](https://bigpanda.cern.ch/task/49888337/) | 77      | 156.639 GB | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_9fa9dd6_output/ |
| JZ7     | [49888339](https://bigpanda.cern.ch/task/49888339/) | 51      | 103.603 GB | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_9fa9dd6_output/ |
| JZ8     | [49888342](https://bigpanda.cern.ch/task/49888342/) | 61      | 100.870 GB | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_9fa9dd6_output/ |
| JZ9incl | [49888345](https://bigpanda.cern.ch/task/49888345/) | 46      | 79.186 GB  | user.fye.801174.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_9fa9dd6_output/ |

## ttbar
- line starts with: 0
- 2 samples

| name      | task id                                             | N_files | size      | output DID                                                                            |
| --------- | --------------------------------------------------- | ------- | --------- | ------------------------------------------------------------------------------------- |
| SingleLep | [50213504](https://bigpanda.cern.ch/task/50213504/) | 174     | 116.19 GB | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| DiLep     | [50213505](https://bigpanda.cern.ch/task/50213505/) | 153     | 49.53 GB  | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |

## single top
- line starts with: 2
- 6 samples

| name                   | task id                                             | N_files | size     | output DID                                                                                        |
| ---------------------- | --------------------------------------------------- | ------- | -------- | ------------------------------------------------------------------------------------------------- |
| tb_lep_antitop         | [50213506](https://bigpanda.cern.ch/task/50213506/) | 6       | 2.16 GB  | user.fye.601348.PhPy8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/             |
| tb_lep_top             | [50213508](https://bigpanda.cern.ch/task/50213508/) | 20      | 3.49 GB  | user.fye.601349.PhPy8EG_tb_lep_top.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| tqb_lep_antitop        | [50213509](https://bigpanda.cern.ch/task/50213509/) | 15      | 5.21 GB  | user.fye.601350.PhPy8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/             |
| tqb_lep_top            | [50213511](https://bigpanda.cern.ch/task/50213511/) | 16      | 7.85 GB  | user.fye.601351.PhPy8EG_tqb_lep_top.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/ |
| tW_dyn_DR_incl_antitop | [50213512](https://bigpanda.cern.ch/task/50213512/) | 45      | 39.39 GB | user.fye.601352.PhPy8EG.DAOD_PHYS.e8551_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/             |
| tW_dyn_DR_incl_top     | [50213513](https://bigpanda.cern.ch/task/50213513/) | 34      | 39.43 GB | user.fye.601355.PhPy8EG.DAOD_PHYS.e8551_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/             |

## diboson
- line starts with: 8
- 15 samples

| name    | task id                                             | N_files | size      | output DID                                                                                    |
| ------- | --------------------------------------------------- | ------- | --------- | --------------------------------------------------------------------------------------------- |
| llll    | [50213515](https://bigpanda.cern.ch/task/50213515/) | 137     | 31.4 GB   | user.fye.701040.Sh_llll.DAOD_PHYS.e8582_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/         |
| lllv    | [50213516](https://bigpanda.cern.ch/task/50213516/) | 145     | 51.76 GB  | user.fye.701045.Sh_lllv.DAOD_PHYS.e8582_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/         |
| llvv_os | [50213518](https://bigpanda.cern.ch/task/50213518/) | 139     | 54.66 GB  | user.fye.701050.Sh_llvv_os.DAOD_PHYS.e8582_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/      |
| llvv_ss | [50213520](https://bigpanda.cern.ch/task/50213520/) | 119     | 90.41 GB  | user.fye.701055.Sh_2214_llvv_ss.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/ |
| lvvv    | [50213522](https://bigpanda.cern.ch/task/50213522/) | 84      | 72.98 GB  | user.fye.701060.Sh_lvvv.DAOD_PHYS.e8582_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/         |
| vvvv    | [50213523](https://bigpanda.cern.ch/task/50213523/) | 46      | 28.78 GB  | user.fye.701065.Sh_vvvv.DAOD_PHYS.e8582_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/         |
| ZqqZll  | [50213524](https://bigpanda.cern.ch/task/50213524/) | 122     | 76.43 GB  | user.fye.701085.Sh_2214_ZqqZll.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| ZbbZll  | [50213525](https://bigpanda.cern.ch/task/50213525/) | 190     | 45.54 GB  | user.fye.701090.Sh_2214_ZbbZll.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| ZqqZvv  | [50213526](https://bigpanda.cern.ch/task/50213526/) | 187     | 145.82 GB | user.fye.701095.Sh_2214_ZqqZvv.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| ZbbZvv  | [50213527](https://bigpanda.cern.ch/task/50213527/) | 115     | 79.01 GB  | user.fye.701100.Sh_2214_ZbbZvv.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| WqqZll  | [50213530](https://bigpanda.cern.ch/task/50213530/) | 131     | 87.8 GB   | user.fye.701105.Sh_2214_WqqZll.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| WqqZvv  | [50213532](https://bigpanda.cern.ch/task/50213532/) | 157     | 178.2 GB  | user.fye.701110.Sh_2214_WqqZvv.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| WlvZqq  | [50213533](https://bigpanda.cern.ch/task/50213533/) | 127     | 118.25 GB | user.fye.701115.Sh_2214_WlvZqq.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| WlvZbb  | [50213535](https://bigpanda.cern.ch/task/50213535/) | 85      | 69.03 GB  | user.fye.701120.Sh_2214_WlvZbb.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| WlvWqq  | [50213536](https://bigpanda.cern.ch/task/50213536/) | 81      | 65.48 GB  | user.fye.701125.Sh_2214_WlvWqq.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |

## W+jets
- line starts with: 23
- 9 samples

| name                          | task id                                             | N_files | size      | output DID                                                                       |
| ----------------------------- | --------------------------------------------------- | ------- | --------- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        | [50213537](https://bigpanda.cern.ch/task/50213537/) | 36      | 34.27 GB  | user.fye.700777.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   | [50213539](https://bigpanda.cern.ch/task/50213539/) | 263     | 187.85 GB | user.fye.700778.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     | [50213540](https://bigpanda.cern.ch/task/50213540/) | 977     | 628.52 GB | user.fye.700779.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wmunu_maxHTpTV2_BFilter       | [50213542](https://bigpanda.cern.ch/task/50213542/) | 31      | 26.15 GB  | user.fye.700780.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  | [50213543](https://bigpanda.cern.ch/task/50213543/) | 355     | 136.88 GB | user.fye.700781.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wmunu_maxHTpTV2_CVetoBVeto    | [50213544](https://bigpanda.cern.ch/task/50213544/) | 923     | 443.23 GB | user.fye.700782.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wtaunu_maxHTpTV2_BFilter      | [50213545](https://bigpanda.cern.ch/task/50213545/) | 19      | 38.09 GB  | user.fye.700783.Sh.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto | [50213546](https://bigpanda.cern.ch/task/50213546/) | 241     | 348.21 GB | user.fye.700784.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   | [50213548](https://bigpanda.cern.ch/task/50213548/) | 865     | 1.08 TB   | user.fye.700785.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |

## Z+jets
- line starts with: 32
- 12 samples

| name                           | task id                                             | N_files | size      | output DID                                                                       |
| ------------------------------ | --------------------------------------------------- | ------- | --------- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          | [50213549](https://bigpanda.cern.ch/task/50213549/) | 62      | 29.31 GB  | user.fye.700786.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Zee_maxHTpTV2_CFilterBVeto     | [50213551](https://bigpanda.cern.ch/task/50213551/) | 177     | 59.85 GB  | user.fye.700787.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Zee_maxHTpTV2_CVetoBVeto       | [50213552](https://bigpanda.cern.ch/task/50213552/) | 1238    | 400.54 GB | user.fye.700788.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Zmumu_maxHTpTV2_BFilter        | [50213555](https://bigpanda.cern.ch/task/50213555/) | 98      | 18.41 GB  | user.fye.700789.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   | [50213556](https://bigpanda.cern.ch/task/50213556/) | 119     | 33.3 GB   | user.fye.700790.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     | [50213558](https://bigpanda.cern.ch/task/50213558/) | 863     | 211.48 GB | user.fye.700791.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Ztautau_maxHTpTV2_BFilter      | [50213559](https://bigpanda.cern.ch/task/50213559/) | 83      | 94.21 GB  | user.fye.700792.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto | [50213561](https://bigpanda.cern.ch/task/50213561/) | 117     | 187.37 GB | user.fye.700793.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   | [50213563](https://bigpanda.cern.ch/task/50213563/) | 888     | 1.2 TB    | user.fye.700794.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Znunu_pTV2_BFilter             | [50213565](https://bigpanda.cern.ch/task/50213565/) | 78      | 84.82 GB  | user.fye.700795.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Znunu_pTV2_CFilterBVeto        | [50213568](https://bigpanda.cern.ch/task/50213568/) | 234     | 224.68 GB | user.fye.700796.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Znunu_pTV2_CVetoBVeto          | [50213569](https://bigpanda.cern.ch/task/50213569/) | 1043    | 1.25 TB   | user.fye.700797.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |

