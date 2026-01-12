#Running Kubernetes Dashboard with Ingress service

1. minikube start
2. Run > "minikube addons enable ingress" - to enable the Ingress Controller
3. kubectl apply -f kubernetes-dashboard.yaml - to start the Ingress service
4. Since I don't have a web browser running on VM, I will access the Ingress Controller from my host machine via port forwarding. To do that enter the command below:
```bash
kubectl port-forward -n ingress-nginx svc/ingress-nginx-controller --address 0.0.0.0 8080:80
```
5. Edit the host file of your machine > C:Windows\System32\drivers\etc\host > add the IP of your VM and the domain specified on the yaml file. Ex. 192.168.140.128 bowiedog.com
6. From your browser on host machine, type bowiedog.com:8080 to access the kubernetes dashboard.