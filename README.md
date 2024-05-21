# VRP_Compiegne
 This code is used for a project modeling the operation and charging process of electric buses with photovoltaic panel support. It defines bus routes using geographic coordinates of stops and observed altitudes along these routes. The resulting altitude variations enable a more precise energy consumption model.


                                            # Usage of Python Codes and Associated Documents #
                                                                  
# Anaconda:

First, install Anaconda from this link : https://www.anaconda.com/products/distribution.
The software offers several IDEs, but we recommend using Jupyter Lab for better usability.

# Codes:

The codes enable successive analysis and data processing.
They are segmented into several parts, including calculations and operations on altitude, distances, etc., to format data for use in Matlab code. Some additional codes exist but remain underutilized. They include daily service definitions with bus stops and various travel time combinations by routes.
It's advisable to verify query results occasionally, as the databases may lack precision in certain areas.


# GTFS Data Excel File:


Working with the initial GTFS file open is crucial for better code understanding.
The Excel file allows code updates and data changes based on bus lines. For example, "id:3" isolates line numbers, though they may not always correspond to names/numbers. Ensure correspondence in the GTFS Excel file.
The file contains many columns; key elements include:
--> id: Direction number at each stop (regardless of route)
--> id1: Stop number (associated with a specific time)
--> id2: Bus line number
--> id3: Trip number
--> id4: Weekly combination number (operational days)

# Shapefiles:

A shapefile is a file format for geographic information systems (GIS).

Typically, it has an SHP extension and is accompanied by two other files:

--> .dbf: Contains attribute data related to shapefile objects.
--> .shx: Stores geometry index.
--> .shp: The geometry of the entity itself.

Other relevant file types include:

--> .prj (recommended): Stores associated projection.
--> .cpg: Specifies the code page for .dbf files.

The shapefile for the Oise department is available from the OTM (Open Transport Map) website:

-- > Click on "Open OTM as data," leading to this page : https://opentransportmap.info/download/.
--> Select country/regions/departments (Note: names may be outdated, e.g., Picardie Region).
--> Download the zip file in shp format and open it in Jupyter.

To convert the shapefile to xlxs, save the processed file from Jupyter in Excel format (Export function available).

# Desired Improvements:

Dynamic display of bus positions. Currently, only stops for one bus line can be shown at a time. It would be useful to see the buses moving.
Reimportation of the map (HTML map) to rewrite and add more bus lines to trace the entire city's bus network. We have yet to find a way to import pre-constructed bus line maps for use. The maps are built using the folium library.
Exploiting road (bus) traffic maps. We have an Excel file with road traffic volume data, which can be mapped using geopandas (see code). Unfortunately, we only managed the display. It would be beneficial to interpolate the map with Compiègne's bus lines to identify congested bus routes and derive delay probabilities.


# Websites:

https://open-elevation.com/

https://github.com/Jorl17/open-elevation

https://www.openstreetmap.org/#map=6/46.449/2.210

https://github.com/openstreetmap/

https://opentransportmap.info/

https://github.com/giggls/openptmap


# Associated Documents:

The GTFS file of Compiègne
The shapefile folder
The shp file in Excel format
An example HTML map
The Python code in IPYNB format
