# AdventureWorksCRUD-.NET9-API
# AdventureWorks Microservices

## Project Overview
The **AdventureWorks Microservices** project is an implementation of a set of microservices that manage the **AdventureWorks** database using .NET Core, Docker, and CI/CD pipelines. It allows users to interact with the system via RESTful APIs, where various microservices handle different aspects of the business domain (e.g., user, product management).

## Architecture

This project follows a **Microservices Architecture** with the following components:

- **Frontend**: (Optional, if applicable) React or Angular frontend that communicates with APIs.
- **Backend**: Microservices built using **ASP.NET Core Web API** for each business domain.
- **Database**: **SQL Server** (AdventureWorks) stored in a Docker container.
- **Containerization**: Docker and Docker Compose are used to containerize services.
- **CI/CD**: Jenkins automates the build, Docker image creation, and deployment processes.

## Prerequisites
- Docker and Docker Compose installed on your local machine.
- Jenkins installed and configured (for CI/CD pipeline).
- GitHub account for version control and webhooks.

## Setup Instructions

1. **Clone the repository**:
   ```bash
   git clone <your-repository-url>
   cd AdventureWorksMicroservices
