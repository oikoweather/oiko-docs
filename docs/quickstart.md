# Quick Start

*From zero to weather hero in 5 minutes.*

We need to know three things when you make a data request:

* **Where** - so we know the location you're interested in. This can be a place name (we'll look up the lat/lon coordinate), the lat/lon coordiates, or a lat/lon boundary. You can even tell us hundreds of locations. 
* **When** - so we know the time span of the data to fetch, since we have more than 80 years of data. If you don't tell us, we'll just assume that you're interested in simple weather forecast.
* **What** - so we know which weather parameters or dataset you're interested in. We have more than 60 parameters and many different datasets. If you don't tell us, we assume the usual suspects like the temperature, wind speed, and total precipitation etc.

## A simple example 
Let's start with a simple example - requesting temperature, wind speed and surface solar radiation data for Toronto, Ontario for the last 30 years. 

The data is accessed REST API by specifying the location, parameters and time-range of the data needed.  


!!! note "Don't forget to use your API key!"

    You can find your API key in your account when you log in.

ECMWF

```py linenums="1"
import requests

api_key = 'your-api-key'

r = requests.get('https://api.oikolab.com/weather',
                 params={'param': ['temperature', 'wind_speed'],
                         'location': 'Toronto, Ontario',
                         'start': '1990-01-01',
                         'end': '2020-12-31'}
                 headers={'api-key': api_key}
                 )
```
This will return data in JSON format, which we can convert to dataframe using Python's Pandas library. Note that we return the dataset name so you know the pedigree of the data source.

```py linenums="1"
import pandas as pd
import json

weather_data = json.loads(r.json()['data'])

df = pd.DataFrame(index=pd.to_datetime(weather_data['index'],unit='s'),
                  data=weather_data['data'],
                  columns=weather_data['columns'])
```

{{ read_csv('./data/sample.csv') }}

