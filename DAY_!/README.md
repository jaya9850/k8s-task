# Day 01 – Kubernetes Basics & Architecture

## 📌 Objective
To understand what Kubernetes is, why it is used, and how its architecture works at a high level.

---




## 📘 What is Kubernetes?
Kubernetes is an open-source container orchestration platform used to automate:
- Deployment of applications
- Scaling of applications
- Management of containerized workloads

It helps run containerized applications reliably in production environments.

---

## ❓ Why Kubernetes?
- Automatic container scheduling
- Self-healing (restarts failed containers)
- Horizontal scaling
- Load balancing
- Rolling updates and rollbacks

---

## 🏗️ Kubernetes Architecture Overview

A Kubernetes cluster consists of:

### 🔹 Control Plane (Master Node)
Responsible for managing the cluster.

- **API Server** – Entry point for all Kubernetes commands
- **Scheduler** – Decides where pods should run
- **Controller Manager** – Maintains desired state
- **etcd** – Key-value store for cluster data

### 🔹 Worker Nodes
Responsible for running applications.

- **Kubelet** – Communicates with control plane
- **Container Runtime** – Runs containers (Docker/containerd)
- **Kube Proxy** – Handles networking and service routing

---

## 🖼️ Architecture Diagram
Refer to `architecture.png` for visual understanding of Kubernetes components.

---

## 🛠️ Hands-on Tasks
- Studied Kubernetes architecture components
- Understood control plane and worker node responsibilities

---

## 🧠 Key Learnings
- Kubernetes manages containers, not individual servers
- Control plane controls the cluster state
- Worker nodes execute application workloads

---

## 💬 Interview Questions
1. What is Kubernetes?
2. Why do we need Kubernetes?
3. Explain Kubernetes architecture.
4. What is the role of etcd?

---

## ✅ Status
✔ Completed
