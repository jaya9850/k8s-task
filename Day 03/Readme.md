# Day 03 – Kubernetes Pod Basics

## 🎯 Objective
Understand what a Pod is and how to run a container inside Kubernetes using a Pod.

## 📌 What is a Pod?
- A Pod is the **smallest deployable unit** in Kubernetes.
- A Pod can contain **one or more containers**.
- All containers in a Pod:
  - Share the same IP
  - Share storage
  - Run together

## 🧠 Why Pods?
- Kubernetes does **not run containers directly**
- Containers are always wrapped inside Pods

## 🛠 Practical
We will create a simple Pod running an NGINX container.

## 📄 Files in this directory
- `pod.yaml` – Pod definition file

## 🚀 Commands
```bash
kubectl apply -f pod.yaml
kubectl get pods
kubectl describe pod nginx-pod
kubectl delete pod nginx-pod
