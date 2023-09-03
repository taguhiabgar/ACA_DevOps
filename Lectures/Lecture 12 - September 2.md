# 7 Layers of the OSI Model
## Network layer

### ICMP
`ping google.com`

Used by network switches.
ICMP does not have port, all other protocols have ports.

Packet has headers and body, in headers (?) is specified the source and destination.

Each router takes the packet and changes the destination in the header.

![[Screenshot 2023-09-02 at 13.17.02.png]]



### IGMP
protocol for routers 

### IP
internet protocol 

Versions:
- **IPv4**
  x.x.x.255 - broadcast
  x.x.x.1 - multicast
  Has 3 types:
  - class A - corporate - public IPs
  - class B - public IPs
  - class C - 10, 192, 172- private IPs
- **IPv6**



# Additional reading

IANA
subnet
dual stack
NAT - network address translation
packets