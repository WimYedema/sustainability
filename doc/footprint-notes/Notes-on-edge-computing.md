# Notes on edge computing

1. I seem to be wrong about the second part of that claim. Edge computing is not seen as a more sustainable form of computing, it is only necessary to meet application requirements {cite:t}`gill2018edge`  regarding (1) data volume/bandwidth, (2) need for autonomy/disconnect (3) privacy protection, (4) local interactivity, (5) latency. {cite:t}`jiangComputationOffloadingEdge2019` adds Quality of Service guarantee.
2. What about cost of ingestion? Is that ever taken into account when choosing edge compute? 
    1. According to {cite:t}`TrendReportEdge2021` the cost of edge computing is believed to be lower than the alternative.
3. It could be interesting to have a survey on whether IoT, edge, and cloud computing is always used correctly.
4. Do organizations move away from edge computing when latencies between endpoint and cloud improve? 
    1. What are the trends in network latency?
5. {cite:t}`TrendReportEdge2021` quantifies some of the reasons organizations move to edge computing:
    
    > *When asked for the latency requirements of their most mission-critical applications, 8% say 30+ milliseconds, 21% say 20 milliseconds, 44% say 10 milliseconds, and 17% say 5 milliseconds or less (Figure 19). As dynamic interaction with users or devices increases, business leaders and IT decision makers expect to require even lower latency: more than half of global IT decision makers say their most mission-critical application will require 5 milliseconds or less latency five years from now (Figure 19)*
    > 
    1. What is the latency that can be achieved by running compute on a cloud?
6. Some research is done on figuring out how to make edge computing, or the combination with cloud, more sustainable {cite:t}`huEdgeCentralCloud2019`
7. What is the difference between edge-compute and an on-premise server park?
    1. Edge computing is a topology. It recognizes (1) the need/usefulness of a centralized compute component, and (2) the usefulness of compute near the sensors, actuators, and other edge devices. The on-premise server park can serve as the “core” for edge computing just as well as a public cloud provider.
    This means that the same advantages and disadvantages hold for an on-premise core as for on-premise server park, like the degree of sustainability.
8. There are some terms that need to be clearly understood in this domain [{cite:t}`gill2018edge` ]:

    
    ![From {cite:t}`gill2018edge` ](Notes-on-edge-computing/gartner-edge-computing.png)
    
    ```{list-table}
    :header-rows: 1
    * - Term
      - Description
      - Examples
    * - IoT
      - The capability of many small, sometimes battery powered devices, to directly connect to the internet
      - RaspberryPi-based devices, Arduino based devices, or similar
    * - Core, (Center) Cloud compute 
      - A centralized data center owned by an enterprise, a service provider or a cloud provider. Gill & Smith, 2018 {cite:t}`gill2018edge`
      - Azure, AWS, Google cloud, but also smaller datacenters
    * - Edge
      - The physical location where things and people connect with the networked digital world. Gill & Smith, 2018 {cite:t}`gill2018edge`
      - 
    * - Endpoint
      - The networked devices that interact with the edge and connect, perhaps indirectly, with the core.
      - IoT devices, laptops, mobile phones.
    * - Edge computing
      - A part of a distributed computing topology in which 
        information processing is located close to the edge - where 
        things and people produce or consume that information. 
        {cite:t}`gill2018edge`.

        Lumen defines edge compute as the delivery of technology services—from data processing, 
        storage, security services and other application services—delivered from a low-latency 
        location near the point of digital interaction. An edge location can be on-premises or at
        a nearby service location—as long as it is close enough to impose less than 10 milliseconds
        of data transfer latency. {cite:t}`TrendReportEdge2021`
      - 
    * - Fog compute 
      - Fog computing is a layered model for enabling ubiquitous access to a shared continuum of 
        scalable computing resources. The model facilitates the deployment of distributed, 
        latency-aware applications and services. […] Fog computing minimizes the request-response
        time from/to supported applications, and provides, for the end-devices, local computing
        resources and, when needed, network connectivity to centralized services. 
        ({cite:t}`iorgaFogComputingConceptual2018`)
    
        As such, fog computing is a form of edge computing, but it only makes sense when there are
        many edge devices and great needs for signal fusion. 
      - From (https://www.spiceworks.com/tech/edge-computing/articles/what-is-fog-computing/):
        * Smart homes / buildings
        * Smart cities
        * Video surveilance
        * Healthcare

        From (https://blog.swim.ai/2017/differentiate-edge-computing-part1)
        * Smart transportation
    * - Fog node
      - The fog nodes are context aware and support a common data management and communication 
        system. They can be organized in clusters - either vertically (to support isolation), 
        horizontally (to support federation), or relative to fog nodes’ latency-distance to the
        smart end-devices. ({cite:t}`iorgaFogComputingConceptual2018`)
      -
    * - Mist computing
      - Fog computing but with low computational resources.
      -
    * - Mobile edge compute (MEC)
      -
      -
    ```
    
    ![From {cite:t}`iorgaFogComputingConceptual2018` ](Notes-on-edge-computing/fog-computing.png)
    
    From {cite:t}`iorgaFogComputingConceptual2018`