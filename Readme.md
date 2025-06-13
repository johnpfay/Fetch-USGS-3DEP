# Fetch USGS 3DEP LiDAR 

Summer 2025<br>
John.Fay@duke.edu

---

This workspace contains code to download all the USGS 3DEP LiDAR tiles for the Hurricane Florence Project. The local files are stored on a [Box drive](https://duke.box.com/s/r336r6eu1optwa342xtmplpym1roj69z) and are organized into folders representing the 13 project folders distributed by the USGFS. 

Links to the source files are contained in the `src`\\`download_links.csv` folder. [*To add: how this file was created*].

Also included is code to download the tile index shapefiles for each of the 13 project areas and merge them into a single feature class in a geodatabase called `USGS3DEP_Indices.gdb` located in the `TileIndices` folder of the Box drive. 

### Scripts

* `00_Create-Download-Link-File.ipynb` - Scrapes the USGS 3DEP Hurricane Florence archive to create a single CSV file of all the direct download links for each tile LAS file.
* `00a_Fetch-Tile-Index-Files.ipynb` - Downloads the geopackage of tile indices for each of the 13 Florence projects and merges the features into a single feature class. 
* `01_Fetch-USGS-3DEP-Tiles.ipynb` - Downloads all the USGS 3DEP Hurricane Florence LAS files. The local files are stored on a [Box drive](https://duke.box.com/s/r336r6eu1optwa342xtmplpym1roj69z) and are organized into folders representing the 13 project folders distributed by the USGFS. 
* `02_Extract-DEM-From-laz.ipynb` - Processes the raw 3DEP LAZ files for each tile intersecting a the footprint of a Duke Drone Team derived LAS dataset, converting each tile into a 0.5m DEM and then mosaicking the tile DEMs into a single DEM.
* `03_Merge-LAS-Files.ipynb` - Creates a LAS Dataset (.lasd) comprised of the individual tiled LAS files for a given pilot project flight area. 
