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
