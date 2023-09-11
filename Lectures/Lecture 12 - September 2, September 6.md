# 7 Layers of the OSI Model

## Physical layer
- Physical structure
- Coax, Fiber, Wireless, Hubs, Repeaters

All devices in the physical layer have MAC addresses (which should be unique). 

**vLAN - virtual local area network** - read about this for homework

IP is a unique identifier for every device.

## Data Link layer
- Frames
- Ethernet, PPP, Switch, Bridge

## Network layer
- Packets
- IP, ICMP, IPSec, IGMP

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
  - class C - 10.10.0.0/8, 192.168.0.0/16, 172.16.0.0/16- private IPs
- **IPv6**

## Transport layer
- End-to-end encryption
- TCP, UDP

## Session layer
- Synch & send to port
- APIs, Sockets, WinSock

Socket is a port. Maximum number of ports on the same IP is 65536.
Ports under 3000 are often used by other protocols, so it's recommended to use ports >3000 for your application.

## Presentation layer
- Syntax layer
- SSL, SSH, SCP IMAP, FTP, MPEG, JPEG

SSL (secure socket layer) does web traffic encryption. - 443 port
**mtls - advanced version of TLS. ???**

SSH (Secure SHell) - 22 port

SCP (secure copy) - 22 port

IMAP and POP protocols - used for emails 

SMTP - used for sending emails

FTP, sFTP (file transfer protocol) - 21 port


## Application layer
- End user layer
- HTTP, FTP, IRC, SSH, DNS


# Additional reading

IANA
subnet
dual stack
NAT - network address translation
packets
**openswan and strongswan** - read about this for homework
**vLAN - virtual local area network** - read about this for homework
curl command