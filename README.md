# Optimizing-Urban-Logistics-with-Network-Analysis-in-Rotterdam
Urban Logistics Network Analysis – Rotterdam

This project explores urban logistics optimization in the city of Rotterdam, Netherlands. By combining geospatial analysis with mathematical optimization, we aim to solve one of the most fundamental supply chain design problems:

**Where should we place warehouses (or distribution centers) to best serve a set of delivery points?**

We approach this using real road network data, simulate delivery demand, and use Mixed Integer Linear Programming (MILP) to minimize total transportation cost.

## Objectives
- Identify optimal warehouse locations to minimize delivery distance.
- Assign each delivery point to its nearest open facility.
- Visualize reachability and routing using real city streets.
- Teach and demonstrate how spatial networks + optimization models can be combined effectively.

## Key Analyses
1. Shortest Route Calculation
- Use Dijkstra’s algorithm to find the shortest path between two warehouse nodes.
- Visualized using Folium over the street network.

2. Closest Facility Assignment
- Generate synthetic delivery points within Rotterdam bounds.
- Find and assign each to its nearest warehouse using KDTree and network distance.

3. Service Area Analysis (Isochrones)
- Visualize how far each warehouse can reach within 5 km and 10 km.
- Uses ego graphs to generate network-based catchment zones.

5. Facility Location Optimization
- Apply PuLP to formulate and solve the MILP model.
- Optimize warehouse placement and demand point assignments based on a cost matrix of distances.

## Tools & Libraries
osmnx | Street network retrieval and graph building
networkx | Graph analysis and shortest path calculation
folium | Interactive mapping
geopandas | Spatial operations and data handling
PuLP | Linear and integer optimization
matplotlib | Result visualization

## Data Source
- Dutch Distribution Centres 2021 Geodata: https://data.4tu.nl/articles/dataset/Dutch_Distribution_Centres_2021_Geodata/19361018
- Road network: OpenStreetMap via OSMnx
