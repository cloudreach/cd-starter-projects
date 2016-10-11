Create a load balanced, autoscaled stack with port 80 open to the public.
Ec2 will communicate to the load balance via port 8080.
Use an Amazon Linux AMI.
Must use the outputs of stack vpc-dev to determine vpc and subnets programatically.