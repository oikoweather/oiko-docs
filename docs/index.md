---
title: Overview on Oikolab Weather Data 
---

# Overview

> It is often said that 80% of data analysis is spent on the process of cleaning and preparing the data. *- Hadley Wickham, Chief Scientist at RStudio*

## Why Oikolab?

If you're a data scientist or an analyst who frequently work with weather data, we save you the most valuable, scarce, and non-renewable resource in the world - **<u>your time</u>**. Many of our users come to us after spending days or weeks trying to find and process historical weather data even before starting to do their analysis. 

<figure markdown>
  ![Image title](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/apoll17_era5.jpg)
  <figcaption>NASA Apollo 17 image of the Earth taken on 7 December 1972 vs. ECMWF forecast initialized with ERA5 reanalysis</figcaption>
</figure>


Oikolab has post-processed hundreds of terabytes of weather data that you can access in seconds - whether you require 1 month or 80 years of weather data - so that you can focus on your analysis rather than spending hours or days downloading and processing raw data.

Here's some examples of what you can do with Oikolab API:

* **Building Simulation** - Download EPW files for any location at a fraction of the cost (Free or less than $1 per AMY file). 
* **Asset Management** - Have assets in hundreds of locations? Download time-series weather data for all locations with a single API call.
* **Climate Change Analysis** - Get decades of weather parameter time-series data in seconds.

### Data Source

We provide post-processed datasets from national weather agencies such as NCEP/NOAA, ECMWF, and Environment Canada so that it's always traceable to a source. These data are often publicly available, but come in a format (GRIB) that is very time consuming to download and use.

We're always adding datasets - if you have a question, please feel free to reach out!

| Type                        |             Dataset              |          Resolution           |              Coverage              |          Updates           | Source 
|-----------------------------|:--------------------------------:|:-----------------------------:|:----------------------------------:|:--------------------------:| :----: 
| **Reanalysis**              |       ERA5 <br/> ERA5-Land       |        28km <br/> 9km         |     from 1940 <br/> from 1950      |     Daily<br/>Monthly      | ECMWF
| **Global<br/>  Forecast**   | GFS <br/> ICON* <br/> GDPS*<br/> | 13/25km <br/> 13km <br/> 15km | 16 days <br/> 5 days <br/> 10 days | 6 hrs<br/>6 hrs<br/>12 hrs | NCEP<br/> DWD<br/>Environment Canada
| **Regional<br/>  Forecast** |    NAM <br/>ICON-EU<br/>HRRR     |   2.5km<br/>6.5km<br/>2.5km   |   3 days<br/> 2 days <br/>2 days   | 6 hrs<br/>6 hrs<br/>6 hrs  | NCEP<br/> DWD <br/> NCEP
| **Seasonal<br/>  Forecast** |               CFS                |             100km             |              9 months              |           Daily            | NCEP
| **Ensemble Forecast**       |          GEFS                    |             25km              |              10 days               |           6 hrs            | NCEP 
| **Air Quality Forecast**    |              SILAM               |             20km              |               5 days               |           Daily            | FMI

*[ECMWF]: European Centre for Medium-Range Weather Forecasts
*[NCEP]: National Centers for Environmental Prediction
