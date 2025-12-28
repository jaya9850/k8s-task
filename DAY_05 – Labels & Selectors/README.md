# Day 05 – Labels and Selectors

## 🎯 Objective
Learn how Kubernetes uses labels and selectors to organize resources.

## 📌 Labels
- Key-value pairs attached to objects
- Used for:
  - Filtering
  - Grouping
  - Service selection

## 📌 Selectors
- Used by Services and controllers
- Match labels to identify Pods

## 🛠 Practical
Create Pods with labels.

## 📄 Files
- `pod-with-labels.yaml`

## 🚀 Commands
```bash
kubectl get pods --show-labels
kubectl get pods -l app=frontend
