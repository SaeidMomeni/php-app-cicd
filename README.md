PHP App with Docker and CI/CD

A simple PHP web application containerized with Docker and deployed using a GitHub Actions CI/CD pipeline. This project showcases foundational DevOps skills, including Git, Docker, and automated CI/CD workflows.

Project Overview

This project demonstrates a basic DevOps workflow for a PHP application:





Application: A simple PHP app served via Apache, displaying a welcome message.



Containerization: Packaged into a Docker container using the official php:8.2-apache image.



CI/CD: Automated pipeline using GitHub Actions to build and push the Docker image to Docker Hub.



Deployment: Can be run locally or deployed to any cloud provider supporting Docker.

Architecture





App: PHP application running in a Docker container with Apache.



CI/CD: GitHub Actions pipeline triggered on push to the main branch, building and pushing the Docker image to Docker Hub.



Local Testing: Docker Compose for easy local setup and testing.



Prerequisites





Docker Desktop installed.



Git installed.



Access to Docker Hub and GitHub (VPN recommended for restricted regions).

Setup Instructions





Clone the repository:

git clone https://github.com/SaeidMomeni/php-app-cicd.git
cd php-app-cicd



Run the app locally with Docker Compose:

docker-compose up --build



Open your browser and navigate to http://localhost:8080.



To pull the pre-built image from Docker Hub:

docker pull saeidmomeni/php-app-cicd:latest
docker run -p 8080:80 saeidmomeni/php-app-cicd:latest

CI/CD Pipeline





Trigger: Runs on every push to the main branch.



Steps:





Checks out the code.



Sets up Docker Buildx.



Logs in to Docker Hub using stored secrets.



Builds and pushes the Docker image to saeidmomeni/php-app-cicd.



View the pipeline in action under the "Actions" tab of the GitHub repository.

Files





src/index.php: The PHP application code.



Dockerfile: Defines the Docker image for the PHP app.



docker-compose.yml: Configures local development and testing.



.github/workflows/cicd.yml: GitHub Actions workflow for CI/CD.

Screenshots



Future Improvements





Add automated tests (e.g., PHP linting) to the CI/CD pipeline.



Deploy the app to a Kubernetes cluster.



Integrate monitoring with Prometheus and Grafana.



Add image versioning for better release management.

Contact





GitHub: SaeidMomeni



LinkedIn: Saeid Momeni
