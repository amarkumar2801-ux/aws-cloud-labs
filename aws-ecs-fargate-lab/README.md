 # AWS ECS Fargate Lab

## Overview

This lab demonstrates how to deploy a Docker container on Amazon ECS using the AWS Fargate launch type without managing EC2 instances.

The Nginx Docker image was pulled from Docker Hub, deployed as an ECS Task, managed by an ECS Service, and accessed through a public IP.

---

## Services Used

- Amazon ECS
- AWS Fargate
- Docker Hub
- Amazon VPC
- Security Groups

---

## Lab Architecture

Browser
↓
Public IP
↓
Security Group (HTTP Port 80)
↓
Amazon ECS Service
↓
Amazon ECS Task
↓
Nginx Docker Container

---

## Steps Performed

### 1. Created ECS Cluster

- Launch Type: AWS Fargate
- Cluster Name: test-cluster

---

### 2. Created Task Definition

Configured:

- Launch Type: Fargate
- CPU: 0.25 vCPU
- Memory: 512 MiB
- Container Name: nginx
- Image: nginx
- Container Port: 80

---

### 3. Created ECS Service

Configured:

- Desired Tasks: 1
- Assigned Public IP
- Selected Public Subnet
- Attached Security Group

---

### 4. Configured Security Group

Inbound Rule:

HTTP
Port 80
Source: 0.0.0.0/0

---

### 5. Verified Deployment

Verified using:

Browser

http://Public-IP

CloudShell

curl http://Public-IP

PowerShell

curl http://Public-IP

Successfully received the default Nginx page.

---

## Screenshots

- ECS Cluster
- Task Definition
- Container Configuration
- ECS Service
- Running Task
- Task Network Configuration
- Security Group
- Browser Output
- CloudShell Verification

---

## Key Learnings

- ECS Cluster
- ECS Task Definition
- ECS Service
- AWS Fargate
- Docker Container Deployment
- Public Networking
- Security Groups
- Public IP Access
- Container Verification

---

## Result

Successfully deployed an Nginx Docker container on Amazon ECS using AWS Fargate and accessed it over the Internet using a public IP.