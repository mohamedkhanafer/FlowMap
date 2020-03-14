# Mapping with flowmap

## Introduction 
While working on a project in the context of Social Network Analysis, I came accross www.flowmap.blue, a very intuitive tool that easily allows to map in and out degrees for geographical data. 
Flowmap only requires 2 things: the latitudes and longitudes of the nodes, and the flows between those nodes with their respective weights.
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
The goal of these maps here is to look at how the bike sharing network of Montreal has evolved from 2016 to 2019. To do so, I used data provided by www.montreal.bixi.com/en/open-data. I took the month of June of each year to make the comparison the less biased possible. And we can clearly see the expansion of the network over the years. The data for the stations is uploaded in the montreal_bikes. However, because the trips' original data files are too large, you can download them from the links posted in the text file and use the month of June as in the lines of code.

### 1.2 Instructions
As in part 1. with the flights' map, here the stations are already provided. The small transformations are needed on the trips data in which I use the code to translate it into data I can use for flowmap. The code is self-explanatory and allows us to get the flows to use in Google Sheet for the map. The code and output are available in the montreal_bikes repository.

### 1.3 Final Maps
Here is how the final map looks like:

<p align="center">
  <img src=https://github.com/mohamedkhanafer/FlowMap/blob/master/montreal_bikes/overtime.gif>
</p>

You can find each of the maps on the following links:

For 2016: https://flowmap.blue/145uEjRIgjMypkbRFmAN62KQ2lTqaNMdAwIGtzBBTmgI?v=45.507602,-73.582851,11.41,0,0&a=0&b=1&bo=75&c=0&d=0&lt=1&lfm=ALL&col=DarkMint&f=50

For 2017: https://flowmap.blue/14_-aINZKivX3_Ma-_iAyiMKb8BlFHcun9GDTVODSl0g?v=45.507602,-73.582851,11.31,0,0&a=0&b=1&bo=75&c=0&d=0&lt=1&lfm=ALL&col=DarkMint&f=50

For 2018: https://flowmap.blue/1J4Bk4Y0B6cJluyulUMzR0xMAKcz9LO-uUUUH-5qE_iI?v=45.507526,-73.582114,11.41,0,0&a=0&b=1&bo=75&c=0&d=0&lt=1&lfm=ALL&col=DarkMint&f=50

For 2019: https://flowmap.blue/1APu7yHTPZg6j0c8ggbj09ViGseqnvN-TDUEO31WVIqA?v=45.509453,-73.602573,11.02,0,0&a=0&b=1&bo=75&c=0&d=0&lt=1&lfm=ALL&col=DarkMint&f=50

The individual outputs should be like these:

![Each year](/montreal_bikes/years.png)

### 1.4 Alternative Analysis 
For a project, I was analysing this bike system as a Social Network to try to find insights. One way I used flowmap differently this time, is to show specific clusters of flows, rather than comparing them for their weights. I applied community detection using the Louvain algorithm in another tool called Gephi (used for Social Networks). I got 6 distinct clusters that I later mapped in flowmap to be able to visualize them. Here is what they looked like:

![Each year](/montreal_bikes/clusters.png)

Here is the link to one of the maps: https://flowmap.blue/1xry0bK8OAEr3gx2JB6Mr7k5gDMuVu_BL8wLH1jpn7cE?v=45.540457,-73.653655,11.18,0,0&a=0&b=1&bo=75&c=0&d=0&lt=0&lfm=ALL&col=Sunset&f=44.
As you can see, in the flows part, I put the same stations in both columns, going from one to the other with equal weights. That is how I was able to show the clusters. This can be reproduced by running any clustering method, using the criteria of choice and later use the stations got in each cluster.
