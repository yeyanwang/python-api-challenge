# Weather Analysis

The `WeatherPy` directory contains 2 Jupyter Source Files `WeatherPy.ipynb` and `VacationPy.ipynb` which request relevant data from 2 API providers **OpenWeatherMap** and **Geoapify** for over 500 cities within the desired coordinates, and a repo `output_data` which contains the output images generated from `WeatherPy.ipynb`. 

The two Jupyter Source Files utilize Pandas library to create DataFrame for each dataset. Matplotlib library was imported to create series of scatter plots based on different variables. Scipy and linregress were also imported to help with statistical computation and generate linear regresssion line for the data points. Citipy was imported to generate list of cities with the coordinates, hvplot was imported for interactive data visualization, and geoviews is imported to explore and visualize data geographically.

### WeatherPy

**Temperature vs. Latitude**
* There is a fairly strong negative correlation between temperature and latitude with a correlation coefficient of -0.8088479825279142 on Northern Hemisphere.
  
  ![image](https://user-images.githubusercontent.com/120543690/221319708-8a81956c-9f1a-45e6-aaa9-48f8bc23112a.png)

* There is a relatively strong positive correlation between temperature and latitude with a correlation coefficient of 0.4395572110498053 on Southern Hemisphere.

  ![image](https://user-images.githubusercontent.com/120543690/221319736-e66846f4-8bd8-4536-92eb-aeb43182c6d4.png)

**Humidity vs. Latitude**
* There is a relatively strong positive correlation between humidity and latitude with a correlation coefficient of 0.45185249370432223 on Northern Hemisphere.

  ![image](https://user-images.githubusercontent.com/120543690/221319757-623c49bc-c4b9-4cc9-ad20-002d25ee9bda.png)

* There is a relatively strong positive correlation correlation between humidity and latitude with a correlation coefficient of 0.5439636787499419 on Southern Hemisphere.

  ![image](https://user-images.githubusercontent.com/120543690/221319782-bf5da06a-42ae-4e55-a0d1-be071a521558.png)

**Cloudiness vs. Latitude**
* There is a weak positive correlation between cloudiness and latitude with a correlation coefficient of 0.30769331493282776 on Northern Hemisphere.

  ![image](https://user-images.githubusercontent.com/120543690/221319835-a8087945-34c7-491f-b9ad-2ff95ab7193e.png)

* There is a relatively strong positive correlation between cloudiness and latitude with a correlation coefficient of 0.4748614054462095 on Southern Hemisphere.

  ![image](https://user-images.githubusercontent.com/120543690/221319867-566a79b9-a00e-49ee-a348-2733745a83de.png)

**Wind Speed vs. Latitude**
* There is a negligible to almost no correlation between wind speed and latitude with a correlation coefficient of 0.21507837130179397 on Northern Hemisphere.

  ![image](https://user-images.githubusercontent.com/120543690/221319887-a099515b-01da-40c7-aea9-e56365834bff.png)

* There is a weak negative correlation between wind speed and latitude with a correlation coefficient of -0.33748967967974725 on Southern Hemisphere.
  
  ![image](https://user-images.githubusercontent.com/120543690/221319913-06ca2938-024f-447f-83f7-d1dc1d00cf03.png)

### VacationPy

* Create `city map` that displays a point for every city in the `city_data_df` DataFrame using data in `output_data/cities.csv`. The size of the point is determined by the humidity level in each city.


* Narrow down cities that fit the criteria and drop any results with null values, the criteria are listed below:
  1. A max temperature lower than 27 degrees but higher than 21
  2. Cloudiness less than 3
  3. Wind speed less than 4.5 m/s
  
* Create a new DataFrame called `hotel_df` which contains columns: `City`, `Country`, `Lat`, `Lng`, `Humidity`, and `Hotel Name`. For each city, use the **Geoapify API** to find the first hotel located within 10,000 metres of each city and append the results to `hotel df` in a column called `Hotel Name'.
    |City |Country| Lat | Lng |Humidity|Hotel Name|
    |:---:|:-----:|:---:|:---:|:------:|:--------:|
     |cidreira|	BR	|-30.1811	|-50.2056|	88	|Hotel Castelo|
    |umm lajj|	SA	|25.0213	|37.2685	|62	|No hotel found|
   |naliya	|IN	|23.2667	|68.8333	|21	|No hotel found|
   |itamaraca|	BR	|-7.7478	|-34.8256|	76|	No hotel found|
   |rio grande	|BR|	-32.0350|	-52.0986	|84	|Hotel Vila Moura Executivo|
 	 |acapulco	|MX	|16.8634	|-99.8901|	65	|Hotel del Valle|
   |jhanjharpur	|IN	|26.2667	|86.2833	|32	|No hotel found|

* Add the hotel name and the country as additional information in the hover message for each city in `hotel map`

