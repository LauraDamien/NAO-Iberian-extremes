# LGEO2185 – NAO Influence on Hydroclimatic Extremes

## Author

Laura Damien

Course: LGEO2185 – Advanced Geo-processing
Institution: UCLouvain – School of Geography

## Description

This repository contains the code, documentation, and project files for a geospatial analysis of the influence of the North Atlantic Oscillation (NAO) on hydroclimatic extremes in the Iberian Peninsula.

The project uses ERA5 precipitation data and a seasonal NAO index to analyse extreme precipitation and drought patterns between 1995 and 2025. Extreme precipitation is identified using the 95th percentile of wet days, while drought is analysed using the Standardized Precipitation Index at a three-month timescale, SPI-3.

The full input data are not stored directly in this GitHub repository because the ERA5 NetCDF files are too large. Instead, the data are available through an external UCLouvain SharePoint folder.

External data folder:
[UCLouvain SharePoint data folder](https://uclouvain-my.sharepoint.com/:f:/r/personal/laura_damien_student_uclouvain_be/Documents/LGEO2185_NAO_Iberian_Hydroclimate_Extremes_LauraDamien?csf=1&web=1&e=EVHYwZ)

## Objective

The objective of this project is to assess whether different NAO phases are associated with clear spatial and seasonal patterns in extreme precipitation and drought across the Iberian Peninsula.

The study focuses on:

* identifying extreme precipitation events using local wet-day percentile thresholds;
* analysing the seasonal and spatial variability of extreme precipitation;
* identifying drought conditions using SPI-3;
* comparing extreme precipitation and drought patterns between positive, negative, and neutral NAO phases;
* assessing these relationships using Welch t-tests and Pearson correlations.

## Repository structure

```text
NAO-Iberian-extremes/
│
├── LICENSE
├── NAO_Iberian_Peninsula.qmd
├── README.md
└── metadata.md
```

## File descriptions

`NAO_Iberian_Peninsula.qmd`
Main Quarto file containing the full analysis, R code, figures, interpretation, discussion, and conclusion.

`metadata.md`
Metadata file describing the input datasets, data sources, study period, study area, expected data structure, and data availability.

`README.md`
General project description and reproduction instructions.

`LICENSE`
License information for the repository.

## Input data

The input data are stored externally and must be downloaded before running the analysis.

Expected local data structure:

```text
data/
├── era5_total_precipitation_1994.nc
├── era5_total_precipitation_1995.nc
├── ...
├── era5_total_precipitation_2025.nc
└── NAO_index.csv
```

The year 1994 is included because DJF 1995 requires December 1994.

The `data/` folder is not included in this GitHub repository because the ERA5 NetCDF files are too large for GitHub.

## Reproducing the analysis

To reproduce the analysis:

1. Download the input data from the external UCLouvain SharePoint folder.
2. Create a local `data/` folder inside the project directory.
3. Place all ERA5 NetCDF files and `NAO_index.csv` inside the `data/` folder.
4. Open `NAO_Iberian_Peninsula.qmd` in RStudio.
5. Install the required R packages if needed.
6. Render the Quarto document.

The required R packages are loaded in the Quarto file using `pacman::p_load()`.

Main R packages used:

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

Package and R version information are provided in the `sessionInfo()` output at the end of the report.

## Method summary

The analysis follows these main steps:

1. ERA5 daily precipitation data are loaded from annual NetCDF files.
2. Precipitation values are converted from metres to millimetres.
3. Extreme precipitation days are identified using the local 95th percentile of wet days.
4. Monthly precipitation totals are calculated.
5. SPI-3 is computed to identify drought months.
6. Seasonal NAO index values are classified into positive, negative, and neutral phases.
7. Extreme precipitation and drought patterns are compared between NAO phases.
8. Welch t-tests and Pearson correlations are used to assess the statistical relationships.

## Data availability

The GitHub repository does not include the full input data.

All input data are available in the external UCLouvain SharePoint folder:

[UCLouvain SharePoint data folder](https://uclouvain-my.sharepoint.com/:f:/r/personal/laura_damien_student_uclouvain_be/Documents/LGEO2185_NAO_Iberian_Hydroclimate_Extremes_LauraDamien?csf=1&web=1&e=EVHYwZ)

Users must download the data and place them in a local `data/` folder before rendering the Quarto file.

## GDPR compliance

No personally identifiable data are included in the analysis.

The project only uses environmental and climate data.

## Dataset citation

Damien, L. (2026).
ERA5 precipitation and NAO index dataset for hydroclimatic extremes in the Iberian Peninsula. UCLouvain.

Further details are provided in:

```text
metadata.md
```

## License

This project is licensed under the MIT License.
See the `LICENSE` file for details.
