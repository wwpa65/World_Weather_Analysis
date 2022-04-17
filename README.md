# World_Weather_Analysis

# Creating A Travel Itinerary

## Overview
The goal of this project was to prepare a travel itinerary app based on weather data of cities using weather API and a Google Maps API (Including google maps directions API. For this task, weather pattern of list of cities were searched to identify potential travel destinations (and nearby hotels) and these destinations were selected from user inputs. Finally, this application was expanded to map a route with fouridentified travel destinations as a testing procedure. 


## Methods
1. Generating a Weather Database:[Weather Database](/Weather_Database/WeatherPy_Database.csv)
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


# Results
The weather database (as a csv file was generated: 

![Vacation Destinations](/Vacation_Search/WeatherPy_vacation_map.png)
**Map showing a some travel destinations in the world**

3. Creating a Travel Itinerary Map
- The spreadsheet of destination cities with hotels were imported into a Pandas data frame.
- Using an HTML-type infobox template, city, country code, weather description and maximum temperature was included into cities.
- These data were stored in a list and also added information into the formatting template.
- A new dataframe with location coordinates was generated.
- A figure was created with marker layer and a heat layer.
- A set of 4 cities were selected (start, stop1, stop2, stop3, end) and tuples containing geo-coordinates (latitude and longitude) by using to_numpy function and list indexing. 
- A map was created and a directions layer was included into the map.

Then these weather data were filtered to match cities based on the preference of maximum and minimum temperatures (weather preferences) obtained from the user inputs. Then these weather preferences were used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, four cities were chosen to create a travel itinerary. Using the Google Maps Directions API, a travel route between the four cities and a marker layer map was created

![Vacation Travel Route](/Vacation_Itinerary/WeatherPy_travel_map.png)

**Map showing a travel toute that include 4 cities of India**



![Vacation Hotels and Conditions](/Vacation_Itinerary/WeatherPy_travel_map_markers.png)
**Map showing a 4 travel destination cities of India**


