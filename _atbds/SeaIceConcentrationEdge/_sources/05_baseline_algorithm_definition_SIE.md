(sie_baseline)=
# Baseline Algorithm Definition for SIE

This chapter describes the algorithm baseline for Sea Ice Extent (SIE) (and Area, SIA). Both SIE and SIA are quantities derived from SIC.

```{important}
Sea Ice Extent (SIE) (and Area) are integrated quantities counting
the total area covered by sea ice. They are indicators, providing one number per day, not swath-based or grid-based fields. They is computed
at Level-3/-4 from daily composited maps of SIC. It requires processing beyond L2, including gridding individual L2 SIC products into
a daily Level-3 SIC field, potentially performing Level-4 gap-filling and corrections, and finally integrating the gridded SIC fields
into a SIE (and SIA) indicator. The computation of a CIMR SIE is thus best handled in downstream services such as C3S, CMEMS, or OSI SAF and
is not a product for the CIMR L2 GPP. An example of such index is the [OSI SAF Sea Ice Index](https://osi-saf.eumetsat.int/products/osi-420).
```

```{note}
A [notebook](./notebooks/DD-JNB%20Sea%20Ice%20Extent%20and%20Area.ipynb), provided as Annex to this ATBD, demonstrates computation of the SIE and SIA.
```

## Retrieval Method

Daily SIE and SIA values are computed from daily averaged SIC maps. All sea-ice covered ocean is included, lake ice is not.

To prepare daily averaged maps of SIC involves several steps, including:
1. gridding / projection of the individual swath-based SICs to a fixed grid. This can use ad-hoc software or future evolutions of the CIMR RGB.
2. daily compositing (averaging) of the gridded SICs.
3. applying flags, climatologies, etc...

SIE is computed as the sum of the total area of the grid cells that have a SIC value larger than 15\% SIC.

$$
\text{SIE} = \sum_{grid\_cells} A_{grid\_cell} \times 1_{\text{SIC} \ge 15\%} \times 1_{ocean} \times 1_{region}
$$

SIA is the sum of the area of all grid cells weighted by the SIC values (no threshold on SIC).

$$
\text{SIA} = \sum_{grid\_cells} \text{SIC} \times A_{grid\_cell} \times 1_{\text{SIC} \ge 0\%} \times 1_{ocean} \times 1_{region}
$$

$1_{x}$ is the Heaviside step function. $1_{ocean}$ is the land/ocean mask that excludes land and lake cells. $1_{\text{SIC} \ge T}$ selects only the grid
cells where the SIC is larger than a threshold $T$. $A_{grid\_cells}$ is the grid cell area expressed in $km^2$. For and equal area projection, it is a single
number. For other projections it is a 2D field. $1_{region}$ is a mask selecting a region in the map.

The timeseries of daily SIE and SIA indicators can be further aggregated into monthly and yearly timeseries. Trends and climatologies can be derived.

## End to end algorithm functional flow diagram

```{include} sie_diagram.md
```
%```{image} ./static_imgs/sie_diagram.png
%:name: sie_diagram
%```

