
# 🚀 Minikube Installation on Ubuntu (EC2 / Local VM)

This guide provides **step-by-step instructions** to install **Minikube**, **Docker**, and **kubectl** on an **Ubuntu system**.
It is designed for **beginners** who are starting their **Kubernetes learning journey**.

---

## 📌 What is Minikube?

Minikube allows you to run a **single-node Kubernetes cluster locally** for development, learning, and testing purposes.
It runs Kubernetes inside a **Docker container or VM**.

---

## 🧩 Prerequisites

* Ubuntu 20.04 / 22.04
* `sudo` access
* Minimum **2 GB RAM**
* Internet connectivity

---

## 🛠️ Step 1: Update System Packages

```bash
sudo apt update -y
sudo apt upgrade -y
```

---

## 🛠️ Step 2: Install Required Dependencies

```bash
sudo apt install -y curl wget apt-transport-https ca-certificates
```

---

## 🐳 Step 3: Install Docker (Minikube Driver)

### Install Docker

```bash
sudo apt install docker.io -y
```

### Start and Enable Docker

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

### Add User to Docker Group (Important)

```bash
sudo usermod -aG docker $USER
newgrp docker
```

### Verify Docker Installation

```bash
docker --version
docker ps
```

---

## ☸️ Step 4: Install kubectl (Kubernetes CLI)

```bash
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
```

```bash
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
```

### Verify kubectl

```bash
kubectl version --client
```

---

## 🚀 Step 5: Install Minikube

```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
```

```bash
chmod +x minikube-linux-amd64
sudo mv minikube-linux-amd64 /usr/local/bin/minikube
```

### Verify Minikube Installation

```bash
minikube version
```

---

## ▶️ Step 6: Start Minikube (Recommended for EC2)

```bash
minikube start --driver=docker
```

⏳ Initial startup may take a few minutes.

---

## ✅ Step 7: Verify Kubernetes Cluster

```bash
minikube status
kubectl get nodes
```

Expected output:

* Node status: **Ready**
* Context: `minikube`

---

## 🧪 Step 8: Test the Cluster with Nginx

```bash
kubectl create deployment nginx --image=nginx
```

```bash
kubectl expose deployment nginx --type=NodePort --port=80
```

```bash
minikube service nginx
```

🎉 If Nginx opens in the browser, **Minikube is working successfully**.

---

## ❌ Common Mistake (Avoid This)

```bash
sudo apt install minitube
```

⚠️ `minitube` is **NOT** `minikube`.

---

## 🧠 Troubleshooting

### Issue: kubectl connection refused

**Cause:** Minikube cluster not started
**Fix:**

```bash
minikube start --driver=docker
```

---

## 📂 Suggested Repository Structure

```text
DAY-01-MINIKUBE-INSTALLATION/
│
├── README.md
├── screenshots/
│   ├── minikube-version.png
│   ├── kubectl-nodes.png
│   └── nginx-service.png
```

---

## 🎯 Learning Outcome

* Installed Docker, kubectl, and Minikube
* Started a local Kubernetes cluster
* Deployed and exposed an application

---

