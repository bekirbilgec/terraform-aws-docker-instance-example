# Terraform Module for Provisioning an AWS EC2 Instance with the Latest Amazon Linux 2 AMI and Docker

![Terraform Version](https://img.shields.io/badge/Terraform-%3E%3D0.12-blueviolet)
![AWS Provider Version](https://img.shields.io/badge/AWS%20Provider-%3E%3D2.0-orange)
![License](https://img.shields.io/badge/License-MIT-green)

This Terraform module facilitates the provisioning of an AWS EC2 instance, featuring the latest Amazon Linux 2 AMI with Docker pre-installed.

**Note: This module is designed solely for illustrative purposes and is not intended for production use.**

## Key Features

- Creates an EC2 instance equipped with Amazon Linux 2 and Docker, ready for use.
- Demonstrates the procedure for structuring and publishing a module within the Terraform Registry.

## Usage

```hcl
provider "aws" {
  region = "us-east-1"
}

module "docker_instance" {
  source   = "bekirbilgec/docker-instance/aws"
  key_name = "first"
}
```

## Inputs

| Name       | Description                   | Type   | Default | Required |
|------------|-------------------------------|--------|---------|----------|
| key_name   | Name of the SSH key pair      | string | -       | yes      |

## Outputs

| Name           | Description                 |
|----------------|-----------------------------|
| instance_id    | ID of the EC2 instance      |
| instance_ip    | Public IP address of the instance |
| instance_arn   | ARN of the EC2 instance     |

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

