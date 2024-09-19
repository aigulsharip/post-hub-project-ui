<h1 align="center"> Post-Wave Project </h1>

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

## ⚙️ Project Overview

Post-Wave is a microservices-based platform that enables users to register, create posts and comments, and track all actions performed on the platform. The project serves as a learning tool for understanding microservices architecture, integration, and deployment.

## 🛠️ Tech Stack

The following technologies and tools were used in this project:

- **Java:** The primary programming language for developing microservices.
- **Spring Boot:** Used to build the microservices with RESTful APIs.
- **JWT & Spring Security:** Ensures secure user authentication and authorization.
- **Kafka:** Facilitates asynchronous communication between microservices.
- **Flyway:** Manages database migrations.
- **H2 & PostgreSQL:** H2 is used for local development, and PostgreSQL is used for production.
- **Docker:** Containerizes the application and its services.
- **IntelliJ IDEA Ultimate:** Integrated Development Environment (IDE) used for coding.

## 🚀 Deployment Workflow

The deployment process involves the following steps:

1. **Image Logs Stage:** Retrieve the last 1000 lines of Docker container logs from the remote server via SSH.
2. **Docker Stop Stage:** Stop and remove the current Docker container to prepare the server for deployment.
3. **Data Check Stage:** Validate the Docker environment, network, and user data on the server.
4. **Build JAR Stage:** Compile the application code into a JAR file using Maven.
5. **Build Docker Stage:** Create a new Docker image from the JAR file and push it to the Docker Registry.
6. **Deploy Stage:** Pull the new Docker image from the registry and deploy it on the server.

## 🗄️ Database & Hosting

The project uses a managed PostgreSQL database hosted on the ScaleGrid platform, leveraging AWS for high availability and scalability. The application is hosted on a dedicated server that uses Docker for deployment, ensuring flexible resource management and maintaining high performance.

