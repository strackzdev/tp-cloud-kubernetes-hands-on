# Kubernetes Hands-On Project

This repository contains two implementations of the same Kubernetes application:

## Project Structure

- **kubernetes/** - Contains raw Kubernetes manifests (YAML files) that define a basic cluster with standard Kubernetes components. This implementation uses the traditional approach without any package manager.

- **helm/** - Contains a similar application configured as a Helm chart. While the functionality remains identical to the basic version, this implementation leverages Helm as a package manager to simplify deployment, upgrades, and management of the Kubernetes resources.

## Getting Started

### Getting Started

**Basic Kubernetes Deployment**

To deploy using the basic Kubernetes manifests:
```shell
kubectl apply -f basic/
```
**Helm Deployment**

To deploy using Helm:
```shell
cd helm
helm upgrade --install tp-cloud-kubernetes-hands-on .
```

## Cleanup

**Basic Kubernetes Deployment**
```shell
kubectl delete -f kubernetes/
```

**Helm Deployment**
```shell
cd helm
helm uninstall tp-cloud-kubernetes-hands-on
```