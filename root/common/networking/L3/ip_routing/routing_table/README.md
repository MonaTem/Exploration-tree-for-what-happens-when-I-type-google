
-
The IP routing table contains information in the following columns:

# Destination

The destination is the destination host, subnet address, network address, or default route. The destination for a default route is 0.0.0.0.

# Network mask

The network mask is used in conjunction with the destination to determine when a route is used. For example, a host route has a mask of 255.255.255.255, a default route has a mask of 0.0.0.0, and a subnet or network route has a mask between these two extremes.

A mask of 255.255.255.255 means that only an exact match of the destination uses this route. A mask of 0.0.0.0 means that any destination can use this route. When a mask is written in binary, a 1 is significant (must match) and a 0 is insignificant (does not need to match).

For example, a destination of 172.16.8.0 has a network mask of 255.255.248.0. This network mask means that the first two octets must match exactly, the first five bits of the third octet must match (248=11111000), and the last octet does not matter. The third octet of 172.16.8.0 (that is, 8) equals 00001000 in binary. Without changing the first 5 bits (the masked-off portion shown in bold), you can go up to 15, or 00001111 in binary. So a route with a destination of 172.16.8.0 and a mask of 255.255.248.0 applies to all packets destined for 172.16.8.0 through 172.16.15.255.

# Gateway

The gateway is the IP address of the next router where a packet must be sent. On a local area network (LAN) link (such as Ethernet or token ring), the gateway must be directly reachable by this router by using the interface indicated in the Interface column. On a LAN link, both the gateway and interface determine how the traffic is being forwarded by the router. For a demand-dial interface, the gateway address cannot be configured. On a point-to-point link, the interface determines how the traffic is being forwarded by the router.

# Interface

The interface indicates the LAN or demand-dial interface that is to be used to reach the next router.

# Metric

The metric indicates the relative cost of using the route to reach the destination. A typical metric is hops, or the number of routers to cross to reach the destination. A metric value is basically a preference number. If there are two routes to the same destination then the one with the lowest metric is assumed to be the most efficient. Routers will always use this route first until it fails, in which case it will then try the route with the next lowest metric and so on. As a consequence, this is important to state that when packets take a certain route to their destination they DO NOT have to take the same route back.


# Protocol

The protocol shows how the route was learned. If the Protocol column lists RIP, or anything other than Local, then the router is receiving routes (this is called [dynamic routing](../dynamic_routing/))
