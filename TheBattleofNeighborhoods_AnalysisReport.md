#TheBattleofNeighborhoods Analysis Report
Now that you have been equipped with the skills and the tools to use location data to explore a geographical location, over the course of two weeks, you will have the opportunity to be as creative as you want and come up with an idea to leverage the Foursquare location data to explore or compare neighborhoods or cities of your choice or to come up with a problem that you can use the Foursquare location data to solve. If you cannot think of an idea or a problem, here are some ideas to get you started:

In Module 3, we explored New York City and the city of Toronto and segmented and clustered their neighborhoods. Both cities are very diverse and are the financial capitals of their respective countries. One interesting idea would be to compare the neighborhoods of the two cities and determine how similar or dissimilar they are. Is New York City more like Toronto or Paris or some other multicultural city? I will leave it to you to refine this idea.
In a city of your choice, if someone is looking to open a restaurant, where would you recommend that they open it? Similarly, if a contractor is trying to start their own business, where would you recommend that they setup their office?
These are just a couple of many ideas and problems that can be solved using location data in addition to other datasets. No matter what you decide to do, make sure to provide sufficient justification of why you think what you want to do or solve is important and why would a client or a group of people be interested in your project.

# 1. Introduction/Business Problem

A description of the problem and a discussion of the background.

Clearly define a problem or an idea of your choice, where you would need to leverage the Foursquare location data to solve or execute. Remember that data science problems always target an audience and are meant to help a group of stakeholders solve a problem, so make sure that you explicitly describe your audience and why they would care about your problem.


***The idea of this study is to help people planning to open a new coffee shop in Toronto to chose the right location by providing data about the income and population of each neighborhood as well as the competitors already present on the same regions.***

# 2. Data

A description of the data and how it will be used to solve the problem

Describe the data that you will be using to solve the problem or execute your idea. Remember that you will need to use the Foursquare location data to solve the problem or execute your idea. You can absolutely use other datasets in combination with the Foursquare location data. So make sure that you provide adequate explanation and discussion, with examples, of the data that you will be using, even if it is only Foursquare location data.

***To provide the stakeholders the necessary information I'll be combining Toronto's newest Census that contains Population, Average income per Neighborhood with Toronot's Neighborhoods shapefile and Foursquare API to collect competitors on the same neighborhoods.
Toronto's Census data is publicly available at this website: https://www.toronto.ca/city-government/data-research-maps/open-data/open-data-catalogue/#8c732154-5012-9afe-d0cd-ba3ffc813d5a***

***Toronto Neighborhoods' shapefile is publicly available at this website: https://www.toronto.ca/city-government/data-research-maps/open-data/open-data-catalogue/#a45bd45a-ede8-730e-1abc-93105b2c439f***

***Foursquare data***

## 3.Methodology 
Methodology section which represents the main component of the report where you discuss and describe any exploratory data analysis that you did, any inferential statistical testing that you performed, and what machine learnings were used and why.

***I had used the map to help a new investor to decide the best neighborhood to open a coffee shop in Toronto based on it's income, population and available competitors. In order to do that I used the Census information combined with choropleth maps to visually display the wealthier and more populational neighborhoods and Foursquare data to display the current coffee shop in each region.***

## 4.Results
Results section where you discuss the results.

***Comparing the maps we can notice the majority of the coffee shop grouped on main streets and nearby park, welthiest neighborhoods have not shown more interest in coffee. Also, the areas with a dense population don't reflect on the number of Café.***

## 5. Discussion
Discussion section where you discuss any observations you noted and any recommendations you can make based on the results.

***When I first decided to create this study I was expecting to find clusters of coffeeshop in certain regions and find some connection between Coffee consumption and welth/population, but the final result didn't meet that expectation.***

## 6.Conclusion
Conclusion section where you conclude the report.

***This report may be helpful for someone planning on opening a coffee shop in Toronto, by comparing the current offers and neighborhoods profiles, however it may not cover all variables such as access to public transportation or even the coffee shop profiles, so it shall not be used as a single decidion making tool.***