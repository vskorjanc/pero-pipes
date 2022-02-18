---
tags: []
---
# *EQE* containers
metadata:: [[date]]
scripts:: [[niama2_EQE_data_prep]], [[EQE_analysis]]
## Assets
### Raw

| short description                                                                               | naming convention     | example        |
| ----------------------------------------------------------------------------------------------- | --------------------- | -------------- |
| EQE spectrum output by SuSi.^[Do not add the calibration curve, the data is already calibrated] | `substrate_pixel.TQR` | `VikA01_a.TQR` |

### Global

| type   | short description                                                                      | file name    |
| ------ | -------------------------------------------------------------------------------------- | ------------ |
| AM1.5G | Link to AM1.5G spectrum in `scripts/common/EQE/reference_spectra` for calculating Jsc. | `AM1.5G.pkl` |                  

### Formatted

| type        | short description                                                                                                                                 | file name         |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- |
| EQE_df      | raw data w/ energy axis, pickled for analysis.                                                                                                    | `EQE_df.pkl`      |
| EQE_metrics | DataFrame with calculated band gap, Urbach energy, J0, Jsc and Voc,rad.^[a `.cvs` file with same data is saved in the same folder for inspection] | `EQE_metrics.pkl` |
| EQE_plot    | Plot for checking EQE analysis. Contains measured and interpolated, and curves for J0 and Jsc calculation.                                        | `EQE_plot.html`   | 


## Scripts

| file name                   | priority |             autorun             | 
| --------------------------- |:--------:|:-------------------------------:|
| [[niama2_EQE_data_prep]] |    0     | <input type="checkbox" checked> |
| [[EQE_analysis]]         |    1     | <input type="checkbox" checked> |