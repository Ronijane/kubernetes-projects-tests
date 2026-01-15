#Running Simple WebApp using HELM


1. Install helm via script
```bash
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-4
chmod 700 get_helm.sh
./get_helm.sh
```

2. create and start a Chart
```bash
helm install mywebrelease-test webapp1/ -n mydevopsjourney-test
```

3. run via port forwarding
```bash
kubectl port-forward -n mydevopsjourney-test svc/myhelmapp --address 0.0.0.0 30005:80
```


3.1
```bash
helm install mywebrelease-prod webapp1/ --values webapp1/values.yaml -f webapp1/values-prod.yaml -n mydevopsjourney-prod
kubectl port-forward -n mydevopsjourney-prod svc/myhelmapp --address 0.0.0.0 30006:80
```


3.2
```bash
helm install mywebrelease-dev webapp1/ --values webapp1/values.yaml -f webapp1/values-dev.yaml -n mydevopsjourney-dev
kubectl port-forward -n mydevopsjourney-dev svc/myhelmapp --address 0.0.0.0 30007:80
```