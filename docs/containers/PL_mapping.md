---
tags: [gradient]
---
# *PL_mapping* containers
## Metadata
- [[date]]

## Assets
### Raw

| type               | short description    | naming convention | example      |
| ------------------ | -------------------- | ----------------- | ------------ |
| PL_mapping_spectra | raw spectra          | `substrate.txt`   | `VikG01.txt` |
| PL_mapping_meta    | measurement metadata | `substrate.tvb`   | `VikG01.tvb` |

### Formatted

| type                  | short description                                  | file name               |
| --------------------- | -------------------------------------------------- | ----------------------- |
| PL_mapping_df         | imported raw data pickled for analysis             | `PL_mapping_df.pkl`     |
| PL_mapping_param_plot | plot w/ peak position, fwhm and intensity heatmaps | `PL_mapping_param_plot` | 

## Scripts

| file name                  | priority |             autorun             |
| -------------------------- |:--------:|:-------------------------------:|
| `SNI_PL_data_prep.py`    |    0     | <input type="checkbox" checked> |
| `PL_mapping_analysis.py` |    1     | <input type="checkbox" checked> |