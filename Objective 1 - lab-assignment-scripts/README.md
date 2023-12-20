
# Kubernetes Scripts for Todo Application Deployment

This directory hosts scripts and configuration files essential for deploying a Todo application on Kubernetes. The configurations cover various components including namespaces, config maps, database services, persistent volumes and claims, MySQL database deployment, Todo application deployment, and the application's load balancer service.

## Pre-requisites

- Ensure microk8s/Kubernetes nodes have the following container images:
  - MySQL
  - Todo Application

## Scripts Overview

### 1. Namespace Configuration

- `1_lab_assign_namespace.yml`: Defines the Kubernetes namespace for the Todo application.

### 2. ConfigMap Configuration

- `2_lab_assign_configmap.yml`: Configures environment-specific variables or configurations.

### 3. Database Service Configuration

- `3_lab_assign_db_service.yml`: Defines the service for the database.

### 4. Database Persistent Volume Configuration

- `4_lab_assign_db_pv.yml`: Configures the persistent volume for the MySQL database.

### 5. Database Persistent Volume Claims Configuration

- `5_lab_assign_db_pvc.yml`: Defines the persistent volume claims for the MySQL database.

### 6. MySQL Database Deployment Configuration

- `6_lab_assign-db-deployment.yml`: Sets up the deployment for the MySQL database.

### 7. Todo Application Deployment Configuration

- `7_lab_assign_todoapi_app.yml`: Configures the deployment for the Todo application.

### 8. Application Load Balancer Service Configuration

- `8_lab_assign_todoapp_svc.yml`: Sets up the load balancer service for the Todo application.

## Usage

1. Ensure the pre-requisites are met.
2. Apply the configurations in the following order:
   ```bash
   kubectl apply -f 1_lab_assign_namespace.yml
   kubectl apply -f 2_lab_assign_configmap.yml
   kubectl apply -f 3_lab_assign_db_service.yml
   kubectl apply -f 4_lab_assign_db_pv.yml
   kubectl apply -f 5_lab_assign_db_pvc.yml
   kubectl apply -f 6_lab_assign-db-deployment.yml
   kubectl apply -f 7_lab_assign_todoapi_app.yml
   kubectl apply -f 8_lab_assign_todoapp_svc.yml
   ```

## Notes

- Customize the configurations based on your environment and application requirements.
- Verify and adjust resource allocations as needed.

---

This Markdown provides a structured overview of the repository's contents and instructions for deploying the Todo application on Kubernetes. Feel free to adapt it based on your actual file names, specific configurations, or additional instructions required for your deployment.