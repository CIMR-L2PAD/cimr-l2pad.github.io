(sec:definitions)=
# Acronyms and definitions

Here follows a formatted list of acronyms.

```{glossary}
AMSR2
AMSR-E
    Advanced Microwave Scanning Radiometer

ATBD
    Algorithm Theoretical Basis Document

EASE2
    {term}`Equal Area Scalable Earth v2`

CCI
    {term}`Climate Change Initiative`

CI
    {term}`Consolidated Ice`

CIMR
    {term}`Copernicus Imaging Microwave Radiometer`

DAL
    Distance Along the (ice) Line

FYI
    First-Year Ice

GR
    Gradient Ratio

GPP
    Ground-Processor Prototype

L1B
    Level-1B

L2PP
    {term}`Level-2 Pre-Processed`

LIC
    {term}`Lake Ice Cover`

MIZ
    Marginal Ice Zone

MWI
    {term}`MicroWave Imager`

MYI
    MultiYear ice

NRT1H
    {term}`Near Real Time 1H`

NRT3H
    {term}`Near Real Time 3H`

OSI SAF
    {term}`Ocean and Sea Ice Satellite Application Facility`

OW
    Open Water

OWF
    Open Water Filter

RTM
    Radiative Transfer Model

SIC
    {term}`Sea Ice Concentration`

SIC1H
    {term}`Sea Ice Concentration 1H`

SIC3H
    {term}`Sea Ice Concentration 3H`

SIE
    {term}`Sea Ice Extent`

SIED
    {term}`Sea Ice Edge`

SIED1H
    {term}`Sea Ice Edge 1H`

SIED3H
    {term}`Sea Ice Edge 3H`

SMMR
    Scanning Multichannel Microwave Radiometer

SSM/I
    Special Sensor Microwave Imager

SSMIS
    Special Sensor Microwave Imager/Sounder

TB
    Brightness Temperature

TOA
    Top Of Atmosphere

```


***

Here follows a glossary, or list of definitions

```{glossary}
Climate Change Initiative
    A programme of the European Space Agency (ESA) to prepare satellite-based Climate Data Records of
    selected Essential Climate Variables.

Consolidated Ice
    In this context, ice with 100% concentration irrespective of its type.

Copernicus Imaging Microwave Radiometer
    The Copernicus Imaging Microwave Radiometer is a Microwave Radiometer which launch is planned by ESA in 2029.

Equal Area Scalable Earth v2
    Equal area projection grid definition based on a Lambert Azimuthal projection and a WGS84 datum.
    Defined in {cite:t}`brodzik:2012:ease2`.

Lake Ice Cover
    In this document, a quantity equivalent to {term}`Sea Ice Concentration` but for lake (fresh) water.

Level-2 Pre-Processed
    Fields (in particular TBs) prepared in the *L2 pre-processing* sub-system. Output of the L1B/L2 Bridge chain.

MicroWave Imager
    Microwave Radiometer on board EPS Second Generation satellites.

Near Real Time 1H
    Product delivered in $\le$1 hour to the point of user pickup after data acquisition by the satellite.
    NRT1H products are used for nowcasting operational applications
    (e.g. navigation bulletins in the Arctic) from sea ice services, operational oceanography and meteorology.

Near Real Time 3H
    Product delivered in $\le$3 hour to the point of user pickup after data acquisition by the satellite.
    NRT3H products are used for operational applications such as sea ice services,
    operational oceanography and meteorology.

Nscanl
    Number of scanlines

Nscanp
    Number of positions along the scans

Ocean and Sea Ice Satellite Application Facility
    An service started in 1997 to provide operational and climate products of the ocean surface and sea-ice
    cover relevant for Numerical Weather Prediction and Marine Forecasting services. Led by Météo-France
    and part of the distributed ground segment of EUMETSAT.

Open Water
    In this context, ocean surface with no sea ice (0% SIC).

Sea Ice Concentration
    The Sea Ice Concentration is the fraction of the sea surface covered by sea ice. It is a measure of the amount of sea ice in a given area. It is usually expressed as a percentage.
    The latency requirement for the nominal CIMR Level-2 SIC product is {term}`Near Real Time 3H`.

Sea Ice Concentration 1H
    See {term}`Sea Ice Concentration` but with a {term}`Near Real Time 1H` requirement.

Sea Ice Concentration 3H
    See {term}`Sea Ice Concentration`.

Sea Ice Edge
    Sea Ice Edge is a binary product indicating where the sea ice cover is. By extension it can be a binary mask showing classes of {term}`Sea Ice Concentration`. The CIMR
    Level-2 {term}`SIED` product is derived from the results of the Level-2 {term}`SIC` processing, and has a {term}`Near Real Time 3H` latency requirement.

Sea Ice Edge 1H
    See {term}`Sea Ice Edge` but with a {term}`Near Real Time 1H` requirement.

Sea Ice Edge 3H
    See {term}`Sea Ice Edge`.

Sea Ice Extent
    A measure of the total area covered by sea ice in a region. It is a single number describing the area of sea-ice covered ocean. It has
    unit km2 (typically millions km2 for the whole Arctic). SIE is computed from a time-composite (typically a daily aggregate) of CIMR L2 SICs.
```

