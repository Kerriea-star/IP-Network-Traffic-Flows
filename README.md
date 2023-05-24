# IP-Network-Traffic-Flows
#### Data Science project on Network Protocol Prediction based on IP Network Traffic Flows.

## Introductory Information

A flow consists of all <b>traffic</b> that belongs to the same communication context, basically, <b>IP data packets</b> that belongs to the same connection. While IP is completely packet based and has no nortion of connection, chances are applications that communicate with each other using IP will exchange in general more than one packet when they start communicating.

For example, a file transfer application breaks the file to be transferred into several individual packets. All packets are for the same transfer and need to be delivered over a network and may <b>"flow"</b> over the same router. The same applies for an image that is to be transfered for viewing a web page or a <b>Voice over IP</b> conversation carried out between two users. This way, when a router sees one packet passing over from one point to a certain destination, chances are there may be more coming . A flow ,may as well consist of only a single packet transfer.

Statistical information about IP-based data traffic that <b>"flows"</b> over a router is communicated by <b>Netflow</b>. The statistics are provided on a <b>per-flow</b> basis.

A flow is uniquely identified by the following pieces of information

    * Source Address
    * Source Port
    * Destination Address
    * Destination Port
    * Protocol type (for example whether the packet carries TCP or UDP)
    * Input logic Interface (identified by the same index that is used for the interface in SNMP MIBs; this is needed because, in           addition to the source address and port, in the case of private networks with private IP address spaces, the other pieces of           information might not be unique to one flow)
    * Knowing how much traffic of what type was sent at what time from where to where allows network managers to account for detailed       network use by individual users. This is important if a network provider wants to charge based on actual traffic consumption           instead of charging simply a flat access fee. As traffic flows across multiple routers, the network provider must be sure to           avoid double-counting the same traffic on multiple counters. This can be ensured by correlating flow records that are collected       on multiple routers, or by taking into account only the flow records generated by the access router through which a particular         user is known to connect to the rest of the network
    * It provides a wealth of data for traffic analysis, bottleneck, and network planning.
    * It can provide an invaluable tool to spot and defend against attacks on a network that carry certain characteristics in terms of       the traffic patterns they generate.

## Data

The dataset is based on IP Network Flows labelled by 75 apps. It was collected in a network section from Universidad Del Cauca, Popayán, Colombia by performing packet captures at different hours during morning and afternoon for six days. A total of 3577296 instances were collected and stored in a csv file.
Content of the Dataset

The dataset contains 87 features. Each instance contains information of an IP flow generated by a network device, i.e., source and destination IP address, ports, interarrival times, layer 7 protocol (application) used on that flow as the class e.t.c.

From this data, a Machine Learning model aimed at predicting protocol name will be created, trained and evaluated for performance. The dataset will be thoroughly cleaned to ensure high accuracy and great performance of the model on new data.
