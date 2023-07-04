# Overview

## Why Oikolab?

We save you the most valuable, scarce, and non-renewable resource in the world - <u>your time</u>. Many of our users
come to us after spending days or weeks trying to find and process historical weather data to do their analysis. 

<figure markdown>
  ![Image title](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/apoll17_era5.jpg)
  <figcaption>NASA Apollo 17 image of the Earth taken on 7 December 1972 vs. ECMWF forecast initialized with ERA5 reanalysis</figcaption>
</figure>


Oikolab has post-processed hundreds of terabytes of weather data that you can access in seconds - whether you require 1 month or 80 years of weather data - so that you can focus on your analysis rather than spending hours or days downloading and processing raw data.

You don't have to take our word for it - here are some list of what our users do instead of dealing with slow downloads or wrangling with GRIB files:

* Predict crop yield for all of Northern India
* Develop new building code for Poland
* Predict retail sales 
* Analyze smart-meter electricity data in the US
* ... and many, many others. 

*[ECMWF]: European Centre for Medium-Range Weather Forecasts
*[NCEP]: National Centers for Environmental Prediction

## Key Concepts

To help understand our service, here are some key concepts to help you along.

### Data Source & Datasets (or Models)

A common question that we get is - where do we get our data? We get them from the same place like everyone else - national weather agencies such as NCEP/NOAA, ECMWF, and Environment Canada. These data are often freely available, but come in a format that makes it very time consuming to download and use.


We're always adding datasets - if you have a question, please feel free to reach out!

| Type                        |             Dataset              |          Resolution           |              Coverage              |          Updates           | Source 
|-----------------------------|:--------------------------------:|:-----------------------------:|:----------------------------------:|:--------------------------:| :----: 
| **Reanalysis**              |       ERA5 <br/> ERA5-Land       |        28km <br/> 9km         |     from 1940 <br/> from 1950      |     Daily<br/>Monthly      | ECMWF
| **Global<br/>  Forecast**   | GFS <br/> ICON* <br/> GDPS*<br/> | 13/25km <br/> 13km <br/> 15km | 16 days <br/> 5 days <br/> 10 days | 6 hrs<br/>6 hrs<br/>12 hrs | NCEP<br/> DWD<br/>Environment Canada
| **Regional<br/>  Forecast** |    NAM <br/>ICON-EU<br/>HRRR     |   2.5km<br/>6.5km<br/>2.5km   |   3 days<br/> 2 days <br/>2 days   | 6 hrs<br/>6 hrs<br/>6 hrs  | NCEP<br/> DWD <br/> NCEP
| **Seasonal<br/>  Forecast** |               CFS                |             100km             |              9 months              |           Daily            | NCEP
| **Ensemble Forecast**       |          GEFS                    |             25km              |              10 days               |           6 hrs            | NCEP 
| **Air Quality Forecast**    |              SILAM               |             20km              |               5 days               |           Daily            | FMI

### Reanalysis data

Our historical dataset is based on ECMWF's reanalysis data, which is available with about 5 day delay. To provide continuity, we use the first 6 hours of the GFS data for the past 5 days to re-contruct the recent weather. These are different from observation data in that it observation data as measurement samples and combine with other sources of data such as satellites and weather balloons to create a holistic picture of the atmosphere consistent with atmospheric physics.

When calling our API, there is no need to specify the dataset.

### Data Units

Unlike typical API service, our usage is not metered by the number of API calls. With a single API call, the returned data volume can range anywhere from 10 KB to 10 GB so we define one unit as a single parameter for a location for a period of one month.