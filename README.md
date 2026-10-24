# DevOps Task 2: Jenkins CI/CD Pipeline

## Project Overview
This project demonstrates a basic CI/CD pipeline for a Node.js application using Jenkins and Docker.

## Application
The application is built with Node.js and Express. It provides:
- `/` — returns a greeting message.
- `/health` — returns the application health status.

## Pipeline Stages
1. **Checkout:** Retrieves the source code from GitHub.
2. **Install Dependencies:** Installs dependencies using `npm ci`.
3. **Test:** Runs automated tests using `npm test`.
4. **Build Docker Image:** Builds a Docker image for the application.
5. **Push to Docker Hub:** Publishes the image to Docker Hub using Jenkins credentials.
6. **Deploy Container:** Runs the application in a Docker container.

## Tools Used
- Jenkins
- Git and GitHub
- Node.js and npm
- Docker
- Docker Hub

## Execution Status
The Jenkinsfile defines the intended pipeline. Actual execution and deployment must be verified on a configured Jenkins agent with Docker installed and the required credentials configured.

## Repository
https://github.com/Pallavikosuvari/devops-task-2-jenkins-cicd
