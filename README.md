# Kubernetes Challenge

This repository provides a guide to deploying a simple web application on Kubernetes using Minikube, Ingress, and basic Kubernetes resources such as Deployment, Service, and Ingress.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Setup and Deployment](#setup-and-deployment)
3. [Verification](#verification)

## Prerequisites

Before starting, ensure you have the following tools installed:

- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

## Setup and Deployment

1. **Start Minikube:**

   ```sh
   minikube start

   ```

2. **Enable Ingress Addon:**

   ```sh
   minikube addons enable ingress

   ```

3. **Clone the Repository:**
   ```sh
   git clone https://github.com/learnk8s/kubernetes-challenge.git
   cd kubernetes-challenge
   ```
4. **Apply Kubernetes Configurations:**
   ```sh
   kubectl apply -f deployment.yaml
   kubectl apply -f service.yaml
   kubectl apply -f ingress.yaml
   ```

## Verification

**Access the Application:**
Retrieve the Minikube IP address and access the application.

    curl http://$(minikube ip)
