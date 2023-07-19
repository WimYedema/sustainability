# Literature on edge computing

* {cite:t}`gill2018edge`
* {cite:t}`jiangComputationOffloadingEdge2019`
* {cite:t}`TrendReportEdge2021`
* {cite:t}`huEdgeCentralCloud2019`
* {cite:t}`machMobileEdgeComputing2017`

## Summary

Edge computing is not seen as a more sustainable form of computing, it is only
necessary to meet application requirements regarding{cite}`gill2018edge`: 
* data volume/bandwidth, 
* need for autonomy/disconnect, 
* privacy protection, 
* local interactivity,
* latency, and 
* Quality of Service guarantee{cite}`jiangComputationOffloadingEdge2019`.

## Comparison with on-premise computing

Edge computing is a topology. It recognizes (1) the need/usefulness of a
centralized compute component, and (2) the usefulness of compute near the
sensors, actuators, and other edge devices. The on-premise server park can serve
as the “core” for edge computing just as well as a public cloud provider. This
means that the same advantages and disadvantages hold for an on-premise core as
for on-premise server park, like the degree of sustainability.

## Comparison with compute offloading

Compute offloading seems to be studied most for *mobile edge computing*
{cite:t}`jiangComputationOffloadingEdge2019`(section A). Also according to that
paper:

> Due to the bandwidth fluctuations in wireless environments, static application
> partitioning is not suitable for mobile platforms with fixed bandwidth, while
> dynamic program partitioning will result in high overheads.

Later:

> Computation offloading is regarded as an effective way to guarantee user
> service quality by offloading the compute-intensive or latency-sensitive tasks
> to the edge devices or nearby edge servers {cite}`machMobileEdgeComputing2017`

It seems that most computation offloading is done just-in-time.

## Questions

1. Do organizations move away from edge computing when latencies between
   endpoint and cloud improve? 
2. What are the trends in network latency?
3. What is the latency that can be achieved by running compute on a cloud?