# Overview

## 1. Why Oikolab?

We save you the most valuable, scarce, and non-renewable resource in the world - <u>your time</u>. Many of our users
come to us after spending days or weeks trying to find historical weather data to do their analysis. 

<figure markdown>
  ![Image title](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/apoll17_era5.jpg)
  <figcaption>NASA Apollo 17 image of the Earth taken on 7 December 1972 vs. ECMWF forecast initialized with ERA5 reanalysis</figcaption>
</figure>


Oikolab has processed hundreds of terabytes of weather data that you can access in seconds - whether you require 1 month 
or 80 years of weather data - so that you can focus on your analysis rather than spending hours or days 
downloading and processing raw data.

You don't have to take our word for it - our data was/is used to:

* Predict crop yield for all of Northern India
* Develop new building code for Poland
* Predict retail sales 
* Analyze smart-meter electricity data in the US
* ... and many, many others. 

We get our data from ECMWF, NCEP, and FMI.

*[ECMWF]: European Centre for Medium-Range Weather Forecasts
*[NCEP]: National Centers for Environmental Prediction


### 1.1 Datasets (or Models)

We're always adding datasets - if you have a question, please feel free to reach out!

Type                 |                  Dataset                  |             Resolution             |                   Coverage                   |               Updates               | Source 
---------            |:-----------------------------------------:|:----------------------------------:|:--------------------------------------------:|:-----------------------------------:| :----: 
**Reanalysis**       |           ERA5 <br/> ERA5-Land            |           28km <br/> 9km           |          from 1940 <br/> from 1950           |          Daily<br/>Monthly          | [ECMWF](https://www.ecmwf.int/)<br/>[ECMWF](https://www.ecmwf.int/)
**Global<br/>  Forecast**  |     GFS <br/> ICON* <br/> GDPS*<br/>      |   13/25km <br/> 13km <br/> 15km    |      16 days <br/> 5 days <br/> 10 days      |     6 hrs<br/>6 hrs<br/>12 hrs      | [NCEP](https://www.weather.gov/ncep/)<br/> [DWD](https://www.dwd.de)<br/>[Environment Canada](https://weather.gc.ca/canada_e.html)
**Regional<br/>  Forecast**|         NAM <br/>ICON-EU<br/>HRRR         |2.5km<br/>6.5km<br/>2.5km | 3 days<br/> 2 days <br/>2 days | 6 hrs<br/>6 hrs<br/>6 hrs | [NCEP](https://www.weather.gov/ncep/) <br/> [DWD](https://www.dwd.de) <br/> [NCEP](https://www.weather.gov/ncep/)
**Seasonal<br/>  Forecast**|                    CFS                    |               100km                |                   9 months                   |                Daily                | [NCEP](https://www.weather.gov/ncep/)
**Ensemble Forecast**      |             GEFS  <br/> HREF*             |           25km <br/> 5km           |             10 days <br/> 3 days             |           6 hrs<br/>6 hrs           | [NCEP](https://www.weather.gov/ncep/) <br/> [NCEP](https://www.weather.gov/ncep/)
**Air Quality Forecast**   |                   SILAM                   |                20km                |                    5 days                    |                Daily                | [FMI](https://en.ilmatieteenlaitos.fi/)

### 1.2 Reanalysis data



With a single API call, you can request data volume anywhere from 10 KB to 10 GB. 

### 1.2 Data Units

With a single API call, you can request data volume anywhere from 10 KB to 10 GB. 