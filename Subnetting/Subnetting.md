Subnetting



Class:

A - 0-127

B - 128-191

C - 191-223

D - 224-239

E - 204-255



IANA assigns companies ipv4 address/networks



2 to the power of x = subnet calculator



Class C

Prefix     Number of Subnets     Hosts

/25              2                126

/26              4                62

/27              8                30

/28             16                14

/29             32                6

/30             64                2

/31             128               0 (2)

/32             256               0 (2)



VLSM

Variable-Length Subnet Masks

subnets of different sizes



Lab 15:



R1: G0/0- 192.168.5.190 255.255.255.192

G0/1 - 192.168.5.126 255.255.255.128



G0/0/0- 192.168.5.226 255.255.255.252



R2: G0/0- 192.168.5.206 255.255.255.240

G0/1 - 192.168.5.222 255.255.255.240



G0/0/0- 192.168.5.225 255.255.255.252



PC1: 192.168.5.129

PC2: 192.168.5.1

PC3: 192.168.5.193

PC4: 192.168.5.209



Example- 172.30.0.0/16, need 100 subnets with 500 hosts per subnet



**To find usable hosts:**

2^h - 2

2^9 - 2 = 510 (over 500 hosts)



9 host bits

32-9= /23



**Subnet number:**

/23-/16= 7

2^7 = 128 (over 100 subnets)



**Block size:**

Example- 255.255.240.0

256-240=16

Subnets jump by 16



**Prefix length:**

Host bits + original prefix length





**Network:**

Increments of block size



**Broadcast:**

Network octet + (block size-1)

