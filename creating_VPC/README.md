# There I wrote the AWS CloudFormation template to create the VPC as show in vpc_diagram.png file.


We have to create 2 key-pairs for our JumpServer and Private Server and import them to AWS
We can do it via aws cli :
Generate ssh keys via ssh-keygen
 ssh-keygen -C "jumpserver_key" -f jumpserver_key
 ssh-keygen -C "privateserver_key" -f privateserver_key

Then import them via aws cli
 aws ec2 import-key-pair --key-name jumpserver_key --public-key-material "$(cat jumpserver_key.pub)"
 aws ec2 import-key-pair --key-name privateserver_key --public-key-material "$(cat .\privateserver_key.pub)"

Then connect from Jump Server to server in the private subnet and check the internet connection.

