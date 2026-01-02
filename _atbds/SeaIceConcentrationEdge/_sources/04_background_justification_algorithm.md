(sec_background)=
# Background and justification of selected algorithm

## Sea Ice Concentration

The proposed algorithm for {term}`SIC3H` stems from the long history of developments
by the EUMETSAT {term}`OSI SAF` and the ESA {term}`CCI` Sea Ice teams.

Since the early 2000s, the OSI SAF have been developing state-of-the-art algorithms including swath-based
retrievals, dynamic generation of tie-points, atmospheric correction
of the brightness temperatures using {term}`RTM`s, and per-FoV uncertainties. Traditionally,
these algorithms have used the K and Ka microwave bands from the {term}`SSMIS` and 
later the {term}`AMSR2` missions.

Since the mid 2010s, the CCI Sea Ice projects have contributed critical R&D input to the
original OSI SAF approach. Of particular relevance to the proposed CIMR Level-2 SIC algorithm are
the demonstration of the benefits of using C-band (in combination with Ka-band) radiometry, and
the demonstration of using pan-sharpening techniques to take advantage of high(er) resolution microwave
imagery. {cite:t}`lavergne:2019:sicv2` gives an overview of the algorithm baseline including the
use of C-band radiometry, and {cite:t}`sicci+1:2021:sic_atbd` describes the use of pan-sharpening
(using near-90 GHz imagery).

The proposed CIMR Level-2 SIC algorithm take full advantage of these approaches by exploiting
the C-, K-, and Ka-band imagery of CIMR with dynamic tuning of the tie-points, and pan-sharpening
techniques to obtain <5 km, <5% SICs meeting the CIMR mission requirements {doc}`[RD-1] <./01_applicable_ref_docs>`.

Although many developments have been materialized through OSI SAF and CCI SIC R&D, the proposed
algorithm also relates to earlier and recent developments by other investigators, e.g. the 
Bootstrap and Bristol SIC algorithms {cite:p}`comiso:1986:sic,smith:1996:bristol` and the use of
pan-sharpening techniques {cite:p}`kloster:1996:eocompendium,kilic:2020:sic`.

## Sea Ice Concentration NRT1H (SIC1H)

The CIMR {term}`SIC1H` Level-2 product has two driving requirements: the {term}`Near Real Time 1H` latency, and
the <5 km resolution to support operational sea-ice services with safe navigation. Compared to the nominal 
{term}`SIC3H` Level-2 product, the requirement for accuracy of the {term}`SIC1H` Level-2 product is relaxed.

We propose to implement the CIMR {term}`SIC1H` Level-2 processing chain with building blocks from the {term}`SIC3H`
algorithm but removing some steps that require most computing time. For example, the {term}`SIC1H` product might
be built only on K and Ka, imagery, and do not use {term}`RTM` correction of the brightness temperature. Another
time-saving step can be to not estimate uncertainties, or at least with a simplified algorithm.

## Sea Ice Edge (nominal and SIED1H) 

We derive {term}`Sea Ice Edge` from the SIC, by finding the FoVs whose SIC is higher than a threshold (TBD, but generally
15% SIC). This ensures consistency with the SIC product. The same strategy is adopted for the NRT1H product.

We note that MRD&#8209;915 opens for several classes (e.g. Very Open Drift Ice, Closed Ice, etc...) corresponding to
different ranges of SICs. All these classes can be considered for the CIMR SIED product, but the main product will
be a water / ice mask with a low SIC threshold (TBD).

## Lake Ice Cover (LIC)

Because of the size of most lakes, the retrieval of LIC from CIMR will be limited to the larger high-latitude
(possibly high-latitude) lakes. The lake mask is TBD, but will be the same as that of the CIMR Lake Surface Water
Temperature (LSWT) product. In addition to the lake mask, a lake ice climatology mask must be prepared, to avoid
applying the LIC algorithm on target lakes that can never have ice.

The CIMR MRD ({doc}`[AD-1] <./01_applicable_ref_docs>`) calls for a LIC product with a resolution better than 5 km, which
calls for using the K- and Ka-band imagery only. We thus plan to use the same type of algorithm as for SIC (see above), but
with fixed tie-points that are adapted for lake (fresh water) ice. The method to derive these tie-points is still open and will be
the main element in the R&D plan for this variable, e.g. following the approach of {cite}`ghaffari:2011:caspian`.

