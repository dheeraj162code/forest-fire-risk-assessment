# Fire Risk Mapping Project

## Overview
This project visualizes fire incidents and fire risk zones in the Chamrajnagar region using Leaflet.js. It integrates GeoJSON data to map fire incidents, classify risk zones, and analyze vegetation types to assess fire risk.

## Features
- **Fire Incident Mapping:** Displays fire locations with detailed metadata.
- **Date Filtering:** Allows users to filter incidents by date.
- **Risk Zone Visualization:** Categorizes areas into Low, Medium, and High risk based on fire density.
- **Vegetation-Based Risk Assessment:** Uses Overpass API to classify vegetation and determine risk levels.
- **Convex Hull Algorithm:** Groups fire incidents into clusters and visualizes them as polygons.
- **Interactive Controls:** Toggle risk zones and filter data dynamically.

## Algorithms Used
### 1. **Fire Density Calculation**
   - Groups fire incidents into a grid of 0.1-degree cells.
   - Counts the number of incidents in each cell.
   - Categorizes risk zones based on density.

### 2. **Clustering Algorithm for Fire Incidents**
   - Uses a distance-based approach to cluster fire incidents.
   - Ensures exactly 10 non-overlapping clusters are formed.
   - Prioritizes densest clusters for visualization.

### 3. **Vegetation Classification Algorithm**
   - Fetches vegetation data using the Overpass API.
   - Analyzes vegetation type (grassland, forest, scrub, wetland, etc.).
   - Maps vegetation to fire risk levels.

### 4. **Convex Hull Algorithm for Fire Risk Zones**
   - Uses Graham's scan method to compute the convex hull of fire points.
   - Forms risk zone polygons around clustered fire incidents.
   - Assigns colors based on vegetation type and risk level.

## Setup Instructions
1. Clone the repository.
2. Ensure the `data` directory contains the necessary GeoJSON files.
3. Open `fire_incident_map.html` or `fire_risk_map.html` in a browser.
4. Ensure an internet connection for Overpass API requests.

## Future Improvements
- Implement an AI/ML model for fire risk prediction.
- Enhance vegetation classification using satellite imagery.
- Optimize clustering for dynamic risk assessment.

## Dependencies
- Leaflet.js
- Overpass API
- Convex Hull Algorithm

## Contact
For queries, reach out to dheerajshetty162@gmail.com.

