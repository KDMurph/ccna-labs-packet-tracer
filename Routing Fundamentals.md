Routing Fundamentals



routing is the process routers use to determine the path ip packets take over the network

routers store routes in a routing table

use routing tables to find the best route



dynamic routing- share routing info with each other automatically

static routing- manually configured



show ip route

L- local, route to actual ip address config on int

C- connected, route to the network the int is connected to

when int is config with ip address and no shut, 2 routes automatically added to routing table



route matches a packet's destination if the packet's destination ip address is part of the network specified in the route



router will use **most specific** route

local route- to keep the packet



most specific matching route = the matching route with the **longest prefix length**





