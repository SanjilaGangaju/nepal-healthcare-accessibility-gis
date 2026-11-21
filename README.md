# Nepal Service Accessibility Analysis

## Project Overview

A GIS-based spatial analysis examining the geographic proximity of settlements to mapped healthcare facilities in Pokhara Metropolitan City, Kaski District, Nepal.

The project uses QGIS and open geospatial datasets to identify settlements located farther from mapped health facilities and examine their proximity to the road network.

## Research Question

How well are settlements geographically connected to essential health facilities in Pokhara Metropolitan City?

## Study Area

- **Location:** Pokhara Metropolitan City, Kaski, Gandaki Province, Nepal
- **Coordinate Reference System:** WGS 84 / UTM Zone 44N (EPSG:32644)
- **Software:** QGIS 3.44

## Data Sources

| Dataset | Source |
|---|---|
| Administrative boundary | LocalBoundaries Nepal |
| Health facility locations | Healthsites.io |
| Settlement locations | OpenStreetMap |
| Road network | OpenStreetMap |

## Methodology

1. Collected and prepared administrative boundary, healthcare facility, settlement, and road network datasets.
2. Reprojected spatial layers to EPSG:32644.
3. Cleaned and filtered settlement records within the study boundary.
4. Identified the nearest mapped healthcare facility for each settlement using straight-line distance.
5. Classified settlements into four proximity categories:
   - Very close: 0–1 km
   - Moderate: 1–3 km
   - Far: 3–5 km
   - Very far: More than 5 km
6. Created a 3 km proximity buffer around mapped healthcare facilities.
7. Examined the nearest road distance for settlements located more than 3 km from a mapped healthcare facility.
8. Designed a final thematic map using QGIS Print Layout.

## Key Findings

The analysis included:

- **327** mapped settlements within the study boundary.
- **95** mapped healthcare facilities.
- **255 settlements (78%)** within 3 km of their nearest mapped healthcare facility.
- **72 settlements (22%)** more than 3 km away.

Among the 72 settlements located more than 3 km from a mapped healthcare facility:

- **48 (66.7%)** were within 25 metres of a mapped road.
- **15 (20.8%)** were between 25 and 50 metres away.
- **9 (12.5%)** were more than 50 metres away.

## Limitations

- Distances represent straight-line geographic proximity, not actual road travel distance or travel time.
- OpenStreetMap and Healthsites.io data may be incomplete or contain outdated or inaccurately located features.
- The analysis does not measure healthcare capacity, quality, affordability, or availability of services.
- The 1 km, 3 km, and 5 km categories are study-defined thresholds, not official healthcare accessibility standards.
- Proximity to a mapped road does not necessarily indicate road quality, connectivity, or transport availability.

## Project Output

The final map illustrates healthcare facility locations, settlement proximity categories, and the 3 km healthcare proximity buffer.

## Tools

- QGIS 3.44
- OpenStreetMap
- Healthsites.io
- LocalBoundaries Nepal

---

*This project was developed as a practical GIS and spatial analysis portfolio project focused on healthcare accessibility in Nepal.*