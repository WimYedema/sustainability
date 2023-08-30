# Environmental impact categories

The table below lists the environmental impact categories recognized by the EU
and their weighting and normalization factors:

```{csv-table}
:file: environmental-impact-categories.csv
:header-rows: 1
```

These categories are defined in {cite}`damianiunderstanding`,
{cite}`salaDevelopmentWeightingApproach2018`,
{cite}`fazioSupportingInformationCharacterisation2019`. The sections below gives a bit more detail

:Description: From {cite}`damianiunderstanding`
:EF characterization model: How the category was arrived at, from {cite}`fazioSupportingInformationCharacterisation2019`
:Model source: Literature source of the category model, from {cite}`fazioSupportingInformationCharacterisation2019`
:Normalization Factor: Factor to apply to normalize with other categories, from {cite}`salaDevelopmentWeightingApproach2018`
:Unit: Unit of measurement, from {cite}`damianiunderstanding`
:Unit description: Description of the unit, from {cite}`damianiunderstanding`
:Weight: Importance in percent of this category among the other categories, from {cite}`salaDevelopmentWeightingApproach2018`
:Weight (ex toxicity): Importance in percent of this category among the other categories when the toxicity categories are excluded, from {cite}`salaDevelopmentWeightingApproach2018`

```{todo}
Verify the descriptions of the Environmental impact categories.
```

## Climate change, total

Increase in the average global temperature resulting from greenhouse gas
emissions (GHG)

:EF characterization model: Baseline model of 100 years of the IPCC (based on IPCC 2013)
:Model source: Intergovernamental Panel on Climate Change (IPCC), 2013
:Normalization Factor: 8100
:Unit: kg CO2 eq
:Unit description: Radiative forcing as global warming potential – GWP100
:Weight: 21.06
:Weight (ex toxicity): 22.19

## Particulate matter

Impact on human health caused by particulate matter emissions and its precursors
(e.g. sulfur and nitrogen oxides)

:EF characterization model: PM model
:Model source: Fantke et al., 2016 in UNEP 2016
:Normalization Factor: 0.000595
:Unit: disease incidences
:Unit description: Impact on human health
:Weight: 8.96
:Weight (ex toxicity): 9.54

## Water use

Depletion of available water depending on local water scarcity and water needs
for human activities and ecosystem integrity

:EF characterization model: AWARE model
:Model source: Boulay et al., 2018; UNEP 2016
:Normalization Factor: 11500
:Unit: m3 water eq of deprived water (Regionalised CFs)
:Unit description: Weighted user deprivation potential
:Weight: 8.51
:Weight (ex toxicity): 9.03

## Resource use, fossils

Depletion of non-renewable resources and deprivation for future generations

:EF characterization model: CML 2002 model - Abiotic Depletion Potential (ADP) fossil
:Model source: van Oers et al., 2002 as in CML 2002 method, v.4.8
:Normalization Factor: 65000
:Unit: MJ
:Unit description: Abiotic resource depletion, fossil fuels – ADP-fossil
:Weight: 8.32
:Weight (ex toxicity): 8.92

## Land use

Transformation and use of land for agriculture, roads, housing, mining or other
purposes. The impact can include loss of species, organic matter, soil,
filtration capacity, permeability

:EF characterization model: Soil quality index based on LANCA
:Model source: Soil quality index based on an updated LANCA model (De Laurentiis et al. 2019) and on the LANCA CF version 2.5 (Horn and Meier, 2018)
:Normalization Factor: 819000
:Unit: pt (Regionalised CFs)
:Unit description: Soil quality index, representing the aggregated impact of land use on: Biotic production; Erosion resistance; Mechanical filtration; Groundwater replenishment
:Weight: 7.94
:Weight (ex toxicity): 8.42

## Resource use, minerals and metals

Depletion of non-renewable resources and deprivation for future generations

:EF characterization model: ML2002 model - Abiotic Depletion Potential (ADP) ultimate reserve
:Model source: van Oers et al., 2002 as in CML 2002 method, v.4.8
:Normalization Factor: 0.0636
:Unit: kg Sb eq
:Unit description: Abiotic resource depletion – ADP ultimate reserves
:Weight: 7.55
:Weight (ex toxicity): 8.08

## Ozone depletion

Depletion of the stratospheric ozone layer protecting from hazardous ultraviolet
radiation

