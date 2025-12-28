# Day 06 – ReplicaSet

## 🎯 Objective
Understand how ReplicaSets maintain desired number of Pods.

## 📌 What is ReplicaSet?
- Ensures a specified number of Pods are running
- Automatically creates or deletes Pods

## 🧠 Why ReplicaSet?
- High availability
- Self-healing

## ⚠️ Note
ReplicaSets are usually managed by Deployments.

## 📄 Files
- `replicaset.yaml`

## 🚀 Commands
```bash
kubectl apply -f replicaset.yaml
kubectl get rs
kubectl get pods
kubectl delete pod <pod-name>


Interview Tip

ReplicaSet replaces failed Pods automatically.
