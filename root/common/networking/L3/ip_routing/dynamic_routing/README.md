Dynamic Routing

Maintaining IP routing tables on small networks do not require much administrative effort; once the network is setup and static routes have been added there isn’t much else to do. On large networks however, the network topology is constantly changing; new subnets are added, faster routes learnt, subnets are joined or further subnetted. Updating the routers to reflect this every time a change occurs can be a chore in itself.

This is where dynamic routing comes in. In static routing the administrator manually creates the routes, but in dynamic routing the routes are “learnt” and built automatically by the routers themselves. Dynamic routing allows routers to “talk” to each other to find where other networks are located. When the network topology changes so do the dynamic routes. When routers go down or faster routes become available dynamic routing also detects this and reconfigures the IP routing table accordingly.

Dynamic routing is implemented using IP routing protocols. Some of the more common ones are RIP, OSPF and BGP.
