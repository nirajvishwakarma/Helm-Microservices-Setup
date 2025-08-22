# Helm-Microservices-Setup
In this guide, I'll walk through setting up a Kubernetes cluster with Minikube, deploying two microservices using a reusable Helm chart, and demonstrating ConfigMap-based rolling updates and Helm rollbacks.

Design Notes

Single Helm chart drives multiple services via values files.
Config changes trigger rolling updates via checksum/config.
Optional HPA & PDB per service.
Flexible ServiceAccount creation.
Default image: ealen/echo-server.
