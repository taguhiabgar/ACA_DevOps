Lesson 3 homework

Create ec2 instance ans install nginx web server

Acceptance criteria:
- instances type: t2micro
- instance os ubuntu 22.04
- should be able connect  over ssh
- inbound ports on security group for ports 22, 80,443 must be open
- default volume should not be deleted after instance termination
- instance should have static public ip
- create additional 5gb disk and mount it into the instance as `/data` disk
- stop instance