# A Molecular Atlas of the Adult Mouse Brain
This repository contains the code from the *Science Advances* paper [A Molecular Atlas of the Adult Mouse Brain](https://advances.sciencemag.org/content/6/26/eabb3446).

## Disclaimer
This code is shared for reproducibility purposes. Despite our efforts, some hardcoded paths and poorly commented parts could be remaining. You might need to modify the code to make it work on your system. The sessionInfo() output is available in the bin directory and will provide guidance about the conditions in which scripts were originally run.

## License
This code is shared under the MIT License Agreement. See the LICENSE file for more details.

## Authors
Cantin Ortiz <cantin.ortiz@gmail.com>
Jose Fernandez Navarro <jc.fernandez.navarro@gmail.com>

## Content
Directories 01-registration, 02-qc_normalization, 03-clustering, 04-SC_mapping and 05-DEA correspond to the analysis pipeline and are supposed to be executed sequentially. 
Directories bin and figures contain the code used to render the figures from intermediary data files.
All data files are available at [www.molecularatlas.org](https://www.molecularatlas.org/download-data).

### 01-Registration
This script will generate a meta table and a raw count expression table (this will take several hours). Simply cd to the data directory ([download](https://www.molecularatlas.org/data-to-download/intermediary_data/01-registration.zip)) and run the script.

### 02-qc_normalization
These scripts perform the normalization and batch correction of the expression matrix generated during registration.

### 03-clustering
This script performs the clustering based on the normalized expression matrix generated previously ([download](https://www.molecularatlas.org/data-to-download/processed_data/expr_normalized_table.tsv.gz)).

### 04-SC_mapping


### 05-DEA

### Figures
Figures were generated using many intermediary data files ([download](https://www.molecularatlas.org/data-to-download/intermediary_data/figures.zip)). In order to render the figures, make sure to source the script 'includes.R' from the bin directory. It will load many functions required for plotting. You must update the two variables defined in the two first lines of includes.R : path.bin should be a string with the absolute path to the bin directory, path.matrices a string with the absolute path to the previously downloaded folder containing all the figures data.
