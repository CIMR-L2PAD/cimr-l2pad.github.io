# Introduction, purpose and scope

{term}`Sea Ice Concentration` (SIC), aka sea-ice area fraction, measures the fraction of a pre-defined ocean area (sensor footprint, grid cell,...) that is covered by sea ice.
SIC is unitless and can equally be reported in the range [0,1] as well as [0%,100%].

The retrieval of SIC from space-borne passive microwave radiometer (PMR) data has a long and successful history {cite:p}`comiso:1986:sic,cavalieri:1984:sic`. The retrieval is based
on the contrast in emissivity (ε), and thus brightness temperature ({term}`TB`), between open water (low ε, low TB) and sea ice (high ε, high TB). This contrast depends on frequency,
polarization, and type of sea-ice observed, as illustrated in {numref}`fig_emis`.

```{figure} static_imgs/sea_ice_emis.png
---
name: fig_emis
---
Average top of atmosphere brightness temperatures (TB) and standard deviations of Arctic open water ({term}`OW`), first-year ({term}`FYI`) and multiyear ({term}`MYI`) sea ice.
Data from 6.9 to 89 GHz based on AMSR-E/2 observations with incidence angle 55°, at 1.4 GHz on SMOS observations averaged over 50° to 55° incidence angle, collected for footprints
with pure surface types in the Round Robin data package of the ESA Climate Change Initiative project on sea ice {cite:p}`pedersen:2021:rrdp`. Solid lines denote vertically
polarized TBs, and H horizontally. Note that lines connecting the TBs are meant for easy reading, but not for interpolation between the observation frequencies. Source: {cite:t}`lu:2018:emis`.
```

On {numref}`fig_emis` it appears clearly that better contrast between 0% SIC (Open Water, {term}`OW`) and 100% SIC (split here in two Arctic sea-ice types sea-ice  First Year Ice, {term}`FYI`,
and Multiyear Ice, {term}`MYI`) is achieved with horizontal polarization (H-pol) radiation, and at low frequencies, e.g. L-band (1.4 GHz), C-band (6.9 GHz), and X-band (10.7 GHz).

However, with real-aperture space-borne PMR sensors like {term}`SSMIS`, {term}`AMSR2`, and also {term}`CIMR`, the low frequency channels are those with the coarsest spatial resolution. Even in
the case of CIMR, the Level-2 SIC product cannot rely only on the L- or C-band imagery as the resulting spatial resolution would be too coarse.

```{important}
The crux of designing SIC algorithms for passive microwave satellite missions is to achieve high retrieval accuracy (which calls for using the low-frequency channels) and high spatial
resolution (which calls for using the higher-frequency channels) at the same time.
```

This is further illustrated on {numref}`fig_crux`.

```{figure} static_imgs/sic_crux_diagram.png
---
name: fig_crux
---
Illustration how spatial resolution (left y-axis) improves with increasing frequencies (x-axis) for the main three classes of passive microwave radiometer missions
(SSM/I and {term}`MWI` in purple, AMSR-E/2/3 in orange, and CIMR in yellow). The SIC retrieval uncertainties (right y-axis) get larger with frequency (blue line).
The dashed horizontal line represents the objective for CIMR mission in terms of SIC: less than 5 km and less than 5% uncertainty.
```

{numref}`fig_crux` illustrates how the SSMIS and MWI do not meet the CIMR objectives in terms of resolution. AMSR-E/2/3 can meet the objective of spatial resolution,
but not accuracy, by using its 89 GHz imagery channels. CIMR can meet both resolution and accuracy requirements, pending appropriate algorithms are designed and adopted.

Key assets of {term}`CIMR` in terms of SIC monitoring are:
1. high resolution (4-5 km) capabilities at K- and Ka-band, two microwave frequencies that are at the core of most state-of-the-art sea-ice concentration algorithms today;
2. medium resolution (15 km) capabilities at C-band, a channel where the atmosphere is mostly transparent and the sea-ice emissivities do not vary too much with sea-ice type;
3. the swath width and especially the "no hole at the pole" capability to improve coverage of sea ice monitoring in the Arctic;
4. the availability of a forward and a backward scan to improve the accuracy of retrievals.

