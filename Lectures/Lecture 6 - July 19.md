### Commands

`visudo`

`sudo fsck` - fsck is for filesystem check

`groupadd root_group`

`ufw status` - firewall

### Files

**/etc/sudoers.tmp**
in this file, change 

`# User privilege specification`
`root    ALL=(ALL:ALL) ALL` (after *root* there should be a tab in this line)
`sergey    ALL=(ALL:ALL) NOPASSWD:ALL` (after *sergey* there should be a tab in this line)


`# Allow members of group sudo to execute any command`
`sudo    ALL=(ALL:ALL) ALL` (after *sudo* there should be a tab in this line)
`root_group    ALL=(ALL:ALL) NOPASSWD:ALL` (after *root_group* there should be a tab in this line)

### systemctl, systemd

**who, w, id, last** commands 

`date` command - shows date and time
`cal` - calendar, install with the instructions if needed
`uptime` - when was the server started, shows load average with 3 numbers: average in 1, 5 and 10 minutes
`htop` 
`hostname` - is read from /etc/hostname, to see it, do `cat /etc/hostname`, can be changed from this file, but will need a reboot
otherwise, can be changed this way:
`hostnamectl set-hostname -H NEWHOSTNAME`

`init` is the first process. `systemd` is a part of `init`. `systemctl` is a wrapper over `systemd`.

`systemctl enable nginx`
on startup, nginx will run

to prevent this:
`systemctl disable nginx`

to start the process
`systemctl start nginx`

to stop the process
`systemctl stop nginx`

to restart the process
`systemctl restart nginx`

to reload the process (reads from the config file):
`systemctl reload nginx`

to understand if nginx is enabled:
`systemctl is-active nginx`

to understand if nginx is started:
`systemctl is-enabled nginx`

to understand if nginx is failed:
`systemctl is-failed nginx`

