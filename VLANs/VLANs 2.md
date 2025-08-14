switches tag all frames that are sent over a trunk link so that it knows which VLAN the frame belongs to



trunk ports = tagged ports

access ports = untagged ports



ISL inter-switch link - Cisco proprietary protocol old



802.1Q



tag is between Source and Type fields of ethernet frame 

TPID- Tag Protocol Identifier

TCI- Tag Control Information 

VID- VLAN ID



range of usable VLANs 1-4094



normal vlans - 1-1005

extended vlans - 1006-4094



native vlan - 1 

switch does not add tag to frames in native vlan

best to change it to an unused VLAN



router on a stick (roas)

sub-interfaces:

int g0/0

no shut

int g0/0.10

encapsulation dot1q *vlan #*

ip address



recommended for sub-interface number to match vlan



commands:

switchport trunk encapsulation dot1q

switchport mode trunk

show int trunk

switchport trunk allowed vlan

* WORD- VLAN IDs of the allowed VLANs when port is in trunking mode
* add- add VLANs to current list
* all
* except- all VLANs except the following
* none
* remove

switchport trunk native vlan *#*



