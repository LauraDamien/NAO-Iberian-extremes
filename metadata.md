# Data metadata

## Project

- Title: Influence of the North Atlantic Oscillation on extreme precipitation and drought in the Iberian Peninsula
- Author: Laura Damien
- Course: LGEO2185 – Advanced Geo-processing
- Institution: UCLouvain
- Study period: 1995–2025

## Data access

The input data are stored in an external UCLouvain SharePoint folder because the ERA5 NetCDF files are too large to include directly in the GitHub repository.

External data folder:  
[UCLouvain SharePoint data folder](https://uclouvain-my.sharepoint.com/:f:/r/personal/laura_damien_student_uclouvain_be/Documents/LGEO2185_NAO_Iberian_Hydroclimate_Extremes_LauraDamien?csf=1&web=1&e=EVHYwZ)

Before running the analysis, users must download the data from this folder and place all files in the local `data/` folder.

## Data included

The dataset contains two main inputs:

1. **ERA5 precipitation data**:
   Annual NetCDF files with daily total precipitation for the Iberian Peninsula.

2. **Seasonal NAO index**:
   A CSV file with seasonal North Atlantic Oscillation index values.

Local file structure:

```text
data/
├── era5_total_precipitation_1994.nc
├── era5_total_precipitation_1995.nc
├── ...
├── era5_total_precipitation_2025.nc
└── NAO_index.csv
```

## ERA5 precipitation data

- Source: Copernicus Climate Change Service, Climate Data Store
- Dataset: ERA5 daily precipitation data derived from ERA5 reanalysis
- Producing centre: ECMWF
- Variable: Total precipitation
- Original unit: metres
- Processed unit: millimetres
- Format: NetCDF `.nc`
- Temporal coverage used: 1994–2025
- Spatial coverage used: Iberian Peninsula
- Bounding box: 45°N to 35°N, 12°W to 6°E

The year 1994 is included because December 1994 is needed to calculate the first complete winter season, DJF 1995.

## NAO index data

- Source: NCAR Climate Data Guide
- Dataset: PC-based Hurrell North Atlantic Oscillation index
- File: `NAO_index.csv`
- Format: CSV
- Temporal resolution: Seasonal
- Columns: `Year`, `DJF`, `MAM`, `JJA`, `SON`

The NAO index is used to classify seasons into positive, neutral and negative NAO phases.

## Use in the project

The ERA5 precipitation files are used to calculate:

* extreme precipitation days using the 95th percentile of wet days;
* monthly precipitation totals;
* SPI-3 drought months.

The NAO index file is used to compare extreme precipitation and drought patterns between positive, neutral and negative NAO phases.

## Data availability

The GitHub repository does not include the input data files.  
All input data are available in the external UCLouvain SharePoint folder:

[UCLouvain SharePoint data folder](https://uclouvain-my.sharepoint.com/:f:/r/personal/laura_damien_student_uclouvain_be/Documents/LGEO2185_NAO_Iberian_Hydroclimate_Extremes_LauraDamien?csf=1&web=1&e=EVHYwZ)

Users must download the ERA5 NetCDF files and the `NAO_index.csv` file and place them in the `data/` folder before rendering `NAO_Iberian_Peninsula.qmd`.

## Data sensitivity

The data are environmental climate data and do not contain personal or sensitive information.
