# OSI model

The Open Systems Interconnection model (OSI model) is a conceptual model that characterizes and standardizes the communication functions of a telecommunication or computing system without regard to their underlying internal structure and technology. Its goal is the interoperability of diverse communication systems with standard protocols. The model partitions a communication system into abstraction layers. The original version of the model defined seven layers.

A layer serves the layer above it and is served by the layer below it. For example, a layer that provides error-free communications across a network provides the path needed by applications above it, while it calls the next lower layer to send and receive packets that comprise the contents of that path. Two instances at the same layer are visualized as connected by a horizontal connection in that layer.

The model is a product of the Open Systems Interconnection project at the International Organization for Standardization (ISO), maintained by the identification ISO/IEC 7498-1.


# The layers

| # | Layers        | Protocol data unit (PDU)      | Function  | Example protocols |
| -- | ------------- |-------------| -----| --- |
| 7 | Application | Data | High-level APIs, including resource sharing, remote file access | HTTP, FTP, DNS, SNMP |
| 6  | Presentation  | Data  | Translation of data between a networking service and an application; including character encoding, data compression and encryption/decryption  | SSL, TLS  |
| 5  | Session  | Data  | Managing communication sessions, i.e. continuous exchange of information in the form of multiple back-and-forth transmissions between two nodes  | PPTP, L2TP  |
| 4 | Transport  | Segment (TCP) / Datagram (UDP)  | Reliable transmission of data segments between points on a network, including segmentation, acknowledgement and multiplexing  | TCP, UDP  |
| 3  | Network   | Packet  | Structuring and managing a multi-node network, including addressing, routing and traffic control  | IP, ARP, ICMP, IPSec  |
| 2  | Data link  | Frame  | Reliable transmission of data frames between two nodes connected by a physical layer  | PPP, ATM, Ethernet, WiFi 802.11  |
| 1  | Physical  | Bit  | Transmission and reception of raw bit streams over a physical medium  | Ethernet, USB, Bluetooth, WiFi 802.11  |


Each layer payload is encapsulated into its lower layer unit :

![](encapsulation.jpg)
