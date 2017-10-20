# how a machine sends a message to another machine with ip address

When a machine knows the IP address of the destination (Layer 3 of the OSY model), it needs to get its "Layer 2" address. This is where the ARP protocol comes ino play (Address Resolution Protocol).

- The "ARP" cache is first checked for an ARP entry for our target IP. If it is in the cache, the library function returns the result: Target IP = MAC.
- Else, the machines perform an ARP request to receive the MAC address corresponding to the IP from the network.
