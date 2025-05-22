Global Earthquake Data Visualization Project
Overview
This project retrieves real-time earthquake data with a magnitude of 2.5 and above from the United States Geological Survey (USGS) API. The data is processed and mapped using Python libraries such as folium, pandas, and matplotlib, creating an interactive world map that visualizes recent earthquakes.

How to run the code
- If the script contains a Colab link, simply click on it or copy-paste the URL into your browser.
- This will open the notebook in Google Colab, an interactive cloud-based environment.

Purpose & Features
The project aims to:
- Fetch earthquake data from the USGS API for the past week.
- Extract key earthquake details such as magnitude, latitude, longitude, and location.
- Store the earthquake data into a structured format using pandas.
- Visualize global earthquake events on an interactive world map with labeled markers.
- Save the visualization as an HTML file for offline viewing.

How It Works
1. Fetching Earthquake Data
- The script accesses the USGS earthquake API:
https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/2.5_week.geojson
- Converts the raw JSON response into a Python dictionary using json.loads().
- Extracts relevant earthquake details:
- Magnitude
- Longitude
- Latitude
- Location description
2. Storing & Processing Data
- The earthquake details are stored in lists (mags, lons, lats, locs).
- A pandas DataFrame is created with structured earthquake records.
3. Creating an Interactive World Map
- A Folium map is initialized with a default view centered at [20, 0] (OpenStreetMap).
- Each earthquake is plotted as a marker at its location, with:
- Magnitude
- Location name
- Interactive pop-up information
4. Saving the Interactive Map
- The complete map, showing all earthquake events, is saved as an HTML file:
m.save('Earthquake Data: 2.5+ Week.html')
- The user can open this file in a browser to explore earthquake occurrences.
