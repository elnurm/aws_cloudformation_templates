# VPC Peering

## Getting Started
Here We create VPC Peering as shown on the diagram via cloudformation stack set 

### Prerequisites
For cloudformation stack sets working properly , first of all you have to execute `AWSCloudFormationStackSetAdministrationRole.yml` and `AWSCloudFormationStackSetExecutionRole.yml` for creating proper IAM roles
You can do this with below commands:

aws cloudformation create-stack --stack-name CFStackSetAdministrationRole --template-body file://AWSCloudFormationStackSetAdministrationRole.yml


aws cloudformation create-stack --stack-name CFStackSetExecutionRole --template-body file://AWSCloudFormationStackSetExecutionRole.yml


### Creating stack set
First We have to create stack set  `peering.yml` . I chose 3 regions for testing purposes.
![Screenshot](regions.png)
After that we have to create second stack set `PEERING-RULES.yml` with the same regions.


