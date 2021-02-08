# nkg_transformation_test

This repository has a QGIS project where the NKG transformation between EPSG:7789 and EPSG:4936(EPSG:25833) is tested.

## Content

- no_kv_NKGETRF14_EPSG7922_2000.tif (ETRD14-EPSG7922 correction grid)
- NKG.gpkg (data in GeoPackage format)
- NKG_transformation.qgz (QGIS workspace)
- QGIS layers:
  1. NKG_original_Helmert (original PAR_2020_NO)
  2. NKG_modified_Helmert (modified PAR_2020_NO)

1. Input to the transformation:
    - geocentric ITRF2014 coordinates of the norwegian PGS stations in epoch 2020.0.
    
2. Input coordinates are transformed to EPSG:25833 in Proj based on the NGK implementation from the branch:
    - https://github.com/kbevers/PROJ/tree/nkg_transformations
    
3. The output coordinats from Proj are compared to the fixed native EPGS:25833 coordinates.     
