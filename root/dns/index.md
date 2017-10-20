# The browser looks for how to contact google.com

Internet is a giant network of interconnected machines, mainly "routers" that "route" packets to the "next hop" to reach the destination. But machines does not use "google.com" as addresses : those representations are for humans. Instead, machines use IP addresses, on which they can perform operations to know how to route the packet. [go deeper](../common/networking/L3/ip_routing/index.md)

So your browser needs to know what is the IP addresse corresponding to "google.com". This is called a "domain name resolution". Here are the different steps involved :


- Browser checks if the domain is in its cache. (to see the DNS Cache in Chrome, go to chrome://net-internals/#dns).
- If not found, the browser calls `gethostbyname` library function (varies by OS) to do the lookup. [explore](./gethostbyname/index.md)
- Now that your computer has the IP address for google.com, it can access that host. [see what's next](../request/index.md)
