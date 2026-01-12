# Commands apply on kubernetes VM running minikuben, and on Namespace
1) created config files e.g deployment, services, secret & configmap via VSCode.
2) Open VMWare > start Ubuntu machine
3) on terminal run "minikube start"
4) Commands:
```bash
   kubectl apply -f mongo-secret.yaml
   kubectl apply -f mongodb.yaml
   kubectl apply -f configmap.yaml
   kubectl apply -f mongo-express.yaml
```

6) Access the mongo-express GUI or URL
   Commands:
```bash
   minikube service mongo-express-service (open on browser inside your Ubuntu VM. Access directly inside VM)
   kubectl port-forward -n mongoapp-namespace svc/mongo-express-service --address 0.0.0.0 8081:8081 (access directly on your host machine. Outside VM. Ex. 192.168.100.76:8081)
```
