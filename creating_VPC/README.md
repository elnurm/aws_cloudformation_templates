There I wrote the AWS CloudFormation template to create the VPC as show in vpc_diagram.png file.


After creating stack with the vpc.yml file  create 2 EC2 instances. One of them will be "Jump Server", the other one is "server in the private subnet".
Then connect from Jump Server to server in the private subnet and check the internet connection.

