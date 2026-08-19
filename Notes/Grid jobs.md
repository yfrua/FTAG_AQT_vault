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
- append the line number at the end of each line in vim: `:%s/$/\=line('.')`

# data
| name   | task id                                             | N_files | size | output DID                                                                               |
| ------ | --------------------------------------------------- | ------- | ---- | ---------------------------------------------------------------------------------------- |
| data22 | [52060619](https://bigpanda.cern.ch/task/52060619/) |         |      | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp22_v01_p7019.CNF_2J_L2J_5062f37_output/ |
| data23 | [52061004](https://bigpanda.cern.ch/task/52061004/) |         |      | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp23_v01_p7019.CNF_2J_L2J_ada3219_output/ |
| data24 |                                                     |         |      |                                                                                          |

# mc23a
- without systematics.
- total: 

## ttbar

| name      | task id                                             | N_files | size | output DID                                                                            |
| --------- | --------------------------------------------------- | ------- | ---- | ------------------------------------------------------------------------------------- |
| SingleLep | [52060672](https://bigpanda.cern.ch/task/52060672/) |         |      | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| DiLep     | [52060675](https://bigpanda.cern.ch/task/52060675/) |         |      | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |

## Wjets

| name                          | task id                                             | N_files | size | output DID                                                                       |
| ----------------------------- | --------------------------------------------------- | ------- | ---- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        | [52060677](https://bigpanda.cern.ch/task/52060677/) |         |      | user.fye.700777.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   | [52060680](https://bigpanda.cern.ch/task/52060680/) |         |      | user.fye.700778.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     | [52060682](https://bigpanda.cern.ch/task/52060682/) |         |      | user.fye.700779.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wmunu_maxHTpTV2_BFilter       | [52060685](https://bigpanda.cern.ch/task/52060685/) |         |      | user.fye.700780.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  | [52060688](https://bigpanda.cern.ch/task/52060688/) |         |      | user.fye.700781.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wmunu_maxHTpTV2_CVetoBVeto    | [52060691](https://bigpanda.cern.ch/task/52060691/) |         |      | user.fye.700782.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wtaunu_maxHTpTV2_BFilter      | [52060694](https://bigpanda.cern.ch/task/52060694/) |         |      | user.fye.700783.Sh.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto | [52060696](https://bigpanda.cern.ch/task/52060696/) |         |      | user.fye.700784.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   | [52060699](https://bigpanda.cern.ch/task/52060699/) |         |      | user.fye.700785.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |

## Zjets

| name                           | task id                                             | N_files | size | output DID                                                                       |
| ------------------------------ | --------------------------------------------------- | ------- | ---- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          | [52060701](https://bigpanda.cern.ch/task/52060701/) |         |      | user.fye.700786.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Zee_maxHTpTV2_CFilterBVeto     | [52060703](https://bigpanda.cern.ch/task/52060703/) |         |      | user.fye.700787.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Zee_maxHTpTV2_CVetoBVeto       | [52060706](https://bigpanda.cern.ch/task/52060706/) |         |      | user.fye.700788.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Zmumu_maxHTpTV2_BFilter        | [52060708](https://bigpanda.cern.ch/task/52060708/) |         |      | user.fye.700789.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   | [52060711](https://bigpanda.cern.ch/task/52060711/) |         |      | user.fye.700790.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     | [52060714](https://bigpanda.cern.ch/task/52060714/) |         |      | user.fye.700791.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Ztautau_maxHTpTV2_BFilter      | [52060717](https://bigpanda.cern.ch/task/52060717/) |         |      | user.fye.700792.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto | [52060720](https://bigpanda.cern.ch/task/52060720/) |         |      | user.fye.700793.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   | [52060722](https://bigpanda.cern.ch/task/52060722/) |         |      | user.fye.700794.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Znunu_pTV2_BFilter             | [52060724](https://bigpanda.cern.ch/task/52060724/) |         |      | user.fye.700795.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Znunu_pTV2_CFilterBVeto        | [52060727](https://bigpanda.cern.ch/task/52060727/) |         |      | user.fye.700796.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Znunu_pTV2_CVetoBVeto          | [52060730](https://bigpanda.cern.ch/task/52060730/) |         |      | user.fye.700797.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |

## dijet

| name | task id                                             | N_files | size | output DID                                                                          |
| ---- | --------------------------------------------------- | ------- | ---- | ----------------------------------------------------------------------------------- |
| JZ2  | [52060733](https://bigpanda.cern.ch/task/52060733/) |         |      | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ3  | [52060736](https://bigpanda.cern.ch/task/52060736/) |         |      | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ4  | [52060738](https://bigpanda.cern.ch/task/52060738/) |         |      | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ5  | [52060741](https://bigpanda.cern.ch/task/52060741/) |         |      | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ6  | [52060744](https://bigpanda.cern.ch/task/52060744/) |         |      | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ7  | [52060746](https://bigpanda.cern.ch/task/52060746/) |         |      | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ8  | [52060749](https://bigpanda.cern.ch/task/52060749/) |         |      | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |


# mc23d
- without systematics.
- total: 

## ttbar

| name      | task id | N_files | size | output DID                                                                            |
| --------- | ------- | ------- | ---- | ------------------------------------------------------------------------------------- |
| SingleLep |         |         |      | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| DiLep     |         |         |      | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |

## Wjets

| name                          | task id | N_files | size | output DID                                                                       |
| ----------------------------- | ------- | ------- | ---- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        |         |         |      | user.fye.700777.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   |         |         |      | user.fye.700778.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     |         |         |      | user.fye.700779.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wmunu_maxHTpTV2_BFilter       |         |         |      | user.fye.700780.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  |         |         |      | user.fye.700781.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output  |
| Wmunu_maxHTpTV2_CVetoBVeto    |         |         |      | user.fye.700782.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wtaunu_maxHTpTV2_BFilter      |         |         |      | user.fye.700783.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto |         |         |      | user.fye.700784.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   |         |         |      | user.fye.700785.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |

## Zjets

| name                           | task id | N_files | size | output DID                                                                       |
| ------------------------------ | ------- | ------- | ---- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          |         |         |      | user.fye.700786.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Zee_maxHTpTV2_CFilterBVeto     |         |         |      | user.fye.700787.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Zee_maxHTpTV2_CVetoBVeto       |         |         |      | user.fye.700788.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| Zmumu_maxHTpTV2_BFilter        |         |         |      | user.fye.700789.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   |         |         |      | user.fye.700790.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     |         |         |      | user.fye.700791.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| Ztautau_maxHTpTV2_BFilter      |         |         |      | user.fye.700792.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto |         |         |      | user.fye.700793.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   |         |         |      | user.fye.700794.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| Znunu_pTV2_BFilter             |         |         |      | user.fye.700795.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Znunu_pTV2_CFilterBVeto        |         |         |      | user.fye.700796.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Znunu_pTV2_CVetoBVeto          |         |         |      | user.fye.700797.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |

## dijet

| name | task id | N_files | size | output DID                                                                          |
| ---- | ------- | ------- | ---- | ----------------------------------------------------------------------------------- |
| JZ2  |         |         |      | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ3  |         |         |      | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ4  |         |         |      | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ5  |         |         |      | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ6  |         |         |      | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ7  |         |         |      | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ8  |         |         |      | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |


# mc23e
- without systematics.
- total: 

## ttbar

| name      | task id | N_files | size | output DID                                                                            |
| --------- | ------- | ------- | ---- | ------------------------------------------------------------------------------------- |
| SingleLep |         |         |      | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| DiLep     |         |         |      | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |

## Wjets

| name                          | task id | N_files | size | output DID                                                                       |
| ----------------------------- | ------- | ------- | ---- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        |         |         |      | user.fye.700777.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   |         |         |      | user.fye.700778.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     |         |         |      | user.fye.700779.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wmunu_maxHTpTV2_BFilter       |         |         |      | user.fye.700780.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  |         |         |      | user.fye.700781.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wmunu_maxHTpTV2_CVetoBVeto    |         |         |      | user.fye.700782.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wtaunu_maxHTpTV2_BFilter      |         |         |      | user.fye.700783.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto |         |         |      | user.fye.700784.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   |         |         |      | user.fye.700785.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |

## Zjets

| name                           | task id | N_files | size | output DID                                                                       |
| ------------------------------ | ------- | ------- | ---- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          |         |         |      | user.fye.700786.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Zee_maxHTpTV2_CFilterBVeto     |         |         |      | user.fye.700787.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Zee_maxHTpTV2_CVetoBVeto       |         |         |      | user.fye.700788.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Zmumu_maxHTpTV2_BFilter        |         |         |      | user.fye.700789.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   |         |         |      | user.fye.700790.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     |         |         |      | user.fye.700791.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Ztautau_maxHTpTV2_BFilter      |         |         |      | user.fye.700792.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto |         |         |      | user.fye.700793.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   |         |         |      | user.fye.700794.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Znunu_pTV2_BFilter             |         |         |      | user.fye.700795.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Znunu_pTV2_CFilterBVeto        |         |         |      | user.fye.700796.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Znunu_pTV2_CVetoBVeto          |         |         |      | user.fye.700797.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |

## dijet

| name    | task id | N_files | size | output DID                                                                          |
| ------- | ------- | ------- | ---- | ----------------------------------------------------------------------------------- |
| JZ2     |         |         |      | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ3     |         |         |      | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ4     |         |         |      | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ5     |         |         |      | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ6     |         |         |      | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ7     |         |         |      | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ8     |         |         |      | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |

