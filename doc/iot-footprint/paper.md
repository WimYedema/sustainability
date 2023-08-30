# Paper

:Title: How to take environmental footprint into account when designing IoT solutions

## Introduction

::::{margin}
:::{admonition} Context
Environmental footprint of IOT systems.
:::
::::

IoT systems are everywhere, from finance to health, from manufacturing, to
agriculture, and their number and complexity is continuing to
grow{cite}`reinselDigitizationWorldEdge2018`. But while the benefits to society
are great, when we put that growth in the perspective of the ever growing
greenhouse gas (GHG) emissions from ICT, it is clear that we need to start to
take the environmental footprint into account when designing, developing, and
maintaining such systems.

An architect of IoT systems needs to take many aspects into account in his
design, like latency, security, and cost, but environmental footprint is rarely
one of them{cite}`gill2018edge`. And when it is, choices are made more on the
basis of belief than on facts.

---

::::{margin}
:::{admonition} Goal
*long-term goal. Not necessary the goal of the paper.*
:::
::::

Ideally the architects have tooling that aids them in their design and an IoT
system framework that manages environmental footprint during use. Environmental
footprint is calculated on the entire equipment life-cycle, manufacturing,
distribution, use, end-of-life, but these numbers are very hard to come by, and
may change significantly over time. Such a framework must encompass both design
and use because the choices in design affect the capabilities during use, and
the current capabilities affect the choices in the inevitable redesign.

---

::::{margin}
:::{admonition} Scope
.
:::
::::

An IoT system is not static. It is a continuously evolving system with updates,
upgrades, and extensions of both software and hardware. In this article we
explore how choices in software architecture affect choices in equipment, we
explore the environmental footprint of equipment used in IoT systems, and how
that relates to the IoT system as a whole. How to manage the environmental
footprint over the entire lifetime of the IoT system and how to integrate
environmental footprint into other system-level concerns is out of scope.

IOT systems are frequently used to manage equipment that consumes power. In this
regard an IOT system can have a net positive effect on environmental footprint
by reducing the energy consumption of the equipment it controls. This reduction
is caused by the IOT application, not the IOT system that implements it. As
such, these footprint reductions are out of scope.

Moreover, and where applicable, we will also limit the scope to the ecological
priorities defined by the European Union.

---

**[Contributions]**

- *Deliverables zonder relatie onderling (bvb. proof of concept/prototype, echte werkomgeving, interviews, new software, …)*
- *De ingredienten waarmee je gaat werken*

*Contributions*

- Approach / methode
    - Hoe ga je aan de contributies komen en wat zijn de afhankelijkheden. Zit er een volgorde in.
    - 
- *We will do an extensive literature study on environmental footprint of equipment in IoT*
- *Life-cycle analysis of equipment*
- *Large trends and statistics*
- *European policy*
- *…*

*Approach*

## Environmental footprint of ICT

::::{margin}
:::{note}
*Explains why we look at the entire life-cycle and why we also take resource use into account*
:::
::::

The environmental footprint of a product is the sum of the ecological impact for
each stage in its life-cycle. In the EU the ecological impact is measured and
weighted on 16 different categories
{cite}`zamporiSuggestionsUpdatingProduct2019`{cite}`zamporiSuggestionsUpdatingOrganisation2019`,
but not all categories are relevant for IT.
{cite:t}`benqassemDigitalTechnologiesEurope2021` identified 8 categories that
are, with the top 3 being: climate change (greenhouse gas emissions), weighted
at 21.5%; minerals and metals resource use, weighted at 6.7%; and fossils
resource use, weighted at 8.3%. Greenhouse gas (GHG) emissions is deemed most
important, by the EU and by others, and has received - by far - most attention
({cite}`unepdtuGreenhouseGasEmissions2020`,
{cite}`belkhirAssessingICTGlobal2018`, {cite}`marcacciHowMuchEnergy2020`,
{cite}`inrWeNR2021Release2021`, and many more). The statistics and predictions are
not without debate, but we can at least conclude that the GHG emissions of ICT
is significant and rising, and that manufacturing of equipment plays a major, if
not dominant role in these emissions.

