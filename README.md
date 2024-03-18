# 🚀 Docker Database Setup Guide

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![MicrosoftSQLServer](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)


## Introduction
### Overview of Docker
Docker is a platform that allows you to develop, ship, and run applications in containers. Containers are lightweight, portable, and self-sufficient environments that contain everything needed to run an application, including code, runtime, system tools, system libraries, and settings. Docker uses containerization technology to package applications and their dependencies into containers, ensuring consistency across different environments.

### Benefits of Using Docker for Database Management
Using Docker for database management offers several benefits:

- **Isolation**: Docker containers provide isolated environments for running databases, ensuring that each database instance operates independently without interference from other applications or databases.

- **Consistency**: Docker ensures consistency between development, testing, and production environments by packaging databases and their dependencies into portable containers. This minimizes compatibility issues and simplifies deployment.

- **Portability**: Docker containers are portable and can be easily deployed across different platforms and cloud providers. This makes it convenient to migrate databases between environments and scale resources as needed.

- **Resource Efficiency**: Docker containers share the host system's kernel and resources, resulting in efficient resource utilization compared to traditional virtualization methods. This allows you to run multiple database instances on the same host without significant overhead.

## Setting up Docker
Installing Docker on Your Operating System
To install Docker on your operating system, follow these steps:

1. Windows:

- Download and install Docker Desktop from the [Docker Hub website](https://docs.docker.com/desktop/install/windows-install/).
- Follow the installation instructions provided by the installer.

2. macOS:

- Download and install Docker Desktop for Mac from the [Docker Hub website](https://docs.docker.com/desktop/install/mac-install/).
- Follow the installation instructions provided by the installer.

3. Linux:

- Docker installation steps vary depending on the Linux distribution you're using. Refer to the official Docker documentation for detailed installation instructions for your distribution:
    - [Install Docker Engine on Ubuntu](https://docs.docker.com/desktop/install/ubuntu/)
    - [Install Docker Engine on Debian](https://docs.docker.com/desktop/install/debian/)
    - [Install Docker Desktop on Fedora](https://docs.docker.com/desktop/install/fedora/)

## Basic Docker Commands and Terminology
Before you start using Docker, familiarize yourself with basic Docker commands and terminology:

- **Image**: An image is a read-only template used to create Docker containers. It contains the application code, libraries, and dependencies needed to run the application.

- **Container**: A container is a lightweight, runnable instance of an image. It encapsulates the application and its dependencies, making it portable and easy to deploy.

- **Pull**: The process of downloading Docker images from a registry (e.g., Docker Hub) to your local system is called pulling.

- **Run**: The run command creates a new container instance from a Docker image and starts it.

- **Dockerfile**: A Dockerfile is a text document that contains instructions for building a Docker image. It specifies the base image, dependencies, and commands needed to set up the application environment.

- **Volume**: A volume is a Docker feature used to persist data generated by and used by Docker containers. Volumes allow data to survive container restarts and can be shared between multiple containers.

Now that you have Docker installed and understand basic Docker commands, you're ready to set up Docker containers for various databases.

## Set up Docker containers for various databases

- [MySQL](docker-MySQL.md)
- [PostgreSQL](docker-PostgreSQL.md)
- [MongoDB](docker-MongoDB.md)
- [Microsoft SQL Server](docker-Microsoft-SQL-Server.md)
- [Oracle](docker-Oracle.md)
- [SQLite](docker-SQLite.md)
- [Redis](docker-Redis.md)
- [Apache Cassandra](docker-Apache-Cassandra.md) 

## Thank you for the Support
- ⭐ Give this repo a ⭐ star ⭐ at the top of the page
- 🐦 Follow me on [X](https://x.com/tshenolo)
- 📺 Subscribe to my [Youtube channel](https://www.youtube.com/@tshenolo?sub_confirmation=1)

<p><a href="https://www.buymeacoffee.com/tshenolo"> <img align="left" src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="50" width="210" alt="tshenolo" /></a></p>