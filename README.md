# GithubActions_to_deploy_terraform
Infrastructure setup using Githubactions to deploy terraform template
# Terraform AWS Infrastructure with GitHub Actions Pipeline

This project demonstrates how to use Terraform to provision AWS infrastructure, including a Virtual Private Cloud (VPC), subnet, internet gateway, security group, and EC2 instance. The Terraform state is managed using an S3 backend. This repository also integrates a GitHub Actions pipeline to automatically trigger Terraform operations such as initialization, planning, and destruction.

## Prerequisites

- [Terraform](https://www.terraform.io/downloads.html) installed on your local machine (for local testing).
- [AWS CLI](https://aws.amazon.com/cli/) configured with your AWS credentials.
- A GitHub repository to store your Terraform code.
- A GitHub Actions CI/CD pipeline configured to automatically trigger Terraform operations.

- `src/main.tf`: Contains additional Terraform configurations (e.g., EC2 instance, VPC, subnet, etc.).
- `.github/workflows/terraform.yml`: GitHub Actions pipeline file to automatically trigger Terraform operations.

## Setup

# AWS Infrastructure with Terraform

This project provisions a basic AWS infrastructure using Terraform. It includes:
- A custom VPC
- A public subnet
- An internet gateway
- A route table with internet access
- A security group allowing SSH and HTTP
- An EC2 instance in the public subnet

## 🧱 Resources Created

- **VPC**: Custom VPC with CIDR `10.0.0.0/16`
- **Subnet**: Public subnet in `us-west-2a` (`10.0.1.0/24`)
- **Internet Gateway**: For internet access
- **Route Table**: Routes `0.0.0.0/0` to the IGW
- **Security Group**: Allows:
  - SSH (port 22)
  - HTTP (port 80)
- **EC2 Instance**: Amazon Linux 2 AMI (`t2.micro`)

How to use:

1. ## Clone the repository to your local machine:
git clone https://github.com/anjana2468/GithubActions_to_deploy_terraform.git
cd GithubActions_to_deploy_terraform

2. Initialize Terraform
terraform init

3. Plan Infrastructure
terraform plan

4. Apply Infrastructure
terraform apply -auto-approve

5. (Optional) Destroy Infrastructure
terraform destroy -auto-approve




