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
| name   | task id | N_files | size | output DID |
| ------ | ------- | ------- | ---- | ---------- |
| data22 |         |         |      |            |
| data23 |         |         |      |            |
| data24 |         |         |      |            |

# mc23a
- without systematics.
- total: 

## ttbar

| name      | task id | N_files | size | output DID                                                                            |
| --------- | ------- | ------- | ---- | ------------------------------------------------------------------------------------- |
| SingleLep |         |         |      | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| DiLep     |         |         |      | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |

## Wjets

| name                          | task id | N_files | size | output DID                                                                       |
| ----------------------------- | ------- | ------- | ---- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        |         |         |      | user.fye.700777.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   |         |         |      | user.fye.700778.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     |         |         |      | user.fye.700779.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Wmunu_maxHTpTV2_BFilter       |         |         |      | user.fye.700780.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  |         |         |      | user.fye.700781.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Wmunu_maxHTpTV2_CVetoBVeto    |         |         |      | user.fye.700782.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Wtaunu_maxHTpTV2_BFilter      |         |         |      | user.fye.700783.Sh.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_3ca963d_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto |         |         |      | user.fye.700784.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   |         |         |      | user.fye.700785.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |

## Zjets

| name                           | task id | N_files | size | output DID                                                                       |
| ------------------------------ | ------- | ------- | ---- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          |         |         |      | user.fye.700786.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Zee_maxHTpTV2_CFilterBVeto     |         |         |      | user.fye.700787.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Zee_maxHTpTV2_CVetoBVeto       |         |         |      | user.fye.700788.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Zmumu_maxHTpTV2_BFilter        |         |         |      | user.fye.700789.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   |         |         |      | user.fye.700790.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     |         |         |      | user.fye.700791.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Ztautau_maxHTpTV2_BFilter      |         |         |      | user.fye.700792.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto |         |         |      | user.fye.700793.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   |         |         |      | user.fye.700794.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Znunu_pTV2_BFilter             |         |         |      | user.fye.700795.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Znunu_pTV2_CFilterBVeto        |         |         |      | user.fye.700796.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |
| Znunu_pTV2_CVetoBVeto          |         |         |      | user.fye.700797.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_3ca963d_output/ |

## dijet

| name    | task id | N_files | size | output DID                                                                          |
| ------- | ------- | ------- | ---- | ----------------------------------------------------------------------------------- |
| JZ2     |         |         |      | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_3ca963d_output/ |
| JZ3     |         |         |      | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_3ca963d_output/ |
| JZ4     |         |         |      | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_3ca963d_output/ |
| JZ5     |         |         |      | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_3ca963d_output/ |
| JZ6     |         |         |      | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_3ca963d_output/ |
| JZ7     |         |         |      | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_3ca963d_output/ |
| JZ8     |         |         |      | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_3ca963d_output/ |
| JZ9incl |         |         |      | user.fye.801174.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_3ca963d_output/ |

# mc23d
- without systematics.
- total: 10977 files, 738.14 GB

## ttbar

