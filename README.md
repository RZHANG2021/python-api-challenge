# python-api-challenge

Part I - WeatherPy

In this section, the goal is to write a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator.  
The simple Python library and the Open Weather Map API have been utilized to generate a data frame that listing 500+ randomly selected cities as well as the weather. 
To analyse the various weather factors relationship towards latitude, a series of scatter plots are generated to showcase the relationships as per below
•	Temperature (F) vs. Latitude
•	Humidity (%) vs. Latitude
•	Cloudiness (%) vs. Latitude
•	Wind Speed (mph) vs. Latitude
In addition, linear regression is also performed on the relationships listed, however this time, the plots were separated into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude), ie:
•	Northern Hemisphere - Temperature (F) vs. Latitude
•	Southern Hemisphere - Temperature (F) vs. Latitude
•	Northern Hemisphere - Humidity (%) vs. Latitude
•	Southern Hemisphere - Humidity (%) vs. Latitude
•	Northern Hemisphere - Cloudiness (%) vs. Latitude
•	Southern Hemisphere - Cloudiness (%) vs. Latitude
•	Northern Hemisphere - Wind Speed (mph) vs. Latitude
•	Southern Hemisphere - Wind Speed (mph) vs. Latitude
Observation:
Regarding the relationship between latitude and temperature, besides a few outliers, the scatter plot appears to be a bell shaped pattern, indicates that there is a non-linear relationship between latitude and temperature. 
Potentially we can check the data, to find the missing variable can help to build a more accurate non-linear relationship among the latitude, temperature and the variable that we found.
Furthermore, based on the linear regression analysis, it appears that there is a strong correlation between temperature and latitude. In northern hemisphere, these two factors appear to have a relatively strong negative correlation, however in northern hemisphere, it also indicates a strong correlation but in positive direction.
The analysis also compared the relationship among humidity, cloudiness, and wind speed to latitude. All indicates that here is no relationship among these factors 



Part II - VacationPy

In this section, the jupyter-gmaps and the Google Places API are utilized to generate a heat map based on the cities and weather data frame generated from the prior section.
A heat map that displays the humidity for every city is generated:

<img width="432" alt="heat map" src="https://user-images.githubusercontent.com/82508049/122574664-3c937a00-d093-11eb-81de-d0082ff2afdb.PNG">

In addition, a new data frame is generated with specific weather condition:
•	A max temperature between 15 to 35.
•	Wind speed less than 15 mph.
•	Humidity in between 25-50
•	cloudiness in between 10-35
 
Based on the new data frame generated, Google Places API is used to find the first hotel for each city located within 5000 meters of your coordinates. Then jupyter-gmaps is used to Plot the hotels on top of the humidity heatmap with each pin containing the Hotel Name, Address, City, and Country.
The plot looks like the below:

<img width="430" alt="hotel" src="https://user-images.githubusercontent.com/82508049/122574894-7e242500-d093-11eb-826d-877cc7e92022.PNG">


