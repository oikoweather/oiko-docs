# Quick Start

*From zero to weather hero in 5 minutes.*

So - how do you get weather data via API? When you make a data request via API, we need to know three key things:

* **Where** - so we know the location you're interested in. This can be an address or a city name that we can look up, the latitutde/longitude coordiates, or a latitude/longitude boundary. 
* **When** - so we know the time span of the data to fetch, since we have more than 80 years of data. If you don't tell us, we'll just assume that you're interested in simple weather forecast.
* **What** - so we know which weather parameters or dataset you're interested in. We have more than 60 parameters and many different datasets. If you don't tell us, we assume the usual suspects like the temperature, wind speed, and total precipitation etc.

## Basic Example 
Let's start with a simple example - requesting temperature and wind speed data for Toronto, Ontario for the last 30 years (1990 to 2020). 

The data is accessed using REST API by specifying the location, parameters and time-range of the data needed as shown below.


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
