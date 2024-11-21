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

### 1. Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/anjana2468/GithubActions_to_deploy_terraform.git
cd terraform-aws-pipeline

2. Configure AWS Credentials
aws configure

3. Initialize Terraform
terraform init

4. Apply the Terraform Configuration 
terraform apply
