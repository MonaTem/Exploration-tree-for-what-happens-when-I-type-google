# how a machine sends a message to another machine with ip address

When a machine knows the IP address of the destination (Layer 3 of the OSY model), it needs to get its "Layer 2" address:

- The ARP cache is first checked for an ARP entry for our target IP. If it is in
the cache, the library function returns the result: Target IP = MAC.
-  Else, the machines perform an ARP (Address Resolution Protocol) request to receive the MAC address corresponding to the IP from the network.





Now that the network library has the IP address of either our DNS server or
the default gateway it can resume its DNS process:

* Port 53 is opened to send a UDP request to DNS server (if the response size
  is too large, TCP will be used instead).
* If the local/ISP DNS server does not have it, then a recursive search is
  requested and that flows up the list of DNS servers until the SOA is reached,
  and if found an answer is returned.
