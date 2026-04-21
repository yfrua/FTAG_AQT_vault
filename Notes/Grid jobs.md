- grid job monitor: [PanDA](https://bigpanda.cern.ch/)
- kill grid jobs:
	- setupATLAS, lsetup panda, pbook
	- kill(`jedTaskID`), python syntax which `jedTaskID` can be a scalar or list.
- check container file size:
	- lsetup rucio, voms-proxy-init -voms atlas
	- rucio list-files `DSID` | grep Total

# data

| name   | task id                                             | N_files | size | output DSID                                                                             |
| ------ | --------------------------------------------------- | ------- | ---- | --------------------------------------------------------------------------------------- |
| data22 | [49865090](https://bigpanda.cern.ch/task/49865090/) |         |      | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp22_v02_p6700.CNF_2J_L2J_cf3fdac_output |
| data23 |                                                     |         |      |                                                                                         |
| data24 |                                                     |         |      |                                                                                         |

# MC
## mc23a
| name    | task id                                             | N_files | size       | output DSID                                                                        |
| ------- | --------------------------------------------------- | ------- | ---------- | ---------------------------------------------------------------------------------- |
| JZ2     | [49865113](https://bigpanda.cern.ch/task/49865113/) | 123     | 153.483 GB | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_b9e313b_output |
| JZ3     | [49865118](https://bigpanda.cern.ch/task/49865118/) |         |            | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_b9e313b_output |
| JZ4     | [49865121](https://bigpanda.cern.ch/task/49865121/) | 257     | 634.957 GB | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_b9e313b_output |
| JZ5     | [49865125](https://bigpanda.cern.ch/task/49865125/) | 137     | 324.916 GB | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_b9e313b_output |
| JZ6     | [49865129](https://bigpanda.cern.ch/task/49865129/) | 94      | 194.925 GB | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_b9e313b_output |
| JZ7     | [49865132](https://bigpanda.cern.ch/task/49865132/) | 52      | 129.007 GB | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_b9e313b_output |
| JZ8     | [49865134](https://bigpanda.cern.ch/task/49865134/) |         |            | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_b9e313b_output |
| JZ9incl | [49865137](https://bigpanda.cern.ch/task/49865137/) | 46      | 99.280 GB  | user.fye.801174.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_b9e313b_output |

---
Previous submission (with wrong event selection): 
# data
- data24_legacy: used wrong trigger
- made a rule to transfer data23 to local disk.

| name          | task id                                             | size      | output DID                                                                            |
| ------------- | --------------------------------------------------- | --------- | ------------------------------------------------------------------------------------- |
| data24_legacy | [49457290](https://bigpanda.cern.ch/task/49457290/) | 33.772 GB | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp24_v01_p6700.CNF_2J_L_a743ad0_output |
| data22        | [49509382](https://bigpanda.cern.ch/task/49509382/) | 43.852 GB | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp22_v02_p6700.CNF_2J_L_cc70672_output |
| data23        | [49514106](https://bigpanda.cern.ch/task/49514106/) | 21.122 GB | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp23_v01_p6700.CNF_2J_L_af02954_output |
| data24        | [49509434](https://bigpanda.cern.ch/task/49509434/) | 84.135 GB | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp24_v01_p6700.CNF_2J_L_d5c091d_output |


# MC
- use dataset in [[DAOD list]]
## mc23a
- r-tag=r14622
- 2.058 TB in total.

| name | task id                                             | size       | output DID                                                                         |
| ---- | --------------------------------------------------- | ---------- | ---------------------------------------------------------------------------------- |
| JZ0  | [49514398](https://bigpanda.cern.ch/task/49514398/) | 129.492 MB | user.fye.801165.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_871edd1_output |
| JZ1  | [49514401](https://bigpanda.cern.ch/task/49514401/) | 38.803 MB  | user.fye.801166.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_871edd1_output |
| JZ2  | [49514403](https://bigpanda.cern.ch/task/49514403/) | 80.395 GB  | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_871edd1_output |
| JZ3  | [49514406](https://bigpanda.cern.ch/task/49514406/) | 517.231 GB | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_871edd1_output |
| JZ4  | [49514408](https://bigpanda.cern.ch/task/49514408/) | 634.955 GB | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_871edd1_output |
| JZ5  | [49514409](https://bigpanda.cern.ch/task/49514409/) | 324.878 GB | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_871edd1_output |
| JZ6  | [49514413](https://bigpanda.cern.ch/task/49514413/) | 194.944 GB | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_871edd1_output |
| JZ7  | [49514414](https://bigpanda.cern.ch/task/49514414/) | 129.007 GB | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_871edd1_output |
| JZ8  | [49514416](https://bigpanda.cern.ch/task/49514416/) | 126.039 GB | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_871edd1_output |
| JZ9  | [49514418](https://bigpanda.cern.ch/task/49514418/) | 99.280 GB  | user.fye.801174.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p6697.CNF_2J_L2J_871edd1_output |

## mc23d
- r-tag=r15224
- 5.305 TB in total.

| name | task id                                             | size       | output DID                                                                         |
| ---- | --------------------------------------------------- | ---------- | ---------------------------------------------------------------------------------- |
| JZ0  | [49514430](https://bigpanda.cern.ch/task/49514430/) | 499.308 MB | user.fye.801165.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p6697.CNF_2J_L2J_9b58101_output |
| JZ1  | [49514431](https://bigpanda.cern.ch/task/49514431/) | 520.122 MB | user.fye.801166.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p6697.CNF_2J_L2J_9b58101_output |
| JZ2  | [49514434](https://bigpanda.cern.ch/task/49514434/) | 203.477 GB | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p6697.CNF_2J_L2J_9b58101_output |
| JZ3  | [49514435](https://bigpanda.cern.ch/task/49514435/) | 1.303 TB   | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p6697.CNF_2J_L2J_9b58101_output |
| JZ4  | [49514437](https://bigpanda.cern.ch/task/49514437/) | 1.597 TB   | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p6697.CNF_2J_L2J_9b58101_output |
| JZ5  | [49514439](https://bigpanda.cern.ch/task/49514439/) | 817.311 GB | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p6697.CNF_2J_L2J_9b58101_output |
| JZ6  | [49514441](https://bigpanda.cern.ch/task/49514441/) | 489.634 GB | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p6697.CNF_2J_L2J_9b58101_output |
| JZ7  | [49514442](https://bigpanda.cern.ch/task/49514442/) | 324.647 GB | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p6697.CNF_2J_L2J_9b58101_output |
| JZ8  | [49514444](https://bigpanda.cern.ch/task/49514444/) | 316.790 GB | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p6697.CNF_2J_L2J_9b58101_output |
| JZ9  | [49514446](https://bigpanda.cern.ch/task/49514446/) | 309.866 GB | user.fye.801174.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p6697.CNF_2J_L2J_9b58101_output |

## mc23e
- r-tag=r16083
- 5.235 TB in total.

| name | task id                                             | size       | output DID                                                                         |
| ---- | --------------------------------------------------- | ---------- | ---------------------------------------------------------------------------------- |
| JZ0  | [49514457](https://bigpanda.cern.ch/task/49514457/) | 419.840 MB | user.fye.801165.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p6697.CNF_2J_L2J_d782b4b_output |
| JZ1  | [49514459](https://bigpanda.cern.ch/task/49514459/) | 560.688 MB | user.fye.801166.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p6697.CNF_2J_L2J_d782b4b_output |
| JZ2  | [49514461](https://bigpanda.cern.ch/task/49514461/) | 191.963 GB | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p6697.CNF_2J_L2J_d782b4b_output |
| JZ3  | [49514462](https://bigpanda.cern.ch/task/49514462/) | 1.246 TB   | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p6697.CNF_2J_L2J_d782b4b_output |
| JZ4  | [49514464](https://bigpanda.cern.ch/task/49514464/) | 1.592 TB   | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p6697.CNF_2J_L2J_d782b4b_output |
| JZ5  | [49514466](https://bigpanda.cern.ch/task/49514466/) | 819.503 GB | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p6697.CNF_2J_L2J_d782b4b_output |
| JZ6  | [49514468](https://bigpanda.cern.ch/task/49514468/) | 488.365 GB | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p6697.CNF_2J_L2J_d782b4b_output |
| JZ7  | [49514470](https://bigpanda.cern.ch/task/49514470/) | 325.850 GB | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p6697.CNF_2J_L2J_d782b4b_output |
| JZ8  | [49514473](https://bigpanda.cern.ch/task/49514473/) | 318.210 GB | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p6697.CNF_2J_L2J_d782b4b_output |
| JZ9  | [49514474](https://bigpanda.cern.ch/task/49514474/) | 309.600 GB | user.fye.801174.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p6697.CNF_2J_L2J_d782b4b_output |
