# Fetch USGS 3DEP LiDAR 

Summer 2025<br>
John.Fay@duke.edu

---

This workspace contains code to download all the USGS 3DEP LiDAR tiles for the Hurricane Florence Project. The local files are stored on a [Box drive](https://duke.box.com/s/r336r6eu1optwa342xtmplpym1roj69z) and are organized into folders representing the 13 project folders distributed by the USGFS. 

Links to the source files are contained in the `src`\\`download_links.csv` folder. [*To add: how this file was created*].

Also included is code to download the tile index shapefiles for each of the 13 project areas and merge them into a single feature class in a geodatabase called `USGS3DEP_Indices.gdb` located in the `TileIndices` folder of the Box drive. 


