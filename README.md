# AWS CloudFormation Lab Template


This repository contains an **AWS CloudFormation template** designed for a challenge lab environment as part of the AWS Restart program. The template provisions the following resources:

- **VPC** with customizable CIDR block
- **Internet Gateway** attached to the VPC
- **Private Subnet**
- **Security Group** allowing SSH access
- **EC2 Instance (t3.micro)** running Amazon Linux 2
- **S3 Bucket** for storage


## ✅ **Architecture**
+-------------------+
| VPC (10.0.0.0/24) |
| +-------------------+ |
| | Private Subnet | |
| | (10.0.0.0/28) | |
| | +--------------+ | |
| | | EC2 Instance | | |
| | +--------------+ | |
| +-------------------+ |
| Internet Gateway |
+---------------------------+

## ✅ **Parameters**
| Parameter             | Default                              | Description                     |
|----------------------|--------------------------------------|---------------------------------|
| `VpcCidr`           | `10.0.0.0/24`                       | CIDR block for the VPC         |
| `PrivateSubnetCidr` | `10.0.0.0/28`                       | CIDR block for private subnet  |
| `AmazonLinuxAMIID`  | `/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2` | SSM Parameter for AMI |

---

