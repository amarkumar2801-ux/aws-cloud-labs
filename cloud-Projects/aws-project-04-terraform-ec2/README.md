 # AWS Project 04 - Terraform EC2 Infrastructure as Code

## Project Overview

This project demonstrates Infrastructure as Code (IaC) using Terraform to provision AWS resources.

Terraform automatically creates:

- Amazon EC2 Instance
- Security Group
- Latest Amazon Linux 2023 AMI (Data Source)
- Outputs (Instance ID, Public IP, Public DNS)

The project uses AWS CLI authentication with an IAM user and deploys infrastructure in the AWS Mumbai (ap-south-1) region.

---

## Services Used

- AWS EC2
- AWS Security Group
- AWS IAM
- AWS CLI
- Terraform

---

## Project Files

provider.tf

Configures the AWS provider.

variables.tf

Defines reusable variables.

terraform.tfvars

Stores variable values.

main.tf

Creates the Security Group and EC2 Instance.

outputs.tf

Displays important resource information after deployment.

---

## Terraform Workflow

Terraform Initialize

terraform init

Validate Configuration

terraform validate

Preview Infrastructure

terraform plan

Deploy Infrastructure

terraform apply

Destroy Infrastructure

terraform destroy

---

## Resources Created

- 1 EC2 Instance
- 1 Security Group

---

## Outputs

- Instance ID
- Public IP Address
- Public DNS

---

## Skills Demonstrated

- Infrastructure as Code (IaC)
- Terraform Basics
- AWS CLI Configuration
- IAM Authentication
- EC2 Provisioning
- Security Group Configuration
- Variables and Outputs
- Terraform Data Sources

---

## Screenshots

- Project Structure
- Terraform Apply Success
- EC2 Running
- Security Group Configuration
- Terraform Plan
- AWS CLI Authentication

---

## Author

Amarjeet Chaudhary

AWS Cloud Engineer (Fresher)

Preparing for AWS Solutions Architect Associate (SAA-C03)