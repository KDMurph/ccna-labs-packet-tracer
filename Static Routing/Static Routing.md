Static Routing

to send packets outside of LAN, need to send them to default gateway



default gateway = default route

route to 0.0.0.0/0

least specific route possible



need two-way reachability



Router(config)# ip route *ip-address netmask next-hop*



ip route *ip address netmask exit-interface*

ip route *ip address netmask exit-interface next-hop*



default route command

ip route 0.0.0.0 0.0.0.0 *next-hop*

