# *JV* containers
metadata:: [[date]]
scripts:: [[niama2_JV_data_prep]]

## Assets
### Raw

| short description   | naming convention | example      |
| ------------------- | ----------------- | ------------ |
| file output by SuSi | `substrate.txt`   | `VikA01.txt` |

### Formatted

| type       | short description                                                                                                | file name        |
| ---------- | ---------------------------------------------------------------------------------------------------------------- | ---------------- |
| JV_metrics | metrics^[J_sc, V_oc, FF, PCE, J_MPP, V_MPP, R_ser, R_par] as calculated by niama2, averaged over `for` and `rev` | `JV_metrics.pkl` |

## Scripts

| file name               | priority |             autorun             |
| ----------------------- |:--------:|:-------------------------------:|
| [[niama2_JV_data_prep]] |    0     | <input type="checkbox" checked> |