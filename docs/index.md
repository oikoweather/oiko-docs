---
title: Overview on Oikolab Weather Data 
description: This page providees overview on Oikolab Weather API service and it's datasets.
---

> It is often said that 80% of data analysis is spent on the process of cleaning and preparing 
> the data. *- Hadley Wickham, Chief Scientist at RStudio*

## Why Oikolab?

Data scientists or analysts often spend days or weeks looking for and processing historical weather data before they can 
begin their analysis. Here’s where Oikolab comes in – we do the work, so you don’t have to. We save you the most valuable, 
scarce, and non-renewable resource in the world – **<u>your time</u>**.

Ready to jump right into your analysis? Oikolab has post-processed hundreds of terabytes of weather data that you can 
access in seconds - whether you require 1 month or 80 years of weather data.

Here are some examples of what you can do with Oikolab API:

* **Building Simulation** - Download AMY EPW files for any location from 1940 to present. 
* **Asset Management** - Have assets in hundreds of locations? Download time-series weather data for all locations with a single API call.
* **Climate Change Analysis** - Get decades of weather parameter time-series data in seconds.


## Datasets

We provide post-processed datasets from national weather agencies such as NCEP/NOAA, ECMWF, and Environment Canada. 
These data are often publicly available, but come in a format (GRIB) that is very time consuming to download and use.



=== "ERA5"

    ![ERA5 Reanalysis Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/era5.png){align=left}
    *[ERA5](https://www.ecmwf.int/en/forecasts/dataset/ecmwf-reanalysis-v5) is the latest generation of the reanalysis dataset produced by ECMWF and is the main dataset that we use for
     historical data. The next generation of reanalysis data, ERA6, is currently in the works and is expected to be 
     released sometime in 2024. Surface data is available from 1940 to present with a 5-day delay.*

=== "ERA5Land"

    ![ERA5Land Reanalysis Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/era5land.png){align=left}
    *[ERA5Land](https://www.ecmwf.int/en/era5-land) dataset provides higher resolution (9km) than the ERA5 dataset for a selected set of surface-parameters.*

=== "GFS"

    ![GFS Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/gfs.png){align=left}
    *The Global Forecast System (GFS) is a numerical weather prediction model developed and maintained by the National 
    Centers for Environmental Prediction (NCEP), which is part of the National Weather Service (NWS) within the 
    National Oceanic and Atmospheric Administration (NOAA) in the United States. The GFS model is one of the most widely 
    used operational weather forecasting models globally, providing forecasts on a global scale out to around two weeks into the future.*

=== "GEFS"

    ![GEFS Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/gefs.png){align=left}
    *The Global Ensemble Forecast System (GEFS) is another numerical weather prediction model developed and 
    maintained by the National Centers for Environmental Prediction (NCEP), which is part of the National Weather Service 
    (NWS) within the National Oceanic and Atmospheric Administration (NOAA) in the United States. Unlike the Global Forecast 
    System (GFS), which produces deterministic forecasts, the GEFS model generates ensemble forecasts, providing a 
    range of possible future weather scenarios based on multiple simulations with slightly different initial 
    conditions or model configurations. .*

=== "CFS"

    ![CFS Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/cfs.png){align=left}
    *The Climate Forecast System (CFS) is a seasonal forecast model developed by the National Centers for Environmental 
    Prediction (NCEP), which is part of the National Oceanic and Atmospheric Administration (NOAA) in the United States. 
    The CFS model is designed to predict climate variations on seasonal to interannual timescales, typically spanning 
    weeks to months into the future.*

=== "HRRR"

    ![HRRR Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/hrrr.png){align=left}
    *The High-Resolution Rapid Refresh (HRRR) model is an advanced, high-resolution numerical weather prediction model 
    developed by the National Centers for Environmental Prediction (NCEP), part of the National Weather Service (NWS) 
    within the National Oceanic and Atmospheric Administration (NOAA) in the United States. The HRRR model is designed 
    to provide short-term, high-resolution forecasts of weather conditions, with a focus on convective weather 
    phenomena such as thunderstorms, heavy precipitation, and other rapidly evolving weather events.*

=== "SILAM (Air Quality)"

    ![SILAM Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/silam.png){align=left}
    *The SILAM (System for Integrated modeLling of Atmospheric coMposition) dataset is an advanced modeling system 
    developed by the Finnish Meteorological Institute (FMI) for simulating and forecasting atmospheric composition, 
    including air quality, aerosols, and chemical species such as ozone, nitrogen dioxide, sulfur dioxide, and particulate matter.*


We're always adding datasets. If you need something that we don’t currently offer, please feel free to reach out and ask.

| Type                        |                       Datasets (Source)                        |      Spatial Resolution       |         Temporal Resolution          |               Coverage               |                 Updates                  |
|-----------------------------|:--------------------------------------------------------------:|:-----------------------------:|:------------------------------------:|:------------------------------------:|:----------------------------------------:|
| **Historical Reanalysis**   |              ERA5 (ECMWF) <br/> ERA5-Land (ECMWF)              |        28km <br/> 9km         |         Hourly <br/> Hourly          |      from 1940 <br/> from 1950       | Daily (5-day lag) <br/>Daily (5-day lag) |
| **Global<br/>  Forecast**   |                           GFS (NCEP)                           |            13/25km            |                Hourly                |               16 days                |                  6 hrs                   |
| **Regional<br/>  Forecast** | HRRR (NCEP) <br/> HRRR-subhourly (NCEP) <br/> NAM-CONUS (NCEP) | 2.5km <br/> 2.5km <br/> 2.5km | Hourly <br/> 15 minutes <br/> Hourly | 2 days <br/> 18 hours <br/> 2.5 days |      6 hrs <br/> Hourly <br/> 6 hrs      |
| **Seasonal<br/>  Forecast** |                           CFS (NCEP)                           |             100km             |               6 hours                |               9 months               |                  Daily                   |
| **Ensemble Forecast**       |                          GEFS (NCEP)                           |             25km              |               3 hours                |               10 days                |                  6 hrs                   |
| **Air Quality Forecast**    |                          SILAM (FMI)                           |             20km              |                Hourly                |                5 days                |                  Daily                   |

*[ECMWF]: European Centre for Medium-Range Weather Forecasts
*[NCEP]: National Centers for Environmental Prediction
*[NOAA]: National Oceanic and Atmospheric Administration
*[FMI]: Finnish Meteorological Institute
*[GRIB]: GRIdded Binary format
*[EPW]: EnergyPlus Weather format
*[AMY]: Actual Meteorological Year
