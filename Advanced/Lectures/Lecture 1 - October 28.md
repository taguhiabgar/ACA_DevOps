Download MTU for mac m1 - virtualization tool



## Virtualization
run robin algorithm
fault tolerance - near zero downtime - almost impossible to achieve in reality
horizontal scaling, vertical scaling
load balancer
-api call, endpoint
disaster recovering - rto (how much time is needed to recover the infrastructure), rpo




## Additional reading
RDS
web server (nginx, apache, ...) բարձրացնել - static content
php fpm
http protocol, http1 vs http2
tcp/ip protocol
http methods
proxy pass / reverse proxy
redirect, how to redirect
webpack
terraform cdk

raid types - 0, 1, 10, 5, 6
elastic search

stickiness in load balancers


AWS SQS - simple queue service



## Homework
make 3 different virtual machines with ubuntu 22.04 server, not desktop
v1 - index.html with name of server
v2 - index.html with name of server
v3 - load balancer, nginx (nginx should work as a load balancer) (upstream)

etc contains applications configs
cd /etc/nginx/
nginx default.conf specifies which html file to read, among many other configs

create bridge in virtualbox so that they are all in the same network

servers should be stateless - not saving any data or state
session, token - can be saved in browser cookies, database (not recommended), memcache

how does nginx work
nginx upstream



redis saves data in memory - which means in RAM
redis dump - incremental dump and full dump
