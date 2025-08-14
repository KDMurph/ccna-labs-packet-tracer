native vlan on a router

2 methods:

* encapsulation dot1q *vlan-id* native on subint
* configure IP for native vlan on router's physical interface



layer 3 switch

* can create virtual interfaces for each VLAN and assign addresses to those interfaces
* SVI - switch virtual interfaces
* configure pcs to use SVI as gateway rather than router



commands:

default int g0/0 - sets to default settings

**ip routing** - enables layer 3 routing on switch

int g0/1

no switchport

ip add



ip route 0.0.0.0 0.0.0.0 *next-hop (router ip)*



SVIs:

int vlan10

ip add

no shut



vlan must already exist for SVIs

switch must have one access port in vlan in up/up AND/OR one trunk port that allows the vlan in up/up

vlan must not be shutdown

SVI must be up

