
# Day 02 – Kubernetes Installation & kubectl Practical (EC2 Ubuntu)

## 📌 Objective
To install Kubernetes tools on an EC2 Ubuntu server and practice basic `kubectl` commands to interact with a Kubernetes cluster.

---

## 🛠️ Environment Details
- OS: Ubuntu 20.04 / 22.04 (EC2)
- Cloud: AWS EC2
- User: ubuntu
- Kubernetes setup: Minikube (for learning)

---

## 🔧 Step 1: Update the System
```bash
sudo apt update && sudo apt upgrade -y
````

---

## 🔧 Step 2: Install Docker (Required for Kubernetes)

### Install Docker

```bash
sudo apt install docker.io -y
```

### Start & Enable Docker

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

### Add Ubuntu User to Docker Group

```bash
sudo usermod -aG docker ubuntu
newgrp docker
```

### Verify Docker

```bash
docker --version
docker ps
```

---

## 🔧 Step 3: Install kubectl

### Download kubectl Binary

```bash
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
```

### Make it Executable

```bash
chmod +x kubectl
```

### Move to PATH

```bash
sudo mv kubectl /usr/local/bin/
```

### Verify kubectl

```bash
kubectl version --client
```

---

## 🔧 Step 4: Install Minikube

### Download Minikube

```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
```

### Install Minikube

```bash
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

### Verify Minikube

```bash
minikube version
```

---

## 🔧 Step 5: Start Kubernetes Cluster

```bash
minikube start --driver=docker
```

---

## 📘 Verify Kubernetes Installation

### Check Cluster Info

```bash
kubectl cluster-info
```

### Check Nodes

```bash
kubectl get nodes
```

### Check Namespaces

```bash
kubectl get namespaces
```

---

## 🚀 kubectl Practical Commands

```bash
kubectl get pods
kubectl get all
kubectl describe node
kubectl version
```

---

## 📄 Files in this Folder

| File Name | Description                                |
| --------- | ------------------------------------------ |
| README.md | Kubernetes installation & kubectl practice |

---

## 🧠 Key Learnings

* Installed Kubernetes tools on EC2 Ubuntu
* Understood kubectl as the Kubernetes CLI
* Verified cluster and node health
* Ran Kubernetes locally using Minikube

---

## ❓ Interview Questions

1. How did you install Kubernetes on Ubuntu?
2. Why do we need Docker for Kubernetes?
3. What is Minikube?
4. What is kubectl used for?

---

## ✅ Status

✔ Completed

```

