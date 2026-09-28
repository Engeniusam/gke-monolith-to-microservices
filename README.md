# Monolith Application

This is the monolithic web application component of the **Monolith to Microservices** workshop/project. It is a Node.js-based application configured to serve static assets and handle API requests.

This project is designed for the Google Cloud Codelab: **[Deploy, scale, and update your website with Google Kubernetes Engine (GKE)](https://codelabs.developers.google.com/codelabs/cloud-deploy-website-on-gke#0)**.

## Prerequisites

Before running this application, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v16 is recommended, as specified in the `Dockerfile`)
- Docker (optional, for containerized execution)

## Getting Started

### Local Development Setup

1. Navigate to the monolith directory:
   ```bash
   cd /home/engeniusam/monolith-to-microservices/monolith
   ```

2. Install the necessary dependencies:
   ```bash
   npm install
   ```

3. Run the application:
   ```bash
   node src/server.js
   ```

### Running with Docker

You can package and run the application in a isolated environment using the provided `Dockerfile`.

1. Build the Docker image:
   ```bash
   docker build -t monolith-service .
   ```

2. Start the container and map port 8080:
   ```bash
   docker run -p 8080:8080 monolith-service
   ```
   Once running, the application will be accessible at `http://localhost:8080`.
