---
layout: page
title: Level-2 products
permalink: /l2products/
---

## Level-2 variables

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

MRD&#8209;XXXX refers to the requirement number in the [CIMR Mission Requirement Document v6](https://esamultimedia.esa.int/docs/EarthObservation/CIMR-MRD-v6.0-20260324-ISSUED.pdf).

<b>NOTE:</b> The table below contains links to ATBDs (Algorithm Theoretical Basis Documents) developed in the CIMR L2PAD project.
None of these ATBDs are in their final versions. These intermediate versions are shared openly and in good faith, for informing
and triggering interaction with the future community of CIMR Level-2 products. If you want to cite or refer to these documents,
please contact the authors (their names are in the footer of each ATBD). Please also contact the authors if you have specific
comments or questions about the ATBDs or Level-2 parameter.
If you have general comments or questions about CIMR or CIMR Level-2, please interact with the project team in our
[discussion forum](https://github.com/orgs/CIMR-L2PAD/discussions).

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
| SWF-L | Surface Water Fraction | Global land | NRT3H/NTC | MRD&#8209;1060 | [ATBD](https://l2atbds.cimr.eu/SurfaceWaterFraction_ATBD/intro.html) |
| LST-L | Land Surface Temperature | Global land | NRT3H/NTC | MRD&#8209;1030 | [ATBD](https://l2atbds.cimr.eu/LandSurfaceTemperature_ATBD/intro.html) |
| LIC-L | Lake Ice Cover | Global land according to Hydrology mask | NRT3H/NTC | MRD&#8209;1010 | [ATBD](https://l2atbds.cimr.eu/SeaIceConcentrationEdge_ATBD/intro.html) |
| LSWT-L | Lake Surface Water Temperature | Global land according to Hydrology mask | NRT3H/NTC | MRD&#8209;1000 | [ATBD](https://l2atbds.cimr.eu/SeaSurfaceTemperature_ATBD/intro.html) |

## Level-2 Product Format

The CIMR L2PAD project developed initial Product Format Specification (PFS) for CIMR Level-2 products. We underline that
this is not the final file format for the future operational CIMR Level-2 products, which will be aligned with formats
from other Copernicus missions.

This being said, many aspects of the L2PAD PFS will probably be adopted for the final operational PFS and future users are
invited to read the <a href="https://drive.google.com/file/d/1c8lPVes3QXi8o5ZnDeXSCJ6qiQ5T5y2P/view?usp=drive_link">current PFS</a>.

In particular, we highlight the use of hierarchical [EASE2](https://nsidc.org/data/user-resources/help-center/guide-ease-grids) grids
with grid postings at 3, 9, 18, and 36 km.

<figure style="margin:1.5rem 0;">
  <img src="/assets/img/ex_CIMR_L2_EASE2_MultiPanel.png" 
       alt="Example CIMR L2 products on EASE2 grids" 
       style="max-width:100%; height:auto; border-radius:4px;">
  <figcaption style="margin-top:0.5rem; font-size:0.9rem; color:#555;">
  Example future CIMR Level-2 products on EASE2 grids: EASE2 Global (top), EASE2 Northern Polar (bottom left) and EASE2 Southern Polar (bottom right). Note: this visualization is only to illustrate the coverage of the future CIMR L2 products.
     The values plotted are not from a prototype L2 retrieval but from model fields (ERA5, ERA5-Land, Copernicus Global Ocean Analysis, etc.) 
  </figcaption>
</figure>

A series of test CIMR Level-2 product files, adhering to the current PFS and filled with dummy data, were also prepared to ease inspection.
These test files are available for download <a href="https://thredds.met.no/thredds/catalog/cimr/L2PAD/L2TDP_PFS_TestFiles/V2_TC3/catalog.html">here</a>.

If you have general comments or questions about the CIMR Level-2 PFS, please interact with the project team in our
[discussion forum](https://github.com/orgs/CIMR-L2PAD/discussions).
