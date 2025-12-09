# WW_data_points
Repository that holds code and example figures for "Urban to Rural Shifts: Quantifying the Time Lag of SARS-Cov-2 between the Bay Area and Central Valley of California through Wastewater-Based Epidemiology

Specifically, it includes the following:
### wastewater_analysis
1025_ww_data_peak_analysis.RMD | R Markdown file that shows how the raw SARS-CoV-2 data was smoothed using a local polynomial regression fitting (LOESS) and 10-day moving average. Smoothed LOESS data was then used to identify the peaks for corresponding waves. This requires the [fANCOV package](https://cran.r-project.org/web/packages/fANCOVA/index.html).

0325_wavelet_analysis.RMD | R markdown files that quantifies that lag between the SARS-CoV-2 waves based on the 10-day smoothed moving average. This requires the [WaveletComp package](https://cran.r-project.org/web/packages/WaveletComp/index.html).


### clinical_analysis
