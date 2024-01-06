# Komplete DevOps Kubernetes Manifests

This repository contains Kubernetes manifests for setting up and managing a full-stack application architecture, including CI/CD with Jenkins, cluster administration with Rancher, monitoring with Prometheus and Grafana, and various microservices.

## Directory Structure

- `cicd/`: CI/CD related Kubernetes manifests.
  - `jenkins/`: Contains Jenkins-related configurations.
    - `jenkins-agent-build/Dockerfile`: Dockerfile for Jenkins agent.
    - `jenkins-master-pod/`: Kubernetes manifests for setting up Jenkins Master pod.
- `cluster-administration/`: Contains manifests for cluster administration tools.
  - `rancher/`: Ingress configurations for Rancher.
- `cluster-management/`: Kubernetes manifests for cluster management tools.
  - `elastic-stack/`: Elastic Stack (ELK) setup for logging.
  - `ingress-controller/`: Contains ingress controller configurations.
  - `monitoring/`: Monitoring setup with Prometheus and Grafana.
    - `prometheus-grafana-stack/`: Full stack setup for Prometheus and Grafana.
- `microservices/`: Manifests for various microservices in the architecture.
  - Contains deployment, service, and ingress manifests for each microservice.

## Setup and Usage

To use these manifests:

1. Clone this repository:
   ```bash
   git clone https://github.com/EJT93/komplete-devops-k8s-manifests.git
   ```
2. Navigate to the desired directory and apply the manifests using `kubectl`:
   ```bash
   kubectl apply -f <path-to-manifest>
   ```
   Replace `<path-to-manifest>` with the relative path to the Kubernetes manifest file.

### CI/CD with Jenkins

Set up a Jenkins CI/CD pipeline by applying the manifests found in the `cicd/jenkins/` directory. This will set up Jenkins with necessary configurations for running in a Kubernetes cluster.

### Cluster Administration with Rancher

Rancher can be set up using the manifests in the `cluster-administration/rancher/` directory, providing an intuitive management interface for Kubernetes clusters.

### Monitoring with Prometheus and Grafana

Apply manifests from the `cluster-management/monitoring/` directory to set up Prometheus for monitoring and Grafana for visualizing metrics.

### Microservices Deployment

Each microservice, including the admin panel, gateway, and web application, has its own set of manifests for deployment, service configuration, and ingress setup located in the `microservices/` directory.