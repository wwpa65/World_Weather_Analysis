# World_Weather_Analysis

# Creating A Travel Itinerary

## Overview
The goal of this project was to prepare a travel itinerary app based on weather data of cities using weather API and a Google Maps API (Including google maps directions API. For this task, weather pattern of list of cities were searched to identify potential travel destinations (and nearby hotels) and these destinations were selected from user inputs. Finally, this application was expanded to map a route with fouridentified travel destinations as a testing procedure. 


## Methods
1. Generating a Weather Database:
- A list of random latitudes and longitudes were generated
- These coordinates were used to generate nearby cities using citipy library
- The weather dataof cities were collected using Weather API (using an api key).
- A Pandas dataframe was generated and finally a csv file (weather database) was created.

2. Identifying Travel Destinations
- The weather database was imported as a Pandas dataframe
- Using users preferences as inputs (minimum and maxmimum temperature), the weather data was filtered using .loc method to create a new data frame. 
- Empty rows were removed.
- A new dataframe was created by including an empty column to be used for hotel names
- Names of nearby hotels in the cities were extracted by using google API and geo-coordinates.
- These hotel names were included into the new data frame.
- Empty rows were removed and this list was used to generate a map. The list was exported into a csv file (to be used in the itinarary).
- A marker layer was added into the map to visualize potential travel destinations. 

![Vacation Destinations](/Vacation_Search/WeatherPy_travel_map.png)

3. Creating a Travel Itinerary Map

Then these weather data were filtered to match cities based on the preference of maximum and minimum temperatures (weather preferences) obtained from the user inputs. Then these weather preferences were used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, four cities were chosen to create a travel itinerary. Using the Google Maps Directions API, a travel route between the four cities and a marker layer map was created

# Results
