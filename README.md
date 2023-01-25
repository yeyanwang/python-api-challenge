# python-api-challenge

The **WeatherPy** directory contains 2 Jupyter Source Files **WeatherPy.ipynb** and **VacationPy.ipynb** which request relevant data from 2 API providers **OpenWeatherMap** and **Geoapify** for over 500 cities within the desired coordinates. The two Jupyter Source Files utilize Pandas library to create DataFrame for each dataset. Matplotlib library was imported to create series of scatter plots based on different variables. Scipy and linregress were also imported to help with statistical computation and generate linear regresssion line for the data points. Citipy was imported to generate list of cities with the coordinates, hvplot was imported for interactive data visualization, and geoviews is imported to explore and visualize data geographically.

### WeatherPy

**Findings:**

**Temperature vs. Latitude**
* There is a fairly strong negative correlation between temperature and latitude with a correlation coefficient of -0.8088479825279142 on Northern Hemisphere.
* There is a relatively strong positive correlation between temperature and latitude with a correlation coefficient of 0.4395572110498053 on Southern Hemisphere.

**Humidity vs. Latitude**
* There is a relatively strong positive correlation between humidity and latitude with a correlation coefficient of 0.45185249370432223 on Northern Hemisphere.
* There is a relatively strong positive correlation correlation between humidity and latitude with a correlation coefficient of 0.5439636787499419 on Southern Hemisphere.

**Cloudiness vs. Latitude**
* There is a weak positive correlation between cloudiness and latitude with a correlation coefficient of 0.30769331493282776 on Northern Hemisphere.
* There is a relatively strong positive correlation between cloudiness and latitude with a correlation coefficient of 0.4748614054462095 on Southern Hemisphere.

**Wind Speed vs. Latitude**
* There is a negligible to almost no correlation between wind speed and latitude with a correlation coefficient of 0.21507837130179397 on Northern Hemisphere.
* There is a weak negative correlation between wind speed and latitude with a correlation coefficient of -0.33748967967974725 on Southern Hemisphere.
