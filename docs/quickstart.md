# Quick Start

*From zero to weather hero in 5 minutes.*

We need to know three things when you make a data request via API:

* **Where** - so we know the location you're interested in. This can be a place name (we'll look up the lat/lon coordinate), the lat/lon coordiates, or a lat/lon boundary. You can even tell us hundreds of locations. 
* **When** - so we know the time span of the data to fetch, since we have more than 80 years of data. If you don't tell us, we'll just assume that you're interested in simple weather forecast.
* **What** - so we know which weather parameters or dataset you're interested in. We have more than 60 parameters and many different datasets. If you don't tell us, we assume the usual suspects like the temperature, wind speed, and total precipitation etc.

## A simple example 
Let's start with a simple example - requesting temperature, wind speed and surface solar radiation data for Toronto, Ontario for the last 30 years (1990 to 2020). 

The data is accessed REST API by specifying the location, parameters and time-range of the data needed.  


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
!!! note "Don't forget to use your API key!"
    You can find your API key in profile page when you log into your account.

This will return data in JSON format, which we can convert to dataframe using Python's Pandas library. Note that we return the dataset name so you know the which dataset was used to generate the data.

```py linenums="1"
import pandas as pd
import json

weather_data = json.loads(r.json()['data'])

df = pd.DataFrame(index=pd.to_datetime(weather_data['index'],unit='s'),
                  data=weather_data['data'],
                  columns=weather_data['columns'])
```

{{ read_csv('./data/sample.csv') }}

For regional dataset, you can provide the bounding latitude and longitude values. In this case, we'll return the data in NetCDF format. For example, the following request will return HRRR forecast data for California. Note that when calling datasets such as this, the response can be several gigabytes in size and can take more than a few seconds to process.

```py linenums="1"
import requests

api_key = 'your-api-key'

r = requests.get('https://api.oikolab.com/weather',
                 params={'param': ['temperature', 'wind_speed'],
                         'north': 65,
                         'south': 45,
                         'east': -110,
                         'west': -130,
                         'model': 'hrrr'}
                 headers={'api-key': api_key}
                 )
```

