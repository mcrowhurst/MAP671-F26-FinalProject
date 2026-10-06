# MAP671 F26 Final Project

## Author

Dr. Mike Crowhurst

## Course

MAP 671 - University of Kentucky

## Project Description

The purpose of this project is to map the locations of colleges and universities in the continental United States.  Symbols on the map will designate where Athletes In Action has staffed campus ministries, where we rely on CRU (via USCM Connect), SportLinc ministries, and where we have no presence.  The use of this map is by Executives of the organization and other planners as we seek to expand our outreach.

## Data Sources

- US Census Bureau -- U.S. State Boundaries 
- Athletes In Action -- Campus Ministry Dataset

## Creation Process
This map was created using QGIS using the following steps:

1. Acquired a US State boundary dataset from the US Census Bureau.  The file we used was cb_2025_us_state-500k.shp.
2. Edited and Imported list of Colleges and Universities with an AIA Status (No, Staffed, USCM Connect, SportLinc) for each school.
3. Converted the latitude and longitude fields in the CSV to decimal (from Text) and then converted those fields into a Point Layer using the Create Points from Table Tool.
4. Changed Symbology based on Status variable.
5. Filtered the state boundary layer to include only the "lower 48" states.
6. Set the Project CRS to EPSG:2163 (US National Atlas Equal Area).
7. Designed Map Layout in QGIS.
8. Exported the Map Layout as a TIFF (for Zoomable map).
9. Reprojected the TIFF image to EPSG:3857 (Web Mercator) using the Warp (Reproject) Tool.
10. Generated Map Web Tiles using GDAL2Tiles with Zoom Levels 5 through 10.
11. Edited Leaflet.html file to make sure map zooming features worked.
12. Verified other html files were correct to ensure Web-based map functionality.
13. Published the project on GitHub as a Private Repository.

## Static Maps

A folder _**\STATIC**_ in this repository contains to png files which are static versions of this map.

AIA Campus Static1200.png  
AIA Campus Static8000.png  

## Interactive Map

An Embedded Zoomable version of this map can be found [here](QGIS-Zoom/tml.
