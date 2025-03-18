# Vehcle Data Analysis and Visuralizaiton
## Introduction

This project is insighted by the following article about data flow of car in a city-scale

Article source: https://www.nature.com/articles/s41597-022-01850-0

Data source: 
Wang, Yimin; Chen, Yixian; Li, Guilong; Lu, Yuhuan; Yu, Zhi; He, Zhaocheng (2022). Command Line Tool for Virtual Traffic Flow Detection of Xuancheng City. figshare. Journal contribution. https://doi.org/10.6084/m9.figshare.18737183.v1

Wang, Yimin; Chen, Yixian; Li, Guilong; Lu, Yuhuan; Yu, Zhi; He, Zhaocheng (2022). Trajecory Reconstruction Related Data of Xuancheng City. figshare. Dataset. https://doi.org/10.6084/m9.figshare.18737165.v1

Wang, Yimin; Chen, Yixian; Li, Guilong; Lu, Yuhuan; Yu, Zhi; He, Zhaocheng (2022). Resampled Traffic Flow Data of Xuancheng City. figshare. Dataset. https://doi.org/10.6084/m9.figshare.18700553.v1

## Project Info

### 1. Data Processing & Cleaning

Used Pandas and PySpark to efficiently handle large datasets.

Performed data extraction, transformation, and loading (ETL) from CSV files.

Cleaned and preprocessed vehicle trajectory data to ensure data consistency and accuracy.

### 2. Big Data & Distributed Computing

Utilized Apache Spark (PySpark) for handling large-scale vehicle datasets.

Applied Spark SQL to query and analyze vehicle movement patterns.

### 3. Geospatial Data Handling & Visualization

Processed geospatial road network data using GeoPandas and Shapely.

Generated interactive Folium maps to visualize roads and vehicle trajectories.

Applied OpenStreetMap and Leaflet.js for location-based data representation.

### 4. Data Analysis & Insights Extraction

Implemented time-series analysis on vehicle movement using Pandas.

Computed travel time, speed variations, and distance metrics for traffic behavior assessment.

Grouped vehicle data based on time thresholds to identify driving patterns.

### 5. Algorithm Development for Route Tracking

Developed a function to compute shortest paths and travel time for vehicles using graph-based approaches.

Applied trajectory tracking techniques to monitor vehicle movements across road networks.

### 6. Data Visualization & Reporting

Created insightful Seaborn and Matplotlib plots to represent vehicle speed, travel distance, and other metrics.

Automated report generation for easy interpretation of results.

### Tools & Technologies Used

Programming Languages: Python

Libraries & Frameworks: Pandas, PySpark, GeoPandas, Folium, Matplotlib, Seaborn, Shapely

Big Data Tools: Apache Spark, Spark SQL

Geospatial Mapping: OpenStreetMap, Leaflet.js



## Notebook Update Log – Shortest Path Trip Connection

### New Features & Enhancements:

#### Road Network Graph Construction:

Loaded road data from road_data.csv and preprocessed the geometry by replacing semicolons with commas.
Built an undirected road network graph using NetworkX by adding edges between road segments (using the dnroad field) with the road length as the edge weight.
Enhancement: This graph structure now allows efficient route computations between segments.

#### Shortest Path Algorithm Integration:

Introduced a function (find_shortest_path) that leverages Dijkstra’s algorithm (via NetworkX) to compute the shortest path between two given road segments.
New Capability: Enables connecting non-adjacent segments when direct road continuity isn’t available.

#### Trip Grouping & Road Segment Connection:

Continued to load and process vehicle trajectory data (veh1_data.csv) by converting time stamps, sorting chronologically, and grouping trips based on a 10-minute time gap.
Developed the connect_road_segments function that iterates through each trip group and, if two consecutive road segments are not directly connected, uses the shortest path function to bridge the gap.
Outcome: Each trip is now enhanced with the computed shortest paths to form a continuous trajectory.

#### Map Visualization Enhancements:

Used Folium for interactive mapping:
Displayed each group with a gradient color scheme created via matplotlib’s color maps, helping to visually distinguish trips.
Added start and end markers (CircleMarkers) for each group along with popup tooltips to indicate group information.
Incorporated a helper function (linestring_to_geojson) to convert LINESTRING data (WKT) to GeoJSON for consistent mapping.

#### New Dependencies and Libraries:

Added support for NetworkX (graph operations), geopy (for potential distance calculations), matplotlib.colors (to generate custom color gradients), and numpy (for numerical operations).
These additions enable more advanced spatial analysis and visualization of the road and vehicle data.
