STP PT2



blocking

listening

learning 

forwarding



listening/learning - transitional states, passed through when int is activated or when Blocking port must change to Forwarding



blocking

* non-designated ports
* disabled to prevent loops
* do not send/receive reg network traffic
* receive STP BPDUs but do not forward 
* do not learn macs



listening

* after blocking state, int with Designated or Root role enter Listening
* Listening state is 15 sec long, determined by Forward delay timer
* only forwards/receives STP BPDUs
* does not send/receive reg traffic
* does not learn macs



learning

* after listening, Designated or Root port will enter learning
* 15 sec long, determined by Forward delay timer
* only sends/receives STP BPDUs
* does not send/receive reg traffic
* will learn macs from reg traffic



switches do not forward BPDUs out of root ports and non-designated ports, only designated ports



STP toolkit

* Portfast- allows port to move to Forwarding, end hosts only
* BPDU Guard- if int receives BPDU from another switch, int will be shut down
* Root guard- even if int receives lower bridge ID BPDU, will not accept new switch as root bridge
* Loop guard- even if int stops receiving BPDUs, it will not start forwarding, int will be disabled



Spanning Tree mode

* mst - multiple
* pvst - per vlan
* rapid-pvst - per vlan rapid



STP Load-Balancing



commands:

spanning-tree portfast

spanning-tree portfast default - enables on all access ports

spanning-tree bpduguard enable

spanning-tree portfast bpduguard default - enables on all Portfast enabled ints

spanning-tree mode pvst

spanning-tree vlan *number* root primary

spanning-tree vlan *number* root secondary

do sh spanning-tree

spanning-tree vlan 1 cost

spanning-tree vlan 1 port-priority

sh spanning-tree int *int-name* detail

