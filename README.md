# Genetic_Context
Python implementation of the analysis used in Boulas et al. "Assessing in vivo the impact of gene context on transcription through DNA supercoiling".
The provided raw data and Jupyter Notebooks allow to reproduce the analysis and figures of the experimental data of the article.
In addition, and to demonstrate how to handle the sequences data, some figures from the supplementary materials are also reproduced here.

## Usage

The code has been tested using `Python 3.9.13`.

### Raw datasets

- F0.csv, F1.csv and F2.csv are 3 raw datasets that denote the plate reader acquisition of OD600, test gene fluorescence and control gene fluorescence, respectively.
- These raw datasets are constituted of labeled time series whose column names are time stamps in hours.
- Labels contain information about the construct in question as well as experimental details.
- For example, p02_uNdB_i0_t37_r3 denotes: promoter p02; upstream distance uN; downstream distance dB; no IPTG; a temperature of 37Â°C; replica nÂ°3.
- Promoter sequences as well as upstream and downstream sequences can be found in the datasets Promoters.csv and Distances.csv.

### Code

- Two Jupyter Notebooks are provided: Proprocessing.ipynb and Plots.ipynb.
- Preprocessing.ipynb takes in input the raw datasets (as well as parameters defined at the beginning of the code) and optionally outputs the proprocessed datasets: FT_OD_final_stats.csv, FC_OD_final_stats.csv and FT_FC_final_stats.csv.
- Plotting.ipynb takes in input the preprocessed datasets (as well as parameters defined at the beginning of the code) and generates the articles' figures.
