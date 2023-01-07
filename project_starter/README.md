### Project Title - Deploy a high-availability web app using CloudFormation
This folder provides the code for the "ND9991 - C2- Infrastructure as Code - Deploy a high-availability web app using CloudFormation" project. This folder contains the following files:


#### Udagram-network.yml
the CloudFormation code using this YAML template for building the network infrastructuret including: VPC, Subnets, InternetGateway, NatGatway, RouteTable... 

#### Udagram-server.yml
the CloudFormation code using this YAML template for building the server infrastructuret including: SecurityGroup, InstanceProfile, LaunchConfiguration, AutoScalingGroup, LoadBalancer, TargetGroup ... 

#### network-params.json
JSON file for increasing the generic nature of the YAML code. For example, the JSON file contains a "ParameterKey" as "EnvironmentName" and "ParameterValue" as "UdagramProject". 

#### server-params.json
JSON file for increasing the generic nature of the YAML code.

In YAML code, the `${EnvironmentName}` would be substituted with `UdagramProject` accordingly.