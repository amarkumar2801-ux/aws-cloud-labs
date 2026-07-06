 # AWS Amazon EKS Kubernetes Lab

## Overview

This lab demonstrates how to deploy a containerized application on Amazon Elastic Kubernetes Service (EKS).

A managed Kubernetes cluster was created, followed by a managed node group. Using kubectl, an Nginx deployment was created, exposed using a Kubernetes LoadBalancer service, and accessed through the AWS Elastic Load Balancer.

---

## AWS Services Used

- Amazon EKS
- Amazon EC2
- Elastic Load Balancer
- IAM
- Amazon VPC
- CloudShell
- kubectl

---

## Kubernetes Components

- Cluster
- Managed Node Group
- Node
- Deployment
- ReplicaSet
- Pod
- Service

---

## Lab Workflow

Create EKS Cluster

↓

Create Managed Node Group

↓

Connect CloudShell using kubectl

↓

Verify Worker Nodes

↓

Deploy Nginx Application

↓

Verify Running Pod

↓

Expose Deployment using LoadBalancer

↓

AWS creates Elastic Load Balancer

↓

Access Application from Browser

---

## Commands Used

```bash
kubectl get nodes

kubectl get pods -A

kubectl create deployment nginx --image=nginx

kubectl get pods

kubectl expose deployment nginx --port=80 --type=LoadBalancer

kubectl get svc
```

---

## Key Learnings

- Amazon EKS Architecture
- Kubernetes Control Plane
- Managed Node Groups
- Worker Nodes
- Pods
- Deployments
- ReplicaSets
- Services
- Load Balancer Integration
- kubectl Basics

---

## Result

Successfully deployed an Nginx container on Amazon EKS, exposed it using a Kubernetes LoadBalancer Service, and accessed the application through an AWS Elastic Load Balancer.