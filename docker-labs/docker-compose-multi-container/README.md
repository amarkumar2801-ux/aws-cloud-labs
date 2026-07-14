 # Docker Compose Multi-Container Application

## 📌 Project Overview

This lab demonstrates Docker Compose for managing multi-container applications. Using a single `docker-compose.yml` file, multiple containers were deployed automatically with one command.

The lab includes two web server containers:

- Nginx
- Apache HTTP Server

Docker Compose automatically created the required network and managed the lifecycle of the containers.

---

## 🎯 Objective

- Learn Docker Compose
- Create a docker-compose.yml file
- Deploy multiple containers
- Understand automatic network creation
- Manage containers using Docker Compose
- Verify services through a web browser

---

## 🏗️ Architecture

```
                docker-compose.yml
                        │
                        ▼
                Docker Compose
                        │
        ┌───────────────┴───────────────┐
        │                               │
   Nginx Container               Apache Container
   Port 8080                     Port 8081
        │                               │
        └──────── Docker Network ───────┘
```

---

## Technologies Used

- Amazon Linux 2023
- Docker Engine
- Docker Compose v2
- Nginx
- Apache HTTP Server
- AWS EC2

---

## Lab Steps

### Step 1

Create Project Directory

```bash
mkdir docker-compose-lab
cd docker-compose-lab
```

---

### Step 2

Create Compose File

```bash
nano docker-compose.yml
```

---

### Step 3

Deploy Containers

```bash
docker compose up -d
```

---

### Step 4

Verify Containers

```bash
docker compose ps
```

```bash
docker ps
```

---

### Step 5

Verify Network

```bash
docker network ls
```

Docker Compose automatically created a default bridge network.

---

### Step 6

Verify in Browser

Nginx

```
http://EC2-PUBLIC-IP:8080
```

Apache

```
http://EC2-PUBLIC-IP:8081
```

---

### Step 7

Cleanup

```bash
docker compose down
```

---

## Screenshots

- Docker Compose Version
- docker-compose.yml
- docker compose up
- docker compose ps
- docker ps
- docker network ls
- Nginx Browser Output
- Apache Browser Output
- docker compose down
- Cleanup Verification

---

## Key Learnings

- Docker Compose manages multiple containers.
- One YAML file defines the complete application.
- One command deploys all services.
- Docker Compose automatically creates a network.
- Docker Compose automatically connects services to the network.
- docker compose down removes containers and the default network.
- Docker Compose simplifies application deployment.

---

## Commands Used

```bash
docker compose version

docker compose up -d

docker compose ps

docker ps

docker network ls

docker compose down
```

---

## Outcome

Successfully deployed a multi-container application using Docker Compose and verified automatic container creation, networking, browser access, and resource cleanup.