FullStack Blogging App

This project is a full-stack blogging application built using various technologies. Below is an overview of the setup and deployment instructions.

Features:
- Full-stack application for blogging
- Docker support
- CI/CD pipeline setup using Jenkins
- Deployment ready for Kubernetes (EKS)

Prerequisites:
- Java (version 11 or higher)
- Maven
- Docker
- Kubernetes cluster (EKS or other)
- Terraform for EKS setup
- Jenkins for CI/CD

Setup Instructions:

1. Build the project:
   ./mvnw clean install

2. Running with Docker:
   Make sure Docker is installed and running, then build the Docker image:
   docker build -t fullstack-blogging-app .

   Run the Docker container:
   docker run -p 8080:8080 fullstack-blogging-app

3. Kubernetes Deployment:
   The project includes a deployment-service.yml file for Kubernetes deployment. Apply it to your cluster using:
   kubectl apply -f deployment-service.yml

4. CI/CD with Jenkins:
   The Jenkins pipeline is defined in Jenkinsfile. Make sure Jenkins is set up with the necessary credentials to pull this repository and build the project.

Directory Structure:
- src/: Source code for the application
- pom.xml: Maven configuration file
- Dockerfile: Docker configuration to containerize the application
- deployment-service.yml: Kubernetes deployment configuration
- EKS_Terraform/: Terraform scripts to set up EKS
- Jenkinsfile: Jenkins pipeline configuration

License:
This project is licensed under the MIT License.
