# ECOSTRESS Collection 2 Data Product Algorithms

This will contain the algorithms for the ECOsystem Spaceborne Thermal Radiometer Experiment on Space Station (ECOSTRESS) collection 2 data products. 

Please refer to the [ECOSTRESS tutorials](https://github.com/ECOSTRESS-Tutorials) for information on accessing and utilizing the ECOSTRESS data products.

ECOSTRESS collection 2 is a precursor to the [Surface Biology and Geology Thermal Infrared (SBG-TIR) Orbiting Terrestrial Thermal Emission Radiometer (OTTER) data products](https://github.com/sbg-tir).

This document will provide background information relevant to the ECOSTRESS mission and data products. 

```mermaid
flowchart TD
L1B_GEO_PGE[L1B GEO PGE]
L1B_RAD_PGE[L1B RAD PGE]
L2_LSTE_PGE[L2 LSTE PGE]
L1T_L2T_RAD_LSTE_PGE[L1T/L2T RAD LSTE PGE]
L2T_STARS_PGE[L2T STARS PGE]
L3T_L4T_JET_PGE[L3T/L4T JET PGE]

L1B_GEO_SWATH[L1B Geolocation Product]
L1B_RAD_SWATH[L1B RAD Swath Product]
L1G_RAD_GRID[L1G RAD Gridded Product]
L1T_RAD_TILE[L1T RAD Tiled Product]
L2T_STARS_TILE[L2T STARS Tiled Product]
L2_LSTE_SWATH[L2 LSTE Swath Product]
L2G_LSTE_GRID[L2G LSTE Gridded Product]
L2T_LSTE_TILE[L2T LSTE Tiled Product]
L2T_STARS_TILE[L2T STARS Tiled Product]
L3T_JET_TILE[L3T JET Tiled Product]
L4T_ESI_TILE[L4T ESI Tiled Product]
L4T_WUE_TILE[L4T WUE Tiled Product]

LP_DAAC[Stage for LP-DAAC]

L1T_RAD_TILE --> LP_DAAC
L1T_L2T_RAD_LSTE_PGE --> L2T_LSTE_TILE
L2T_LSTE_TILE --> LP_DAAC
L2T_LSTE_TILE --> L2T_STARS_PGE
L2T_STARS_PGE --> L2T_STARS_TILE
L2T_STARS_TILE --> LP_DAAC

L1B_GEO_PGE --> L1B_GEO_SWATH

L1B_RAD_PGE --> L1B_RAD_SWATH

L1B_RAD_SWATH --> L1T_L2T_RAD_LSTE_PGE
L1B_RAD_SWATH --> L1B_GEO_PGE
L1B_GEO_SWATH --> L1T_L2T_RAD_LSTE_PGE

L1T_L2T_RAD_LSTE_PGE --> L1G_RAD_GRID
L1T_L2T_RAD_LSTE_PGE --> L1T_RAD_TILE

L1G_RAD_GRID --> LP_DAAC
L1T_RAD_TILE --> LP_DAAC

L1B_GEO_SWATH --> L2_LSTE_PGE
L1B_RAD_SWATH --> L2_LSTE_PGE
L2_LSTE_PGE --> L2_LSTE_SWATH

L2_LSTE_SWATH --> L1T_L2T_RAD_LSTE_PGE
L2_LSTE_SWATH --> LP_DAAC

L2G_LSTE_GRID --> LP_DAAC

L2T_LSTE_TILE --> L3T_L4T_JET_PGE
L2T_STARS_TILE --> L3T_L4T_JET_PGE

L3T_L4T_JET_PGE --> L3T_JET_TILE
L3T_L4T_JET_PGE --> L4T_ESI_TILE
L3T_L4T_JET_PGE --> L4T_WUE_TILE

L3T_JET_TILE --> LP_DAAC
L4T_ESI_TILE --> LP_DAAC
L4T_WUE_TILE --> LP_DAAC
```
