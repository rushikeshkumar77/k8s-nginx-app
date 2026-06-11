# Kubernetes Nginx Application

A simple Kubernetes project created for learning core Kubernetes concepts using a Kind cluster.

## Resources Included

* Namespace
* Deployment
* Service
* PersistentVolume (PV)
* PersistentVolumeClaim (PVC)
* Job

## Project Structure

```text
.
├── namespace.yaml
├── deployment.yaml
├── service.yaml
├── pv.yaml
├── pvc.yaml
└── job.yaml
```

## Kubernetes Concepts Covered

### Namespace

Logical isolation of Kubernetes resources.

### Deployment

Manages Nginx pods and ensures the desired number of replicas are running.

### Service

Exposes the Nginx application inside the cluster.

### PersistentVolume (PV)

Provides persistent storage for application data.

### PersistentVolumeClaim (PVC)

Requests storage from the PersistentVolume.

### Job

Runs a one-time task and exits after completion.

## Deployment Steps

Create the namespace:

```bash
kubectl apply -f namespace.yaml
```

Create storage resources:

```bash
kubectl apply -f pv.yaml
kubectl apply -f pvc.yaml
```

Deploy the application:

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

Create the Job:

```bash
kubectl apply -f job.yaml
```

## Verification

Check resources:

```bash
kubectl get all -n nginx
kubectl get pv
kubectl get pvc -n nginx
```

## Learning Outcomes

* Creating Kubernetes manifests
* Managing Deployments and Services
* Understanding PV and PVC
* Running Kubernetes Jobs
* Working with namespaces
* Persisting application data

## Environment

* Kubernetes
* Kind
* Docker
* Nginx
* Ubuntu / WSL
* Git & GitHub

