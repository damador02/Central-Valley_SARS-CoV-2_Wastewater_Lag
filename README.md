# Central-Valley_SARS-CoV-2_Wastewater_Lag
Repository that holds code and example figures for "Urban to Rural Shifts: Quantifying the Time Lag of SARS-Cov-2 between the Bay Area and Central Valley of California through Wastewater-Based Epidemiology"

The goal of this project is to analyze the wastewater concentrations of SARS-CoV-2 for select Bay Area and Central Valley wastewater treatment plants in order to better understand the the spatial and temporal trends of disease transmission dynamics. This project also includes an analysis of clinical COVID-19 case data.

Specifically, it includes the following:
### wastewater_analysis
**1025_ww_data_peak_analysis.Rmd** | R Markdown file that shows how the raw SARS-CoV-2 wastewater data was smoothed using a local polynomial regression fitting (LOESS) and 10-day moving average. Smoothed LOESS data was then plotted and used to identify the peaks for corresponding wastewater waves. This script requires the [fANCOVA package](https://cran.r-project.org/web/packages/fANCOVA/index.html).


**data_creation_peak_analysis.R** | R script identical to **1025_ww_data_peak_analysis.RMD**. 


**0325_wavelet_analysis.Rmd** | R markdown files that quantifies that lag between the SARS-CoV-2 wastewater waves based on the 10-day smoothed moving average. Also calls **data_creation_peak_analysis.R**. This script requires the [WaveletComp package](https://cran.r-project.org/web/packages/WaveletComp/index.html).


  * Data used for this project for "Lab 1" was dowloaded from the California Open Data Portal: <https://data.ca.gov/dataset/covid-19-wastewater-surveillance-data-california>

  * Up-to-date SARS-CoV-2 data can be downloaded from the California Department of Public Health (CDPH) dashboard: <https://skylab.cdph.ca.gov/calwws/>

  * More information about the difference between Lab 1 and Lab 2 can be found here: <https://www.frontiersin.org/journals/public-health/articles/10.3389/fpubh.2023.1141097/full> 

### clinical_analysis
**clinical_cases_ccf.Rmd** | R Markdown file that quantifies the lag of 7-day moving average COVID-19 case data between Central Valley and Bay Area counties using the cross correlation function (ccf). Calls for the **covid19cases_test.csv** data file.


**covid_variants.Rmd** | R Markdown file that determines the dominant SARS-CoV-2 variant for Region 9 of the U.S. (including all of California)

  * California's county COVID-19 case data can be downloaded from the CalHHS website: <https://data.chhs.ca.gov/dataset/covid-19-time-series-metrics-by-county-and-state/resource/046cdd2b-31e5-4d34-9ed3-b48cdbc4be7a>

  * California's county COVID-19 hospitalization data can be downloaded from the California Open Data Portal: <https://data.ca.gov/dataset/covid-19-hospital-data-archived>

  * COVID-19 variants for the U.S. and speciifc U.S. regions can be downloaded on the U.S. Centers for Disease Control and Prevention (CDC) website:<https://data.cdc.gov/Laboratory-Surveillance/SARS-CoV-2-Variant-Proportions/jr58-6ysp/about_data>


### example_results
This folder contains some results (figures and tables) obtained from the analysis above for both the wastewater and clincal case data that could be used for comparison.


# Acknowledgements
The analyses conducted through WastewaterSCAN was supported by gifts from the CDC Foundation and the Sergey Brin Family Foundation. Additional research support for Healthy Central Valley Together was provided through a philanthropic gift to the University of California, Davis.

This work and research would not be possible without our WWTP (Merced, Modesto, and Los Banos) and public health partners (Merced County Department of Public Health, Stanislaus County Department of Public Health, Yolo County Department of Public Health, and California Department of Public Health). We alsothank the staff of our commercial lab partners.

# Licensing
This repository does not have official licensing yet (tbd) due to the project still being underway. It is expected that this repository will adopt the MIT license, but this is subject to change.
