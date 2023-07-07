---
title: Oikolab FAQ
---


### What does 'Oiko' mean?

The word 'oiko' derives from Greek 'oikos', which is the origin of the word 'eco'. In Korean, this also means 'cucumber nose' that we thought was cute. :smile:

### How do we cite the data?

Each API response will contain a citation to the dataset used. 

### How do you fill in the gaps between ERA5 and recent (< 5 days) historical weather?


### What is the difference between Reanalysis data and Observation data?

> All models are wrong, but some are useful. *- George Box*



|                                           | Reanalyssi Data                                                                                                                                                                                                                                           | Weather Station Data
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| ------------
| **Data Collection Method**                | Reanalysis data is generated using numerical weather prediction models that assimilate various observational data sources, including weather station observations, satellite measurements, and other available data into its atmospheric physics model.   | Weather station observation data is collected directly from ground-based weather stations that measure various meteorological variables like temperature, humidity, wind speed, and precipitation. Typically, these don't include solar radiation data.
| **Data Assimilation and Quality Control** | Reanalysis data undergoes a rigorous process of data assimilation, where observational data from various sources are combined with the model's output to generate a representation of the atmosphere that is consistent with our understanding of atmosheric physics. | Weather station observations are subject to quality control procedures as well, but the level of scrutiny may vary depending on the data source and the organization responsible for data management. 
| **Limitations**                           | Model resolution                                                                                                                                                                                                                                          | Observation Bias and Quality Control. Limited sets of variables.

In general, we recommend using Reanalysis data for most data-intensive application, such as training machine learning models, building energy simulation and forecast prediction. For extreme weather events, it may be more reliable to consult the weather station observation if there is a station nearby. If you're not sure, we're always happy to provide guidance - please feel free to reach out.

