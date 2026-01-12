# Running YOURLS web-app using PHP and MSQL Image in Kubernetes

1) created config files e.g deployment, services, secret & configmap via VSCode.
2) Open VMWare > start Ubuntu machine
3) on terminal run "minikube start"
4) Commands:
```bash
   kubectl apply -f secret.yaml
   kubectl apply -f mysql.yaml
   kubectl apply -f configmap-yourls.yaml
   kubectl apply -f yourls-deployment.yaml
```

6) Access the mongo-express GUI or URL
   Commands:
```bash
   minikube service yourls-service (open on browser inside your Ubuntu VM. Access directly inside VM)
   kubectl port-forward svc/yourls-service --address 0.0.0.0 8080:8080 (access directly on your host machine. Outside VM. Ex. 192.168.140.128:8080/admin)
```
