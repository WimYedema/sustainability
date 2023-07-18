# walshCarbonBenefitsCloud2020

```{bibliography}
:filter: key == "walshcarbonbenefitscloud2020"
:keyprefix: walshcarbonbenefitscloud2020-
```

```{admonition} Summary

Azure cloud is between 22% and 93% more energy efficient than traditional on-premise 
datacenters. They identify 4 reasons why azure cloud is better in terms of 
sustainability than on-premise  computing:

1. IT operational efficiency.
    * Dynamic provisioning
    * Multi-tenancy
2. IT equipment efficiency
3. Datacenter infrastructure efficiency
4. Renewable electricity
```

## Snippets

Analyzed the following Azure services:
* Azure Compute
* Azure Storage
* Exchange Online
* SharePoint Online

Key parameters considered in the analysis included:
* Equipment counts and specifications.
* Device utilization.
* Power draw of servers, storage devices, and networking equipment used within the datacenters.
* Power usage effectiveness (PUE) of datacenters hosting the services.
* Data flows over the internet.
* Carbon intensity of electricity supply.

## Model exclusions

Unless otherwise noted, the following are excluded given their
negligible impact:

* Embedded carbon in the building, including cooling and air conditioning equipment.
* Microsoft corporate overhead, including administration and software development.
* Upstream emissions from extracting the fuel used to power the electric grid.
* Embedded emissions for certain IT equipment not exclusively used by the modeled service, such as datacenter switches not located in the server racks.

## End-of-life disposal
* End-of-life disposal includes emissions associated with landfill and recycling for servers, hard disk drives, and network switches.
* The model assumes a conservative recycling rate of 20 percent. Even with a low assumed recycling rate, these emissions are negative due to the credit based on avoided use of virgin material from recycling.
* End-of-life emissions are amortized over the assumed lifetime of the device.

## Results

The results show that Azure Compute is 52-79 percent more energy efficient than
compute equivalents deployed in traditional enterprise datacenters [...],
depending on the type of enterprise deployment.

When renewable energy is taken into account, carbon emissions from Azure Compute
are 92-98 percent lower than traditional enterprise datacenter deployments of
compute equivalents 

The results show that Azure Storage is 71-79 percent more energy efficient than
storage equivalents deployed in traditional enterprise datacenters [...],
depending on the type of enterprise deployment.

When renewable energy is taken into account, carbon emissions from Azure Storage
are 79-83 percent lower than traditional enterprise datacenter deployments of
storage equivalents

```{admonition} Wim
Exchange and Sharepoint show similar improvements, but are less relevant for this research.
```
