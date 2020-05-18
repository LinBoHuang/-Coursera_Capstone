# Capstone Project - The Battle of the Neighborhoods (Week 1)
### Applied Data Science Capstone by IBM/Coursera

## Table of contents
* [1.Introduction: Business Problem](#introduction)
* [2.Data](#data)
* [3.Methodology](#methodology)
* [4.Analysis](#analysis)
* [5.Results and Discussion](#results)
* [6.Conclusion](#conclusion)

## 1.Introduction: Business Problem <a name="introduction"></a>

In this project we will try to find an optimal location for a restaurant. Specifically, this report will be targeted to stakeholders interested in opening an **seafood restaurant** in **Toronto**, ON, Canada.

Since there are lots of restaurants in Toronto we will try to detect **locations that are not already crowded with much more seafood restaurants**. We would also prefer locations **as close to rich and safe neighborhood as possible**, and we are also particularly interested in **areas with more population in the  neighborhood**, assuming that first condition are met.

We will use our data science powers to generate a few most promissing neighborhoods based on this criteria. Advantages of each area will then be clearly expressed so that best possible final location can be chosen by stakeholders.

## 2.Data <a name="data"></a>

Based on definition of our problem, factors that will influence our decission are:
* number of existing restaurants in the neighborhood (any type of restaurant)
* number of existing seafood restaurants in the neighborhood
* number of criminal case in the neighborhood.
* average income of the neighborhood.
* population of the neighborhood.

Following data sources will be needed to extract/generate the required information:
* ***To provide the stakeholders the necessary information we will combine Toronto's newest Census that contains Population, Average income per Neighborhood with Toronot's Neighborhoods shapefile and Foursquare API to collect competitors on the same neighborhoods.Toronto's Census data is publicly available at this website: https://www.toronto.ca/city-government/data-research-maps/open-data/open-data-catalogue/#8c732154-5012-9afe-d0cd-ba3ffc813d5a***
* ***Toronto Neighborhoods' shapefile is publicly available at this website: https://www.toronto.ca/city-government/data-research-maps/open-data/open-data-catalogue/#a45bd45a-ede8-730e-1abc-93105b2c439f***
* ***Also,we will get the Toronto Crime data from kaggle.com. we can download the data from this website: https://www.kaggle.com/alincijov/toronto-crime-rate-per-neighbourhood***

### Download and Explore Dataset

Prepare the dataset, we can directly download **Toronto Population_data.csv** from website, and should register kaggle first then download **Neighbourhood_Crime_Rates_(Boundary_File)_.csv**

Collecting neighborhoods names

Creat a new dataset for the data we need (Population and Income data of each neighborhood)

Explore the Crime Rate data

Get the newset crime data columns with 2019,and we will use the summary of all type crimes as a crime factor.

### combine **population data** and **crime data**

### Visualize the data

#### (1)**Population Map in Toronto**

#### (2)**Income Map in Toronto**

#### (3)**Crime rate Map in Toronto**

### Foursquare Data
Now that we have our location candidates, let's use Foursquare API to get info on restaurants in each neighborhood.

We're interested in venues in 'food' category, but only those that are proper restaurants - coffe shops, pizza places, bakeries etc. are not direct competitors so we don't care about those. So we will include in out list only venues that have 'restaurant' in category name, and we'll make sure to detect and include all the subcategories of specific 'Seafood restaurant' category, as we need info on seafood restaurants in the neighborhood.

Looking good. So now we have all the restaurants for each neighborhood, and we know which ones are seafood restaurants! We also know which restaurants exactly are in vicinity of every neighborhood candidate center.

This concludes the data gathering phase - we're now ready to use this data for analysis to produce the report on optimal locations for a new seafood restaurant!

## 3.Methodology <a name="methodology"></a>

In this project we will direct our efforts on detecting areas of Toronto that have low restaurant density, particularly those with low number of Seafood restaurants. 

In first step we have collected the required data: location and type (category) of every restaurant within 500m from each neighborhood center. We have also identified seafood restaurants (according to Foursquare categorization).

Second step in our analysis will be calculation and exploration of 'restaurant density' across different areas of Toronto - we will use choropleth maps to identify a few promising areas with low number of restaurants in general (and no seafood restaurants in vicinity) .

In third and final step we will use the data to create clusters of locations , and try to find out a cluster that meet some basic requirements established in discussion with stakeholders: we will take into consideration locations with low number of restaurants in the neigherhood, and we want locations without seafood restaurant in radius of 500 meters, we also want locations at lower crime rate and high income neighborhood. We will present map of all such locations but also create clusters (using k-means clustering) of those locations to identify general zones / neighborhoods / addresses which should be a starting point for final 'street level' exploration and search for optimal venue location by stakeholders.

## 4.Analysis <a name="analysis"></a>
Let's perform some basic explanatory data analysis and derive some additional info from our raw data. First let's count the number of restaurants in every area candidate:

Now, we have Seafood Restaurant's numbers and total numbers of all restaurants with each neighborhood.We will combine the population, income, crimeRate, totalRestaurantsNum, SeafoodRestaurantsNum of each neighborhood in a dataset


### Restaurants map in Toronto
We use choropleth map to show the restaurants and seafood restaurants of each neighborhood

### The clustering results show that the dataset is divided into four categories:
- **The first group** is characterized by the largest population, the lowest income, the highest crime rate, and a small number of restaurants (including seafood restaurants).
- **The second group** is characterized by a small population, the highest income, the lowest crime rate, and a large number of restaurants (including seafood restaurants).
- **The third group** is characterized by a large population, low income, high crime rate and the largest number of restaurants (including seafood restaurants).
- **The fourth group** is characterized by a small population, low income, a moderate crime rate, and the fewest restaurants (including seafood restaurants).

Based on the several key factors we selected when choosing a restaurant address in the "Business Problem" paragrah , we will consider the final selection in the second and third group. One of the reasons is that the price of seafood is usually higher than the price of general food, so we need to consider the affordability of residents. Second, we need to consider the safety of the neigborhood, and then the number of existing restaurants and the number of people.
 
#### Finally, we decided to choose the two group which is a group of the highest income and the safest neighborhoods.


Now let ’s look at these neighborhood on the different  choropleth map

#### (1) Selected Neighborhoods on **the Crime Rate Map**

#### (2) Selected Neighborhoods on **the Income Map**

#### (3) Selected Neighborhoods on **the Population Map**

#### (4) Selected Neighborhoods on **the Restaurants Map** (By Heatmap)

#### (5) Selected Neighborhoods on **the Sedfood Restaurants Map** (By Heatmap)

## 5.Results and Discussion <a name="results"></a>

According to several choropleth maps, we will eventually choose a location  in Lawrence Park South or Forest Hill to open a seafood restaurant. There are currently no seafood restaurant in these two neighborhoods, also there are just relatively few restaurants and low crime rate, higher income residents and tha a moderate population.


Result of all this is 2 neighborhoods containing largest number of potential new restaurant locations based on crime rate, income, population and existing venues - both restaurants in general and seafood restaurants particularly. This, of course, does not imply that those zones are actually optimal locations for a new restaurant! Purpose of this analysis was to only provide info on areas of toronto's neighorhood but not crowded with existing restaurants (particularly Seafood) - it is entirely possible that there is a very good reason for small number of restaurants in any of those areas, reasons which would make them unsuitable for a new restaurant regardless of lack of competition in the area. Recommended zones should therefore be considered only as a starting point for more detailed analysis which could eventually result in location which has not only no nearby competition but also other factors taken into account and all other relevant conditions met.

## 6.Conclusion <a name="conclusion"></a>

Purpose of this project was to identify Toronto areas with low number of restaurants (particularly seafood) in order to aid stakeholders in narrowing down the search for optimal location for a new seafood restaurant.  We collected data on the population, income, and crime rate of 140 neighborhoods in the Toronto area from the public database of the Toronto Municipality. We also obtained data from Foursquare about restaurants (including seafood restaurants) within 500 meters of each neighborhood center. According to the data we got, the population, income, crime rate, number of restaurants, and number of seafood restaurants in each neighborhood are used as variables, and then used k-means clustering to create the main classification group. Through the analysis of the classificated data, the neighborhoods that satisfied the business requirements conditions proposed at the beginning of this article, were selected to be used as starting points for final exploration by stakeholders.

Final decission on optimal restaurant location will be made by stakeholders based on specific characteristics of neighborhoods and locations in every recommended zone, taking into consideration additional factors like attractiveness of each location (proximity to park or water), levels of noise / proximity to major roads, real estate availability, prices, social and economic dynamics of every neighborhood etc.

