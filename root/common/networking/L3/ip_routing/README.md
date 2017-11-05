- Routing is the process of forwarding IP packets from one network to another.
- A router is a device that joins networks together and routes traffic between them.
- When a router receives a frame (L2 layer) :
  - check if the frame is correct. If not, drop the frame.
  - De-encapsulate the IP packet from the frame, and discard the Ethernet (or other) frame.
  - Look for a match in the routing table for the destination IP address, figure out what the outgoing interface and optionally, the next hop IP address is. [see how](./routing_table/)
  - perform some operations to reconstruct IP header (decrease ttl, recalculate checksum)
  - encapsulate the IP packet in a new L2 frame (e.g. Ethernet)
  - Check the ARP table for the next hop IP address.
  - transmit the frame




# Internet IP Routing

The Internet routes traffic exactly the same way a private network does, but on a much larger scale with thousands of networks and routers. EVERY time a router receives a new packet it is evaluated against the routing table for a match. If it can’t find one it forwards the packet to it’s own default gateway. This process continues until eventually a router finds a match. If a router finds two matches to the same network (for redundancy) it will always favour the entry with the lowest metric value first.

The main difference between IP routing on the Internet and routing on private networks is how the routing table is built. Private networks tend to use static routing whereas the Internet uses Dynamic Routing [go deeper](./dynamic_routing/).
