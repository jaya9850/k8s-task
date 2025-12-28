# Day 07 – Deployment

## 🎯 Objective
Learn how Deployments manage ReplicaSets and enable rolling updates.

## 📌 What is Deployment?
- Manages ReplicaSets
- Provides:
  - Rolling updates
  - Rollbacks
  - Version control

## 🧠 Why Deployment?
- Zero-downtime updates
- Easy rollback

## 📄 Files
- `deployment.yaml`

## 🚀 Commands
```bash
kubectl apply -f deployment.yaml
kubectl get deploy
kubectl rollout status deployment nginx-deployment
kubectl rollout history deployment nginx-deployment
