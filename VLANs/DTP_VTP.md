DTP/VTP



dynamic trunking protocol

* cisco proprietary protocol that allows switches to dynamically determine if int is access or trunk
* enabled by default
* for security- manual config and dtp should be disabled
* will not form a trunk with router, PC, etc



switchport mode dynamic

auto - will NOT actively try to form a trunk, but will form a trunk if the connected switch is actively trying

modes:

* trunk
* dynamic desirable

desirable- will actively try to form a trunk with other cisco switches if switchports in following modes:

* trunk
* dynamic desirable
* dynamic auto



show int g0/0 switchport



static access- access port that belongs to single vlan that doesn't change

dynamic access- server automatically assigns the vlan depending on the mac of connected device



to disable: switchport nonegotiate



switchport trunk encapsulation negotiate



vlan trunking protocol

* allows config of vlans on a central VTP server switch, and other switches (VTP clients) will sync their vlan database to the server
* designed for large networks with many vlans so you don't have to config each vlan on every switch 
* rarely used, recommended to not
* 3 versions: 1, 2, 3
* 3 modes: server, client, transparent
* cisco switches operate in server mode by default



VTP servers:

* can add/modify/delete vlans
* database stored in NVRAM
* revision number increased every time a vlan is added/modified/deleted
* advertise latest version on trunk int
* VTP servers also function as VTP clients
* VTP server will sync to another VTP server with higher revision number



VTP clients:

* cannot add/modify/delete vlans
* does not store vlan db in NVRAM (except VTPv3)
* will sync their vlan db to highest revision number in their VTP domain
* advertise their vlan db and forward advertisements to other clients over trunk ports



show vtp status

vtp domain *cisco*

vtp mode client

vtp mode transparent

vtp version #



danger of VTP:

* if you connect old switch with higher revision number to network (and domain name matches), all switches will sync vlan db to that switch



VTP transparent:

* does not participate in VTP domain (does not sync)
* has own vlan db- can modify vlans but will not advertise
* will forward VTP advertisements from same domain
* changing mode to transparent will reset revision number to 0



changing VTP domain to unused domain will reset revision number to 0

















