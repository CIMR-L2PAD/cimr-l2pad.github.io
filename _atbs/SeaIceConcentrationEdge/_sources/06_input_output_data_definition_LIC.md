
(lic_iodd)=
# Algorithm Input and Output Data Definition (IODD) for LIC

## Input data

### Input L1 data
The input data for the LIC algorithm are the same as for the SIC and SIED algorithm: 'Water' Level-2 Pre-Processed {term}`L2PP` TBs produced
by the L1B/L2 Bridge. Only the K, and Ka channels (not C) are used. All bands are used at V-pol except Ka that is used
at both V- and H-pol. These TBs are corrected for land spill-over contamination.


| Name | Description | Units | Data Type | Shape |
| ---  | ---         | ---   | ---       | ---   |
| L2PP Land TB K-band | {term}`Level-2 Pre-Processed` (Water-corrected) TBs at 18.7 GHz (V pol.) | K | float | l1b | 
| L2PP Land TB Ka-band | {term}`Level-2 Pre-Processed` (Water-corrected) TBs at 36.5 GHz (V and H pol.) | K | float | l1b | 
| L2PP Land TB Uncert K-band | {term}`Level-2 Pre-Processed` (Water-corrected) TB Uncertainties at 18.7 GHz (V pol.) | K | float | l1b | 
| L2PP Land TB Uncert Ka-band | {term}`Level-2 Pre-Processed` (Water-corrected) TBs Uncertainties at 36.5 GHz (V and H pol.) | K | float | l1b | 
| L2PP Land Lat/Long K-band | Latitude and Longitude of the K-Band L2PP Land TB   | degrees (N/E) | float | L1b |
| L2PP Land Lat/Long Ka-band | Latitude and Longitude of the Ka-Band L2PP Land TB   | degrees (N/E) | float | l1b |

### Input L2 data

#### Nominal scenario

No input Level-2 data are needed.

#### Backup scenario

No input Level-2 data are needed, thus no backup scenario is needed.

### Auxiliary data

No auxiliary data are foreseen at this stage (beyond the geographic masks, that will come in the input L1 files from the Bridge).

Atmospheric correction of the TBs, as well as lake surface emissivity roughness correction could be implemented in the course of the project. All auxiliary
fields to perform these corrections would then already be available as collocated fields in the input L2PP files, as a result of the OZA compensation
step in the L1B/L2 Bridge.

## Output data

| Name | Description | Units | Data Type | Shape |
| ---  | ---         | ---   | ---       | ---   |
| L2 LIC | Lake Ice Cover from KKa@Ka | 1 | float |  | 
| L2 LIC Raw | Raw (non-thresholded and non-filtered) Lake Ice Cover from KKa@Ka | 1 | float | EASE2 3km | 
| L2 LIC Uncert | Total (and component) uncertainty of L2 LIC from KKa@Ka | 1 | float | EASE2 3km | 
| L2 LIC Flags | Status flags of L2 LIC from KKa@Ka | n/a | int | EASE2 3km | 
| L2 LIED | Lake Ice Edge from KKa@Ka | 1 | int | EASE2 3km | 
| L2 LIED Uncert | Probability of LIED from KKa@Ka | 1 | float | EASE2 3km | 
| L2 LIC Lat/Long | Latitude and Longitude of the KKa@Ka LIC | degrees (N/E) | float | EASE2 3km | 

```{note}
In the table above we introduce the concept of a Lake Ice Edge (LIED) 'binary' product, derived
from the LIC in the same manner as SIED is derived from SIC (by thresholding). A LIED 'binary'
product takes minimal computation resource and disk space.
```

