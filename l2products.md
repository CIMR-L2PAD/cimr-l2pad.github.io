---
layout: page
title: Level-2 products
permalink: /l2products/
---

The CIMR L2PAD project focuses on Level-2 products under ESA's operational responsibility, that is
Level-2 products in the *Polar Oceans* (incl. sea ice) and *Global Land* (incl. lakes) family. The
*Global Oceans* and *Atmosphere* products are not covered, as they are under EUMETSAT's operational
responsibility.

The table below lists the Level-2 products that are covered by the CIMR L2PAD team (-P: Polar Oceans, -L: Global Land).

Depending on the Level-2 product, different delivery timeliness are specified:
* *Near-Real-Time-3-Hour (NTR3H)*: Product delivered in <3 hour to the point of user pickup after data acquisition by
   the satellite. This is the nominal timeliness for the Copernicus Space Component.
* *Near-Real-Time-1-Hour (NRT1H)*: Product delivered in <1 hour to the point of user pickup after data acquisition by
   the satellite. In the case of CIMR, NRT1H targets support to safe Arctic navigation.
* *Non-Time-Critical (NTC)*: Product delivered in less than 30 days to the point of user pickup after data acquisition by
   the satellite.

MRD&#8209;XXXX refers to the requirement number in the [CIMR Mission Requirement Document v5](https://esamultimedia.esa.int/docs/EarthObservation/CIMR-MRD-v5.0-20230211_(Issued).pdf).

| L2 Variable ID | Description | Coverage Domain | Delivery Timeliness | MRD&#8209;XXXX | ATBD | 
| ---            | ---         | ---             | ---                 | ---      | --- | 
| SIC-P | Sea Ice Concentration | Polar Regions and Adjacent Seas | NRT1H/NRT3H/NTC | MRD&#8209;890, MRD&#8209;1110 | [ATBD](https://l2atbds.cimr.eu/SeaIceConcentrationEdge_ATBD/intro.html) |
| SIT-P | Thin Sea Ice Thickness | Polar Regions and Adjacent Seas | NRT3H/NTC | MRD&#8209;910 | [ATBD](https://l2atbds.cimr.eu/ThinSeaIceThickness_ATBD/intro.html) |
| SIED-P | Sea Ice Edge | Polar Regions and Adjacent Seas | NRT1H/NRT3H/NTC | MRD&#8209;915, MRD&#8209;1110 | [ATBD](https://l2atbds.cimr.eu/SeaIceConcentrationEdge_ATBD/intro.html) |
| SID-P | Sea Ice Drift | Polar Regions and Adjacent Seas | NRT1H/NRT3H/NTC | MRD&#8209;920, MRD&#8209;1110 | [ATBD](https://l2atbds.cimr.eu/SeaIceDrift_ATBD/intro.html) |
| ITY-P | Ice stage of development / type | Polar Regions and Adjacent Seas | NRT3H/NTC | MRD&#8209;930 | [ATBD](https://l2atbds.cimr.eu/SeaIceTypeAndSnowDepth_ATBD/intro.html) |
| SND-P | Snow Depth on Sea Ice | Polar Regions and Adjacent Seas | NRT3H/NTC | MRD&#8209;940 | [ATBD](https://l2atbds.cimr.eu/SeaIceTypeAndSnowDepth_ATBD/intro.html) |
| SIST-P | Sea Ice Surface Temperature | Polar Regions and Adjacent Seas | NRT3H/NTC | MRD&#8209;970 | [ATBD](https://l2atbds.cimr.eu/SeaIceSurfaceTemperature_ATBD/intro.html) |
| SST-P | Sea Surface Temperature | Polar Regions and Adjacent Seas | NRT3H/NTC | MRD&#8209;905 | [ATBD](https://l2atbds.cimr.eu/SeaSurfaceTemperature_ATBD/intro.html) |
| SSS-P | Sea Surface Salinity | Polar Regions and Adjacent Seas | NRT3H/NTC | MRD&#8209;985 | [ATBD](https://l2atbds.cimr.eu/SeaSurfaceSalinityAndOceanWindVectors_ATBD/intro.html) |
| OWV-P | Ocean Surface Wind Vector | Polar Regions and Adjacent Seas | NRT3H/NTC (+ Speed as NRT1H) | MRD&#8209;995, MRD&#8209;1110 | [ATBD](https://l2atbds.cimr.eu/SeaSurfaceSalinityAndOceanWindVectors_ATBD/intro.html) |
| ---            | ---         | ---             | ---                 | ---      | --- | 
| SCE-L | Snow Cover Extent | Global land | NRT3H/NTC | MRD&#8209;950 | [ATBD](https://l2atbds.cimr.eu/SnowCoverExtent_ATBD/intro.html) |
| SWE-L | Terrestrial Snow Water Equivalent | Global land | NRT3H/NTC | MRD&#8209;960 | [ATBD](https://l2atbds.cimr.eu/SnowWaterEquivalent_ATBD/intro.html) |
| FT-L | Soil Freeze/thaw state | Global land | NRT3H/NTC | MRD&#8209;1020 | [ATBD](https://l2atbds.cimr.eu/SoilFreezeThawState_ATBD/intro.html) |
| SM-L | Soil Moisture | Global land | NRT3H/NTC | MRD&#8209;1040 | [ATBD](https://l2atbds.cimr.eu/SoilMoisture_Vegetation_ATBD/intro.html) |
| MMVI-L | Multi-frequency Microwave Vegetation Indicators | Global land | NRT3H/NTC | MRD&#8209;1050 | [ATBD](https://l2atbds.cimr.eu/SoilMoisture_Vegetation_ATBD/intro.html) |
| SWF-L | Surface Water Fraction | Global land | NRT3H/NTC | MRD&#8209;1060 | [ATBD](https://l2atbds.cimr.eu/SoilMoisture_Vegetation_ATBD/intro.html) |
| LST-L | Land Surface Temperature | Global land | NRT3H/NTC | MRD&#8209;1030 | [ATBD](https://l2atbds.cimr.eu/LandSurfaceTemperature_ATBD/intro.html) |
| LIC-L | Lake Ice Cover | Global land according to Hydrology mask | NRT3H/NTC | MRD&#8209;1010 | [ATBD](https://l2atbds.cimr.eu/SeaIceConcentrationEdge_ATBD/intro.html) |
| LSWT-L | Lake Surface Water Temperature | Global land according to Hydrology mask | NRT3H/NTC | MRD&#8209;1000 | [ATBD](https://l2atbds.cimr.eu/SeaSurfaceTemperature_ATBD/intro.html) |

