SSH Proxies
===========

Make a proxy to another server:

    ssh -f -N -L <your port>:<remote host from remote>:<remote port from remote> <user>@<remote host> 

For example, to connect from my laptop/desktop to a server foo:

    ssh -f -N -L 33060:Stagedb04b:3306 ktrue@foo 

Or to connect to an EC2 instance running tinyproxy:

    ssh -f -N -L 7777:localhost:8888 -i $EC2_RSAKEYPAIR ubuntu@ec2-107-20-2-131.compute-1.amazonaws.com 

Or to connect to an EMR cluster:

    ssh -N -L 9100:localhost:9100 -L 9101:localhost:9101 hadoop@ec2-23-23-34-233.compute-1.amazonaws.com
