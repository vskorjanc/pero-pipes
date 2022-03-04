---
tags: [evaporation]
---
# *evap_logs* containers

## Assets
### Raw

| short description                                                                                          | naming convention       | example                 |
| ---------------------------------------------------------------------------------------------------------- | ----------------------- | ----------------------- |
| log files output by PeroVap. File path: `C:\Logs\ProcessLog\<startTime>`. Add all the files in the folder! | defined by the software | `XL_LTE1_LifeTime0.csv` |

### Formatted

| type          | short description       | file name                |
| ------------- | ----------------------- | ------------------------ |
| evap_log_plot | plot of a single source | `<source>_log_plot.html` | 

## Scripts

| file name                   | priority |             autorun             |
| --------------------------- |:--------:|:-------------------------------:|
| `peroVap_log_data_prep.py` |    0     | <input type="checkbox" checked> |
| `peroVap_log_analysis.py`    |    1     | <input type="checkbox" checked> |
