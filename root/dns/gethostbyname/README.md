# The OS function `gethostbyname` does the IP lookup (domain name resolution)


- `gethostbyname` checks if the hostname resolution is in its cache
- `gethostbyname` checks if the hostname can be resolved by reference in the local "hosts file" (whose location varies by OS). This file is a local file that enables an admin to locally define some [domain name]-[IP address] correspondance.
- If `gethostbyname` does not have it cached nor can find it in the hosts file then it makes a request to the "DNS" server configured in the network stack. DNS servers (for Domain Name System) are like the white pages directory of the internet. [go deeper in the DNS query](./name_servers/index.md)
