(lic_baseline)=
# Baseline Algorithm Definition for LIC

This chapter describes the algorithm baseline for the Lake Ice Cover (LIC) fields.

```{note}
A [notebook to demonstrate the LIC retrieval over the Great Lakes from daily averaged AMSR2 TBs](<./notebooks/DD-JNB Sea Ice Concentration Edge and Lake Ice Cover AMSR2.ipynb>) is in annex to this ATBD (at the bottom of the notebook).

Readers are invited to browse the notebook in complement to the algorithm description below.
```

## Retrieval Method

We retrieve {term}`LIC` as a scalar between 0 and 1 (or 0% and 100%) using the {ref}`sic_baseline`, but with small adjustments,
that are listed below.

### Use of K and Ka channels
To achieve LIC product with a resolution better than 5 km, we cannot use C-band and thus the `CKa` algorithm. Instead,
we will use the `KKa`, possibly pan-sharpened with the `Ka` algorithm. We note that {cite}`du:2017:lake_pheno` uses
only the 36.5GHz H-polarization channel of AMSR-E and AMSR2 to retrieve lake ice phenology, arguing that H-pol is
more sensitive to lake freeze-up/break-up signals {cite}`kang:2012:lake_pheno`.

### Fixed lake tie-points
Lake ice is different from sea ice: it is less saline, usually thinner, and accumulates less snow
on its surface. Lake ice is also seasonal (it melts fully during summer) and there are thus no multiyear ice in lakes.
This calls for a different set of algorithm tie-points for lake ice than for sea ice. The method to derive such fixed
lake ice tie-points is still open at time of writing, noting the work of {cite}`ghaffari:2011:caspian`.

## CIMR Level-1b re-sampling approach

There are no additional requirements on Level-1b for LIC than for SIC.

We nonetheless underline the importance of the land spill-over correction step
(implemented as part of the L1B/L2 Bridge {doc}`[RD-2] <./01_applicable_ref_docs>`) as it is
critical to the accuracy of lake ice information in smaller lakes.

We also note that, being on land, lakes will naturally be closer to Radio-Frequency Interference (RFI)
sources, and that its detection and mitigation in the L1B processing will be important.

## Algorithm Assumptions and Simplifications

Microwave emission does not originate from the snow surface, but rather from layers within the ice and snow. For thin
ice (< 20 cm), algorithms based on microwave radiometry tend to underestimate ice fraction. The underestimation is
less at K and Ka band than at L or C bands.

Despite the fact that lake ice is seasonal and does not generally deform, the brightness temperature of fully-iced lakes
(that defines the 100% LIC tie-point) can vary in time especially due to variations in temperature (incl. a diurnal cycle)
and because of melt/freeze processes in the snow layer on top of the ice (wet ice has a higher emissivity than dry ice).
We will start the developments of the LIC algorithm aiming at a fixed ice tie-point, but further refinement could aim
at time-varying tie-points, like in the SIC algorithm. We note the work of {cite}`du:2017:lake_pheno` who discusses
the time-variation of AMSR-E and AMSR2 TBs (at 36.5 GHz H-pol) of fully-iced lakes.

