# CloudFormation Stack: Security Group and EC2 Instance

This CloudFormation template deploys an Amazon Web Services (AWS) infrastructure consisting of a security group and an EC2 instance. The EC2 instance runs a basic web server that serves content from a GitHub repository.

## Template Description

The provided AWS CloudFormation template creates the following resources:

- **Security Group (MySecurityGroup)**: This security group allows inbound SSH (port 22) and HTTP (port 80) traffic from any IP address (0.0.0.0/0).

- **EC2 Instance (MyInstance)**: An Amazon EC2 instance of type t2.micro is launched with Amazon Linux 2 (AMI ID: ami-0f34c5ae932e6f0e4). The instance is associated with the MySecurityGroup security group. The user data script installs and configures an Apache HTTP server (`httpd`) and clones a GitHub repository to serve its contents on the web.

## Instructions

1. **Parameters**: Before deploying the template, you can customize the parameters based on your requirements.

2. **Deployment**: Use the AWS CloudFormation console or AWS Command Line Interface (CLI) to deploy this template.

3. **Access the Website**: Once the stack is deployed, you can access the website hosted on the EC2 instance by navigating to the public IP address of the instance in a web browser or the Output section of the CloudFormation Stack

## Template Details

For more information about the parameters, resources, and outputs of this CloudFormation template, please refer to the [AWS CloudFormation documentation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-reference.html).
