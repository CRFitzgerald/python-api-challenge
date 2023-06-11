# python-api-challenge

In this challenge, I use API requests to pull weather data from websites and parse the resulting JSONs for visualizations using Pandas and PyPlot. The two deliverables - described below - can be found in the WeatherPy folder.

## WeatherPy
For the first deliverable, I have created a Python script to visualize the weather of over 500 cities of varying distances from the equator. Through use of the citipy Python library, I was able to find city names associated with iterative lists of coordinate combinations. Using the resulting list of cities, I made the API call to OpenWeatherMap for temperature, humidity, and cloudiness data. I created scatter plots to show the relationship between these cities' latitudes and weather data points retrieved. Then I computed the linear regression of these models and overlaid it on the plots. 

### Tools Used:
* citipy Python library
* OpenWeatherMap API
* Python
* Pandas
* PyPlot

### Scatter Plots Showcasing Relationships:
* Latitude vs. Temperature
* Latitude vs. Humidity
* Latitude vs. Cloudiness
* Latitude vs. Wind Speed

### Linear Regression Computations of Relationships:
* Northern Hemisphere: Temperature vs. Latitude
* Southern Hemisphere: Temperature vs. Latitude
* Northern Hemisphere: Humidity vs. Latitude
* Southern Hemisphere: Humidity vs. Latitude
* Northern Hemisphere: Cloudiness vs. Latitude
* Southern Hemisphere: Cloudiness vs. Latitude
* Northern Hemisphere: Wind Speed vs. Latitude
* Southern Hemisphere: Wind Speed vs. Latitude

## VacationPy
Now it's time to narrow down the perfect vacation spot! Using the city weather data found in the WeatherPy deliverable, I used hvplot to create a map displaying a point for each city. The point size for each city is reflective of that city's humidity. Using .loc on the City Data dataframe, I narrowed down the cities to those with a specific temperature range, low wind speed, and no clouds. These resulting "ideal" cities were placed in a new dataframe with an empty column for hotel information. This column was filled through an API call to the GeoApify API. Finally, I added the hotel name and country as additional information in the hover for each city in the previously generated map
### Tools Used:
* GeoApify API 
* geoViews Python library
* Python
* Pandas
