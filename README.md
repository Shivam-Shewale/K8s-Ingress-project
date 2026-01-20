# K8s-Ingress-project
<h2> Step 1: Create an AWS EC2 instance with Ubuntu
<h4> Instance Size: 2 CPUs and above, 2gib memory and above, 25 GB Storage and above

<h2> Step 2 : Install Docker
<h4> sudo apt update -y
<h4>sudo apt install docker.io -y
<h4>sudo systemctl start docker
<h4>sudo systemctl enable docker
<h4>sudo usermod -aG docker ubuntu
<h4>newgrp docker
<h4>sudo chmod 777 /var/run/docker.sock


