# Walking Accessability Anaysis from Buildings to Supermarkets (Open-Street-Maps)



Here in this project Open-Street-Map-Data was used to extract every residential buildings and supermarkets of the city Duisburg. Furthermore pedestrian network was used to calculate the nearest path from each supermarket to every existing residential building. 

## 
This presentation provides the code for Network Accessability Analysis of walking distance of each residential building to the nearest supermarket. The product was derived with networkx, pyrosm, osmnx, geopandas, numpy, matplotlib and itertools.



# Highlights 

You ever wondered how far each citizen in your city has to walk to the nearest supermarket? This project makes it possible to establish an understanding of the walking distances for every residential building existing within the corresponding city boundary to its nearest supermarket. It derives the residential buildings, supermarkets and the cities pedestrian network, cleans and manages OMS-derived datasets, links the nearest nodes of each building and supermarket and computes the shortest-path distances with the help of the walking graph. 

The main script is accessible in the notebook: 


# Research Question

1. How far is the walking distance of every residential building in town to the nearest supermarket?
2. What district has on average the closest distance to the supermarkets? 


# Tools and Packages

- Python
- Pyrosm
- NetworkX
- OSMnx
- GeoPandas
- pandas
- Matplotlib
- NumPy
- pathlib
- itertools 


# Data
Data was extracted from OpenStreetMap with Pyrosm. For buildings the following tags were used: 

# Method
1. Define Input and Output Directory
2. Download and create a graph within the boundaries of Duisburg (`network_type = walk`).
3. Project the graph to an appropriate UTM (Zone 32N / EPSG:32632).
4. Retrieve residential buildings and supermarkets by the boundary of Duisburg.
5. Transform geometry of buildings and supermarkets to points with `.geometry.representative_point()` and snap each to the nearest node available.
6. Calculate shortest weighted path length with NetworkX `multi_source_dijkstra_path_length()`
7. Categories the results for better interpretation and `plot()` them.  

## Results



## Author

Master Degree in Environmental Science with the Specialization of Geoinformatics and Remote Sensing. I am a huge OSM-Enthusiast and deeply faszinated by the sheer endless possibilities that came with it. 

*Information about me and why it did what i did*

## References 


