# Introduction

Bangkok is the capital and most important city in Thailand, with a population of over eight million people. Thanks to its growing economic development and massive popularity as an international tourist destination, it become one of southeast Asia's most influential and modern cities.

Millions of tourist come here every year to enjoy the beautiful seightseeing, heritage sites, hanging around the city and visit shopping centers and one important thing is the thai tranditional food which is always easy to find and try on it. This is a key of success who those want to start the business about the food or others likes Thai Spa to serve for foreigners. 


# Business Problems

In part of Restaurant or food and beverage business, so there are always unlimited possibilities for those who want to open their own restaurants. But the biggest challenge they are facing is which location is the best that relatively small competition, large passenger, tourists flow and good surrounding resources.

To solve this inquiry, this project is going to do neighborhood segmentation in Bangkok using a popular clustering techniques, and try to figure out a solution for potential restaurant investors.


# Data 

The neighborhood segmentation in Bangkok, the neighborhood data is scraped by using BeautifulSoup function from Wikipedia (https://en.wikipedia.org/wiki/List_of_districts_of_Bangkok) to find out the districts in Bangkok, and corresponding coordinates are obtained by using GeoCoder. All data of venues in each neighborhoods is retrieved by Foursquare API. 

There are 51 districts in Bangkok is considered and selected 80% to scope down the areas which are contained 926 venues with 166 different venue categories in Bangkok for further segmenting the neighborhoods.


# Methodologies

Several techniques are applied for data acquisition, data pre-processing and analytic model in Python as following.

## Data Acquisition
The official neighborhood list is retreived from Wikipedia (https://en.wikipedia.org/wiki/List_of_districts_of_Bangkok) which scraped by using BeautifulSoup including Requests packages with python (jupyter notebook). The corresponding coordinates (Latitude & Longtitude) of each neighborhoods are obtained by using Geocoder and all venue information is retreived from Foursquare API.

## Data Pre-processing
The official neighborhoods scraped from Wikipedia is cleaned to get 51 districts(neighborhoods) in Bangkok Thailand and converted to Neighborhood dataframe to getting the cooresponding coordinates. 

Once getting the neighborhood list, the correspoding are retreived from Geocoder which searching through ArcGIS to be further location references.

The neighborhood coordinates and neighborhood names are cleaned and pre-processed, the venue informations sorted by each name and its corresponding coordinates are retrieved from FourSquare API that communicated through Web URL configured by CLIENT_ID, CLIENT_SECRET, VERSION, LATITUDE, LONGTITUDE, RADIUS amd LIMIT. The Radius is set to search the nearby neighborhood names which set default at 500 methers and limited 100 venues per each neighborhood. The venue information consists of Venue Name, Venue Location (Latitude and Longtitude coordinates, Venue Categories within the Radius and Limits.

The Venue information, a categorical feature is transformed to numerical features by using One-Hot-Encoding. The frequency of each venue category in each neighborhood is calculated to be used as key features in neighborhood segmentation. The Top 10 most common venues category are identified for each neighborhood.

# Model Development
The K-Mean unsupervised machine learning technique are selected to cluster similar neighborhoods, and Elbow method is applied to get the optimal number of cluster, and Folium is used to visualize those resulting clusters on the map.

# Result;
Please follow ; 

