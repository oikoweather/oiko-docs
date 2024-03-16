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

Oikolab has post-processed hundreds of terabytes of weather data that you can access in seconds - whether you require 1 month or 80 years of weather data.

## Datasets

We provide post-processed datasets from national weather agencies such as NCEP/NOAA, ECMWF, and Environment Canada. 
These data are often publicly available, but come in a format (GRIB) that is very time consuming to download and use.

=== "ERA5"

    ![ERA5 Reanalysis Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/era5.png){align=left}
    *[ERA5](https://www.ecmwf.int/en/forecasts/dataset/ecmwf-reanalysis-v5) is the latest generation of the reanalysis 
     dataset produced by ECMWF and is the main dataset that we use for historical data. The next generation of 
     reanalysis data, ERA6, is currently in the works and is expected to be 
     released sometime in 2024.*

    *ERA5 surface data is available from 1940 to present with a 5-day delay, published at around 12 UTC by ECMWF. 
    Once new data is downloaded, it is processed and made available via API with about 1 hour delay.*


=== "ERA5Land"

    ![ERA5Land Reanalysis Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/era5land.png){align=left}
    *[ERA5Land](https://www.ecmwf.int/en/era5-land) dataset provides higher resolution (9km) than the ERA5 dataset for 
    a selected set of surface-parameters.*

    *Data is available from 1950 to present with a 5-day delay, published at around 12 UTC by ECMWF. New data is 
    downloaded, processed and made available via API with about 1~3 hour delay.*

=== "GFS"

    ![GFS Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/gfs.png){align=left}
    *The Global Forecast System (GFS) is a numerical weather prediction model developed and maintained by the National 
    Centers for Environmental Prediction (NCEP), which is part of the National Weather Service (NWS) within the 
    National Oceanic and Atmospheric Administration (NOAA) in the United States. The GFS model is one of the most widely 
    used operational weather forecasting models globally, providing forecasts on a global scale out to 16 days into the future.*

    *GFS data is published four times a day, initialized at 00Z, 06Z, 12Z and 18Z and published around 
    [5 hr 10 minutes](https://www.nco.ncep.noaa.gov/pmb/nwprod/prodstat/index.html) after 
    the initialized time. Once published, the dataset is downloaded and made available from Oikolab API with about 
    15 minute delay.*

=== "GEFS"

    ![GEFS Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/gefs.png){align=left}
    *The Global Ensemble Forecast System (GEFS) is another numerical weather prediction model developed and 
    maintained by the National Centers for Environmental Prediction (NCEP). Unlike the Global Forecast 
    System (GFS), which produces deterministic forecasts, the GEFS model generates ensemble forecasts, providing a 
    range of possible future weather scenarios based on multiple simulations with slightly different initial 
    conditions or model configurations.*

    *GEFS data is published four times a day, initialized at 00Z, 06Z, 12Z and 18Z and published around 
    [6 hr 30 minutes after](https://www.nco.ncep.noaa.gov/pmb/nwprod/prodstat/index.html) 
    the initialized time. Once published, the dataset is downloaded and made available from Oikolab API 
    with about 15 minute delay.*

=== "CFS"

    ![CFS Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/cfs.png){align=left}
    *The Climate Forecast System (CFS) is a seasonal forecast model developed by the National Centers for Environmental 
    Prediction (NCEP), which is part of the National Oceanic and Atmospheric Administration (NOAA) in the United States. 
    The CFS model is designed to predict climate variations on seasonal to interannual timescales, typically spanning 
    weeks to months into the future.*

    *CFS data is published four times a day, initialized at 00Z, 06Z, 12Z and 18Z. 
    Currently, only the CFS 00Z hour data is processed and made available from Oikolab API.*


=== "HRRR"

    ![HRRR Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/hrrr.png){align=left}
    *The [High-Resolution Rapid Refresh (HRRR)](https://rapidrefresh.noaa.gov/hrrr/) model is 
    an advanced, high-resolution numerical weather prediction model 
    developed by the National Centers for Environmental Prediction (NCEP). The HRRR model is designed 
    to provide short-term, high-resolution forecasts of weather conditions, with a focus on convective weather 
    phenomena such as thunderstorms, heavy precipitation, and other rapidly evolving weather events.*

    *HRRRR hourly dataset is published four times a day, initialized at 00Z, 06Z, 
    12Z and 18Z with forecast out to 48 hours and HRRR-subhourly data is published from NCEP each 
    every hour. Once published by NCEP, both HRRR and HRRR-subhourly datasets are available from Oikolab with about 
    5-minute delay.*


=== "NAM-CONUS"

    ![NAM Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/nam2.png){align=left}
    *The [North American Mesoscale (NAM)](https://www.ncei.noaa.gov/products/weather-climate-models/north-american-mesoscale) 
    one of the National Centers For Environmental Prediction’s (NCEP) major models for producing weather forecasts. 
    NAM generates multiple grids (or domains) of weather forecasts over the North American continent at various horizontal resolutions.*

    *NAM dataset is published four times a day, initialized at 00Z, 06Z, 12Z and 18Z with forecast out to 60 hours. 
    Once published, NAM-CONUS data is made vailable from Oikolab with about 5-minute delay.*


=== "SILAM (Air Quality)"

    ![SILAM Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/silam.png){align=left}
    *The SILAM (System for Integrated modeLling of Atmospheric coMposition) dataset is an advanced modeling system 
    developed by the Finnish Meteorological Institute (FMI) for simulating and forecasting atmospheric composition, 
    including air quality, aerosols, and chemical species such as ozone, nitrogen dioxide, sulfur dioxide, 
    and particulate matter.*

    *SILAM data is published daily at around 06Z.*


We're always adding datasets. If you need something that we don’t currently offer, please feel free to reach out and ask.

| Type                             |                        Datasets                        | Spatial <br/> Resolution |    Temporal <br/> Resolution     |  Coverage / <br/> Forecast Horizon  | Notes                                                                   |
|----------------------------------|:------------------------------------------------------:|:------------------------:|:--------------------------------:|:-----------------------------------:|:------------------------------------------------------------------------|
| **Historical <br/>  Reanalysis** |                  ERA5 <br/> ERA5-Land                  |      28km <br/> 9km      |       Hourly <br/> Hourly        | 1940 - present <br/> 1950 - present | Data is made available with 5-day delay                                 |        
| **Global<br/>  Forecast**        |                          GFS                           |         13/25km          |              Hourly              |               16 days               | Hourly forecast steps up to 120 hr and 3-hours afterward                |        
| **Regional<br/>  Forecast**      | HRRR <br/> <nobr>HRRR-subhourly</nobr> <br/> NAM-CONUS | 3km <br/> 3km <br/> 3km  | Hourly <br/> 15 min <br/> Hourly |  2 days <br/> 18 hrs <br/> 60 hrs   | Lambert conformal conic projection is re-mapped to regular lat/lon grid | 
| **Seasonal<br/>  Forecast**      |                          CFS                           |          100km           |             6 hours              |              9 months               |                                                                         |  
| **Ensemble<br/>  Forecast**      |                          GEFS                          |           25km           |             3 hours              |               10 days               |                                                                         | 
| **Air Quality <br/>  Forecast**  |                         SILAM                          |           20km           |              Hourly              |               5 days                | Includes data from 5 previous days                                      | 


## Uses

Here are some examples of what you can do with Oikolab API:

* **Building Simulation** - Download TMY or AMY EPW files for any location from 1940 to present. 
* **Asset Management** - Have assets in hundreds of locations? Download time-series weather data for all locations with a single API call.
* **Climate Change Analysis** - Get decades of weather parameter time-series data in seconds.


*[ECMWF]: European Centre for Medium-Range Weather Forecasts
*[NCEP]: National Centers for Environmental Prediction
*[NOAA]: National Oceanic and Atmospheric Administration
*[FMI]: Finnish Meteorological Institute
*[GRIB]: GRIdded Binary format
*[EPW]: EnergyPlus Weather format
*[AMY]: Actual Meteorological Year
*[TMY]: Typical Meteorological Year
*[GEFS]: Global Ensemble Forecast System
*[GFS]: Global Forecast System
