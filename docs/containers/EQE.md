---
tags: []
---
# *EQE* containers
## Metadata
- [[date]]

## Assets
### Raw

| short description                                                                               | naming convention     | example        |
| ----------------------------------------------------------------------------------------------- | --------------------- | -------------- |
| EQE spectrum output by SuSi.[^1] | `substrate_pixel.TQR` | `VikA01_a.TQR` |

### Global

| type   | short description                                                                      | file name    |
| ------ | -------------------------------------------------------------------------------------- | ------------ |
| AM1.5G | Link to AM1.5G spectrum in `scripts/common/EQE/reference_spectra` for calculating Jsc. | `AM1.5G.pkl` |                  

### Formatted

| type        | short description                                                                                                                                 | file name         |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- |
| EQE_df      | raw data w/ energy axis, pickled for analysis.                                                                                                    | `EQE_df.pkl`      |
| EQE_metrics | DataFrame with calculated band gap, Urbach energy, J0, Jsc and Voc,rad.[^2] | `EQE_metrics.pkl` |
| EQE_plot    | Plot for checking EQE analysis. Contains measured and interpolated, and curves for J0 and Jsc calculation.                                        | `EQE_plot.html`   | 


## Scripts

| file name                   | priority |             autorun             | 
| --------------------------- |:--------:|:-------------------------------:|
| `niama2_EQE_data_prep.py` |    0     | <input type="checkbox" checked> |
| `EQE_analysis.py`         |    1     | <input type="checkbox" checked> |

[^1]: Do not add the calibration curve as an asset, the data is already calibrated. It is nevertheless recommended to add it to the folder to keep the data together.
[^2]: a `.cvs` file with same data is saved in the same folder for inspection