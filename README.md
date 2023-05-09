# AlpineWELLS_LIC

The lake ice data in this repository consists of relative lake ice coverage (%) data from 2017-03-28 to 2023-03-30 based on Sentinel-1, Sentinel-2 and Landsat imagery.

## Data columns:
| Column            | Description                                           |
|:-------------     | -------------                                         |
| LANDSAT_SCENE_ID  | Short Landsat Scene Identifier                        |
| ST                | Aggregated (median) ST (K)                            |
| ST_CDIST          | Distance to cloud (km)                                |
| ST_QA             | Uncertainty of the Surface Temperature band (K) *     |
| coverage          | Percentage of unmasked lake area                      |
| px_count          | No. of unmasked pixels available for datapoint        |
| sensor            | Landsat sensor platform used (e.g. LANDSAT_9)         |
| time_utc          | Time of the observations as at center of scene in UTC |

* *The ST_QA values provide uncertainty values using a combination of uncertainty from a standard error propagation and distance to cloud. The method used is described in [Laraby et al. (2018)](https://doi.org/10.1016/j.rse.2018.06.026) for Landsat 7 but is also used in the entirety of Collection 2 ST products.*

## EE datasets and documentations

Landsat Collection 2 Surface Tempearture general information  
https://www.usgs.gov/landsat-missions/landsat-collection-2-surface-temperature

Landsat 4: USGS Landsat 4 Level 2, Collection 2, Tier 1  
ee.ImageCollection('LANDSAT_LT04_C02_T1_L2')  
Documentation: https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT04_C02_T1_L2

Landsat 5: USGS Landsat 5 Level 2, Collection 2, Tier 1  
ee.ImageCollection('LANDSAT/LT05/C02/T1_L2')  
Documentation: https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT05_C02_T1_L2

Landsat 7: USGS Landsat 7 Level 2, Collection 2, Tier 1  
ee.ImageCollection('LANDSAT/LE07/C02/T1_L2')  
Documentation: https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C02_T1_L2

Landsat 8: USGS Landsat 8 Level 2, Collection 2, Tier 1  
ee.ImageCollection('LANDSAT/LC08/C02/T1_L2')  
Documentation: https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C02_T1_L2

Landsat 9: USGS Landsat 9 Level 2, Collection 2, Tier 1  
ee.ImageCollection('LANDSAT/LC09/C02/T1_L2')  
Documentation: https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC09_C02_T1_L2
