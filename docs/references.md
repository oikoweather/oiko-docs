The following endpoints are available.

## /weather 

Parameter | Description                            | Notes
--------- |----------------------------------------| -------------
param   | Valid parameters                       | Default: temperature, dewpoint_temperature, wind_speed, mean_sea_level_pressure, surface_solar_radiation, surface_thermal_radiation, total_cloud_cover
start   | start datetime string YYYY-MM-DD (UTC) | Defaults to 3 days into the past. Provided time is interpreted as UTC.
end     | end datetime string YYYY-MM-DD (UTC)   | Defaults to 7 days into the future. Provided time is interpreted as UTC.
freq    | H (hourly), D (daily), or M (monthly)  | Defaults to H 
resample_method   | max, mean, min, or sum                 | When the frequency is set to daily (D) or monthly (M), use this to specify the aggregation method.
location| city name or zipcode                   | This value is used to look up latitude/longitude.
location_id| reference for location                 | This is handy when making requests for multiple locations.
lat     | latitude(s)                            | If location is not provided. Up to 100 locations allowed.
lon     | longitude(s)                           | If location is not provided. Up to 100 locations allowed.
north   | latitude north                         | For bounding box.
south   | latitude south                         | For bounding box.
east    | longitude east                         | For bounding box.
west    | longitude west                         | For bounding box.
model   | era5, era5land, gfs, gefs, hrrr, cfs   | Use to specify dataset if applicable.
format  | json, csv, or netcdf                   | Defaults to json

#### Example
```py linenums="1"
import requests

api_key = 'your-api-key'

r = requests.get('https://api.oikolab.com/weather',
                 params={'param': ['temperature', 'wind_speed'],
                         'lat': [32, 24, 40],
                         'lat': [32, 24, 40],
                         'location_id': ['store1', 'store2','store3'],
                         'start': '2022-01-01',
                         'end': '2022-12-31'}
                 headers={'api-key': api_key}
                 )
```


## /airquality

Parameter | Description           | Notes
--------- |-----------------------| -------------
param   | Valid parameters      | Default: NO, SO, PM10, PM25, Ozone
location| city name or zipcode  | This value is used to look up latitude/longitude.
lat     | latitude(s)           | If location is not provided. Up to 100 locations allowed.
lon     | longitude(s)          | If location is not provided. Up to 100 locations allowed.

```py linenums="1"
import requests

api_key = 'your-api-key'

r = requests.get('https://api.oikolab.com/airquality',
                 params={'lat': [32, 24, 40],
                         'lat': [32, 24, 40],
                         'location_id': ['store1', 'store2','store3'],
                 headers={'api-key': api_key}
                 )
```

## /epw

This API will return an EPW file for the given location and year (if applicable). Each EPW files will be 250 units. The EPW is generated from ERA5 data on the fly so it will take 10~15 seconds and is not limited to airport locations. 

Parameter | Description            | Notes
--------- |------------------------| -------------
location  | city name or zipcode   | This value is used to look up latitude/longitude.
year      | year for AMY           | If not specified, a TMY file will be returned using the latest 15 years of data (180 months).
lat       | latitude(s)            | If location is not provided.
lon       | longitude(s)           | If location is not provided.


