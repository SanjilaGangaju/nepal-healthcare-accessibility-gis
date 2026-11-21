# Analysis Notes — Pokhara Healthcare Accessibility

## 1. Study Area
Pokhara Metropolitan City, Kaski District, Gandaki Province, Nepal.

## 2. Dataset Summary

| Dataset | Feature Count |
|---|---:|
| Settlements within boundary | 327 |
| Mapped healthcare facilities | 95 |
| Clipped road network | 9,157 |

## 3. Nearest Healthcare Facility Analysis

Calculated straight-line distance from each settlement to its nearest mapped healthcare facility.

| Distance category | Settlements | Percentage |
|---|---:|---:|
| Very close (≤1 km) | 122 | 37.3% |
| Moderate (1–3 km) | 133 | 40.7% |
| Far (3–5 km) | 56 | 17.1% |
| Very far (>5 km) | 16 | 4.9% |
| **Total** | **327** | **100%** |

- Mean distance: approximately 1.94 km
- Median distance: approximately 1.51 km
- Maximum distance: approximately 10.32 km

## 4. Healthcare Proximity Buffer

Created a dissolved 3 km buffer around mapped healthcare facilities.

- Within 3 km: 255 settlements (78%)
- Outside 3 km: 72 settlements (22%)

## 5. Nearest Road Analysis

Analysed the nearest mapped road for the 72 settlements located more than 3 km from a mapped healthcare facility.

| Road distance category | Settlements | Percentage |
|---|---:|---:|
| Very close (≤25 m) | 48 | 66.7% |
| Close (25–50 m) | 15 | 20.8% |
| Further away (>50 m) | 9 | 12.5% |

Mean nearest-road distance: approximately 23.62 m.

## 6. Interpretation

Most mapped settlements are within 3 km of a mapped healthcare facility. However, 72 settlements are located beyond this proximity threshold. Most of these 72 settlements are also geographically close to a mapped road.

This suggests that distance from a healthcare facility and proximity to a road are different aspects of geographic accessibility.

## 7. Important Limitations

- Distances are straight-line measurements, not actual travel distances.
- Road proximity does not confirm road connectivity or transport availability.
- Healthcare facility data may be incomplete or outdated.
- The analysis does not assess facility capacity, quality, or service availability.
- Accessibility categories are study-defined thresholds.

## 8. Technical Information

- Software: QGIS 3.44.15
- CRS: EPSG:32644 — WGS 84 / UTM Zone 44N
- Analysis tools: Reproject Layer, Extract by Location, Join Attributes by Nearest, Buffer, Statistics by Categories, Extract by Expression.