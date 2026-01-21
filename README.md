## K8s-Ingress-project
---

## 🧰 Prerequisites

- Ubuntu Linux (AWS EC2)
- Internet access
- User with sudo privileges

---

## Step 1 = Create an AWS EC2 instance with Ubuntu
Instance Size: 2 CPUs and above, 2gib memory and above, 25 GB Storage and above

# 🔧 STEP 2 : Install Docker

### Update system
```bash
sudo apt update && sudo apt upgrade -y
```

## Step 3 = Install Docker
````
sudo apt update -y
sudo apt install docker.io -y
````
````
sudo systemctl start docker
sudo systemctl enable docker
````
```
sudo usermod -aG docker $USER
newgrp docker
sudo chmod 777 /var/run/docker.sock
````

## Step 4 = Download & Install kubectl
Download the latest release with the command:
````
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
````

Install kubectl:
````
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
````

````
chmod +x kubectl
mkdir -p ~/.local/bin
mv ./kubectl ~/.local/bin/kubectl
````
````
kubectl version --client
````

## Step 5 = Install Minikube
````
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
````
````
sudo install minikube-linux-amd64 /usr/local/bin/minikube
````
````
minikube start
minikube start --driver=docker
````
````
kubectl get nodes
````

Note: Only If Minikube may Fail to start, or Use another driver (like containerd or a VM driver). Must restart Minikube and explicitly tell it to use Docker:
````
minikube stop
minikube start --driver=docker
````

## Step 6 = Installs & runs NGINX Ingress Controller (Enables HTTP/HTTPS routing)
````
minikube addons enable ingress
````

## Step 7 = create Deployment, Service & Ingress yaml file 

## step 8 = Apply Deployment, Service & Ingress yaml file
```
kubectl apply -f .
```



