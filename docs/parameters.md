---
title: Weather Parameters
---

## Parameters

The following is a list of parameters available through Oikolab API. Please note that not all parameters will be available for each dataset.
For example, the GEFS dataset does not include wind speed at 100m height.

### Group 1: Temperature
  
| Parameter                               | Unit              | Description                                                                                                                                                                   | 
|:----------------------------------------|:------:           |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `temperature`                           | *<sup>o</sup>C*   | Drybulb temperature of the air at 2 m above the surface of land, sea or inland waters.                                                                                        |
| `dewpoint_temperature`                  | *<sup>o</sup>C*   | The temperature to which the air at 2 m above the surface of the Earth would have to be cooled for saturation to occur.                                                       |
| `wetbulb_temperature`                   | *<sup>o</sup>C*   | The temperature read by a thermometer covered in water-soaked cloth over which air is passed. [Reference](https://en.wikipedia.org/wiki/Wet-bulb_temperature)                 |
| `humidex_index`                         | *<sup>o</sup>C*   | Humidex Index as defined by [Canadian Meteorologists](https://en.wikipedia.org/wiki/Humidex)                                                                                  |
| <nobr>`soil_temperature_level_1`</nobr> | *<sup>o</sup>C*   | Soil temperature at level 1 (0 - 7 cm), in the middle of layer.                                                                                                               |
| `soil_temperature_level_2`              | *<sup>o</sup>C*   | Soil temperature at level 2 (7 - 28 cm), in the middle of layer.                                                                                                              |
| `soil_temperature_level_3`              | *<sup>o</sup>C*   | Soil temperature at level 3 (28 - 100 cm), in the middle of layer.                                                                                                            |
| `soil_temperature_level_4`              | *<sup>o</sup>C*   | Soil temperature at level 4 (100 - 289 cm), in the middle of layer.                                                                                                           |
| `skin_temperature`                      | *<sup>o</sup>C*   | The theoretical temperature that is required to satisfy the surface energy balance; it represents the temperature of the uppermost surface layer, which has no heat capacity. |


### Group 2: Wind

| Parameter                  |  Unit   | Description                                       |
|:---------------------------|:-------:|---------------------------------------------------|
| `wind_speed`               | *m/s*   | Wind speed at 10 m above the surface.             |
| `wind_direction`           |  *deg*  | Wind direction at 10 m above the surface.         |
| `10m_wind_gust`            |  *m/s*  | Instantaneous wind gust at 10 m above surface.    |
| `10m_u_component_of_wind`  |  *m/s*  | U component of wind at 10 m above the surface.    |
| `10m_v_component_of_wind`  |  *m/s*  | V component of wind at 10 m above the surface.    |
| `100m_wind_speed`          |  *m/s*  | Wind speed at 100 m above the surface.            |
| `100m_wind_direction`      |  *deg*  | Wind direction at 100 m above the surface.        |
| `100m_u_component_of_wind` |  *m/s*  | U component of wind at 100 m above the surface.   |
| `100m_v_component_of_wind` |  *m/s*  | V component of wind at 100 m above the surface.   |


### Group 3: Radiation

| Parameter                                      | Unit              | Description                                                                                                                                                                                                                                    |
|:-----------------------------------------------|:------:           |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface_solar_radiation`                      | *W/m<sup>2</sup>* | Solar radiation (shortwave) that reaches a horizontal plane at the surface of the Earth. This parameter comprises both direct and diffuse solar radiation.                                                                                     |
| `surface_net_solar_radiation`                  | *W/m<sup>2</sup>* | Solar radiation (shortwave) that reaches a horizontal plane at the surface of the Earth minus the amount reflected by the Earth's surface (which is governed by the albedo). This value is positive downwards, following the ECMWF convention. |
| `surface_thermal_radiation`                    | *W/m<sup>2</sup>* | Thermal radiation (longwave) emitted by the atmosphere and clouds that reaches a horizontal plane at the surface of the Earth.                                                                                                                 |
| `surface_net_thermal_radiation`                | *W/m<sup>2</sup>* | This parameter is the difference between downward and upward thermal radiation at the surface of the Earth. This value is positive downwards, following the ECMWF convention.                                                                  |
| `surface_direct_solar_radiation`               | *W/m<sup>2</sup>* | Direct solar radiation (shortwave) reaching the surface of the Earth, passing through a horizontal plane.                                                                                                                                      |
| `direct_normal_solar_radiation`                | *W/m<sup>2</sup>* | Solar radiation received per unit area normal to the direction of the sun.                                                                                                                                                                     |
| <nobr>`surface_diffuse_solar_radiation`</nobr> | *W/m<sup>2</sup>* | Scattered solar radiation received per horizontal unit area on the surface.                                                                                                                                                                    |


### Group 4: Pressure, Humidity, & Precipitation

| Parameter                                    | Unit    | Description                                                                                                                                                                    |
|:---------------------------------------------|:------: |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `relative_humidity`                          | -       | Relative humidity calculated from dewpoint temperature, drybulb temperature, and pressure. Relative humidity values range from 0 to 1.                                         |
| `surface_pressure`                           | *Pa*    | The pressure (force per unit area) of the atmosphere at the surface of land, sea, and inland water.                                                                            |
| `mean_sea_level_pressure`                    | *Pa*    | The pressure (force per unit area) of the atmosphere at sea level.                                                                                                             |
| `total_cloud_cover`                          | -       | Single level field calculated from the cloud occurring at different model levels through the atmosphere.                                                                       |
| `total_precipitation`                        | *mm*    | The accumulated liquid and frozen water, comprising rain and snow, that falls to the Earth's surface. It is the sum of large-scale precipitation and convective precipitation. |
| `snowfall`                                   | *mm*    | The accumulated snow that falls to the Earth's surface. It is the sum of large-scale snowfall and convective snowfall.                                                         |
| `volumetric_soil_water_layer_1`              | -       | Soil moisture at level 1 (0 - 7 cm)                                                                                                                                            |
| `volumetric_soil_water_layer_2`              | -       | Soil moisture at level 2 (7 - 28 cm)                                                                                                                                           |
| `volumetric_soil_water_layer_3`              | -       | Soil moisture at level 3 (28 - 100 cm)                                                                                                                                         |
| <nobr>`volumetric_soil_water_layer_4`</nobr> | -       | Soil moisture at level 4 (100 - 289 cm)                                                                                                                                        |


### Group 5: Other Parameters

| Parameter                                            |             Unit              | Description                                                                                                                                                                                                            |       
|:-----------------------------------------------------|:-----------------------------:|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `boundary_layer_height`                              |              *m*              | The depth of air next to the Earth's surface which is most affected by the resistance to the transfer of momentum, heat, or moisture across the surface.                                                               |
| `cloud_base_height`                                  |              *m*              | The height above the Earth's surface of the base of the lowest cloud layer, at the specified time.                                                                                                                     |
| <nobr>`convective_available_potential_energy`</nobr> |            *J/kg*             | Indication of the instability (or stability) of the atmosphere and can be used to assess the potential for the development of convection, which can lead to heavy rainfall, thunderstorms, and other severe weather.   |
| `convective_inhibition`                              |              *J/kg*           | This parameter is a measure of the amount of energy required for convection to commence.                                                                                                                               |
| `downward_uv_radiation_at_the_surface`               |       *W/m<sup>2</sup>*       | The amount of ultraviolet (UV) radiation reaching the surface. It is the amount of radiation passing through a horizontal plane.                                                                                       |
| `evaporation`                                        |             *mm*              | The accumulated amount of water that has evaporated from the Earth's surface, including a simplified representation of transpiration (from vegetation), into vapour in the air above.                                  |
| `forecast_albedo`                                    |               -               | A measure of the reflectivity of the Earth's surface.                                                                                                                                                                  |
| `forecast_surface_roughness`                         |              *m*              | The aerodynamic roughness length in metres as a measure of the surface resistance.                                                                                                                                     |
| `friction_velocity`                                  |             *m/s*             | A theoretical wind speed at the Earth's surface that expresses the magnitude of stress.                                                                                                                                |
| `high_cloud_cover`                                   |               -               | The proportion of a grid box covered by cloud occurring in the high levels of the troposphere.                                                                                                                         |
| `high_vegetation_cover`                              |               -               | The fraction of the grid box that is covered with vegetation that is classified as "high". The values vary between 0 and 1 but do not vary in time.                                                                    |
| `leaf_area_index_high_vegetation`                    | *m<sup>2</sup>/m<sup>2</sup>* | The surface area of one side of all the leaves found over an area of land for vegetation classified as "high".                                                                                                         |
| `leaf_area_index_low_vegetation`                     | *m<sup>2</sup>/m<sup>2</sup>* | The surface area of one side of all the leaves found over an area of land for vegetation classified as "low".                                                                                                          |
| `low_cloud_cover`                                    |               -               | The proportion of a grid box covered by cloud occurring in the lower levels of the troposphere.                                                                                                                        |
| `low_vegetation_cover`                               |               -               | The fraction of the grid box that is covered with vegetation that is classified as "low". The values vary between 0 and 1 but do not vary in time.                                                                     |
| `medium_cloud_cover`                                 |               -               | The proportion of a grid box covered by cloud occurring in the middle levels of the troposphere.                                                                                                                       |
| `potential_evaporation`                              |             *mm*              | A measure of the extent to which near-surface atmospheric conditions are conducive to the process of evaporation.                                                                                                      |
| `skin_reservoir_content`                             |             *mm*              | The amount of water in the vegetation canopy and/or in a thin layer on the soil.                                                                                                                                       |
| `sub_surface_runoff`                                 |             *mm*              | The water  that drains away under the ground.                                                                                                                                                                          |
| `surface_latent_heat_flux`                           |       *W/m<sup>2</sup>*       | The transfer of latent heat (resulting from water phase changes, such as evaporation or condensation) between the Earth's surface and the atmosphere.                                                                  |
| `surface_runoff`                                     |             *mm*              | The water  that drains away over the ground.                                                                                                                                                                           |
| `total_column_rain_water`                            |      *kg/m<sup>2</sup>*       | The total amount of water in droplets of raindrop size (which can fall to the surface as precipitation) in a column extending from the surface of the Earth to the top of the atmosphere.                              |
| `total_column_water_vapour`                          |      *kg/m<sup>2</sup>*       | The total amount of water vapour in a column extending from the surface of the Earth to the top of the atmosphere.                                                                                                     |
| `zero_degree_level`                                  |              *m*              | The height above the Earth's surface where the temperature passes from positive to negative values, corresponding to the top of a warm layer.                                                                          |


### Group 6: Air Quality

| Parameter   |        Unit         | Description                                                                                                   |
|:------------|:-------------------:|---------------------------------------------------------------------------------------------------------------|
| `CO`        | *ug/m<sup>3</sup>*  | Carbon Monoxide                                                                                               |
| `NO`        | *ug/m<sup>3</sup>*  | Nitrogen Oxide                                                                                                |
| `NO2`       | *ug/m<sup>3</sup>*  | Nitrogen Dixoide                                                                                              |
| `O3`        | *ug/m<sup>3</sup>*  | Ozone                                                                                                         |
| `PM10`      | *ug/m<sup>3</sup>*  | Particulate Matters (PM) inhalable particles, with diameters that are generally 10 micrometers and smaller.   |
| `PM25`      | *ug/m<sup>3</sup>*  | Particulate Matters (PM) inhalable particles, with diameters that are generally 2.5 micrometers and smaller.  |
| `SO2`       | *ug/m<sup>3</sup>*  | Sulfur Dioxide                                                                                                |  


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
