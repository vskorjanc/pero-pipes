# *JV* containers
*JV* scans measured in a same instance. 
If the container contains multiple measurements for the same substrate and pixel, only the last measurement is taken into account for further analysis. The measurement order is determined by sorting the files by name, e.g.:  

``` mermaid
flowchart LR
JV --- A(VikA01.d0_01.txt) & B(VikA01.d0_02.txt) & C(VikA02.d0_01.txt) & D(VikA03.d0_01.txt) & E(VikA03.d0_02.txt) & F(VikA01.d0_03.txt)
subgraph VikA01
A & B
end
subgraph VikA02
C
end
subgraph VikA03
D & E & F
end

classDef green fill:#61FF8C,stroke:#23C552;
classDef red fill:#FF827A,stroke:#F84F31;
class A,D,E red;
class B,C,F green;
```
Files kept for further analysis are colored green.
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
| JV_metrics | metrics[^1] as calculated by niama2, averaged over `for` and `rev` | `JV_metrics.pkl` |

## Scripts

| file name               | priority |             autorun             |
| ----------------------- |:--------:|:-------------------------------:|
| `niama2_JV_data_prep.py` |    0     | <input type="checkbox" checked> |

[^1]: J_sc, V_oc, FF, PCE, J_MPP, V_MPP, R_ser, R_par