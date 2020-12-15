# python-api-challenge

## There are two parts in the project thay are accompanied by two jupiter notebooks:
#### Part I 
[WeatherPy](WeatherPy/WeatherPy.ipynb)
Python script to visualizes the weather of 500+ cities across the world of varying distance from the equator. I'm utilizing [Python library](https://pypi.python.org/pypi/citipy) and [OpenWeatherMap API](https://openweathermap.org/api) to create a representative model of weather across world cities

The script creates a series of scatter plots to showcase the following relationships:
* [Temperature (F) vs. Latitude](Images/city_latitude_vs_max_temp.png)
* [Humidity (%) vs. Latitude](Images/city_latitude_vs_humidity.png)
* [Cloudiness (%) vs. Latitude](Images/city_latitude_vs_cloudiness.png)
* [Wind Speed (mph) vs. Latitude](Images/city_latitude_vs_wind_speed.png)

The second step of the first exersize, I separated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). Then with the new data sets I have visualized the following relations including linear regression for all of them:

* [Northern Hemisphere - Temperature (F) vs. Latitude](Images/NH_max_tem_vs_lat.png)
* [Southern Hemisphere - Temperature (F) vs. Latitude](Images/SH_max_tem_vs_lat.png)
* [Northern Hemisphere - Humidity (%) vs. Latitude](Images/NH_humidity_vs_lat.png)
* [Southern Hemisphere - Humidity (%) vs. Latitude](Images/SH_humidity_vs_lat.png)
* [Northern Hemisphere - Cloudiness (%) vs. Latitude](Images/NH_cloudiness_vs_lat.png)
* [Southern Hemisphere - Cloudiness (%) vs. Latitude](Images/SH_cloudiness_vs_lat.png)
* [Northern Hemisphere - Wind Speed (mph) vs. Latitude](Images/NH_wind_speed_vs_lat.png)
* [Southern Hemisphere - Wind Speed (mph) vs. Latitude](Images/SH_wind_speed_vs_lat.png)

#### Part II
[VacationPy](VacationPy/VacationPy.ipynb)

This part of the project utilises gmaps extension to create a [heat map](Images/heat_map.png) that displays the humidity for every city from **Part I**

As the next, step I narrowed down the list of citiest by applying the following weather conditions:
  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.

  Then, using oogle Places API I found the first hotel for each city located within 5000 meters of each city coordinates.
  Finally, I plotted the hotels on [on the map](Images/heat_map_with_citymarkers.png) by adding markers to it 