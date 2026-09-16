# Kalimantan Wildfire Mapping
Earth observation and geospatial analysis of wildfire hotspots and vegetation change in Kalimantan, Indonesia, using hotspot observations and Sentinel-2 imagery.

## Overview
Wildfires in Indonesia can affect large and geographically dispersed areas, making satellite-based monitoring useful for identifying where fire activity is concentrated and assessing possible vegetation impacts.

This project explores wildfire activity in Kalimantan by combining hotspot observations with Sentinel-2 satellite imagery. The analysis focuses on identifying hotspot concentrations and examining whether selected areas show corresponding vegetation changes consistent with fire impacts.

Three areas were selected for closer examination:
- Ketapang, West Kalimantan
- Kotawaringin Timur, Central Kalimantan
- Berau, East Kalimantan

The project combines spatial hotspot analysis, before-and-after satellite imagery, NBR/dNBR calculation, and visual interpretation.

## Objectives
The analysis aims to:
- identify spatial concentrations of wildfire hotspots;
- select representative areas for closer examination;
- compare Sentinel-2 imagery before and after periods of fire activity;
- calculate Normalized Burn Ratio (NBR) and differenced NBR (dNBR);
- examine the spatial relationship between hotspot observations and vegetation change;
- interpret satellite-observed changes while acknowledging the limitations of each dataset.

## Data
The analysis uses publicly available geospatial datasets.

### Wildfire Hotspots
Hotspot observations were obtained from Indonesia's **SiPongi** forest and land fire monitoring system.
Hotspots are used as indicators of detected thermal anomalies and as an initial basis for identifying areas with concentrated fire activity.

### Sentinel-2
Sentinel-2 multispectral imagery was accessed and processed using **Google Earth Engine**.
Imagery from periods before and after fire activity was used to examine changes in vegetation condition.

### Reference Boundaries
Administrative and other reference boundaries were used to provide geographic context for analysis and visualization.

Large satellite imagery and raw datasets are not stored directly in this repository.

## Analytical Workflow
```text
Hotspot observations
        ↓
Spatial screening and hotspot concentration analysis
        ↓
Selection of study areas
        ↓
Sentinel-2 before/after imagery
        ↓
NBR calculation
        ↓
dNBR vegetation-change analysis
        ↓
Hotspot and dNBR overlay
        ↓
Spatial interpretation and visual verification
```

## Study Areas
### 1. Ketapang, West Kalimantan
Ketapang was selected as one of the study areas based on the concentration and spatial pattern of hotspot observations.
The analysis compares hotspot locations with changes observed in Sentinel-2 imagery before and after the period of fire activity.

### 2. Kotawaringin Timur, Central Kalimantan
Kotawaringin Timur was examined as a second case study to assess whether areas of concentrated hotspot activity correspond with observable vegetation change.

### 3. Berau, East Kalimantan
Berau provides an additional case from a different part of Kalimantan, allowing comparison of hotspot patterns and satellite-observed vegetation change across different geographic contexts.

## NBR and dNBR
The **Normalized Burn Ratio (NBR)** uses near-infrared and shortwave-infrared reflectance to characterize vegetation condition.
It is calculated as:
```text
NBR = (NIR - SWIR) / (NIR + SWIR)
```

The **differenced Normalized Burn Ratio (dNBR)** represents the change between pre-event and post-event NBR:
```text
dNBR = NBR_before - NBR_after
```
Higher positive dNBR values can indicate stronger vegetation change that may be consistent with fire impacts.
In this project, dNBR is interpreted together with hotspot observations and visual examination of Sentinel-2 imagery rather than being treated as standalone evidence of burned area.

## Tools
- Google Earth Engine
- QGIS
- Sentinel-2 multispectral imagery
- SiPongi hotspot data
- Geospatial analysis and visualization

## Repository Structure
```text
kalimantan-wildfire-mapping/
│
├── README.md
├── scripts/
├── figures/
└── data/
    └── README.md
```

### `scripts/`
Contains selected processing and analysis scripts used in the workflow.

### `figures/`
Contains selected maps and visual outputs from the analysis.

### `data/`
Contains documentation and links to the public data sources used in the project. Large raw datasets and satellite imagery are not stored in the repository.

## Interpretation and Limitations
This analysis is intended as an exploratory Earth observation assessment rather than a definitive burned-area product.
Several limitations should be considered:
- **Hotspots are not burned-area boundaries.** They represent detected thermal anomalies and indicate possible fire activity at a specific time and location.
- **dNBR measures vegetation change, not fire directly.** Changes may also be influenced by vegetation dynamics, land-cover changes, image timing, or other environmental factors.
- **Cloud cover and image availability** can affect the selection of suitable Sentinel-2 observations.
- **Spatial correspondence is important.** Stronger interpretation is possible when hotspot activity, before-and-after imagery, and dNBR patterns show consistent spatial and temporal relationships.

For these reasons, the analysis combines hotspot observations, satellite imagery, vegetation indices, and visual interpretation rather than relying on a single indicator.

## Key Principle
> Hotspots indicate where potential fire activity becomes visible, while satellite-based vegetation indices help examine what changed on the ground.
The combination of both provides a stronger basis for spatial interpretation than either dataset alone.

## Author
**Jesika Taradini**
Geospatial & Earth Observation Specialist  
Remote Sensing · GIS · Google Earth Engine · Environmental Spatial Analysis
