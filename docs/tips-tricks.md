### Specifying locations

When specifying locations using latitude & longitude coordinate, there is no need to specify <a href="https://xkcd.com/2170/" target="_blank">more than two decimal places</a>.

### Calling multiple locations

If you need weather data for say thousands of locations, it's easier to do it with `POST` operation. Note the slight difference in the way data is specified.

```py linenums="1"
import requests

api_key = 'your-api-key'

r = requests.post('https://api.oikolab.com/weather',
                 params={'param': ['temperature', 'wind_speed'],
                         'lat': [ ... ],
                         'lon': [ ... ]',
                         'location_id': [ ... ]',
                         }
                 headers={'api-key': api_key}
                 )
```

### Notes on Precipitation

Weather forecasting would be much simpler if we didn't have to deal with water. From clouds to hails and deluge, hydrodynamics of water in the atmospher is an incredibly complex phenomena which not easily captured by reanalysis or even observation data. For application where this is critical, we recommend using TODO: rain dataset over ERA5 or ERA5Land data.

