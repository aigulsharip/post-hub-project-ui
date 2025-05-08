<h1 align="center"> Post-Hub live-demo project</h1>

<p align="center">
 <img src="https://user-images.githubusercontent.com/74038190/213844263-a8897a51-32f4-4b3b-b5c2-e1528b89f6f3.png" width="50px" />

  <a href="https://nick8787.github.io/post-wave-demo-project/" target="_blank">
    <img src="https://img.shields.io/badge/Visit%20Live%20Project%20Site-Click%20Here-brightgreen?style=for-the-badge&logo=github&logoColor=white" alt="Visit Live Project Site">
  </a>
 <img src="https://user-images.githubusercontent.com/74038190/213844263-a8897a51-32f4-4b3b-b5c2-e1528b89f6f3.png" width="50px" />
</p>

<p align="center">
  <img src="images/post-wave-gif-1-last.gif" alt="Post-Wave Logo" />
</p>

# 📬 Post-Hub – microservices demo project

**Post-Hub** is a demo microservices project built to learn and showcase how different services work together in a modern backend system. It allows users to register, log in, create posts and comments, and tracks all user actions through a logging system.

## 🔍 What the project does

- User registration and login
- Post and comment creation
- Action logging via Kafka
- Secure endpoints using JWT
- Web access via Gateway and Nginx
- Full microservices architecture + CI/CD deployment

## 🧩 Microservices overview

The project is divided into four key services:

- **IAM-service:** Handles user accounts, authentication, and post/comment creation. Uses JWT for security and Flyway for database migrations.
- **UTILS-service:** Logs user activities like post/comment creation. Receives events from IAM-service via Kafka.
- **GATEWAY-service:** Main entry point for all external requests. Routes traffic to the correct service and checks authentication.
**DISCOVERY-service:** Uses Consul for automatic service registration and communication.

## ⚙️ Tech stack

- **Java + Spring Boot** — backend microservices
- **Spring Security + JWT** — authentication and authorization
- **Kafka** — messaging between services
- **Docker** — containerized deployment
- **PostgreSQL (on AWS)** — main production database
- **Flyway** — database migration tool
- **Consul** — service discovery
- **Nginx** — reverse proxy and SSL termination

## 🚀 Deployment Process

Each microservice is packaged as a Docker image and pushed to Docker Hub. CI/CD is managed through GitLab, and the deployment pipeline includes:

1. Fetching logs from the server
2. Stopping and removing running containers
3. Building the project JAR files
4. Creating and pushing Docker images
5. Deploying updated containers on the server

## 🗄️ Database & Hosting

- **Database:** PostgreSQL hosted on AWS via ScaleGrid
- **Hosting:** Deployed on a VPS with Docker and Nginx configured for routing, HTTPS, and performance
