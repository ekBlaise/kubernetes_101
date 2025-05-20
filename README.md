# Web App with MongoDB Deployment

This project contains Kubernetes configuration files for deploying a web application and a MongoDB database.

## Files Overview

- **`webapp.yaml`**:  
    Used for deploying the web application and its associated services.

- **`mongo.yaml`**:  
    Used for deploying the MongoDB database and its associated services.

## How to Use

1. Apply the MongoDB configuration:
     ```bash
     kubectl apply -f mongo.yaml
     ```

2. Apply the Web Application configuration:
     ```bash
     kubectl apply -f webapp.yaml
     ```

3. Verify the deployments and services:
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