CIMR has a requirement to provide some Level-2 products with 1 hour latency (see {term}`Near Real Time 1H`), including SIC, to
support safety at sea in Arctic regions. This requirement is translated in a dedicated {term}`SIC1H` Level-2 product that has to achieve
high resolution within a short latency. This might lead to reduced accuracy wrt to the nominal {term}`SIC3H` product. Typically, it means
the SIC1H algorithm should focus on K- and Ka-band imagery and potential skip some parts of the {term}`SIC3H` algorithm, e.g. atmospheric
correction of the brightness temperatures or deriving uncertainty estimates.

{term}`Sea Ice Edge` is a binary surface classification product derived from SIC. Users of the {term}`SIED` product typically do not need
to know how much the sea-ice area fraction is, just that sea ice significantly covers an area. {term}`SIED` can for example be used to mask
FoVs and regions where other algorithms are not to be processed or to indicate regions where vessels should not enter.

Lake ice has many shared characteristics with sea ice at the CIMR microwave channels. Lake ice is fresh (no salt) and seasonal
(no multiyear ice), but its emissivity contrast to (fresh) open water is such that mapping it with the same principles
as {term}`SIC` is possible. 

This document presents prototype algorithms for five CIMR Level-2 products:
1. the nominal Sea Ice Concentration (SIC) Level-2 product ({term}`SIC3H`);
2. the nominal Sea Ice Edge (SIED) Level-2 product ({term}`SIED3H`);
3. the Sea Ice Concentration (SIC) Level-2 product with {term}`Near Real Time 1H` latency requirement;
4. the Sea Ice Edge (SIED) Level-2 product with {term}`Near Real Time 1H` latency requirement;
5. the nominal Lake Ice Cover (LIC) Level-2 product ({term}`LIC`);

Below, we reproduce the CIMR MRD requirements that directly describe the variables addressed in the current ATBD.

```{note}
In the requirements below, AD- and RD- documents are numbered as in MRD v5. Refer to the MRD.
```

```{admonition} SIC3H and NTC (MRD&#8209;890)
CIMR shall generate L2 sea ice concentration (SIC) [AD-1], [AD-2] products at a
spatial resolution of ≤5 km and a standard total uncertainty of ≤5% with sub-daily
coverage of the Polar Regions and daily coverage of Adjacent Seas.

Notes:
1. This requirement addresses PRI-OBJ-1 as requested by [AD-1], [AD-2] and [AD3].
2. See also MRD-1110 that requests SIC in NRT1H.
3. The target standard total uncertainty of ≤5% is realistic for homogeneous scenes,
and non-melting surface conditions. In regions of high gradient (e.g., the marginal
ice zone) and under surface melt conditions, the standard total uncertainty will be
larger.
4. With a significant enhancement of spatial resolution compared to current and
planned missions, a 6.925/10.56 GHz channels in combination with a high
resolution 5 km channel at 18.7 and 36.5 GHz is an optimal channel for sea ice
concentration measurements (e.g., Ivanova et al., 2015). See also Zabolotskikh et al.
(2019).
5. The best performance SIC products will be obtained when CIMR data are used
together with other satellite measurements including scatterometer, SAR and
optical data to help e.g., resolve melt water ponds during summer amongst other
issues.
```

