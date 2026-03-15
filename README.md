# DevOps Docker Microservices Project

## Overview

This project demonstrates a simple DevOps microservices architecture using Docker and Docker Compose.

The system includes multiple services running in containers:

* Frontend (NGINX)
* Backend API (Node.js)
* MySQL Database
* Monitoring stack (Prometheus and Grafana)

The goal of this project is to practice containerization, service orchestration, and monitoring in a microservices environment.

---

# Architecture

The application follows a microservices architecture.

User requests go through the frontend service, which communicates with the backend API and database.

Monitoring tools collect metrics from the services.

```
User
 |
 v
Frontend (NGINX)
 |
 v
Backend API (Node.js)
 |
 v
MySQL Database

Monitoring
 ├ Prometheus
 └ Grafana
```

---

# Technologies Used

* Docker
* Docker Compose
* NGINX
* Node.js
* MySQL
* Prometheus
* Grafana

---

# Project Structure

```
devops-docker-microservices-project
│
├── frontend
│   ├── Dockerfile
│   └── index.html
│
├── backend
│   ├── Dockerfile
│   └── server.js
│
├── docker-compose.yml
├── README.md
└── screenshots
```

---

# Services and Ports

| Service     | Port |
| ----------- | ---- |
| Frontend    | 8080 |
| Backend API | 4000 |
| MySQL       | 3306 |
| Prometheus  | 9090 |
| Grafana     | 3001 |

---

# Prerequisites

Before running the project, make sure you have:

* Docker
* Docker Compose
* Git

---

# Run the Project

Start all services:

```
docker-compose up -d
```

Check running containers:

```
docker ps
```

Stop the services:

```
docker-compose down
```

---

# Access the Services

Frontend

```
http://Localhost:8080
```

Backend API

```
http://Localhost:4000
```

Prometheus Monitoring

```
http://Localhost:9090
```

Grafana Dashboard

```
http://Localhost:3001
```

Default Grafana login:

```
username: admin
password: admin
```

---

# Screenshots

## Running Containers

![Docker Containers](screenshots/01_docker_containers_running.png)

## Frontend Service

![Frontend](screenshots/04_frontend_service.png)

## Backend API

![Backend](screenshots/05_backend_api.png)

## Prometheus Monitoring

![Prometheus](screenshots/06_prometheus_monitoring.png)

## Grafana Dashboard

![Grafana](screenshots/07_grafana_dashboard.png)

---

# What I Learned

* Building Docker images using Dockerfile
* Running multi-container applications with Docker Compose
* Creating a simple microservices architecture
* Monitoring containerized services using Prometheus and Grafana
* Managing services and ports inside a container environment

---

# Future Improvements

Possible improvements for this project:

* Add CI/CD pipeline using GitHub Actions
* Deploy the project to a cloud platform
* Add container registry integration
* Improve monitoring dashboards

---

# Author

Ilyass Himi

DevOps learning project.

