# ECOSTRESS Collection 2 Data Product Algorithms

This will contain the algorithms for the ECOsystem Spaceborne Thermal Radiometer Experiment on Space Station (ECOSTRESS) collection 2 data products. 

Please refer to the [ECOSTRESS tutorials](https://github.com/ECOSTRESS-Tutorials) for information on accessing and utilizing the ECOSTRESS data products.

ECOSTRESS collection 2 is a precursor to the [Surface Biology and Geology Thermal Infrared (SBG-TIR) Orbiting Terrestrial Thermal Emission Radiometer (OTTER) data products](https://github.com/sbg-tir).

This document will provide background information relevant to the ECOSTRESS mission and data products. 

```mermaid
flowchart TD
    L1_L2_RAD_LSTE_PGE[L1 L2 RAD LSTE PGE]
    L2T_STARS_PGE[L2T STARS PGE]

    L1T_RAD_product[L1T RAD Product]
    L2T_LSTE_product[L2T LSTE Product]
    L2T_STARS_product[L2T STARS Product]

    L1_L2_RAD_LSTE_PGE --> L1T_RAD_product
    L1_L2_RAD_LSTE_PGE --> L2T_LSTE_product
    L2T_LSTE_product --> L2T_STARS_PGE
    L2T_STARS_PGE --> L2T_STARS_product
```
