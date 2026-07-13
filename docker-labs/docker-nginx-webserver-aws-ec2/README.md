 # Dockerized Nginx Web Server on AWS EC2

## Overview

This lab demonstrates how to deploy a static website using Docker on an AWS EC2 instance running Amazon Linux 2023.

The project covers Docker installation, Dockerfile creation, custom image building, container deployment, port mapping, and hosting a web application using the Nginx web server.

---

## Technologies Used

- AWS EC2
- Amazon Linux 2023
- Docker Engine
- Dockerfile
- Nginx
- HTML

---

## Architecture

```
Internet
    │
HTTP (80 / 8080)
    │
AWS Security Group
    │
EC2 Instance (Amazon Linux 2023)
    │
Docker Engine
 ┌──────────────┐
 │              │
 ▼              ▼
Container-1   Container-2
Port 80       Port 80
 │              │
 ▼              ▼
Nginx         Nginx
 │              │
 ▼              ▼
index.html    index.html
```

---

## Project Workflow

1. Launch AWS EC2 Instance
2. Install Docker
3. Create index.html
4. Create Dockerfile
5. Build Docker Image
6. Run Docker Container
7. Access Website using Browser
8. Run Multiple Containers using Different Host Ports

---

## Dockerfile

```dockerfile
FROM nginx:latest

COPY index.html /usr/share/nginx/html/index.html

EXPOSE 80

CMD ["nginx","-g","daemon off;"]
```

---

## Commands Used

### Build Docker Image

```bash
docker build -t my-web:v1 .
```

### Run First Container

```bash
docker run -d --name webserver -p 80:80 my-web:v1
```

### Run Second Container

```bash
docker run -d --name webserver2 -p 8080:80 my-web:v1
```

### List Images

```bash
docker images
```

### List Running Containers

```bash
docker ps
```

---

## Learning Outcomes

- Understood Docker Architecture
- Created Dockerfile
- Built Custom Docker Image
- Deployed Container on AWS EC2
- Learned Port Mapping
- Ran Multiple Containers from a Single Image
- Hosted Static Website using Nginx

---

## Screenshots

- EC2 Instance
- Security Group
- Docker Version
- Docker Build
- Docker Images
- Docker Containers
- Browser (Port 80)
- Browser (Port 8080)

---

## Author

Amarjeet Chaudhary