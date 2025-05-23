# Web App with MongoDB Deployment

This project contains Kubernetes configuration files for deploying a web application and a MongoDB database.

## Files Overview
- **`mongo-config.yaml`**:  
    Contains the ConfigMap for MongoDB configuration.

- **`mongo-secret.yaml`**:  
    Contains the Secret for MongoDB credentials.

- **`webapp.yaml`**:  
    Used for deploying the web application and its associated services.

- **`mongo.yaml`**:  
    Used for deploying the MongoDB database and its associated services.

## How to Use

1. Apply the MongoDB Secret configuration:
     ```bash
     kubectl apply -f mongo-secret.yaml
     ```

2. Apply the MongoDB ConfigMap configuration:
     ```bash
     kubectl apply -f mongo-config.yaml
     ```

3. Apply the MongoDB configuration:
     ```bash
     kubectl apply -f mongo.yaml
     ```

4. Apply the Web Application configuration:
     ```bash
     kubectl apply -f webapp.yaml
     ```

5. Verify the deployments and services:
     ```bash
     kubectl get deployments
     kubectl get services
     ```

## Prerequisites

- Kubernetes cluster set up and running.
- `kubectl` CLI installed and configured.

## Notes

- Ensure that the MongoDB service is running before deploying the web application to avoid connection issues.
- Modify the configuration files as needed to suit your environment.
