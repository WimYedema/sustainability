# Literature on ICT emissions

* {cite:t}`bordageFiguresUnderstandingEnvironmental2021`: [Need to read](./bordageFiguresUnderstandingEnvironmental2021.md)
* {cite:t}`pirsonAssessingEmbodiedCarbon2021`: [Need to read](./pirsonAssessingEmbodiedCarbon2021.md)
* {cite:t}`maagoeICTImpactStudy2020`: [Need to read](./maagoeICTImpactStudy2020.md)
* {cite:t}`BunthernLifeCycle2019`: Need to read
* {cite:t}`benqassemDigitalTechnologiesEurope2021` : [Environmental life-cycle analysis of ICT in europe](./benqassemDigitalTechnologiesEurope2021.md)
* {cite:t}`belkhirAssessingICTGlobal2018`: [2018 - Assessing global ICT emissions](./belkhirAssessingICTGlobal2018.md)
* {cite:t}`unepdtuGreenhouseGasEmissions2020`: [UNEP DTU presentation](./unepdtuGreenhouseGasEmissions2020.md)
* {cite}`inrWeNR2021Release2021`: [WeNR 2021](./inrWeNR2021Release2021.md)
* {cite:t}`saraevLCAServersR65152021`: [LCA of Dell Servers](./saraevLCAServersR65152021.md)

:::{todo} 
There are many metrics on the SPEC benchmark sites for servers, including power
draw. It is still too limited to get a decent overview, but it might be worth
exploring in an automated way.

* SPECint mostly has performance numbers on integer calculations.
* SPECfp (https://www.spec.org/cpu2017/results/rfp2017.html) has performance on floating-point and may include base and peak energy numbers, although it's rarely calculated.
* SPECssj (https://www.spec.org/power_ssj2008/results/) has power metrics (avg watts @ 100% and idle) and SSJ ops at 100% and some operating stats
:::

## EcoInvent Database

Although {cite:t}`pirsonAssessingEmbodiedCarbon2021` mentions that EcoInvent is not a source of good quality data.

* [IC production](https://ecoquery.ecoinvent.org/3.9.1/cutoff/search?query=integrated+circuit+production&currentPage=1&pageSize=50&sector=Electronics)
* [PWB production](https://ecoquery.ecoinvent.org/3.9.1/cutoff/search?query=printed+wiring+board+production&currentPage=1&pageSize=50&sector=Electronics)
* [Drive production](https://ecoquery.ecoinvent.org/3.9.1/cutoff/search?query=drive+production&currentPage=1&pageSize=50&sector=Electronics)

## Environmental footprint data from companies

:::{list-table}
   :header-rows: 1
  :widths: 2 10
* - Company
  - Description
* - [Apple](https://www.apple.com/environment)
  - Provides information on carbon footprint, also with some options.
* - [Samsung](https://www.samsung.com/global/sustainability/digital-library/policy-document/)
  - Information on more EF metrics, but some devices only use percentages, no
    absolute numbers. Also only results. For tablets they give tables with data on
    many metrics. 
* - [ST micro](https://www.st.com/content/st_com/en/about/st_approach_to_sustainability/sustainability-priorities/sustainable-technology/eco-design/footprint-of-an-ultra-low-power-mcu.html)
  - Provides some numbers on generic products like "Ultra low power MCU" and "Automotive MCU", but no rationale
:::

## Fabrication process

https://semiconductor.samsung.com/support/tools-resources/fabrication-process/


