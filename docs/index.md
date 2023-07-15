---
title: Overview on Oikolab Weather Data 
---

> It is often said that 80% of data analysis is spent on the process of cleaning and preparing the data. *- Hadley Wickham, Chief Scientist at RStudio*

## Why Oikolab?

Data scientists or analysts often spend days or weeks looking for and processing historical weather data before they can begin their analysis. Here’s where Oikolab comes in – we do the work, so you don’t have to. We save you the most valuable, scarce, and non-renewable resource in the world – **<u>your time</u>**.

We provide post-processed datasets from national weather agencies such as NCEP/NOAA, ECMWF, and Environment Canada. These data are often publicly available, but come in a format (GRIB) that is very time consuming to download and use.


=== "ERA5"

    ![ERA5 Reanalysis Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/era5.png)

=== "ERA5Land"

    ![ERA5Land Reanalysis Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/era5land.png)

=== "GFS"

    ![GFS Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/gfs.png)

=== "GEFS"

    ![GFS Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/gefs.png)

=== "HRRR"

    ![HRRR Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/hrrr.png)

=== "SILAM (Air Quality)"

    ![SILAM Forecast Data](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/silam.png)


Ready to jump right into your analysis? Oikolab has post-processed hundreds of terabytes of weather data that you can access in seconds - whether you require 1 month or 80 years of weather data.

Here's some examples of what you can do with Oikolab API:

* **Building Simulation** - Download AMY EPW files for any location from 1940 to present. 
* **Asset Management** - Have assets in hundreds of locations? Download time-series weather data for all locations with a single API call.
* **Climate Change Analysis** - Get decades of weather parameter time-series data in seconds.


## Dataset Overview

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
