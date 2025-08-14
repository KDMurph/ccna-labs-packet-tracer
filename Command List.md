**Command List**

* enable
* config t
* enable password
* exit
* running-config
* startup-config
* write
* write memory
* copy run config startup-config
* service password-encryption
* enable secret
* show int status
* int *interface*
* desc
* show int
* show int description
* no shut
* shutdown
* show mac address-table
* clear mac address-table dynamic
* clear mac address-table dynamic address *mac address*
* clear mac address-table dynamic interface *interface #*



**Routing**

* ip add *ip address subnet mask*
* show ip int brief
* show ip route
* ip route *ip-address netmask next-hop*
* ip route *ip address netmask exit-interface*
* ip route *ip address netmask exit-interface next-hop*
* ip route 0.0.0.0 0.0.0.0 *next-hop*



**VLANs**

* show vlan brief
* switchport mode access
* switchport access vlan *#*
* vlan *#*
* name
* switchport trunk encapsulation dot1q
* switchport mode trunk
* show int trunk

switchport trunk allowed vlan

* WORD- VLAN IDs of the allowed VLANs when port is in trunking mode
* add- add VLANs to current list
* all
* except- all VLANs except the following
* none
* remove

switchport trunk native vlan *#*

Router sub-interface

* int g0/.10
* encapsulation dot1q *vlan #*



