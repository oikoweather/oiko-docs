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
                         'lon': [ ... ]'}
                 headers={'api-key': api_key}
                 )
```

### 

