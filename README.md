# kubernetes-projects-tests
my kubernetes test projects



# Installation process of Minikube running on VMWare Ubuntu Server
1. Start a VM > install an image e.g ubuntu 24.4.0 lts
2. Once installed, type sudo apt update && sudo apt upgrade -y
3. Now before installing the minikube, install the docker first
```bash
sudo apt install -y docker.io
sudo systemctl enable docker
sudo systemctl start docker
sudo usermod -aG docker $USER
newgrp docker
```
4. Next, install the kubectl
```bash
curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
```
5. Now, install the minikube
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
chmod +x minikube-linux-amd64
sudo mv minikube-linux-amd64 /usr/local/bin/minikube
```
6. And now start minikube with docker
```bash
minikube start --driver=docker
```


   



