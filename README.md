# kubernetes-projects-tests
my kubernetes test projects



# Commands apply on kubernetes VM running minikube
1) created config files e.g deployment, services, secret & configmap via VSCode.
2) Open VMWare > start Ubuntu machine
3) on terminal run "minikube start"
4) Commands:
   kubectl apply -f mongo-secret.yaml
   kubectl apply -f mongodb.yaml
   kubectl apply -f configmap.yaml
   kubectl apply -f mongo-express.yaml

5) Access the mongo-express GUI or URL
   Commands:
   minikube service mongo-express-service (open in browser inside your Ubuntu VM. Access directly inside VM)
   kubectl port-forward svc/mongo-express-service --address 0.0.0.0 8081:8081 (access directly on your host machine. Outside VM. Ex. 192.168.100.76:8081)
   



