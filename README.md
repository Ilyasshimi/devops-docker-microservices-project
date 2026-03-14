# DevOps Docker Monitoring Project

## Overview

This project demonstrates a simple DevOps architecture using containerized services.
The stack includes a reverse proxy, a web application, a database, and a monitoring system.

All services run using Docker containers and are orchestrated with Docker Compose.

---

## Architecture

```
                 +--------+
                 |  User  |
                 +--------+
                      |
                      v
                 +--------+
                 | NGINX  |
                 +--------+
                      |
                      v
               +-------------+
               | Application |
               |  (Node.js)  |
               +-------------+
                      |
                      v
               +-------------+
               |   MySQL     |
               +-------------+

 Monitoring Stack
 -----------------------------
 | Prometheus  |   Grafana   |
 -----------------------------
```

---

## Technologies Used

* Docker
* Docker Compose
* NGINX
* Node.js
* MySQL
* Prometheus
* Grafana

---

## Services

| Service     | Description           | Port |
| ----------- | --------------------- | ---- |
| NGINX       | Reverse proxy server  | 8080 |
| Application | Node.js container     | 3000 |
| MySQL       | Database container    | 3306 |
| Prometheus  | Monitoring system     | 9090 |
| Grafana     | Monitoring dashboards | 3001 |

---

## Project Structure

```
devops-docker-nginx-project/
│
├── docker-compose.yml
├── README.md
│
└── screenshots/
    ├── docker-ps.png
    ├── app.png
    ├── prometheus.png
    └── grafana.png
```

---

## Run The Project

Clone the repository:

```
git clone https://github.com/YOUR_USERNAME/devops-docker-nginx-project.git
```

Go to the project folder:

```
cd devops-docker-nginx-project
```

Start the containers:

```
docker-compose up -d
```

---

## Access the Services

Application via NGINX:

```
http://localhost:8080
```

Application direct access:

```
http://localhost:3000
```

Prometheus:

```
http://localhost:9090
```

Grafana:

```
http://localhost:3001
```

---

## Screenshots

Add screenshots of the running containers and dashboards in the `screenshots` folder.

Example screenshots:

* Docker containers running
* Application page
* Prometheus monitoring page
* Grafana dashboard

---

## DevOps Concepts Demonstrated

This project demonstrates several important DevOps practices:

* Containerized application deployment
* Multi-service architecture
* Reverse proxy configuration
* Monitoring with Prometheus
* Visualization with Grafana
* Infrastructure defined with Docker Compose

---

## Future Improvements

Possible improvements for this project:

* Add CI/CD pipeline (GitHub Actions)
* Add container health checks
* Deploy the stack to a cloud environment
* Implement logging stack (ELK or Loki)

---

## Author

Ilyass Himi

DevOps / Cloud Learning Project