In 2021, the European Parliament group of the Greens/EFA published a
report{cite}`benqassemDigitalTechnologiesEurope2021` on a more thorough study on
the ecological impact of ICT in Europe. They report that manufacturing is
responsible for 40.1% of the ICT GHG emissions and use 57.8%. However, they also
conclude that although the impact of GHG emissions is great, the impact of
resource use (minerals, metals, and fossil) in manufacturing is greater still.
They advise that *"[…] they should therefore be taken into account first and
foremost in all strategies to reduce environmental impacts."*


[TODO: EU requirements on reporting on AI/ICT footprint.]

## Anatomy of IOT systems

An IOT system provides the means to efficiently and effectively manage a
real-world process. Examples of real-world processes include managing traffic in
a city, managing crop yield in a farm, managing produce quality in a factory,
and so on. To do so the system needs to sense or measure a variety of attributes
at a variety of locations, deduce what is happening, make any necessary changes
to the process, and report on the state of the whole. For example, in a
greenhouse sensing  that the inside temperature is too high, the solar radiation
is good, and the outside temperature is high, the system deduces that cooling is
necessary, reports the situation, and activates the equipment.

The physical environment that we want to sense and control is called the *edge*
{cite:t}`gill2018edge`. Sensing and controlling is done through *endpoints*
(this is where the network "ends") which can be sensors, actuators or both. The
system is IOT when it includes a *core* that is responsible for *compute* and
*storage*. By necessity the system includes *communications* between endpoint
and core.

In this configuration one can apply *edge computing* which is a network topology
that places some compute, but not all, closer to the endpoints. *Fog computing*
is a form of edge computing where compute is at the endpoint, and some
orchestration may be done.

The *core*, the central location that performs compute and storage, can be an
on-premise datacenter, a remote hyperscale cloud datacenter, or anything in
between.

IOT equipment manufacturers typically offer for the following layers
{cite}`MT85ChallengesEdge`,{cite}`IoTArchitectureTopology`:

| Layer | Device type                | Communication              | Description                                            |
| ----- | -------------------------- | -------------------------- | ------------------------------------------------------ |
| Edge  | Endpoint, Sensor, Actuator | *Anything, often wireless* | Things + management, sense and control                 |
|       | Gateway                    | Ethernet                   | Low-latency compute, filtering, normalization          |
|       | On-Premise compute         | Ethernet                   | Filtering, normalization, analytics, store and forward |
| Core  | Datacenter, Cloud          | Ethernet                   | Analysis, management, archiving                        |
| User  | Laptop, Tablet, Mobile     | Ethernet, Wifi, 4G, 5G     | Insights and actions                                   |

## Considerations for IOT systems

## Environmental footprint in IOT
Zooming in, we see that a variety of energy sources may be used. Some devices
are battery powered, others have solar panels, and yet others are plugged into
the electric grid. The source of energy is relevant as it greatly affects the
balance of environmental impact between production and use. All-in-all, the
following physical components are major contributors to the environmental impact
of an IOT system:

* Batteries
* Displays
* Memories and storage
* Compute ICs and PWBs/PCBs

:::{todo}
Use {cite:t}`pirsonAssessingEmbodiedCarbon2021` in the composition of this list.
:::

We have excluded the components that are used for actuation, like electric
motors, and sensing, like camera sensors. While they have an obvious
environmental impact, we assume that the choices here are driven by the use-case.

There are many forms of computing and storage that can be used in an IOT system:

1. **Cloud computing.** Sensors, actuators and dashboards are connected to the
   internet and directly accessed and controlled from software running in a
   cloud data center. All data is stored in the cloud.
2. **On-premise computing.** All servers are on-premise, close to the sensors,
   actuators, and dashboards. This is where all compute is done, including
   training, and where all data is stored.
3. **Edge computing.** The software is partitioned into tasks that need to
   happen close to the sensors and actuators, and other tasks. **There are
   servers on-premise for the edge tasks, but other tasks are done in a cloud
   data center. This is also where data is stored and training is done.
4. **Fog / Mist computing.** The software is partitioned as in *edge computing*,
   but rather than centralizing the edge tasks to local servers the tasks are
   distributed among existing local compute like sensors, actuators, and network
   equipment. Data is still stored in cloud data centers where training happens.

