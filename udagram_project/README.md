### Project Title - Deploy a high-availability web app using CloudFormation
This folder provides the code for the "ND9991 - C2- Infrastructure as Code - Deploy a high-availability web app using CloudFormation" project. This folder contains the following files:

### APP URL
http://udagr-webap-e4w9egvzh9re-779544370.us-east-1.elb.amazonaws.com/

#### Udagram-network.yml
the CloudFormation code using this YAML template for building the network infrastructuret including: VPC, Subnets, InternetGateway, NatGatway, RouteTable... 

#### Udagram-server.yml
the CloudFormation code using this YAML template for building the server infrastructuret including: SecurityGroup, InstanceProfile, LaunchConfiguration, AutoScalingGroup, LoadBalancer, TargetGroup ... 

#### network-params.json
JSON file for increasing the generic nature of the YAML code. For example, the JSON file contains a "ParameterKey" as "EnvironmentName" and "ParameterValue" as "UdagramProject". 

#### server-params.json
JSON file for increasing the generic nature of the YAML code.

In YAML code, the `${EnvironmentName}` would be substituted with `UdagramProject` accordingly.

### How to run the Cloudformation?
You can run it in two easy steps:
```bash
# Ensure that the AWS CLI is configured before runniing the command below
# Create the network infrastructure
# Check the region in the create.sh file
./create.sh myFirstStack udagram-network.yml network-params.json
# Create servers
# Change the AMI ID and key-pair name in the servers.yml
# Check the region in the update.sh file
./update.sh mySecStack udagram-server.yml server-params.json