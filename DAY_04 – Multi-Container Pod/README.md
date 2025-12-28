# Day 04 – Multi-Container Pods

## 🎯 Objective
Understand how multiple containers can run inside a single Pod.

## 📌 Multi-Container Pod
- A Pod can have **more than one container**
- Containers:
  - Share network
  - Share volumes
  - Communicate via localhost

## 🧠 Real Use Case
- Sidecar container for:
  - Logging
  - Monitoring
  - Proxy

## 🛠 Practical
We deploy:
- One NGINX container
- One BusyBox container (sidecar)

## 📄 Files
- `multi-container-pod.yaml`

## 🚀 Commands
```bash
kubectl apply -f multi-container-pod.yaml
kubectl get pods
kubectl describe pod multi-container-pod
