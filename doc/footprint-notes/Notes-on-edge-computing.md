# Notes on edge computing

1. I seem to be wrong about the second part of that claim. Edge computing is not seen as a more sustainable form of computing, it is only necessary to meet application requirements [Gill & Smith, 2018](https://www.notion.so/Gill-Smith-2018-dfb47e769f3a49f9a038e36efc310212?pvs=21)  regarding (1) data volume/bandwidth, (2) need for autonomy/disconnect (3) privacy protection, (4) local interactivity, (5) latency. [Jiang et al., 2019](https://www.notion.so/Jiang-et-al-2019-eebc84347d184f0da2cb77165da4c504?pvs=21) adds Quality of Service guarantee.
2. What about cost of ingestion? Is that ever taken into account when choosing edge compute? 
    1. According to [Trend Report: The Edge Compute Imperative, 2021](https://www.notion.so/Trend-Report-The-Edge-Compute-Imperative-2021-fc3ba87c90b04a52a551218b557e862e?pvs=21) the cost of edge computing is believed to be lower than the alternative.
3. It could be interesting to have a survey on whether IoT, edge, and cloud computing is always used correctly.
4. Do organizations move away from edge computing when latencies between endpoint and cloud improve? 
    1. What are the trends in network latency?
5. [Trend Report: The Edge Compute Imperative, 2021](https://www.notion.so/Trend-Report-The-Edge-Compute-Imperative-2021-fc3ba87c90b04a52a551218b557e862e?pvs=21) quantifies some of the reasons organizations move to edge computing:
    
    > *When asked for the latency requirements of their most mission-critical applications, 8% say 30+ milliseconds, 21% say 20 milliseconds, 44% say 10 milliseconds, and 17% say 5 milliseconds or less (Figure 19). As dynamic interaction with users or devices increases, business leaders and IT decision makers expect to require even lower latency: more than half of global IT decision makers say their most mission-critical application will require 5 milliseconds or less latency five years from now (Figure 19)*
    > 
    1. What is the latency that can be achieved by running compute on a cloud?
6. Some research is done on figuring out how to make edge computing, or the combination with cloud, more sustainable [Hu et al., 2019](https://www.notion.so/Hu-et-al-2019-934c2faad9484314b9587f46a6707788?pvs=21)
7. What is the difference between edge-compute and an on-premise server park?
    1. Edge computing is a topology. It recognizes (1) the need/usefulness of a centralized compute component, and (2) the usefulness of compute near the sensors, actuators, and other edge devices. The on-premise server park can serve as the “core” for edge computing just as well as a public cloud provider.
    This means that the same advantages and disadvantages hold for an on-premise core as for on-premise server park, like the degree of sustainability.
8. There are some terms that need to be clearly understood in this domain [[Gill & Smith, 2018](https://www.notion.so/Gill-Smith-2018-dfb47e769f3a49f9a038e36efc310212?pvs=21) ]:

    
    ![From [Gill & Smith, 2018](https://www.notion.so/Gill-Smith-2018-dfb47e769f3a49f9a038e36efc310212?pvs=21) ](Notes-on-edge-computing/gartner-edge-computing.png)
    
    
    | Term | Description | Examples |
    | --- | --- | --- |
    | IoT | The capability of many small, sometimes battery powered devices, to directly connect to the internet | RaspberryPi-based devices, Arduino based devices, or similar |
    | Core, (Center) Cloud compute | A centralized data center owned by an enterprise, a service provider or a cloud provider. Gill & Smith, 2018 (https://www.notion.so/Gill-Smith-2018-dfb47e769f3a49f9a038e36efc310212?pvs=21)  | Azure, AWS, Google cloud, but also smaller datacenters |
    | Edge | The physical location where things and people connect with the networked digital world. Gill & Smith, 2018 (https://www.notion.so/Gill-Smith-2018-dfb47e769f3a49f9a038e36efc310212?pvs=21) 
     |  |
    | Endpoint | The networked devices that interact with the edge and connect, perhaps indirectly, with the core. | IoT devices, laptops, mobile phones |
    | Edge computing | A part of a distributed computing topology in which information processing is located close to the edge — where things and people produce or consume that information. Gill & Smith, 2018 (https://www.notion.so/Gill-Smith-2018-dfb47e769f3a49f9a038e36efc310212?pvs=21) 
    Lumen defines edge compute as the delivery of technology services—from data processing, storage, security services and other application services—delivered from a low-latency location near the point of digital interaction. An edge location can be on-premises or at a nearby service location—as long as it is close enough to impose less than 10 milliseconds of data transfer latency. Trend Report: The Edge Compute Imperative, 2021 (https://www.notion.so/Trend-Report-The-Edge-Compute-Imperative-2021-fc3ba87c90b04a52a551218b557e862e?pvs=21)  |  |
    | Fog compute | Fog computing is a layered model for enabling ubiquitous access to a shared continuum of scalable computing resources. The model facilitates the deployment of distributed, latency-aware applications and services. […] Fog computing minimizes the request-response time
    from/to supported applications, and provides, for the end-devices, local computing resources and,
    when needed, network connectivity to centralized services. Iorga et al., 2018 (https://www.notion.so/Iorga-et-al-2018-91b7128306cd468cb578c494216c624c?pvs=21)
    As such, fog computing is a form of edge computing, but it only makes sense when there are many edge devices and great needs for signal fusion. | From (https://www.spiceworks.com/tech/edge-computing/articles/what-is-fog-computing/):
    * Smart homes / buildings
    * Smart cities
    * Video surveilance
    * Healthcare
    From (https://blog.swim.ai/2017/differentiate-edge-computing-part1)
    * Smart transportation |
    | Fog node | The fog nodes are context aware and support a
    common data management and communication system. They can be organized in clusters - either
    vertically (to support isolation), horizontally (to support federation), or relative to fog nodes’
    latency-distance to the smart end-devices. Iorga et al., 2018 (https://www.notion.so/Iorga-et-al-2018-91b7128306cd468cb578c494216c624c?pvs=21)  |  |
    | Mist computing | Fog computing but with low computational resources. |  |
    | Mobile edge compute (MEC) |  |  |
    
    ![From [Iorga et al., 2018](https://www.notion.so/Iorga-et-al-2018-91b7128306cd468cb578c494216c624c?pvs=21) ](Notes-on-edge-computing/fog-computing.png)
    
    From [Iorga et al., 2018](https://www.notion.so/Iorga-et-al-2018-91b7128306cd468cb578c494216c624c?pvs=21)