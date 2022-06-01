# sqlalchemy-challenge
# Unit 10 Homework: Surf’s Up using SQLAlchemy 

### Part 1: Climate Analysis and Exploration
* I used Python and SQLAlchemy to perform basic climate analysis and data exploration of the climate database.

#### A. Precipitation Analysis
* To perform an analysis of precipitation in the area, I found the most recent date in the dataset. Using this date, I retrieved the previous 12 months of precipitation data by querying the 12 previous months of data. Selecting only the Date and the precipitation values, a dataframe with date as the index was created. Using Matplotlib, the data was plotted to show the precipitation for the last year. After sorting the data by date , a summary statistics of the precipitation data was shown.

#### B. Station Analysis
* To perform an analysis of stations in the area, to answer the following questions:
* Calculate the total number of stations in the dataset.

* Query to find the most active stations (the stations with the most rows).

    * List the stations and observation counts in descending order.

    * Which station id has the highest number of observations?

    * Using the most active station id, calculate the lowest, highest, and average temperatures.
* Design a query to retrieve the previous 12 months of temperature observation data (TOBS).

    * Filter by the station with the highest number of observations.

    * Query the previous 12 months of temperature observation data for this station.

    * Plot the results as a histogram with `bins=12`

### Part 2: Design Your Climate App
* Flask API based on the queries that have just developed.
* Used Flask to create the routes:
* `/`

    * Homepage.

    * List all available routes.

* `/api/v1.0/precipitation`

    * Convert the query results to a dictionary using `date` as the key and `prcp` as the value.

    * Return the JSON representation of your dictionary.

* `/api/v1.0/stations`

    * Return a JSON list of stations from the dataset.

* `/api/v1.0/tobs`

    * Query the dates and temperature observations of the most active station for the previous year of data.

    * Return a JSON list of temperature observations (TOBS) for the previous year.

* `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`

    * Return a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a given start or start-end range.

    * When given the start only, calculate `TMIN`, `TAVG`, and `TMAX` for all dates greater than or equal to the start date.

    * When given the start and the end date, calculate the `TMIN`, `TAVG`, and `TMAX` for dates from the start date through the end date (inclusive).

