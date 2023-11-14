(notes from youtube video he will send)
HTTPS handshake, certificate, sending request through HTTPS
...
The browser generates a key with the certificate and sends to the server, opens with the symmetric key.

---
## EC2 -  Elastic Compute Cloud

EC2 is a VM (virtual machine). 

EC2 calculator on AWS to calculate prices.

![[Pasted image 20231104102725.png]]

RAID-ից մի կտոր քեզ ա տալիս


EBS - Elastic Block Store



It is not recommended to use elastic IPs if you have more than one VMs.
Elastic IP is a regional resource. Elastic IP and the associated VM should be in the SAME region.


## Connecting to EC2 instance
![[Pasted image 20231104111740.png]]
click "Connect"
![[Pasted image 20231104111805.png]]

## Volumes
EBS (elastic block storage) - Block Storage Volume
One EBS can be attached to one VM.
Few EBS storages can be attached to the same VM, but one EBS is attached to only one VM.

IO1 and IO2 with specific file system can be attached to more than one VMs. But generally one volume is attached to one VM.

NFS - network file system - used in Linux.
EFS - elastic file system is Amazon's NFS.

Object storage - for object storage Amazon uses S3 bucket.

gp2 vs gp3
IOPS - input/output per second


[additional reading] volume snapshot
difference of volume snapshot and volume backup

**Reserved instance**

**Spot instances** are good to use for worker applications.


---
XFS (file system) works better with databases, especially with oracle DB.
### Additional
NAT
firewall
memcache
instance family (aws)
mount

AWS - cluster, partition, spread

AWS - snow family, snowmobile