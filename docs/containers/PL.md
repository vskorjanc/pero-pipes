# *PL* containers
metadata:: [[date]]
scripts:: [[BQY_data_prep]], [[absolute_PL]]


## Assets
### Raw

| short description             | naming convention                                                                   | example        |
| ----------------------------- | ----------------------------------------------------------------------------------- | -------------- |
| File output by the BQY setup. | `substrate_mesNumber.txt`^[Old convention also possible, defined in the asset note] | `VikA01_1.txt` |

### Global
| type         | short description                                     | name               |
| ------------ | ----------------------------------------------------- | ------------------ |
| BQY_calib_df | Link to calibration file in `scripts/common/PL/calib` | `BQY_calib_df.pkl` |

### Formatted

| type       | file extension | short description                                                                                                                   |
| ---------- | -------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| PL_df      | PKL            | Imported and calibrated raw data pickled for analysis.                                                                              |
| PL_metrics | PKL            | DataFrame with calculated QFLS, temperature and band gap.^[a `.cvs` file with same data is saved in the same folder for inspection] |
| PL_plot    | HTML           | Plot of the PL spectra of a single substrate zoomed-in into the 1.5 - 1.9 eV region. Double click to see the full spectrum.         |
| HETF_plot  | HTML           | Plot of log of PL and the linear fit for HETF.                                                                                                                                    |


## Scripts
| file name         | priority |             autorun             |
| ----------------- |:--------:|:-------------------------------:|
| [[BQY_data_prep]] |    0     | <input type="checkbox" checked> |
| [[absolute_PL]]   |    1     | <input type="checkbox" checked> |
