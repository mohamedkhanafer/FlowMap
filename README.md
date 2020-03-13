# Mapping with flowmap

## Introduction 
While working on a project in the context of Social Network Analysis, I came accross www.flowmap.blue, a very intuitive tool that easily allows to map in and out degrees for geographical data. 
Flowmap only requires 2 things: the latitudes and longitudes of the nodes, and the flows between those nodes with weights of these edges.
I thus have decided to continuously build maps using this tool, and share the small work needed in data preparation in this repository.

## 1. Global Airplane Routes

### 1.1 Data Source
The first map I built is regarding the network of flights around the world. Using www.openflights.org 's data, I was easily able to get the requirements for the map. They hold a collection that contains around 67663 routes between 3321 airports on 548 airlines. You can find one file for the airports' data and one for the routes' data in the global_airplane_routes folder. 

### 1.2 Instructions
As mentionned above, in order to reproduce this map, all you need will be the airports with their geolocalisation. This data is directly provided by Open Flights. The second element you need is the number of flows between the airports, representing routes offered by an airline. I get these using the routes data and a few lines of code. All these are available in the global_airplane_routes folder in this repository.

### 1.3 Final Map
Here is how the final map looks like:

![Final Result](/global_airplane_routes/final_result.png)

You can find it on the following link: https://flowmap.blue/1ndHiKo8z2B99ZQpToSfoIhI0RCbUsPZhqwNT0-U-TMk?v=38.642519,4.729908,1.54,0,0&a=0&b=1&bo=75&c=0&d=0&lt=1&lfm=ALL&col=PuBuGn&f=50

You can easily edit the colours,the animations, and clusters on the map itself. And you can analyze the graph as well, filtering for specific airports for instance. This is shown here:


![Examples](/global_airplane_routes/examples.png)

## 2. Montreal' Bike Sharing System BIXI - Evolution over time

### 2.1 Data Sources
The goal of these maps here is to look at how the bike sharing network of Montreal has evolved from 2016 to 2019. To do so, I used data provided by www.montreal.bixi.com/en/open-data. I took the month of June of each year to make the comparison the less biased possible. And we can clearly see the expansion of the network over the years. The data for each month as well as for the stations is uploaded in the montreal_bikes.

### 1.2 Instructions
As in part 1. with the flights' map, here the stations are already provided. The small transformations are needed on the trips data in which I use the code to translate it into data I can use for flowmap. The code is self-explanatory and allows us to get the flows to use in Google Sheet for the map. The code and output are available in the montreal_bikes repository.

### 1.3 Final Map
Here is how the final map looks like:

![Animation over years](/montreal_bikes/Montreal_overtime.png)
