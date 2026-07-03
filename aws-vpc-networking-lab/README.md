 # AWS VPC Networking Lab

## Overview

This lab demonstrates how to build a secure AWS Virtual Private Cloud (VPC) from scratch. It covers creating a custom VPC, configuring public and private subnets, attaching an Internet Gateway, configuring route tables, launching EC2 instances, and securely accessing a private EC2 instance through a Bastion Host.

---

# Architecture

```
                Internet
                    │
            Internet Gateway
                    │
          Public Route Table
                    │
        ┌───────────┴───────────┐
        │                       │
 Public Subnet            Private Subnet
 10.0.1.0/24              10.0.2.0/24
        │                       │
 Public EC2               Private EC2
(Bastion Host)         (No Public IP)
        │
        └────── SSH ──────► Private EC2
```

---

# AWS Services Used

- Amazon VPC
- Public Subnet
- Private Subnet
- Internet Gateway (IGW)
- Route Table
- Security Groups
- Amazon EC2
- Bastion Host
- SSH

---

# Network Configuration

| Resource | Configuration |
|----------|---------------|
| VPC | 10.0.0.0/16 |
| Public Subnet | 10.0.1.0/24 |
| Private Subnet | 10.0.2.0/24 |
| Internet Gateway | Attached |
| Public Route | 0.0.0.0/0 → Internet Gateway |
| Public EC2 | Public IP Enabled |
| Private EC2 | No Public IP |

---

# Lab Workflow

### Step 1
Create a custom VPC.

### Step 2
Create Public and Private Subnets.

### Step 3
Create and attach an Internet Gateway.

### Step 4
Create a Public Route Table and associate it with the Public Subnet.

### Step 5
Launch a Public EC2 instance and configure it as a web server.

### Step 6
Launch a Private EC2 instance without a Public IP.

### Step 7
Use the Public EC2 as a Bastion Host to securely SSH into the Private EC2.

---

# Security Design

- Public EC2 has a Public IP.
- Private EC2 does not have a Public IP.
- Internet traffic reaches only the Public Subnet.
- Private EC2 is accessed only through the Bastion Host.
- Security Groups are configured to allow secure SSH access.

---

# Screenshots

```
Screenshot/
│
├── 01-vpc-created.png
├── 02-public-private-subnets-created.png
├── 03-internet-gateway-attached.png
├── 04-public-route-table.png
├── 05-public-ec2-running.png
├── 06-public-ec2-webserver.png
├── 07-private-ec2-running.png
└── 08-bastion-host-ssh-success.png
```

---

# Key Concepts Learned

- AWS VPC
- CIDR Blocks
- Public Subnet
- Private Subnet
- Internet Gateway
- Route Tables
- Security Groups
- Public vs Private EC2
- Bastion Host Architecture
- Secure SSH Connectivity

---

# Real World Use Case

In production environments, backend servers and databases are deployed inside private subnets without public IP addresses. Administrators first connect to a Bastion Host located in a public subnet and then securely access private instances using SSH. This architecture improves security by preventing direct internet access to critical infrastructure.

---

# Lab Outcome

Successfully built a secure AWS VPC environment with:

- Custom VPC
- Public & Private Subnets
- Internet Gateway
- Route Table Configuration
- Public EC2 Web Server
- Private EC2 Instance
- Bastion Host Architecture
- Secure SSH Access

---

**Author**

**Amarjeet Chaudhary**

AWS Solutions Architect Associate (SAA-C03) Hands-on Lab Portfolio