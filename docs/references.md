
## /weather 

Parameter | Description                                 | Notes
--------- |---------------------------------------------| -------------
`param`   | Valid parameters                            | Default: `temperature`, `dewpoint_temperature`, `wind_speed`, `mean_sea_level_pressure`, `surface_solar_radiation`, `surface_thermal_radiation`, `total_cloud_cover`
`start`   | start datetime string `YYYY-MM-DD` (UTC)    | Defaults to 3 days into the past. Provided time is interpreted as UTC.
`end`     | end datetime string `YYYY-MM-DD` (UTC)      | Defaults to 7 days into the future. Provided time is interpreted as UTC.
`freq`    | `H` (hourly), `D` (daily), or `M` (monthly) | Defaults to `H` 
`resample_method`   | `max`, `mean` or `min`                      | When the frequency is set to daily (`D`) or monthly (`M`), this can be used to request maximum or minimum value during the specififed period.
`location`| city name or zipcode                        | This value is used to look up latitude/longitude.
`lat`     | latitude(s)                                 | If `location` is not provided. Up to 100 locations allowed.
`lon`     | longitude(s)                                | If `location` is not provided. Up to 100 locations allowed.
`north`   | latitude north                              | For bounding box.
`south`   | latitude south                              | For bounding box.
`east`    | longitude east                              | For bounding box.
`west`    | longitude west                              | For bounding box.
`model`   | `era5`, `gfs`, `era5land`, `hrrr`, `cfs`    | Use to specify dataset if applicable.
`format`  | `json`, `csv`, or `netcdf`                  | Defaults to `json`

## /airquality

Parameter | Description                              | Notes
--------- |------------------------------------------| -------------
`param`   | Valid parameters                         | Default: `NO`, `SO`, `PM10`, `PM25`, `Ozone`
`location`| city name or zipcode                        | This value is used to look up latitude/longitude.
`lat`     | latitude(s)                                 | If `location` is not provided. Up to 100 locations allowed.
`lon`     | longitude(s)                                | If `location` is not provided. Up to 100 locations allowed.
