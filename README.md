## Introduction: Mapping with flowmap
While working on a project in the context of Social Network Analysis, I came accross www.flowmap.blue, a very intuitive tool that easily allows to map in and out degrees for geographical data. 
Flowmap only requires 2 things: the latitudes and longitudes of the nodes, and the flows between those nodes with weights of these edges.
I thus have decided to continuously build maps using this tool, and share the small work needed in data preparation in this repository.

## 1. Global Airplane Routes
The first map I built is regarding the network of flights around the world. Using www.openflights.org 's data, I was easily able to get the requirements for the map. They hold a collection that contains around 67663 routes between 3321 airports on 548 airlines.
