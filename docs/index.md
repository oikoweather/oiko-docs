---
title: Overview on Oikolab Weather Data 
---

# Overview

> It is often said that 80% of data analysis is spent on the process of cleaning and preparing the data. *- Hadley Wickham, Chief Scientist at RStudio*

## Why Oikolab?

If you're a data scientist or an analyst who frequently work with large volumes of weather data, we save you the most valuable, scarce, and non-renewable resource in the world - **<u>your time</u>**. Many of our users come to us after spending days or weeks trying to find and process weather data even before starting their analysis. Our goal is to give that time back to you.

Oikolab has post-processed hundreds of terabytes of weather data that you can access in seconds - whether you require 1 month or 80 years of weather data - so that you can focus on your analysis rather than spending hours or days downloading and processing raw data.

Here's some examples of what you can do with Oikolab API:

* **Building Simulation** - Download AMY EPW files for any location from 1940 to present. 
* **Asset Management** - Have assets in hundreds of locations? Download time-series weather data for all locations with a single API call.
* **Climate Change Analysis** - Get decades of weather parameter time-series data in seconds.

## Data Source

We provide post-processed datasets from national weather agencies such as NCEP/NOAA, ECMWF, and Environment Canada. These data are often publicly available, but come in a format (GRIB) that is very time consuming to download and use.


=== "ERA5"

    ![ERA5 Reanalysis Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/era5.png){ align=left, width="500" }
    ERA5 Reanalysis data

=== "ERA5Land"

    ![ERA5Land Reanalysis Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/era5land.png){ align=right, width="500" }
    ERA5Land Reanalysis data

=== "GFS"

    ![GFS Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/gfs.png){ align=left, width="500" }
    GFS Forecast data

=== "GEFS"

    ![GFS Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/gefs.png){ align=left, width="500" }
    GEFS Forecast data

=== "HRRR"

    ![HRRR Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/hrrr.png){ align=left, width="500" }
    HRRR Forecast data

=== "SILAM (Air Quality)"

    ![SILAM Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/silam.png){ align=left, width="500" }
    SILAM

We're always adding datasets - if you have a question, please feel free to reach out!

| Type                        |       Dataset        |   Resolution   |         Coverage          |      Updates      | Source 
|-----------------------------|:--------------------:|:--------------:|:-------------------------:|:-----------------:| :----: 
| **Reanalysis**              | ERA5 <br/> ERA5-Land | 28km <br/> 9km | from 1940 <br/> from 1950 | Daily<br/>Monthly | ECMWF
| **Global<br/>  Forecast**   |         GFS          |    13/25km     |          16 days          |       6 hrs       | NCEP
| **Regional<br/>  Forecast** |         HRRR         |     2.5km      |          2 days           |       6 hrs       | NCEP
| **Seasonal<br/>  Forecast** |         CFS          |     100km      |         9 months          |       Daily       | NCEP
| **Ensemble Forecast**       |         GEFS         |      25km      |          10 days          |       6 hrs       | NCEP 
| **Air Quality Forecast**    |        SILAM         |      20km      |          5 days           |       Daily       | FMI

*[ECMWF]: European Centre for Medium-Range Weather Forecasts
*[NCEP]: National Centers for Environmental Prediction
*[NOAA]: National Oceanic and Atmospheric Administration
*[GRIB]: GRIdded Binary format
