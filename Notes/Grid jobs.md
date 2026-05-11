- grid job monitor: [PanDA](https://bigpanda.cern.ch/)
- kill grid jobs:
	- setupATLAS, lsetup panda, pbook
	- kill(`jedTaskID`), python syntax which `jedTaskID` can be a scalar or list.
- check container file size:
	- lsetup rucio, voms-proxy-init -voms atlas
	- rucio list-files `DSID` | grep Total
- rucio Web UI: https://atlas-rucio-webui.cern.ch/
- rucio UI: https://rucio-ui.cern.ch/
- requested RSE: BEIJING-LCG2-EOS_LOCALGROUPDISK

# data

| name   | task id                                             | N_files | size      | output DID                                                                               |
| ------ | --------------------------------------------------- | ------- | --------- | ---------------------------------------------------------------------------------------- |
| data22 | [49888309](https://bigpanda.cern.ch/task/49888309/) | 1240    | 45.400 GB | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp22_v02_p6700.CNF_2J_L2J_0ad54d4_output/ |
| data23 |                                                     |         |           |                                                                                          |
| data24 |                                                     |         |           |                                                                                          |

# mc23a
## dijet
- Total number of files: 916
- Total size: 1.709 TB

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
- Total number of files: 
- Total size: 

| name      | task id                                             | N_files | size | output DID                                                                            |
| --------- | --------------------------------------------------- | ------- | ---- | ------------------------------------------------------------------------------------- |
| SingleLep | [50213504](https://bigpanda.cern.ch/task/50213504/) | 566     |      | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| DiLep     | [50213505](https://bigpanda.cern.ch/task/50213505/) | 722     |      | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |

## single top
- Total number of files: 
- Total size: 

| name                   | task id                                             | N_files | size | output DID                                                                                        |
| ---------------------- | --------------------------------------------------- | ------- | ---- | ------------------------------------------------------------------------------------------------- |
| tb_lep_antitop         | [50213506](https://bigpanda.cern.ch/task/50213506/) | 28      |      | user.fye.601348.PhPy8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/             |
| tb_lep_top             | [50213508](https://bigpanda.cern.ch/task/50213508/) | 99      |      | user.fye.601349.PhPy8EG_tb_lep_top.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| tqb_lep_antitop        | [50213509](https://bigpanda.cern.ch/task/50213509/) | 72      |      | user.fye.601350.PhPy8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/             |
| tqb_lep_top            | [50213511](https://bigpanda.cern.ch/task/50213511/) | 68      |      | user.fye.601351.PhPy8EG_tqb_lep_top.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/ |
| tW_dyn_DR_incl_antitop | [50213512](https://bigpanda.cern.ch/task/50213512/) | 213     |      | user.fye.601352.PhPy8EG.DAOD_PHYS.e8551_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/             |
| tW_dyn_DR_incl_top     | [50213513](https://bigpanda.cern.ch/task/50213513/) | 157     |      | user.fye.601355.PhPy8EG.DAOD_PHYS.e8551_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/             |

## diboson
- Total number of files: 
- Total size: 

| name    | task id                                             | N_files | size | output DID                                                                                    |
| ------- | --------------------------------------------------- | ------- | ---- | --------------------------------------------------------------------------------------------- |
| llll    | [50213515](https://bigpanda.cern.ch/task/50213515/) | 486     |      | user.fye.701040.Sh_llll.DAOD_PHYS.e8582_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/         |
| lllv    | [50213516](https://bigpanda.cern.ch/task/50213516/) | 546     |      | user.fye.701045.Sh_lllv.DAOD_PHYS.e8582_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/         |
| llvv_os | [50213518](https://bigpanda.cern.ch/task/50213518/) | 556     |      | user.fye.701050.Sh_llvv_os.DAOD_PHYS.e8582_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/      |
| llvv_ss | [50213520](https://bigpanda.cern.ch/task/50213520/) | 559     |      | user.fye.701055.Sh_2214_llvv_ss.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/ |
| lvvv    | [50213522](https://bigpanda.cern.ch/task/50213522/) | 411     |      | user.fye.701060.Sh_lvvv.DAOD_PHYS.e8582_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/         |
| vvvv    | [50213523](https://bigpanda.cern.ch/task/50213523/) | 228     |      | user.fye.701065.Sh_vvvv.DAOD_PHYS.e8582_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/         |
| ZqqZll  | [50213524](https://bigpanda.cern.ch/task/50213524/) | 405     |      | user.fye.701085.Sh_2214_ZqqZll.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| ZbbZll  | [50213525](https://bigpanda.cern.ch/task/50213525/) | 556     |      | user.fye.701090.Sh_2214_ZbbZll.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| ZqqZvv  | [50213526](https://bigpanda.cern.ch/task/50213526/) | 443     |      | user.fye.701095.Sh_2214_ZqqZvv.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| ZbbZvv  | [50213527](https://bigpanda.cern.ch/task/50213527/) | 444     |      | user.fye.701100.Sh_2214_ZbbZvv.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| WqqZll  | [50213530](https://bigpanda.cern.ch/task/50213530/) | 396     |      | user.fye.701105.Sh_2214_WqqZll.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| WqqZvv  | [50213532](https://bigpanda.cern.ch/task/50213532/) | 392     |      | user.fye.701110.Sh_2214_WqqZvv.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| WlvZqq  | [50213533](https://bigpanda.cern.ch/task/50213533/) | 411     |      | user.fye.701115.Sh_2214_WlvZqq.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| WlvZbb  | [50213535](https://bigpanda.cern.ch/task/50213535/) | 381     |      | user.fye.701120.Sh_2214_WlvZbb.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |
| WlvWqq  | [50213536](https://bigpanda.cern.ch/task/50213536/) | 356     |      | user.fye.701125.Sh_2214_WlvWqq.DAOD_PHYS.e8543_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/  |

## W+jets
- Total number of files: 
- Total size: 

| name                          | task id                                             | N_files | size | output DID                                                                       |
| ----------------------------- | --------------------------------------------------- | ------- | ---- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        | [50213537](https://bigpanda.cern.ch/task/50213537/) | 132     |      | user.fye.700777.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   | [50213539](https://bigpanda.cern.ch/task/50213539/) | 986     |      | user.fye.700778.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     | [50213540](https://bigpanda.cern.ch/task/50213540/) | 3359    |      | user.fye.700779.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wmunu_maxHTpTV2_BFilter       | [50213542](https://bigpanda.cern.ch/task/50213542/) | 135     |      | user.fye.700780.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  | [50213543](https://bigpanda.cern.ch/task/50213543/) | 1367    |      | user.fye.700781.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wmunu_maxHTpTV2_CVetoBVeto    | [50213544](https://bigpanda.cern.ch/task/50213544/) | 3810    |      | user.fye.700782.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wtaunu_maxHTpTV2_BFilter      | [50213545](https://bigpanda.cern.ch/task/50213545/) | 82      |      | user.fye.700783.Sh.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto | [50213546](https://bigpanda.cern.ch/task/50213546/) | 878     |      | user.fye.700784.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   | [50213548](https://bigpanda.cern.ch/task/50213548/) | 4008    |      | user.fye.700785.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |

## Z+jets
- Total number of files: 
- Total size: 

| name                           | task id                                             | N_files | size | output DID                                                                       |
| ------------------------------ | --------------------------------------------------- | ------- | ---- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          | [50213549](https://bigpanda.cern.ch/task/50213549/) | 307     |      | user.fye.700786.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Zee_maxHTpTV2_CFilterBVeto     | [50213551](https://bigpanda.cern.ch/task/50213551/) | 637     |      | user.fye.700787.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Zee_maxHTpTV2_CVetoBVeto       | [50213552](https://bigpanda.cern.ch/task/50213552/) | 3832    |      | user.fye.700788.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Zmumu_maxHTpTV2_BFilter        | [50213555](https://bigpanda.cern.ch/task/50213555/) | 353     |      | user.fye.700789.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   | [50213556](https://bigpanda.cern.ch/task/50213556/) | 526     |      | user.fye.700790.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     | [50213558](https://bigpanda.cern.ch/task/50213558/) | 3578    |      | user.fye.700791.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Ztautau_maxHTpTV2_BFilter      | [50213559](https://bigpanda.cern.ch/task/50213559/) | 302     |      | user.fye.700792.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto | [50213561](https://bigpanda.cern.ch/task/50213561/) | 549     |      | user.fye.700793.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   | [50213563](https://bigpanda.cern.ch/task/50213563/) | 3640    |      | user.fye.700794.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Znunu_pTV2_BFilter             | [50213565](https://bigpanda.cern.ch/task/50213565/) | 257     |      | user.fye.700795.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Znunu_pTV2_CFilterBVeto        | [50213568](https://bigpanda.cern.ch/task/50213568/) | 598     |      | user.fye.700796.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |
| Znunu_pTV2_CVetoBVeto          | [50213569](https://bigpanda.cern.ch/task/50213569/) | 4162    |      | user.fye.700797.Sh.DAOD_PHYS.e8514_s4162_r15540_p6697.CNF_2J_L2J_0c6744b_output/ |

