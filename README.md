# LGEO2185 – NAO Influence on Hydroclimatic Extremes

## AUTHOR

* Laura Damien

Course: LGEO2185 – Advanced Geo-processing
Institution: UCLouvain – School of Geography

## DESCRIPTION

This repository contains the code, documentation and report for a geospatial analysis of the influence of the North Atlantic Oscillation (NAO) on hydroclimatic extremes in the Iberian Peninsula. The project uses ERA5 precipitation data and a seasonal NAO index to analyse extreme precipitation and drought patterns between 1995 and 2025.

The ERA5 NetCDF files and the NAO index file are not stored directly in this GitHub repository because the input data are stored in an external UCLouvain SharePoint folder.

External data folder:
[UCLouvain SharePoint data folder](https://uclouvain-my.sharepoint.com/:f:/r/personal/laura_damien_student_uclouvain_be/Documents/LGEO2185_NAO_Iberian_Hydroclimate_Extremes_LauraDamien?csf=1&web=1&e=EVHYwZ)

### Objective

The objective of this project is to assess whether different NAO phases are associated with clear spatial and seasonal patterns in extreme precipitation and drought across the Iberian Peninsula. Extreme precipitation is identified using the 95th percentile of wet days, while drought is analysed using the Standardized Precipitation Index at a three-month timescale, SPI-3.

## FILE STRUCTURE

`report.qmd`
Main Quarto report containing the full analysis, figures, interpretation and discussion.

`R/functions_helpers.R`
Helper R script containing repeated statistical functions used in the analysis, such as Welch t-tests and Pearson correlation functions.

`data/`
Folder where the input data must be placed before running the analysis.

Expected data files:

`→ era5_total_precipitation_1994.nc`
`→ era5_total_precipitation_1995.nc`
`→ ...`
`→ era5_total_precipitation_2025.nc`
`→ NAO_index.csv`

The `data/` folder is not fully included in the GitHub repository because the ERA5 NetCDF files are too large.

`METADATA.md`
Metadata file describing the input datasets, data sources, expected file structure and data availability.

`README.md`
General project description and reproduction instructions.

`LICENSE`
License information for the repository.

## REPRODUCING THE ANALYSIS

The analysis can be reproduced by:

1. Downloading the input data from the external UCLouvain SharePoint folder.
2. Placing the ERA5 NetCDF files and `NAO_index.csv` in the local `data/` folder.
3. Opening `report.qmd` in RStudio.
4. Installing the required R packages if needed.
5. Rendering the Quarto report.

The required R packages are loaded in the report using `pacman::p_load()`. The main packages used are:

* tidyverse
* lubridate
* terra
* ncdf4
* sf
* ggplot2
* paletteer
* rnaturalearth
* rnaturalearthdata
* SPEI
* ggspatial
* grid
* ecmwfr

Package and R version information are provided through the `sessionInfo()` output at the end of the report.

## DATA AVAILABILITY

The GitHub repository does not include the full input data.
All input data are available in the external UCLouvain SharePoint folder:

[UCLouvain SharePoint data folder](https://uclouvain-my.sharepoint.com/:f:/r/personal/laura_damien_student_uclouvain_be/Documents/LGEO2185_NAO_Iberian_Hydroclimate_Extremes_LauraDamien?csf=1&web=1&e=EVHYwZ)

Users must download the data and place them in the `data/` folder before rendering the report.

## GDPR COMPLIANCE

No personally identifiable data are included.
The project only uses environmental and climate data.

## DATASET CITATION

Damien, L. (2026).
ERA5 precipitation and NAO index dataset for hydroclimatic extremes in the Iberian Peninsula. UCLouvain.

The full data metadata are available in:

`METADATA.md`

## LICENSE

This project is licensed under the MIT License.
See the `LICENSE` file for details.
