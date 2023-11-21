### Commands
ip a
sudo su -
ifconfig - նաև ցույց ա տալիս ինտերֆեյսները
`netstat -rnv` ցույց ա տալիս որն ա gateway-ը
`route -n` նույնն ա ցույց տալիս ինչ որ netstat-ը
`route`
`ip route`
`route add 192.168.9.0/24 via 192.168.9.1`
`routed` - route daemon (old)
`gated` - route daemon (new)
`arp -a`
`arp -d 10.0.3.2`
`tcpdump`
`networkctl`

sftp

Նայել ինչ ինտերֆեյսներ կան կպած:
- `lshw`   (list hardware)
- `nmcli device status` (network manager CLI)
- `ls /sys/class/net/`

### NAT (network address translation)

In Linux it's called **mascarading**. 

### Additional Reading
https://linuxhint.com/route_command_linux/
route
NAT - network address translation
mascarading in Linux
Firewall
ARP - address resolution protocol
iptables
UFW - add, delete, allow, deny command options
ethtool
half duplex