```{admonition} SIED3H and NTC (MRD&#8209;915)
CIMR shall generate L2 Sea Ice Edge (SIED) [AD-1], [AD-2] products at a spatial
resolution of ≤5 km with a confidence of >85% or <10 km (whichever is smaller)
with sub-daily coverage of the Polar Regions and daily coverage of Adjacent Seas.

Notes:
1. Sea Ice Edge is a surface classification product that assigns ocean grid cells to
sea-ice classes (e.g., Open Water, Very Open Drift Ice, Open Drift Ice, Closed
Ice, etc.). For the CIMR product, classes are TBD depending on the
implementation of CIMR. The EUMETSAT OSI SAF and C3S both provide seaice edge products with the following classes: Open Water (~<30% SIC), Open
Ice (~ 30-70% SIC) and Closed Ice (~>=70% SIC). See Aaboe et al. (2018).
2. The SIED product is a refined ICE/NO_ICE mask, that can be used for navigation
and used masking sea-ice signal in other CIMR products and/or satellite
missions (e.g., altimeter-based SSH, IR-radiometer-based SSTs, OC products,
etc.).
3. The uncertainty specification assumes a confidence matrix is used to discriminate
the sea-ice classes when compared to SAR and Scatterometer data (e.g., Aaboe
et al, 2016).
4. An alternative uncertainty characterization of the SIED product is the mean
distance to SAR/ice-chart sea-ice edge, expressed in km (Aaboe et al, 2016).
In this case, the requirement would be < 10 km.
5. See definition of Sea Ice Edge.
```

```{admonition} SIC1H and SIED1H (MRD&#8209;1110)
In support of Arctic polar navigational applications, CIMR Sea Ice Concentration
(SIC), Sea Ice Edge (SIED), Sea Ice Drift (SID), and as a goal: Ocean Wind Speed
(OWS), shall be available over specific regions of the Polar Arctic in Near Real
Time 1-hour (NRT1H).

Notes:
1. Communication in the Polar Regions remains a challenge with limited coverage
for data delivery using conventional approaches. Given that CIMR is focussed on
the timely delivery of data to support activities in the Arctic Ocean, including
operational aspects associated with shipping, exploration, general operations,
and other applications requiring real-time access to information enhanced
timeliness in the polar regions is highly desirable.
2. Several ice service providers (also providing ice charts to CMEMS) state that a
major advantage of an operational high-resolution microwave radiometer is in the
synergy with Sentinel-1 for which the requirement is <60 minutes from data
downlink over specific regions. This synergy can involve artificial intelligence (AI)
techniques, for combining the active and passive data.
3. In ice charting the validity and utility of data decrease exponentially with the delay
from sensing since ice is dynamic.
4. An option to address this requirement could include the use of a pass-through
downlink transmitting acquired data to a core ground station while the data is
being acquired by the instrument (as used by Sentinel-1 over specific areas).
5. Users in other Polar regions and adjacent Seas may have similar requirements
that are to be confirmed.
6. The coverage of the station(s) used for data downlink shall be compatible with the
polar areas where NRT1H data access is required.
7. NRT1H Tbs and L2 products may have a higher uncertainty
8. Other products of relevance indicated in [AD-1] could include Sea Ice Thickness
(SIT) and Ice Type/Stage of development (ITY).
9. The ice service requirement for Sentinel-1 is delivery of L1 SAR data <1 hour
after downlink. CIMR will be used in Synergy with these Sentinel-1 data.
10. This requirement may have implications for the selection and number of ground
stations required.
11. The order of importance for NRT1H products is 1) Tbs (K- and Ka-band, H and
V pol), 2) SIC, 3) OWS, 4) SID, 5) SIED. Strategies should be investigated to
speed-up processing, and to make available data products as fast as they are
processed (i.e., do not wait for all products to be produced before issuing) and
within 1H of sensing.
12. This requirement implies that navigation information is available (e.g.,
interleaved) with science data during the downlink to ensure processing can start
as soon as possible.
```

```{admonition} LIC NRT3H and NTC (MRD&#8209;1010)
CIMR shall generate terrestrial lake ice cover (LIC) L2 data products in freezing
conditions at a spatial resolution of ≤5 km, with a standard total uncertainty of
<10% and daily coverage for inland water areas that have no land within 20 km of
a target defined by a Hydrology Target mask.

Notes:
1. Channels that can measure lake ice cover include 18.7 and 36.5 GHz.
2. As a Secondary Objective, this requirement does not drive the instrument design.
```

