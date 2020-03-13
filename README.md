# Mapping with flowmap

## Introduction 
While working on a project in the context of Social Network Analysis, I came accross www.flowmap.blue, a very intuitive tool that easily allows to map in and out degrees for geographical data. 
Flowmap only requires 2 things: the latitudes and longitudes of the nodes, and the flows between those nodes with weights of these edges.
I thus have decided to continuously build maps using this tool, and share the small work needed in data preparation in this repository.

## 1. Global Airplane Routes

### 1.1 Data Source
The first map I built is regarding the network of flights around the world. Using www.openflights.org 's data, I was easily able to get the requirements for the map. They hold a collection that contains around 67663 routes between 3321 airports on 548 airlines.

### 1.2 Final Map
Here is how the final map looks like:

![Final Result](/global_airplane_routes/final_result.png)

You can find it on the following link: https://flowmap.blue/1ndHiKo8z2B99ZQpToSfoIhI0RCbUsPZhqwNT0-U-TMk?v=38.642519,4.729908,1.54,0,0&a=0&b=1&bo=75&c=0&d=0&lt=1&lfm=ALL&col=PuBuGn&f=50

You can easily edit the colours,the animations, and clusters on the map itself. And you can analyze the graph as well, filtering for specific airports for instance. This is shown here:


![Examples](/global_airplane_routes/examples.png)
