# Notes on IOT

More related papers:

- Google Scholar:
    
    [](https://scholar.google.com/scholar?q=green+edge+computing)
    

This is an active area of research. There seem to be several proposals, how effective are they, and are they used anywhere?

# Terms

:SCADA: supervisory control and data acquisition. A category of software
applications for controlling industrial processes, which is the gathering of
data in real time from remote locations in order to control equipment and
conditions. 

# Considerations and Observations

1. CAP theorem
([https://en.wikipedia.org/wiki/CAP_theorem](https://en.wikipedia.org/wiki/CAP_theorem))
In a distributed system one has to choose 2 out of the 3 of **consistency**,
**availability**, and **partition tolerance**. In the presence of network
partitions (compute nodes being in a different subnet, like edge compute and
cloud compute) one has to choose between *consistency*, returning an error or
time-out in case of failure, and **availability**, returning the latest value in
case of failure.
2. Azure IOT edge
   ([https://azure.microsoft.com/en-us/products/iot-edge/#iotedge-overview](https://azure.microsoft.com/en-us/products/iot-edge/#iotedge-overview))
   offers compute for a on-premise server with container support. Not the actual
   edge devices (not this service at least)
3. There are a number of choices for IoT connectivity:
    1. OpenConnectivity.org [OPEN CONNECTIVITY FOUNDATION (OCF)](https://openconnectivity.org/)
       With reference implementation: [Architecture](https://iotivity.org/architecture/)
       Another standard with implementation they’ve defined [Home](https://github.com/alljoyn/alljoyn.github.com/wiki)
        
    2. OPC Foundation for **Industry 4.0** [Home Page - OPC Foundation](https://opcfoundation.org/)
       With specifications: [Documents - OPC Foundation](https://opcfoundation.org/developer-tools/documents/?type=Specification)
       Introduction: [What is OPC UA? A practical introduction](https://www.opc-router.com/what-is-opc-ua/)
       