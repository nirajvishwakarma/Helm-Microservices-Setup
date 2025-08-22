# Helm Microservices Demo (One Reusable Chart → Two Services)

This project demonstrates:
- Standing up a Kubernetes cluster (Minikube),
- Authoring a reusable Helm chart,
- Deploying **two** services from the same chart with different values,
- Triggering **rolling updates** on ConfigMap changes via checksum annotation,
- Using Helm history and rollback safely,
- Clear, reproducible steps with commands.

> Tested with: Minikube v1.33+, Kubernetes v1.29+, Helm v3.14+

---

## 0) Prereqs

- **kubectl** `kubectl version --client --short`
- **helm** `helm version`
- **minikube** `minikube version` (or any K8s cluster of your choice)

## 1) Start a local cluster (Minikube)

```bash
minikube start --kubernetes-version=v1.29.0
kubectl get nodes
