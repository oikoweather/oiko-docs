---
title: Oikolab FAQ
---

### What does 'Oiko' mean?

The word 'oiko' derives from Greek 'oikos', which is the origin of the word 'eco'. 


!!! note "Did you know?"
    In Korean, 'oiko' is a homonym of 'cucumber nose'.

### How do you derive the recent (< 5 days) historical data?

New weather forecast data is created every 6 to 12 hours and reanalysis datasets such as ERA5 are published with a 5-day delay. This gap is filled using the first 6 hours of global forecast data. As the reanalysis data is published, these data points will be over-written.

!!! note "Checking data source"
    With every data timestamp, we indicate the dataset source.

### How do you derive data for a specific coordinate from the underlying dataset?

The data is [bilinearly interpolated](https://en.wikipedia.org/wiki/Bilinear_interpolation) to the coordinate given. 

### What's the difference between Reanalysis vs. Observation data?

We get this question a lot, especially from those who are used to getting weather data from weather stations. In engineering and science, we recognize that perfect observation is not possible and even if you're measuring air temperature with a digital thermometer, it is a modelled representation of the air temperature. 

What the thermometer is telling you is that according to the model of the resistence values of a thermistor, the current reading corresponds to a temperature. Notice that this is not the temperature of the air but the temperature of the thermistor itself - here is an implicit assumption that the temperature of the thermistor will be approximately the same as the air. 

In reality, we know that if there is a large warm body nearby (e.g. a Boeing 747 taxing) this measurement will be skewed. We know this intuitively - if we were sweating in Hong Kong in July and the temperature reads -20 <sup>o</sup>C, it's likely that the reading is wrong.

So how do we know if what we're measuring is correct? The trick is to combine all sources of data - so that instead of a single measurement, we take billions of sample data, and we combine them with our known understanding of atmospheric physics to yield the most representative estimate of the weather.

> All models are wrong, but some are useful. *- George Box*

<figure markdown>
  ![Image title](https://oikostatic.nyc3.cdn.digitaloceanspaces.com/apoll17_era5.jpg)
  <figcaption>NASA Apollo 17 image of the Earth taken on 7 December 1972 vs. ECMWF forecast initialized with ERA5 reanalysis</figcaption>
</figure>


|                                           | Reanalysis Data                                                                                                                                                                                                                                                       | Weather Station Data
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| ------------
| **Data Collection Method**                | Reanalysis data is generated using numerical weather prediction models that assimilate various observational data sources, including weather station observations, satellite measurements, and other available data into its atmospheric physics model.               | Weather station observation data is collected directly from ground-based weather stations that measure various meteorological variables like temperature, humidity, wind speed, and precipitation. Typically, these don't include solar radiation data.
| **Data Assimilation and Quality Control** | Reanalysis data undergoes a rigorous process of data assimilation, where observational data from various sources are combined with the model's output to generate a representation of the atmosphere that is consistent with our understanding of atmosheric physics. | Weather station observations are subject to quality control procedures as well, but the level of scrutiny may vary depending on the data source and the organization responsible for data management. 
| **Limitations**                           | Model resolution                                                                                                                                                                                                                                                      | Observation Bias and Quality Control. Limited sets of variables.

In general, we recommend using Reanalysis data for most data-intensive application, such as training machine learning models, building energy simulation and forecast prediction. For extreme weather events, it may be more reliable to consult the weather station observation if there is a station nearby. If you're not sure, we're always happy to provide guidance - please feel free to reach out.


### What are Data Units?

With a single API call, the returned data size can range anywhere from 10 KB to 10 GB so we meter the usage based on the concept of 'data unit'. One data unit is equivalent to a single parameter for a location for a period of one month for a time-series data, or 1<sup>o</sup> latitude by 1<sup>o</sup> longitude by 1 month for NetCDF area format.

For example, requesting 10 years of temperature and wind speed data for 10 locations is:

* 10 years x 12 months x 2 parameters x 10 locations = 2400 units

Alternatively, an area box for Texas will be:

* 11<sup>o</sup> latitude x 13<sup>o</sup> longitude x 1 month x 5 parameters = 715 units


### Can you provide custom datasets?

Yes! Please contact us at info@oikolab.com for any special project needs.