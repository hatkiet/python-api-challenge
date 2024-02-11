For the python-api-challenge, I have used the knowledge from the lecture and activities in class and with the help from ChatGPT to check my errors (if I have).

In this assignment, we have been required to use Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"
The answer might be obvious: "It gets hotter.” But how would we prove that?

Part 1: WeatherPy

I've used a Python script to visualize the weather of over 550 cities generated randomly at varying distances from the equator and then retrieve weather data from the OpenWeatherMap API. 
I have created a series of scatter plots to showcase the following relationships:
  - Latitude vs. Temperature

   <img width="572" alt="Screenshot 2024-02-10 at 9 50 01 PM" src="https://github.com/hatkiet/python-api-challenge/assets/154276115/3fc8a2f3-0cbe-402b-b9e3-6983a2615490">

  - Latitude vs. Humidity

   <img width="571" alt="Screenshot 2024-02-10 at 9 50 12 PM" src="https://github.com/hatkiet/python-api-challenge/assets/154276115/db5216d2-d4fd-4fa0-ba10-01278269670b">
 
  - Latitude vs. Cloudiness

    <img width="570" alt="Screenshot 2024-02-10 at 9 50 22 PM" src="https://github.com/hatkiet/python-api-challenge/assets/154276115/bee14c16-4282-47fe-b228-767980bfa53b">

  - Latitude vs. Wind Speed

   <img width="562" alt="Screenshot 2024-02-10 at 9 50 31 PM" src="https://github.com/hatkiet/python-api-challenge/assets/154276115/4bf39ce3-7693-4dae-b898-d268b8a61ca9">


Next, with the separation the plots into Northern and Southern Hemispheres, I computed the linear regression for each relationship and created linear regression plots of the following:

 - Northern Hemisphere: Temperature vs. Latitude
 - Southern Hemisphere: Temperature vs. Latitude
 - Northern Hemisphere: Humidity vs. Latitude
 - Southern Hemisphere: Humidity vs. Latitude
 - Northern Hemisphere: Cloudiness vs. Latitude
 - Southern Hemisphere: Cloudiness vs. Latitude
 - Northern Hemisphere: Wind Speed vs. Latitude
 - Southern Hemisphere: Wind Speed vs. Latitude

Part 2: VacationPy

I've used weather data obtained from part 1 to plan a future vacation with the help of Jupyter notebooks, geoViews Python library, and the Geoapify API

Here is the map displaying a point for every city in the "city_data_df" DataFrame, the size of the point is the humidity in each city.

<img width="1080" alt="Screenshot 2024-02-10 at 9 51 57 PM" src="https://github.com/hatkiet/python-api-challenge/assets/154276115/8a924fce-f2a1-4389-956c-a6927661d374">


Next, I have narrowed down the city list to find my ideal weather condition, which satisfy the following requirements: 
  - A max temperature lower than 27 degrees but higher than 21
  - Wind speed less than 4.5 m/s
  - Zero cloudiness

Then, use Geoapify API to find the first hotel located within 10 Km of the city coordinates and plot the map, which includes the information of hotel name and the country of each city on the map.

<img width="1037" alt="Screenshot 2024-02-10 at 9 52 09 PM" src="https://github.com/hatkiet/python-api-challenge/assets/154276115/4ec1bda9-6278-4d67-a5c4-0ef179237d9d">
