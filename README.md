# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
- Practicing API calls and understanding the importance of reading responses to efficiently parse and extract the desired data.
- Preparing data for further analysis or model building by assessing what information is essential and what can be omitted.
- Building the model, understanding the meaning of the output, and exploring how it can be used in the future.

## Process
### Step 1 Connecting to CityBikes API
I connected to [City Bikes](https://citybik.es) on Saturday, August 3, to collect data for bike stations in Vancouver. I retrieved information on 254 stations, from which I decided to keep data on bike availability, slot availability, location, station name, and their unique identifiers. The process and further details are documented in the [city_bikes notebook](notebooks/city_bikes.ipynb).
### Step 2 Connecting to Foursquare and Yelp APIs
I connected with Foursquare and Yelp to acquire data about the nearest points of interest for each bike station. This was challenging due to API call limitations, particularly with Yelp, where only 300 calls are free per 24 hours. To make a fair comparison, I decided to request data for the same categories from both Yelp and Foursquare. The process and further details are documented in the [yelp_foursquare_EDA notebook](notebooks/yelp_foursquare_EDA.ipynb).

### Step 3 Joining Data
I combined the data from the previous steps and performed basic exploratory data analysis using Matplotlib and Seaborn. Additionally, I created an SQL database from the obtained data in this step. The process and further details are documented in the [joining_data notebook](notebooks/joining_data.ipynb).

### Step 4 Building a Model
I build a linear regression model in this step. The process and further details are documented in the [model_building notebook](notebooks/model_building.ipynb)

## Results
I built a simple linear regression model to see if we could predict the number of free bikes based on the distance to nearby venues. The model finds a statistically significant relationship between the distance from the bike station and the number of available bikes. However, the effect is so small that it may not be meaningful. The low R-squared value indicates that distance alone is not a good predictor of available bikes, suggesting that other factors should be explored to better explain the variation in the number of available bikes.

## Challenges 
- Understanding API data and parsing JSON was the most time-consuming and challenging part of the project. The complex data structures made it difficult to extract the information I needed.

- The data acquired from different sources through APIs varies in quality. Depending on our goals, preparing this data for further analysis can be very time consuming.


## Future Goals
- If I had more time, I would try obtaining data on different points of interest to see if any patterns emerge. For example, I would investigate whether there is a pattern in bike availability on weekends considering the proximity of parks around the stations.
- I would improve the structure of my SQL database.
- I would explore building different types of models. For instance, a Multivariate Linear Regression model might provide better insights.
