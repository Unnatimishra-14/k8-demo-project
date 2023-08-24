# Kubernetes Demo Project

Welcome to the Kubernetes Demo Project repository! This repository contains a basic example of a Kubernetes setup using YAML configuration files. The project includes a MongoDB deployment and a web application deployment, demonstrating how different Kubernetes resources can work together.
This is a kubernetes demo project that I created while learning kubernetes basics with techworld-by-nana on youtube.

## Table of Contents

- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Usage](#usage)
- [Contributing](#contributing)


## Project Overview

This project showcases the deployment of two main components: a MongoDB database and a web application, within a Kubernetes cluster. The MongoDB deployment is used to store data, while the web application interacts with the database.

The project includes the following Kubernetes resources:
- ConfigMap for MongoDB configuration
- Secret for sensitive information (MongoDB credentials)
- Deployment for MongoDB instance
- Service for MongoDB
- Deployment for web application
- Service for web application

## Prerequisites

Before you begin, ensure you have the following prerequisites:
- A running Kubernetes cluster
- `kubectl` command-line tool configured to interact with your cluster

## Setup

1. Clone this repository to your local machine:

   ```
   git clone https://github.com/Unnatimishra-14/k8-demo-project.git
   cd k8s-demo-project
   ```

2. Apply the Kubernetes configuration files:

   ```
   kubectl apply -f mongo-config.yaml
   kubectl apply -f mongo-secret.yaml
   kubectl apply -f mongo-deployment.yaml
   kubectl apply -f mongo-service.yaml
   kubectl apply -f webapp-deployment.yaml
   kubectl apply -f webapp-service.yaml
   ```

3. Monitor the deployment:

   ```
   kubectl get pods
   kubectl get services
   ```

## Usage

Once the resources are deployed, you can access the web application through your web browser using the NodePort assigned to the `webapp-service`. The web application will connect to the MongoDB instance using the credentials provided in the `mongo-secret` and the MongoDB URL from the `mongo-config`.

## Contributing

Contributions are welcome! If you want to contribute to this project, follow these steps:
1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit them: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a pull request



---

