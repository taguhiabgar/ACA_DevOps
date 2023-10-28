# Disk/Storage Management

NFS - Network file system - works only with network
S3 - Amazon service storage
HDD - hard disk drive - slow
SSD - solid state drive
NvME
NvMESSD


RAID - redundant array of independent disk - guarantees fault tolerance
RAID Levels 0, 1, 5, 10 (1+0)

LVM - linux volume manager - fault tolerant

fdisk - utility for working with disks


# Commands
`swapon`
`dd if=/dev/zero ...`
`du -sh /filename`
`mkswap /filename`
`swapoff /filename`
`ls /dev/sd`
`df -h`
`lshw`
`mkfs`

`pvcreate` - physical volume create

`vgcreate` - volume group create
`vgextend` - add volume to group

`lvcreate` - logical volume create

file /etc/fstab






#### Additional reading
mount
**iostat - to compare read/write speed on disk**