## Drivers of IOT Environmental footprint

**What are the main contributors to the environmental footprint of an IOT system?**

We will start exploring this question with physical contributors, like CPUs and
memories, and then see whether we can identify logical/virtual contributors,
like algorithms and data streams.

Physically we can break this question down into: (1) the environmental footprint
of the equipment that needs to be manufactured for this solution, (2) the
environmental footprint of the energy being used during usage, and (3) the
contribution of this solution to the demand on common infrastructure.

However, the physical characteristics of the system are determined by its
logical, application requirements. Typical application requirements for an IOT
system are ({cite:t}`gill2018edge` and
{cite:t}`jiangComputationOffloadingEdge2019`):

* Data volume for both persistent data and transitory data.
* Need for autonomy or disconnect
* Privacy and security concerns
* Local interactivity
* Low or deterministic latency
* Quality of Service

The amount of compute required is a consequence of the application need and the
resulting data volume and latency requirements.

Lacking from this list are the needs that arise from AI and machine learning.
Beside a large volume of persistent data, machine learning may also require a
significant amount of compute. The scale of machine learning compute is mostly
dependent on the volume of data and the rate at which machine learning is
performed.

The chain of consequence is as follows:
1. Application requirement (e.g.: more or more accurate information on a process)
2. Algorithm choices. The required information can be computed by applying
   algorithms A and B
3. Sensor choices. The algorithms need data that Sensors C and D can produce.
4. Topology. The required latency, security, and QoS can be achieved with a
   local/distributed compute and communication topology.
5. Compute and storage power. For the required latency and learning rate and the
   given topology and data volume, the necessary compute and storage
   requirements can be determined.

Intuitively data volume seems to be indirectly responsible for a large portion
of the environmental footprint of an IOT solution. With higher data volumes we
get:
* More storage capacity
* More communication
* More compute power 
* More and/or more complex sensors

Also, lower latencies seem to have an adverse effect on the environmental
footprint, even for the same data volume. With lower latencies we get:
* More compute power
* More localized topologies. This might not be a problem, but the power use
  effectiveness (PUE) of local topologies is usually worse than more distributed
  topologies that can benefit from multi-tenancy.

```{todo}
Analyze latency trends using data from https://www.fcc.gov/reports-research/reports/measuring-broadband-america/measuring-fixed-broadband-twelfth-report 
```

Physical contributors:

* Use-phase Energy sources
  * Batteries
  * Local power generation
  * Power grid
* Dedicated Equipment manufacturing
  * Sensors, Actuators, Displays, etc.
  * Dedicated compute and storage
* Common infrastructure contribution
  * Communication
  * Storage
  * Compute

### Research questions

The question we wish to answer in this article is how to take ecological impact
into account when designing IoT solutions. When does it make sense to use local
edge computers, on-premise data servers, or compute services in the cloud? What
are the conditions of this decision, and how frequently do they change? And,
finally, would it make sense to change the location of compute dynamically, or
is the rate or magnitude of change too low?

As a working scenario we use a system where the edge is comprised of several IoT
sensors and actuators, and some dashboards for aggregate data; where compute is
done on the data streams for monitoring, control, and aggregation, and where
historical data is recorded to train new (machine learning) models.

## Environmental footprint of hardware

### IT life cycle

There are four life cycle phases for IT equipment, each with a unique ecological
impact: manufacturing, distribution, use, and end-of-life. The ecological impact
of IT is dominated by the manufacturing
phase{cite}`benqassemDigitalTechnologiesEurope2021`, mostly because of mineral
and metal use. Unsurprisingly, greenhouse gas emissions dominate the ecological
impact for IT usage. While relevant in general, in our comparison we will not
take into account the differences in distribution phase, useful life, and
end-of-life phase. We expect the impact to be negligible, and differences are
greatly influenced by varying operating conditions or organizational policies.

### Manufacturing

We must take manufacturing into account, given its impact. Throughout the
lifespan of an IoT solution, IT equipment will probably be replaced several
times. The main difference between the various scenarios is in where compute is
done, and so in which servers are used at which location.

