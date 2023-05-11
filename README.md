# AlpineWELLS_LIC
The lake ice data in this repository consists of relative lake ice coverage (%) and lake ice phenology data from 2017-03-28 to 2023-03-30 based on Sentinel-1, Sentinel-2 and Landsat imagery.

Formatted file names can be linked to Simstrat names according to "id_list.csv".

## LIC (raw) columns:
| Column            | Description                                           |
|:-------------     | -------------                                         |
| dt64              | Timestamp (pandas.Timestamp)                          |
| OBJECT_ID         | ID from [EU-Hydro polygons](https://land.copernicus.eu/imagery-in-situ/eu-hydro/eu-hydro-river-network-database)|
| coverage          | rel. data coverage of lake area (%)                   |
| date              | timestamp (ISO 8601 string)                           |
| ice_off_prob      | Aggregated ice-off probability output [0-1]           |
| ice_on_prob       | Aggregated ice-on probability output [0-1]            |
| lic               | Rel. lake ice coverage (%) [0-100]                    |
| sensor            | Senor platform                                        |
| sensor_w          | Sensor-weight [0-1]                                   |
| prob              | Combined aggregated probability output (%) [0-100]    |
| w	                | Combined datapoint weight (%) [0-100]                 |
| outlier           | Outlier flag                                          |
| unwanted	        | Unwanted flag                                         |
| lic_w	            | Lake ice coverage, weighted (%) [0-100]               |

## LIC (fit*) columns:
| Column            | Description                                           |
|:-------------     | -------------                                         |
| dt64              | Timestamp (pandas.Timestamp)                          |
| lic_result        | Fitted lake ice coverage (%)                          |

* *The LIC fit is generated using interpolation and weighted rolling window aggregation (weights based ond data coverage, probability and sensor-specific weight) to produce daily values.*
## LIP columns:
Each row is one full ice event. Events crossing the start end end of the observation period are not included.

| Column            | Description                     |
|:-------------     | -------------                   |
| FUS               | Freeze-up Start (30%, growing)  |
| FUE               | Freeze-up End (70%, growing)    |
| BUS               | Break-up Start (70%, declining) |
| BUE               | Break-up End (30% declining)    |
| ICD               | Ice Coverage Duration (FUS to BUE)  |
| CFD               | Complete Freeze Duration (FUE to BUS|