| name      | task id                                             | N_files | size    | output DID                                                                            |
| --------- | --------------------------------------------------- | ------- | ------- | ------------------------------------------------------------------------------------- |
| SingleLep | [51677715](https://bigpanda.cern.ch/task/51677715/) | 806     | 35.1 GB | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| DiLep     | [51677719](https://bigpanda.cern.ch/task/51677719/) | 824     | 14.5 GB | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |

## Wjets

| name                          | task id                                             | N_files | size     | output DID                                                                       |
| ----------------------------- | --------------------------------------------------- | ------- | -------- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        | [51677722](https://bigpanda.cern.ch/task/51677722/) | 67      | 3.45 GB  | user.fye.700777.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   | [51677726](https://bigpanda.cern.ch/task/51677726/) | 385     | 19.16 GB | user.fye.700778.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     | [51677730](https://bigpanda.cern.ch/task/51677730/) | 150     | 35.85 GB | user.fye.700779.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wmunu_maxHTpTV2_BFilter       | [51677734](https://bigpanda.cern.ch/task/51677734/) | 63      | 2.59 GB  | user.fye.700780.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  | [51677737](https://bigpanda.cern.ch/task/51677737/) | 470     | 13.46 GB | user.fye.700781.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output  |
| Wmunu_maxHTpTV2_CVetoBVeto    | [51677740](https://bigpanda.cern.ch/task/51677740/) | 925     | 25.03 GB | user.fye.700782.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wtaunu_maxHTpTV2_BFilter      | [51677744](https://bigpanda.cern.ch/task/51677744/) | 72      | 5.83 GB  | user.fye.700783.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto | [51677748](https://bigpanda.cern.ch/task/51677748/) | 497     | 34.39 GB | user.fye.700784.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   | [51677751](https://bigpanda.cern.ch/task/51677751/) | 867     | 61.83 GB | user.fye.700785.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |

## Zjets

| name                           | task id                                             | N_files | size     | output DID                                                                       |
| ------------------------------ | --------------------------------------------------- | ------- | -------- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          | [51677754](https://bigpanda.cern.ch/task/51677754/) | 109     | 2.94 GB  | user.fye.700786.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Zee_maxHTpTV2_CFilterBVeto     | [51677756](https://bigpanda.cern.ch/task/51677756/) | 226     | 6.13 GB  | user.fye.700787.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Zee_maxHTpTV2_CVetoBVeto       | [51677758](https://bigpanda.cern.ch/task/51677758/) | 834     | 23.77 GB | user.fye.700788.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| Zmumu_maxHTpTV2_BFilter        | [51677760](https://bigpanda.cern.ch/task/51677760/) | 127     | 1.51 GB  | user.fye.700789.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   | [51677763](https://bigpanda.cern.ch/task/51677763/) | 165     | 3.26 GB  | user.fye.700790.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     | [51677764](https://bigpanda.cern.ch/task/51677764/) | 981     | 12.09 GB | user.fye.700791.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| Ztautau_maxHTpTV2_BFilter      | [51677765](https://bigpanda.cern.ch/task/51677765/) | 88      | 9.3 GB   | user.fye.700792.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto | [51677767](https://bigpanda.cern.ch/task/51677767/) | 226     | 18.75 GB | user.fye.700793.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   | [51677769](https://bigpanda.cern.ch/task/51677769/) | 158     | 71.34 GB | user.fye.700794.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |
| Znunu_pTV2_BFilter             | [51677771](https://bigpanda.cern.ch/task/51677771/) | 56      | 4.48 GB  | user.fye.700795.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Znunu_pTV2_CFilterBVeto        | [51677773](https://bigpanda.cern.ch/task/51677773/) | 192     | 13.22 GB | user.fye.700796.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| Znunu_pTV2_CVetoBVeto          | [51677774](https://bigpanda.cern.ch/task/51677774/) | 621     | 38.19 GB | user.fye.700797.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_f6a173e_output/ |

## dijet

| name    | task id                                             | N_files | size     | output DID                                                                          |
| ------- | --------------------------------------------------- | ------- | -------- | ----------------------------------------------------------------------------------- |
| JZ2     | [51677776](https://bigpanda.cern.ch/task/51677776/) | 130     | 16.81 GB | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ3     | [51677777](https://bigpanda.cern.ch/task/51677777/) | 369     | 64.69 GB | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ4     | [51677778](https://bigpanda.cern.ch/task/51677778/) | 516     | 82.34 GB | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ5     | [51677780](https://bigpanda.cern.ch/task/51677780/) | 465     | 42.86 GB | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ6     | [51677782](https://bigpanda.cern.ch/task/51677782/) | 188     | 25.73 GB | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ7     | [51677784](https://bigpanda.cern.ch/task/51677784/) | 132     | 16.98 GB | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ8     | [51677785](https://bigpanda.cern.ch/task/51677785/) | 139     | 16.52 GB | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |
| JZ9incl | [51677787](https://bigpanda.cern.ch/task/51677787/) | 129     | 16.03 GB | user.fye.801174.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_f6a173e_output/ |

# mc23e
- without systematics.
- total: 11222 files, 658.13 GB

## ttbar

| name      | task id                                             | N_files | size     | output DID                                                                            |
| --------- | --------------------------------------------------- | ------- | -------- | ------------------------------------------------------------------------------------- |
| SingleLep | [51693208](https://bigpanda.cern.ch/task/51693208/) | 940     | 35.32 GB | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| DiLep     | [51693210](https://bigpanda.cern.ch/task/51693210/) | 848     | 14.67 GB | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |

## Wjets

| name                          | task id                                             | N_files | size     | output DID                                                                       |
| ----------------------------- | --------------------------------------------------- | ------- | -------- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        | [51693213](https://bigpanda.cern.ch/task/51693213/) | 63      | 3.19 GB  | user.fye.700777.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   | [51693215](https://bigpanda.cern.ch/task/51693215/) | 598     | 17.65 GB | user.fye.700778.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     | [51693218](https://bigpanda.cern.ch/task/51693218/) | 1008    | 36.75 GB | user.fye.700779.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wmunu_maxHTpTV2_BFilter       | [51693221](https://bigpanda.cern.ch/task/51693221/) | 54      | 2.55 GB  | user.fye.700780.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  | [51693223](https://bigpanda.cern.ch/task/51693223/) | 268     | 13.45 GB | user.fye.700781.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wmunu_maxHTpTV2_CVetoBVeto    | [51693226](https://bigpanda.cern.ch/task/51693226/) | 740     | 25.13 GB | user.fye.700782.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wtaunu_maxHTpTV2_BFilter      | [51693228](https://bigpanda.cern.ch/task/51693228/) | 55      | 5.85 GB  | user.fye.700783.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto | [51693231](https://bigpanda.cern.ch/task/51693231/) | 170     | 20.62 GB | user.fye.700784.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   | [51693234](https://bigpanda.cern.ch/task/51693234/) | 196     | 56.36 GB | user.fye.700785.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |

## Zjets

| name                           | task id                                             | N_files | size     | output DID                                                                       |
| ------------------------------ | --------------------------------------------------- | ------- | -------- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          | [51693236](https://bigpanda.cern.ch/task/51693236/) | 120     | 2.95 GB  | user.fye.700786.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Zee_maxHTpTV2_CFilterBVeto     | [51693239](https://bigpanda.cern.ch/task/51693239/) | 189     | 6.2 GB   | user.fye.700787.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Zee_maxHTpTV2_CVetoBVeto       | [51693242](https://bigpanda.cern.ch/task/51693242/) | 1086    | 23.89 GB | user.fye.700788.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Zmumu_maxHTpTV2_BFilter        | [51693243](https://bigpanda.cern.ch/task/51693243/) | 109     | 1.52 GB  | user.fye.700789.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   | [51693246](https://bigpanda.cern.ch/task/51693246/) | 183     | 3.34 GB  | user.fye.700790.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     | [51693249](https://bigpanda.cern.ch/task/51693249/) | 821     | 11.97 GB | user.fye.700791.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Ztautau_maxHTpTV2_BFilter      | [51693251](https://bigpanda.cern.ch/task/51693251/) | 107     | 9.33 GB  | user.fye.700792.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto | [51693253](https://bigpanda.cern.ch/task/51693253/) | 319     | 19.07 GB | user.fye.700793.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   | [51693256](https://bigpanda.cern.ch/task/51693256/) | 251     | 14.33 GB | user.fye.700794.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Znunu_pTV2_BFilter             | [51693258](https://bigpanda.cern.ch/task/51693258/) | 66      | 4.47 GB  | user.fye.700795.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Znunu_pTV2_CFilterBVeto        | [51693260](https://bigpanda.cern.ch/task/51693260/) | 183     | 13.29 GB | user.fye.700796.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| Znunu_pTV2_CVetoBVeto          | [51693263](https://bigpanda.cern.ch/task/51693263/) | 632     | 38.52 GB | user.fye.700797.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |

## dijet

| name    | task id                                             | N_files | size     | output DID                                                                          |
| ------- | --------------------------------------------------- | ------- | -------- | ----------------------------------------------------------------------------------- |
| JZ2     | [51693266](https://bigpanda.cern.ch/task/51693266/) | 245     | 15.82 GB | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ3     | [51693268](https://bigpanda.cern.ch/task/51693268/) | 373     | 61.75 GB | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ4     | [51693271](https://bigpanda.cern.ch/task/51693271/) | 684     | 81.93 GB | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ5     | [51693274](https://bigpanda.cern.ch/task/51693274/) | 336     | 42.95 GB | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ6     | [51693277](https://bigpanda.cern.ch/task/51693277/) | 176     | 25.65 GB | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ7     | [51693280](https://bigpanda.cern.ch/task/51693280/) | 130     | 17.03 GB | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ8     | [51693283](https://bigpanda.cern.ch/task/51693283/) | 140     | 16.58 GB | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
| JZ9incl | [51693286](https://bigpanda.cern.ch/task/51693286/) | 132     | 16 GB    | user.fye.801174.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_43ccc0c_output/ |
