# CIMR L2 SIC, SIED, SIC1H, SIED1H and LIC ATBD

This document describes the algorithm theoretical basis for five closely related CIMR Level-2 products:
1. the nominal Sea Ice Concentration (SIC) Level-2 product ({term}`SIC3H`);
2. the nominal Sea Ice Edge (SIED) Level-2 product ({term}`SIED3H`);
3. the Sea Ice Concentration (SIC) Level-2 product with {term}`Near Real Time 1H` latency requirement;
4. the Sea Ice Edge (SIED) Level-2 product with {term}`Near Real Time 1H` latency requirement;
5. the nominal Lake Ice Cover (LIC) Level-2 product ({term}`LIC`);

The first four products are from the Polar Ocean product family, while LIC is from the Land product family. Their algorithms are nonetheless presented together because the retrieval principles are much similar.

In addition, this ATBD describes how {term}`SIE` (Sea Ice Extent) is computed from SIC. SIE is an integrated quantity that is not derived at L2 but rather downstream in the processing chain (after L3/L4). SIE will thus not be implemented in the CIMR L2PAD {term}`GPP`.


```{tableofcontents}
```