:EF characterization model: EDIP model based on the ODPs of the World Meteorological Organization (WMO) over an infinite time horizon
:Model source: World Metereological Organisation (WMO), 2014
:Normalization Factor: 0.0536
:Unit: kg CFC-11 eq
:Unit description: Ozone Depletion Potential – ODP
:Weight: 6.31
:Weight (ex toxicity): 6.75

## Acidification

Acidification from air, water, and soil emissions (primarily sulfur compounds)
mainly due to combustion processes in electricity generation, heating, and
transport

:EF characterization model: Accumulated Exceedance model
:Model source: Seppala et al., 2006; Posch et al., 2008
:Normalization Factor: 55.6
:Unit: mol H+ eq
:Unit description: Accumulated Exceedance – AE
:Weight: 6.2
:Weight (ex toxicity): 6.64

## Ionising radiation, human health

Impact of exposure to ionising radiations on human health

:EF characterization model: Human Health effect model
:Model source: Frischknecht et al, 2000 (as developed by Dreicer et al. 1995)
:Normalization Factor: 4220
:Unit: kBq U-235 eq.
:Unit description: Human exposure efficiency relative to U-235
:Weight: 5.01
:Weight (ex toxicity): 5.37

## Photochemical ozone formation, human health

Potential of harmful tropospheric ozone formation (“summer smog”) from air
emissions

:EF characterization model: LOTOS-EUROS model
:Model source: Van Zelm et al., 2008, as applied in ReCiPe 2008
:Normalization Factor: 40.6
:Unit: kg NMVOC eq.
:Unit description: Tropospheric ozone concentration increase
:Weight: 4.78
:Weight (ex toxicity): 5.1

## Eutrophication, terrestrial

Eutrophication and potential impact on ecosystems caused by nitrogen and
phosphorous emissions mainly due to fertilizers, combustion, sewage systems

:EF characterization model: Accumulated Exceedance model
:Model source: Seppala et al., 2006; Posch et al., 2008
:Normalization Factor: 177
:Unit: mol N eq
:Unit description: Accumulated Exceedance – AE
:Weight: 3.71
:Weight (ex toxicity): 3.91

## Eutrophication, marine

Eutrophication and potential impact on ecosystems caused by nitrogen and
phosphorous emissions mainly due to fertilizers, combustion, sewage systems

:EF characterization model: EUTREND model
:Model source: Struijs et al., 2009 as applied in ReCiPe 2008
:Normalization Factor: 19.5
:Unit: kg N eq
:Unit description: Fraction of nutrients reaching marine end compartment
:Weight: 2.96
:Weight (ex toxicity): 3.12

## Eutrophication, freshwater

Eutrophication and potential impact on ecosystems caused by nitrogen and
phosphorous emissions mainly due to fertilizers, combustion, sewage systems

:EF characterization model: EUTREND model
:Model source: Struijs et al., 2009 as applied in ReCiPe 2008
:Normalization Factor: 1.61
:Unit: kg P eq
:Unit description: Fraction of nutrients reaching freshwater end compartment
:Weight: 2.8
:Weight (ex toxicity): 2.95

## Human toxicity, cancer

Impact on human health caused by absorbing substances through the air, water,
and soil. Direct effects of products on humans are not measured

:EF characterization model: USEtox model
:Model source: based on USEtox2.1 model (Fantke et al. 2017), adapted as in Saouter et al., 2018
:Normalization Factor: 0.0000169
:Unit: CTUh
:Unit description: Comparative Toxic Unit for humans
:Weight: 2.13

## Ecotoxicity, freshwater

Impact of toxic substances on freshwater ecosystems

:EF characterization model: USEtox model
:Model source: based on USEtox2.1 model (Fantke et al. 2017), adapted as in Saouter et al., 2018
:Normalization Factor: 42700
:Unit: CTUe
:Unit description: Comparative Toxic Unit for ecosystems
:Weight: 1.92

## Human toxicity, non-cancer

Impact on human health caused by absorbing substances through the air, water,
and soil. Direct effects of products on humans are not measured

:EF characterization model: USEtox model
:Model source: based on USEtox2.1 model (Fantke et al. 2017), adapted as in Saouter et al., 2018
:Normalization Factor: 0.00023
:Unit: CTUh
:Unit description: Comparative Toxic Unit for humans
:Weight: 1.84

