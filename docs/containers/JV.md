# *JV* containers
*JV* scans measured in the same instance. 
If measured data for the same substrate and pixel are added within the same container, only the last measurement is kept. The measurement order is determined by sorting the files by name, e.g. (files kept shown in green):  

``` mermaid
flowchart LR
JV --- A(VikA01.d0_01.txt) & B(VikA01.d0_02.txt) & C(VikA02.d0_01.txt) & D(VikA03.d0_01.txt) & E(VikA03.d0_02.txt) & F(VikA01.d0_03.txt)

classDef green fill:#23C552;
classDef red fill:#F84F31;
class A,D,E red;
- class B,C,F green;
```
## Metadata
- [[date]]


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
| `niama2_JV_data_prep.py` |    0     | <input type="checkbox" checked> |