A major difference between on-premise servers and datacenter servers is in how
peak performance demand is handled. With a data center peak performance can be
managed by the elasticity of the data center. A fully on-premise server park
must be scaled for the worst case performance and may have high manufacturing
impact simply because it must have more servers. As such we will use the
*average* compute load to calculate the manufacturing impact for data centers,
and the *worst case* compute load to calculate the manufacturing impact for
on-premise solutions.

You could argue that the total manufacturing impact of a datacenter dwarfs the
contribution of a single IoT solution, but that does not mean it is negligible
when compared to alternative solutions. We should not assume the manufacturing
impact on a datacenter is zero, as this would give an unfair advantage to
datacenter use.

To reduce the ecological impact of manufacturing, the solution should use as few
computers as possible. It is better to increase the compute power of a computer
than it is to add another low-power computer. If we were to take this to
extremes we should increase the compute power at the sensors and actuators and
forego additional servers. **[provide numbers and references to warrant this]**

### Usage

We can characterize the differences between the various solutions as follows:

- **Networking equipment utilization**. The network distance between edge and
  compute is highest in cloud computing which will utilize the most networking
  equipment.
- **Idle and stand-by time.** Cloud computing can be designed to allow for
  multi-tenant server usage and thereby reduce energy waste by reducing idle and
  stand-by time.
- **Power-use Effectiveness (PUE).** The percentage of energy used for actual
  computation.

#### On-premise computing

Studies sponsored by Microsoft, {cite}`walshCarbonBenefitsCloud2020`, and
Amazon, {cite}`bizoCarbonReductionOpportunity2019`, and reaffirmed in
{cite}`benqassemDigitalTechnologiesEurope2021`, indicate that cloud computing
has a significantly better carbon footprint than traditional on-premise
datacenters. The reasons are that traditional datacenters tend to be
overprovisioned to cater for potential worst-case demands. Cloud vendors
mitigate this through multi-tenancy. To quote Walsh: *“Generally, as the number
of users increases, the ratio of the peak demand to the average demand for the
user set decreases.”* 

Another reason is that cloud datacenters tend to have more efficient IT
equipment and datacenter infrastructure. 

## Fictional example

Company A has an IoT solution for their traffic lights and sensors, consisting
of one IoT sensor per traffic light, with the following properties:

- Power draw of 1W (8,76 kWh per year, ~2 kg CO2 per year)
- Production costs of 10 kg CO2
- Expected life span of 10 years, of which 8 have elapsed.

There is a new chip available, with a power draw of 0.5W (~1 kg CO2 per year),
and production costs of 20 kg CO2, with an expected lifespan of 20 years. When
is it worthwhile (or optimal) to replace the chips from a sustainability
standpoint?

The total expected emissions for the old sensors was 10 + 10*2 = 30 kg CO2. With
the current lifespan that is 10 + 8*2 = 26 kg CO2. The new chip will costs in it
expected lifetime 20 + 20*1 = 40 kg CO2, or 2 kg CO2 per year.

Stated differently: the new chip costs 1 kg less per year to operate. To earn
back the initial production costs of 20 kg CO2, the new chip needs to operate
for 20 years. Drawback: comparing two scenarios: one of 20 years (replace
directly) and one of 22 years (wait + replace).

Conclusion: don’t replace, better to use the current hardware for the remaining
2 years? Why?

However, should we include a fixed timespan of the next 30 years and calculate
for the whole timespan the optimal solution?

Replace now: 22 years 2 kg CO2 per year, assuming a similar device is bought
after the lifespan to replace it. Replace later is 2 years 2 kg CO2 per year and
20 years 2 kg CO2 per year. Is the same.

However, don’t fix that ain’t broken, because it costs 20 years to earn back the
production costs. So better to delay that. But how to quantify?

Is this not just a LCA? No, given a LCA, how can we incorporate this in a
software design? Mainly about lifespans.

## Notes


1. Edge and fog computing focuses on minimizing latency, but in real-time situations the latency often does not need to be as small as possible, it just means that there are deadlines that need to be met. **What gains could we get from making edge/fog computing deadline-aware?**
    1. Could SDF be used for this?
2. https://link.medium.com/iOW6q3XrLzb

Wel of niet vervangen in scope? Waarschijnlijk niet.
