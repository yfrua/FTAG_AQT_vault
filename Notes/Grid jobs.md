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
| name   | task id                                             | output DID                                                                               |
| ------ | --------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| data22 | [52060619](https://bigpanda.cern.ch/task/52060619/) | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp22_v01_p7019.CNF_2J_L2J_5062f37_output/ |
| data23 | [52061004](https://bigpanda.cern.ch/task/52061004/) | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp23_v01_p7019.CNF_2J_L2J_ada3219_output/ |
| data24 | [52061136](https://bigpanda.cern.ch/task/52061136/) | user.fye.periodAllYear.physics_Main.DAOD_PHYS.grp24_v01_p7019.CNF_2J_L2J_d09778b_output/ |

# mc23a
- without systematics.
- total: 

## ttbar

| name      | task id                                             | output DID                                                                            |
| --------- | --------------------------------------------------- | ------------------------------------------------------------------------------------- |
| SingleLep | [52060672](https://bigpanda.cern.ch/task/52060672/) | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| DiLep     | [52060675](https://bigpanda.cern.ch/task/52060675/) | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |

## Wjets

| name                          | task id                                             | output DID                                                                       |
| ----------------------------- | --------------------------------------------------- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        | [52060677](https://bigpanda.cern.ch/task/52060677/) | user.fye.700777.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   | [52060680](https://bigpanda.cern.ch/task/52060680/) | user.fye.700778.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     | [52060682](https://bigpanda.cern.ch/task/52060682/) | user.fye.700779.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wmunu_maxHTpTV2_BFilter       | [52060685](https://bigpanda.cern.ch/task/52060685/) | user.fye.700780.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  | [52060688](https://bigpanda.cern.ch/task/52060688/) | user.fye.700781.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wmunu_maxHTpTV2_CVetoBVeto    | [52060691](https://bigpanda.cern.ch/task/52060691/) | user.fye.700782.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wtaunu_maxHTpTV2_BFilter      | [52060694](https://bigpanda.cern.ch/task/52060694/) | user.fye.700783.Sh.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto | [52060696](https://bigpanda.cern.ch/task/52060696/) | user.fye.700784.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   | [52060699](https://bigpanda.cern.ch/task/52060699/) | user.fye.700785.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |

## Zjets

| name                           | task id                                             | output DID                                                                       |
| ------------------------------ | --------------------------------------------------- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          | [52060701](https://bigpanda.cern.ch/task/52060701/) | user.fye.700786.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Zee_maxHTpTV2_CFilterBVeto     | [52060703](https://bigpanda.cern.ch/task/52060703/) | user.fye.700787.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Zee_maxHTpTV2_CVetoBVeto       | [52060706](https://bigpanda.cern.ch/task/52060706/) | user.fye.700788.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Zmumu_maxHTpTV2_BFilter        | [52060708](https://bigpanda.cern.ch/task/52060708/) | user.fye.700789.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   | [52060711](https://bigpanda.cern.ch/task/52060711/) | user.fye.700790.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     | [52060714](https://bigpanda.cern.ch/task/52060714/) | user.fye.700791.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Ztautau_maxHTpTV2_BFilter      | [52060717](https://bigpanda.cern.ch/task/52060717/) | user.fye.700792.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto | [52060720](https://bigpanda.cern.ch/task/52060720/) | user.fye.700793.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   | [52060722](https://bigpanda.cern.ch/task/52060722/) | user.fye.700794.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Znunu_pTV2_BFilter             | [52060724](https://bigpanda.cern.ch/task/52060724/) | user.fye.700795.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Znunu_pTV2_CFilterBVeto        | [52060727](https://bigpanda.cern.ch/task/52060727/) | user.fye.700796.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |
| Znunu_pTV2_CVetoBVeto          | [52060730](https://bigpanda.cern.ch/task/52060730/) | user.fye.700797.Sh.DAOD_PHYS.e8514_s4162_r15540_p7017.CNF_2J_L2J_6bf1c92_output/ |

## dijet

| name | task id                                             | output DID                                                                          |
| ---- | --------------------------------------------------- | ----------------------------------------------------------------------------------- |
| JZ2  | [52060733](https://bigpanda.cern.ch/task/52060733/) | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ3  | [52060736](https://bigpanda.cern.ch/task/52060736/) | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ4  | [52060738](https://bigpanda.cern.ch/task/52060738/) | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ5  | [52060741](https://bigpanda.cern.ch/task/52060741/) | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ6  | [52060744](https://bigpanda.cern.ch/task/52060744/) | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ7  | [52060746](https://bigpanda.cern.ch/task/52060746/) | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |
| JZ8  | [52060749](https://bigpanda.cern.ch/task/52060749/) | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4162_r14622_p7017.CNF_2J_L2J_6bf1c92_output/ |


# mc23d
- without systematics.
- total: 

## ttbar

| name      | task id                                             | output DID                                                                            |
| --------- | --------------------------------------------------- | ------------------------------------------------------------------------------------- |
| SingleLep | [52061045](https://bigpanda.cern.ch/task/52061045/) | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_118f3cf_output/ |
| DiLep     | [52061049](https://bigpanda.cern.ch/task/52061049/) | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_118f3cf_output/ |

## Wjets

| name                          | task id                                             | output DID                                                                       |
| ----------------------------- | --------------------------------------------------- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        | [52061051](https://bigpanda.cern.ch/task/52061051/) | user.fye.700777.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   | [52061055](https://bigpanda.cern.ch/task/52061055/) | user.fye.700778.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     | [52061059](https://bigpanda.cern.ch/task/52061059/) | user.fye.700779.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_118f3cf_output/ |
| Wmunu_maxHTpTV2_BFilter       | [52061061](https://bigpanda.cern.ch/task/52061061/) | user.fye.700780.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  | [52061064](https://bigpanda.cern.ch/task/52061064/) | user.fye.700781.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output  |
| Wmunu_maxHTpTV2_CVetoBVeto    | [52061066](https://bigpanda.cern.ch/task/52061066/) | user.fye.700782.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_118f3cf_output/ |
| Wtaunu_maxHTpTV2_BFilter      | [52061069](https://bigpanda.cern.ch/task/52061069/) | user.fye.700783.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto | [52061072](https://bigpanda.cern.ch/task/52061072/) | user.fye.700784.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   | [52061074](https://bigpanda.cern.ch/task/52061074/) | user.fye.700785.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_118f3cf_output/ |

## Zjets

| name                           | task id                                             | output DID                                                                       |
| ------------------------------ | --------------------------------------------------- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          | [52061077](https://bigpanda.cern.ch/task/52061077/) | user.fye.700786.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Zee_maxHTpTV2_CFilterBVeto     | [52061080](https://bigpanda.cern.ch/task/52061080/) | user.fye.700787.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Zee_maxHTpTV2_CVetoBVeto       | [52061083](https://bigpanda.cern.ch/task/52061083/) | user.fye.700788.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_118f3cf_output/ |
| Zmumu_maxHTpTV2_BFilter        | [52061086](https://bigpanda.cern.ch/task/52061086/) | user.fye.700789.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   | [52061089](https://bigpanda.cern.ch/task/52061089/) | user.fye.700790.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     | [52061091](https://bigpanda.cern.ch/task/52061091/) | user.fye.700791.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_118f3cf_output/ |
| Ztautau_maxHTpTV2_BFilter      | [52061094](https://bigpanda.cern.ch/task/52061094/) | user.fye.700792.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto | [52061097](https://bigpanda.cern.ch/task/52061097/) | user.fye.700793.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   | [52061100](https://bigpanda.cern.ch/task/52061100/) | user.fye.700794.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_118f3cf_output/ |
| Znunu_pTV2_BFilter             | [52061101](https://bigpanda.cern.ch/task/52061101/) | user.fye.700795.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Znunu_pTV2_CFilterBVeto        | [52061104](https://bigpanda.cern.ch/task/52061104/) | user.fye.700796.Sh.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| Znunu_pTV2_CVetoBVeto          | [52061106](https://bigpanda.cern.ch/task/52061106/) | user.fye.700797.Sh.DAOD_PHYS.e8514_s4159_r15530_p7017.CNF_2J_L2J_118f3cf_output/ |

## dijet

| name | task id                                             | output DID                                                                          |
| ---- | --------------------------------------------------- | ----------------------------------------------------------------------------------- |
| JZ2  | [52061109](https://bigpanda.cern.ch/task/52061109/) | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| JZ3  | [52061111](https://bigpanda.cern.ch/task/52061111/) | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| JZ4  | [52061113](https://bigpanda.cern.ch/task/52061113/) | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| JZ5  | [52061116](https://bigpanda.cern.ch/task/52061116/) | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| JZ6  | [52061118](https://bigpanda.cern.ch/task/52061118/) | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| JZ7  | [52061120](https://bigpanda.cern.ch/task/52061120/) | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |
| JZ8  | [52061122](https://bigpanda.cern.ch/task/52061122/) | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4159_r15224_p7017.CNF_2J_L2J_118f3cf_output/ |


# mc23e
- without systematics.
- total: 

## ttbar

| name      | task id                                             | output DID                                                                            |
| --------- | --------------------------------------------------- | ------------------------------------------------------------------------------------- |
| SingleLep | [52061177](https://bigpanda.cern.ch/task/52061177/) | user.fye.601229.PhPy8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| DiLep     | [52061180](https://bigpanda.cern.ch/task/52061180/) | user.fye.601230.PhPy8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |

## Wjets

| name                          | task id                                             | output DID                                                                       |
| ----------------------------- | --------------------------------------------------- | -------------------------------------------------------------------------------- |
| Wenu_maxHTpTV2_BFilter        | [52061182](https://bigpanda.cern.ch/task/52061182/) | user.fye.700777.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Wenu_maxHTpTV2_CFilterBVeto   | [52061185](https://bigpanda.cern.ch/task/52061185/) | user.fye.700778.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Wenu_maxHTpTV2_CVetoBVeto     | [52061188](https://bigpanda.cern.ch/task/52061188/) | user.fye.700779.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Wmunu_maxHTpTV2_BFilter       | [52061190](https://bigpanda.cern.ch/task/52061190/) | user.fye.700780.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Wmunu_maxHTpTV2_CFilterBVeto  | [52061192](https://bigpanda.cern.ch/task/52061192/) | user.fye.700781.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Wmunu_maxHTpTV2_CVetoBVeto    | [52061195](https://bigpanda.cern.ch/task/52061195/) | user.fye.700782.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Wtaunu_maxHTpTV2_BFilter      | [52061198](https://bigpanda.cern.ch/task/52061198/) | user.fye.700783.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Wtaunu_maxHTpTV2_CFilterBVeto | [52061201](https://bigpanda.cern.ch/task/52061201/) | user.fye.700784.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Wtaunu_maxHTpTV2_CVetoBVeto   | [52061204](https://bigpanda.cern.ch/task/52061204/) | user.fye.700785.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |

## Zjets

| name                           | task id                                             | output DID                                                                       |
| ------------------------------ | --------------------------------------------------- | -------------------------------------------------------------------------------- |
| Zee_maxHTpTV2_BFilter          | [52061205](https://bigpanda.cern.ch/task/52061205/) | user.fye.700786.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Zee_maxHTpTV2_CFilterBVeto     | [52061208](https://bigpanda.cern.ch/task/52061208/) | user.fye.700787.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Zee_maxHTpTV2_CVetoBVeto       | [52061211](https://bigpanda.cern.ch/task/52061211/) | user.fye.700788.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Zmumu_maxHTpTV2_BFilter        | [52061214](https://bigpanda.cern.ch/task/52061214/) | user.fye.700789.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Zmumu_maxHTpTV2_CFilterBVeto   | [52061219](https://bigpanda.cern.ch/task/52061219/) | user.fye.700790.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Zmumu_maxHTpTV2_CVetoBVeto     | [52061221](https://bigpanda.cern.ch/task/52061221/) | user.fye.700791.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Ztautau_maxHTpTV2_BFilter      | [52061224](https://bigpanda.cern.ch/task/52061224/) | user.fye.700792.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Ztautau_maxHTpTV2_CFilterBVeto | [52061227](https://bigpanda.cern.ch/task/52061227/) | user.fye.700793.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Ztautau_maxHTpTV2_CVetoBVeto   | [52061230](https://bigpanda.cern.ch/task/52061230/) | user.fye.700794.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Znunu_pTV2_BFilter             | [52061233](https://bigpanda.cern.ch/task/52061233/) | user.fye.700795.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Znunu_pTV2_CFilterBVeto        | [52061236](https://bigpanda.cern.ch/task/52061236/) | user.fye.700796.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| Znunu_pTV2_CVetoBVeto          | [52061237](https://bigpanda.cern.ch/task/52061237/) | user.fye.700797.Sh.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |

## dijet

| name | task id                                             | output DID                                                                          |
| ---- | --------------------------------------------------- | ----------------------------------------------------------------------------------- |
| JZ2  | [52061240](https://bigpanda.cern.ch/task/52061240/) | user.fye.801167.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| JZ3  | [52061243](https://bigpanda.cern.ch/task/52061243/) | user.fye.801168.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| JZ4  | [52061246](https://bigpanda.cern.ch/task/52061246/) | user.fye.801169.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| JZ5  | [52061248](https://bigpanda.cern.ch/task/52061248/) | user.fye.801170.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| JZ6  | [52061251](https://bigpanda.cern.ch/task/52061251/) | user.fye.801171.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| JZ7  | [52061254](https://bigpanda.cern.ch/task/52061254/) | user.fye.801172.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |
| JZ8  | [52061257](https://bigpanda.cern.ch/task/52061257/) | user.fye.801173.Py8EG.DAOD_PHYS.e8514_s4369_r16083_p7017.CNF_2J_L2J_cbdeb73_output/ |

