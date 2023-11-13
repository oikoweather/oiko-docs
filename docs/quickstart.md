# Quick Start

*From zero to weather hero in 5 minutes.*

So - how do you get weather data via API? When you make a data request via API, we need to know three key things:

* **Where** - so we know the location you're interested in. This can be an address or a city name that we can look up, the latitutde/longitude coordiates, or a latitude/longitude boundary. 
* **When** - so we know the time span of the data to fetch, since we have more than 80 years of data. If not specified the default period (from 3 days past to 7 days into the future) will be used.
* **What** - so we know which weather parameters or dataset you're interested in. We have more than 60 parameters and many different datasets. If not specified, it will default to `temperature`, `dewpoint_temperature`, `wind_speed`, `mean_sea_level_pressure`, `surface_solar_radiation`, `surface_thermal_radiation`, and `total_cloud_cover`.

## Basic Example 
Let's start with a simple example - requesting temperature and wind speed data for Toronto, Ontario, for the last 30 years (1990 to 2020). 

The data is accessed using REST API by specifying the location, the parameters, and the time-range of the data needed as shown below.

=== "Python"
    ```py linenums="1"
    import requests 
    
    api_key = 'your-api-key'
    url = 'https://api.oikolab.com/weather'

    # Call the endpoint to get the data
    r = requests.get(url,
                     params={'param': 'temperature',
                             'location': 'Toronto, Ontario',
                             'start': '1990-01-01',
                             'end': '2020-12-31'},
                     headers={'api-key': api_key}
                     )
    ```

=== "R"
    ```r linenums="1"
    library(httr)
     
    api_key <- 'your-api-key'
    url <- 'https://api.oikolab.com/weather'
    
    # Call the endpoint to get the data
    result <- GET(url,
                  query=list(param='temperature',
                             location='Toronto, Ontario',
                             start='1990-01-01',
                             end='2020-12-31'),
                  add_headers('api-key'=api_key)
                  )
    ```

!!! note "Don't forget to use your API key!"
    You can find your API key on the profile page when you log into your account.

This will return data in JSON format, which we can convert to dataframe using Python's [Pandas](https://pandas.pydata.org/) library. Note that the dataset name is returned so you always know which dataset was used to generate the data.

```py linenums="1"
import pandas as pd
import json

weather_data = json.loads(r.json()['data'])

df = pd.DataFrame(index=pd.to_datetime(weather_data['index'],unit='s'),
                  data=weather_data['data'],
                  columns=weather_data['columns'])
```

{{ read_csv('./data/sample.csv') }}

*[JSON]: JavaScript Object Notation
