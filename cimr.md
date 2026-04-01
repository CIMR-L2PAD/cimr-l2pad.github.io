---
layout: page
title: CIMR
permalink: /cimr/
---

CIMR is the Copernicus Imaging Microwave Radiometer mission, a multi-frequency conically-scanning passive microwave imager
designed by ESA to support EU's Arctic Policy, among others. Its launch is scheduled in 2029/30. CIMR refers equally to the mission,
the satellite, and its main instrument.

<figure style="margin:1.5rem 0;">
  <img src="/assets/img/CIMR_inflight.jpg" 
       alt="The CIMR satellite" 
       style="max-width:100%; height:auto; border-radius:4px;">
  <figcaption style="margin-top:0.5rem; font-size:0.9rem; color:#555;">
    Artist view of CIMR in flight (credit: ESA/mlabspace)
  </figcaption>
</figure>

## Official resources about the CIMR mission

Information about CIMR can be found on the official ESA webpage, in particular:
* The [official ESA page about the CIMR mission](https://www.esa.int/Applications/Observing_the_Earth/Copernicus/CIMR)
* The [SentiWiki page about CIMR](https://sentiwiki.copernicus.eu/web/cimr)

ESA has prepared videos introducing the mission,
find them [here](https://www.esa.int/esatv/content/search?SearchText=CIMR&result_type=videos_broadcast&SearchButton=Go).

The [CIMR Mission Requirement Document v6](https://esamultimedia.esa.int/docs/EarthObservation/CIMR-MRD-v6.0-20260324-ISSUED.pdf)
is available online.

## General introduction to the CIMR mission

__The information below is prepared by the CIMR L2PAD team to introduce the CIMR mission to future Level-2 users.
It summarizes and paraphrases information from the official sources listed above. Some of the illustrations used
below are prepared from simulated files and might not fully reflect the final characteristics of CIMR in-flight.__

The CIMR satellite system is developed as part of the Expansion activities in the EU's Copernicus program and is designed to monitor
the rapid changes occurring in the Earth system. Monitoring these rapid changes in the Arctic environment and the polar regions in 
general (including Greenland and Antarctica) is a key objective of the Copernicus Polar Observing System, as specified in the Polar
Expert Group (PEG) reports on user requirements. The prioritized user needs expressed by the European Commission's PEG form the
foundation for the CIMR satellite and their translation into the characteristics of the mission is covered in the Mission
Requirement Document ([MRD](https://esamultimedia.esa.int/docs/EarthObservation/CIMR-MRD-v6.0-20260324-ISSUED.pdf)).

### Spacecraft,  orbit, and constellation
The CIMR satellite will operate in a dawn-dusk orbit, a special type of Sun-synchronous orbit where the satellite travels in constant
sunlight by closely following the boundary between the Earth's day and night sides, called the "terminator." This unique orbit allows
the satellite to cross the equator at 6:00 AM local time when the Sun is rising (dawn) and at 6:00 PM local time when it is setting (dusk).
This orbit minimises daily eclipse periods to mitigate the impact of thermoelastic distortion, maximise power generation and minimise
the complexity and size of the solar array.

In addition, this orbit ensures continuity with the long series of SSMIS, SMAP, and SMOS missions (among others), and ensures short
separation time (< 10 min) with acquisition by the EPS-SG satellites(s) in the polar regions. The dawn-dusk orbit allows better
sensing of the so-called foundation temperature of the oceans, and reduces Sun-glint and ionosphere (Total Electron Content)
contamination at L-band. Note that the AMSR(-E, 2, 3) satellites are flying in a different Sun-Synchronous orbit with equatorial
crossing times at 13:30 local time (descending node) and 01:30 local time (ascending node).

The CIMR orbit has a repeat cycle of 29 days and a cycle length of 412 orbits. It means that the satellite repeats its ground track
every 29 days, and thus revisit the exact same locations on Earth after completing 412 orbits around the planet. This repeat cycle
ensures consistent spatial coverage and allows for comparison of data collected at the same locations over time.

Importantly, the objectives of the CIMR missions are fulfilled with a single satellite, not a pair of satellite like most other Sentinel
missions (e.g. Sentinel-1C and 1D). Still, two CIMR satellites are foreseen, CIMR-A and CIMR-B. The second satellite is purely to extend
the mission lifetime, not to increase revisit frequency. An initial tandem flight phase, whose duration is expected between 6 (minimum)
and 12 (optimum) months is foreseen where one of the two flies right behind the other, to improve inter-calibration between the
two missions. This is critical for CIMR to fully contribute to the generation of Climate Data Records of critical Essential Climate
Variables (ECVs). Outside the tandem phase, the nominal phasing position is at ~180°, and is configurable.

The minimum lifetime of a single CIMR satellite shall be 7.5 years including a commissioning period of at least 6 months. This means
that the CIMR mission should cover at least 15 years, with two satellites.

The launch of the first CIMR satellite is currently planned for 2029/30.

Acquisition of CIMR mission data is expected to be at the Svalbard Satellite Station, operated by KSAT. The high latitude of the station
and the relatively low data volume generated by CIMR sensing ensures that all orbits can be fully downlinked as CIMR flies over the Arctic
Ocean. This means that observations from the Northern Hemisphere and especially the Arctic regions will always be fresher (lower latency)
than those from the Southern Hemisphere and Antarctic region. In this context, the latency is the duration between the the observation
sensing time and the time a product (e.g. a Level-2 product using this observation) is available to a user.

### Instrument and sensing characteristics

The technical solution for the CIMR instrument is implemented by a multi-channel conically scanning microwave radiometer.
The radiometer is optimized with low-noise channels and unique spatial resolutions centered in the L- (1.4 GHz), C- (6.9 GHz),
X- (10.8 GHz), K- (18.7 GHz), and Ka-band (36.5 GHz).

The table below summarizes the characteristics of the CIMR instrument that are most relevant for an end user to understand the
CIMR mission. It is a summary of a similar table in the [MRD](https://esamultimedia.esa.int/docs/EarthObservation/CIMR-MRD-v6.0-20260324-ISSUED.pdf). 
<table width="100%" cellpadding="4" cellspacing="0">
	<col width="57*"/>
	<col width="40*"/>
	<col width="40*"/>
	<col width="40*"/>
	<col width="40*"/>
	<col width="40*"/>
	<tr>
		<td width="22%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.04in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			<b>Band name</b></p>
		</td>
		<td width="16%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.04in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			<b>L</b></p>
		</td>
		<td width="16%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.04in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			<b>C</b></p>
		</td>
		<td width="15%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.04in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			<b>X</b></p>
		</td>
		<td width="16%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.04in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			<b>K</b></p>
		</td>
		<td width="16%" style="border: 1px solid #000000; padding: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			<b>Ka</b></p>
		</td>
	</tr>
	<tr>
		<td width="22%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			Center Frequency [GHz]</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			1.4135</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			6.925</p>
		</td>
		<td width="15%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			10.65</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			18.7</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			36.5</p>
		</td>
	</tr>
	<tr>
		<td width="22%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			Polarization</p>
		</td>
		<td colspan="5" width="78%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			Full Stokes (H-pol, V-pol, 3<sup>rd</sup> Stokes, 4<sup>th</sup>
			Stokes)</p>
		</td>
	</tr>
	<tr>
		<td width="22%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			Scanning sector [°]</p>
		</td>
		<td colspan="5" width="78%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			[0-360] (full scan, sometimes separated in an <i>fore</i> and an
			<i>aft</i> scans)<br/>
(note: short portions are used for on-board
			calibration each scan)</p>
		</td>
	</tr>
	<tr>
		<td width="22%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			Swath width [km]</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0; background: #ffff00">
			?</p>
		</td>
		<td colspan="4" width="62%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			&gt;1900</p>
		</td>
	</tr>
	<tr>
		<td width="22%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			Observation Zenith Angle [°]</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			~51.9</p>
		</td>
		<td colspan="4" width="62%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			~55.5</p>
		</td>
	</tr>
	<tr>
		<td width="22%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			Dual-frequency radiometer feeds</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			No</p>
		</td>
		<td colspan="2" width="31%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			Yes</p>
		</td>
		<td colspan="2" width="31%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			Yes</p>
		</td>
	</tr>
	<tr>
		<td width="22%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			Number of radiometer feeds</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			1</p>
		</td>
		<td colspan="2" width="31%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			4</p>
		</td>
		<td colspan="2" width="31%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			8</p>
		</td>
	</tr>
	<tr>
		<td width="22%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			Number of samples to form a L1b footprint</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			5</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			5</p>
		</td>
		<td width="15%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			5</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			5</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			5</p>
		</td>
	</tr>
	<tr>
		<td width="22%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			L1b Footprint size<a class="sdfootnoteanc" name="sdfootnote1anc" href="#sdfootnote1sym"><sup>1</sup></a>
			(requirement) [km]</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			&lt;60</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			≤15</p>
		</td>
		<td width="15%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			≤15</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			≤5.5</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			&lt;5 (goal=4)</p>
		</td>
	</tr>
	<tr>
		<td width="22%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p style="orphans: 0; widows: 0">
			L1b radiometric resolution (aka NeΔT) [K], 1-sigma at 150K</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			≤0.3</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			≤0.2</p>
		</td>
		<td width="15%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0">
			≤0.3</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in"><p align="center" style="orphans: 0; widows: 0; margin-bottom: 0in">
			≤0.4</p>
			<p align="center" style="orphans: 0; widows: 0">(goal: ≤0.3)</p>
		</td>
		<td width="16%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in"><p align="center" style="orphans: 0; widows: 0">
			≤0.7</p>
		</td>
	</tr>
</table>

All frequencies are recorded in 4 polarizations: vertical, horizontal, 3rd Stokes and 4th Stokes components. The instrument records
along a full [0-360°] scan, providing both a fore and an aft view of each Earth location. This is unlike most past and current
conically scanning radiometer missions for which only part of the scanning arc is available (the rest being hidden by the satellite
itself or its solar panels). To achieve high spatial resolution, a large ~8-meter diameter mesh reflector is implemented.
Multiple dual-frequency polarized radiometer feeds (1 at L-band, 4 at C/X-band, 8 at K/Ka-band) are necessary to minimize the rotation
speed of the reflector, and onboard active calibration units maintain low random (NeΔT) and total standard uncertainty for all measurements.

The conically scanning design enables a very wide swath width of nearly 2000 km (for C- to K-bands, narrower at L-band), providing
sub-daily coverage of the Arctic and 95% coverage of the Earth every day using a single satellite. A driving requirement for the CIMR
mission has been to achieve “no hole at the pole”: the pole points will be observed at the edge of each swath (at C- to Ka-band, not at L-band).

<figure style="margin:1.5rem 0;">
  <img src="/assets/img/CIMR_coverage_light.png" 
       alt="Spatial coverage of one day of CIMR observations" 
       style="max-width:100%; height:auto; border-radius:4px;">
  <figcaption style="margin-top:0.5rem; font-size:0.9rem; color:#555;">
  Illustration of the geographical coverage of the CIMR mission for the global, Arctic, and Antarctic regions. The image plots
  the number of 24h revisits (orbits). Note that the pole point(s) are covered in all orbits. Note that the 29 days repeat
  cycle of CIMR will ensure that the regions that are not observed on a given day are observed the day after.
  </figcaption>
</figure>

The C- to Ka-band frequencies are recorded with an Observation Zenith Angle (OZA) close to 55.5° while the L-band is recorded
with an OZA around 51.8°. The lower OZA at L-band is selected to improve the spatial resolution of the L-band imagery. It
leads to the narrower swath for L-band than for the other frequencies.

<figure style="margin:1.5rem 0;">
  <img src="/assets/img/cimr_CandLband_swath.png" 
       alt="Swath width of CIMR at C- and L-band" 
       style="max-width:100%; height:auto; border-radius:4px;">
  <figcaption style="margin-top:0.5rem; font-size:0.9rem; color:#555;">
  Illustration of the scanning pattern of CIMR. The image shows a short portion of a simulated CIMR orbit, with the C-band
  swath in orange and the narrower L-band swath in yellow. Note the full scan pattern consisting of the fore and aft scans.
  Note that only a subset of the CIMR samples are plotted.
  </figcaption>
</figure>

A defining feature of the CIMR instrument, and a consequence of the multiple radiometer feeds
needed to record a gap-free image of the Earth surface is that the different
feeds have different OZAs. This is different from past conically scanning radiometer missions that used only one feed per frequency.
This difference of OZA between feeds can result in a striping pattern in the raw Tb imagery, that must be accounted for or
compensated to a fixed reference OZA for downstream applications. The striping effect is expected to largest over the
open ocean and over bare soil. Ice and vegetation reduce the sensitivity of Tb to OZA.

Because of the multiple radiometer feeds (1 at L-band, 4 at C/X-band, 8 at K/Ka-band), the raw L1b imagery of CIMR is
more challenging to use than from past and current similar missions. In addition to the per-feed OZA mentioned above,
the on-ground location of each frequency channel is different. Combining several frequency channels in a downstream application,
including in the Level-2 products, thus require resampling and regridding to a common set of positions and sizes.

<figure style="margin:1.5rem 0;">
  <img src="/assets/img/cimr_feed_OZA.png" 
       alt="CIMR Observation Zenith Angle by feed" 
       style="max-width:100%; height:auto; border-radius:4px;">
  <figcaption style="margin-top:0.5rem; font-size:0.9rem; color:#555;">
  OZA variations by feed and along the orbit from a simulated CIMR L1b file for L-band (left), C-band (middle), and K-band (right).
  X- and Ka-band OZAs are similar to C- and K-band since they are recorded by the same feeds. The selected reference OZA values
  are also plotted. The simulation was performed by the CIMR SCEPS project team and the plot is made by the CIMR L2PAD project.
  The simulation corresponds to an ideal case (no ‘wobbling’ along the orbit).
  </figcaption>
</figure>
