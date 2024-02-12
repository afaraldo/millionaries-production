# Rails Application Deployment with Docker

This repository offers a streamlined solution for deploying a Rails web application in production environments. Utilizing Docker Compose, it features a setup with two Rails web services and a Caddy proxy service, encapsulated in a `production.yml` configuration file. This approach ensures a consistent, secure, and scalable deployment.

## Key Features

- **Rails Web Services**: Two Dockerized Rails services for efficient scalability and dependency management.
- **Caddy Proxy Service**: Automates SSL termination and request routing, enhancing security and performance.

## Benefits

- **Automated Deployment**: Simplifies the deployment process, reducing time and minimizing errors.
- **Scalable Architecture**: Facilitates easy service scaling and updates.
- **Enhanced Security**: Provides automated SSL handling and security best practices through Caddy.

## Repository Structure

- `production.yml`: Docker Compose file for orchestrating production services.
- Comprehensive documentation for setup, deployment, and ongoing maintenance.

## Usage Instructions

Ensure you have basic knowledge of Docker, Docker Compose, Rails, and Caddy. Follow the detailed steps in the documentation for seamless deployment.

### Preliminary Step

Login to Docker Hub:

```bash
docker login -u LOGIN -p PASSWORD cloud.docker.com

Deployment Commands
Start all services:

bash
Copy code
docker-compose -f production.yml --env-file .env.production up -d
Stop all services:

bash
Copy code
docker-compose -f production.yml --env-file .env.production down
Access the shell of the web service container:

bash
Copy code
docker-compose -f production.yml --env-file .env.production exec web /bin/bash```

Ideal Use Case
This setup is perfect for development teams looking for an efficient, secure, and easily maintainable deployment solution for Rails applications. Follow the guidelines for a streamlined deployment process.
