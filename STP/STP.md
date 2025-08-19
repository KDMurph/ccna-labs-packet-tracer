STP



broadcast storm - looped broadcast frames

mac address flapping - switch keeps updating mac address table



802.1D 

switches run STP by default

places redundant ports in blocking state

interfaces act as backups that can enter forwarding state if active int fails

blocking state- only send/receive STP messages (BPDUs = Bridge Protocol Data Units)



Hello BPDU



switches use Bridge ID field to elect root bridge

switch with *lowest* Bridge ID becomes root bridge

all ports on root bridge are in forwarding state, other switches must have path to root bridge

lowest mac is root bridge



PVST - Per-VLAN Spanning Tree



bridge priority can only be changed in units of 4096



root bridge ports - designated ports - forwarding

switches assume they are root bridge until they receive lower bridge ID



remaining switches - one int is its root port, lowest root cost, in forwarding state



speed    STP cost

10 mbps - 100

100 mbps - 19

1 gbps - 4

10 gbps - 2



show spanning-tree



neighbor port ID used to break tie

