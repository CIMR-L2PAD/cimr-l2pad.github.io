
(sicsied_iodd)=
# Algorithm Input and Output Data Definition (IODD) for SIC

## Input data

### Input L1 data
The input data for the SIC and SIED (derived from SIC) are the 'Water' Level-2 Pre-Processed {term}`L2PP` TBs produced
by the L1B/L2 Bridge. Only the C, K, and Ka channels are used. All bands are used at V-pol except Ka that is used
at both V- and H-pol. These TBs are corrected for land spill-over contamination.


| Name | Description | Units | Data Type | Shape |
| ---  | ---         | ---   | ---       | ---   |
| L2PP Water TB C-band | {term}`Level-2 Pre-Processed` (Land-corrected) TBs at 6.9 GHz (V pol.) | K | float | l1b | 
| L2PP Water TB K-band | {term}`Level-2 Pre-Processed` (Land-corrected) TBs at 18.7 GHz (V pol.) | K | float | l1b | 
| L2PP Water TB Ka-band | {term}`Level-2 Pre-Processed` (Land-corrected) TBs at 36.5 GHz (V and H pol.) | K | float | l1b | 
| L2PP Water TB Uncert C-band | {term}`Level-2 Pre-Processed` (Land-corrected) TB Uncertainties at 6.9 GHz (V pol.) | K | float | l1b | 
| L2PP Water TB Uncert K-band | {term}`Level-2 Pre-Processed` (Land-corrected) TB Uncertainties at 18.7 GHz (V pol.) | K | float | l1b | 
| L2PP Water TB Uncert Ka-band | {term}`Level-2 Pre-Processed` (Land-corrected) TBs Uncertainties at 36.5 GHz (V and H pol.) | K | float | l1b | 
| L2PP Water Lat/Long C-band | Latitude and Longitude of the C-Band L2PP Water TB   | degrees (N/E) | float | l1b |
| L2PP Water Lat/Long K-band | Latitude and Longitude of the K-Band L2PP Water TB   | degrees (N/E) | float | L1b |
| L2PP Water Lat/Long Ka-band | Latitude and Longitude of the Ka-Band L2PP Water TB   | degrees (N/E) | float | l1b |

### Input L2 data

#### Nominal scenario

No input Level-2 data are needed.

#### Backup scenario

No input Level-2 data are needed, thus no backup scenario is needed.

### Auxiliary data

No auxiliary data are foreseen at this stage (beyond the geographic masks, that will come in the input L1 files from the Bridge).
The geographic mask will include the monthly maximum sea (and lake) ice extent climatology for masking of erroneous retrievals at
lower latitudes.

Atmospheric correction of the TBs, as well as ocean emissivity roughness correction could be implemented in the course of the project. All auxiliary
fields to perform these corrections would then already be available as collocated fields in the input L2PP files, as a result of the OZA compensation
step in the L1B/L2 Bridge.

## Output data

| Name | Description | Units | Data Type | Shape |
| ---  | ---         | ---   | ---       | ---   |
| L2 SIC | Sea Ice Concentration from CKa@Ka | 1 | float | EASE2 3km | 
| L2 SIC Raw | Raw (non-thresholded and non-filtered) Sea Ice Concentration from CKa@Ka | 1 | float | EASE2 3km | 
| L2 SIC Uncert | Total (and component) uncertainty of L2 SIC from CKa@Ka | 1 | float | EASE2 3km | 
| L2 SIC Flags | Status flags of L2 SIC from CKa@Ka | n/a | int | EASE2 3km | 
| L2 SIED | Sea Ice Edge from CKa@Ka | 1 | int | EASE2 3km | 
| L2 SIED Uncert | Probability of SIED from CKa@Ka | 1 | float | EASE2 3km | 
| L2 SIC Lat/Long | Latitude and Longitude of the CKa@Ka SIC | degrees (N/E) | float | EASE2 3km | 

If relevant, these primary SIC and SIED fields (from `CKa@Ka`) can be supplemented with the other SICs (2ary from `KKa@Ka` and 3ary from `Ka`).

| Name | Description | Units | Data Type | Shape |
| ---  | ---         | ---   | ---       | ---   |
| L2 SIC (2ary) | Sea Ice Concentration from KKa@Ka | 1 | float | EASE2 3km | 
| L2 SIC (2ary) Raw | Raw (non-thresholded and non-filtered) Sea Ice Concentration from KKa@Ka | 1 | float | EASE2 3km | 
| L2 SIC (2ary) Uncert | Total (and component) uncertainty of L2 SIC from KKa@Ka | 1 | float | EASE2 3km | 
| L2 SIC (2ary) Flags | Status flags of L2 SIC from KKa@Ka | n/a | int | EASE2 3km | 
| L2 SIED (2ary) | Sea Ice Edge from KKa@Ka | 1 | int | EASE2 3km | 
| L2 SIED (2ary) Uncert | Probability of SIED from KKa@Ka | 1 | float | EASE2 3km | 
| L2 SIC (2ary) Lat/Long | Latitude and Longitude of the KKa@Ka SIC | degrees (N/E) | float | EASE2 3km | 
| L2 SIC (3ary) | Sea Ice Concentration from Ka | 1 | float | EASE2 3km | 
| L2 SIC (3ary) Raw | Raw (non-thresholded and non-filtered) Sea Ice Concentration from Ka | 1 | float | EASE2 3km | 
| L2 SIC (3ary) Uncert | Total (and component) uncertainty of L2 SIC from Ka | 1 | float | EASE2 3km | 
| L2 SIC (3ary) Flags | Status flags of L2 SIC from Ka | n/a | int | EASE2 3km | 
| L2 SIED (3ary) | Sea Ice Edge from Ka | 1 | int | EASE2 3km | 
| L2 SIED (3ary) Uncert | Probability of SIED from Ka | 1 | float | EASE2 3km | 
| L2 SIC (3ary) Lat/Long | Latitude and Longitude of the Ka SIC | degrees (N/E) | float | EASE2 3km | 


