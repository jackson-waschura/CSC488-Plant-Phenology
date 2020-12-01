# CSC488-Plant-Phenology

Code for the CCS 448 Collaborative Bioinformatics group project studying Plant Phenology. This project produced 5 jupyter notebooks which were used at different stages of our work. Below, the purpose and content of each notebook is explained.

## Notebooks

### merging_queries.ipynb

This notebook served to construct a single dataframe of CCH2 samples from a set of many queries from the online CCH2 portal. It also consolidates flowering/fruiting labels on each sample from multiple potential pieces of information, groups variants and subspecies together, drops rows missing crucial information, and finally, imputes missing values in the startDayOfYear column using the middle of the provided month. The end result of running this notebook is a `full_dataset.csv` containing our cleaned CCH2 samples.

### measuring_missing_labels.ipynb

This notebook served to quantify the number of CCH2 samples missing phenological scores from each institution to help us understand which permissions we should ask of the CCH2 administrator in order to improve our sample sizes the most.

### ExploringPRISMClimateData.ipynb

This notebook served as an introduction to the PRISM climate dataset and the `.hdr` and `.bil` file formats used by the dataset. The end of this notebook also contains some prototype code for matching CCH2 specimens to PRISM data using Lat/Lon coords. A visualization in this notebook shows some CCH2 specimens from northern mexico failing to match with PRISM data.

### JoiningClimateAndCCH2Data.ipynb

This notebook served to match CCH2 samples to PRISM climate data and create the merged dataset. Some visualizations in this notebook show the distributions of climate variables across all CCH2 samples. The final result of this notebook is an overwritten `full_dataset.csv` with climate variable columns added.

### ChangeInPhenology.ipynb

This notebook performed the phenological sensitivity analysis described in our paper and produced many of the visualizations. It first performs linear regressions between year and startDatOfYear for flowering samples of each study species, then visualizes the temporal distribution of study species samples, produces a visualization of the moving average of MFT for each study species, displays the change in a climate variable over time, and concludes by producing sensitivity scores for each species relative to each climate variable and ranking the species.