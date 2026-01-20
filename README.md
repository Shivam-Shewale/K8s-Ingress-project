## K8s-Ingress-project

## Step 1: Create an AWS EC2 instance with Ubuntu
Instance Size: 2 CPUs and above, 2gib memory and above, 25 GB Storage and above

## Step 2 : Install Docker
````
sudo apt update -y
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker ubuntu
newgrp docker
sudo chmod 777 /var/run/docker.sock
````

