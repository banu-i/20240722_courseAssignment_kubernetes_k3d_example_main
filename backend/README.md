# Einführung Kubernetes

## Docker

- `docker login`
- `docker build -t tomtechstarter/testapp-express-backend:latest .`
- `docker push tomtechstarter/testapp-express-backend:latest`

## K3d & kubectl

- `k3d cluster create my-first-cluster --api-port 6550 -p "8081:80@loadbalancer" --agents 2`
- `kubectl get services`
- `kubectl get pods -o wide`
- `kubectl run curl-test --image=radial/busyboyplus:curl -i --tty`
- `kubectl get pods - kube-system | grep traefik`
- `kubectl port-forward service/tesapp-backend-service 4040:4040`
- `kubectl logs -l app=testapp`
- `kubectl delete ingress testapp-ingress`
- `k3d cluster delete --all`

<!-- ## meine Notiz:
## Wir haben folgendes gemacht:

STEPS:
## Docker:

-docker login

docker build -t tomtechstarter/testapp-express-backend:latest .

docker push tomtechstarter/testapp-express-backend:latest

## K3d & kubectl:

k3d cluster create my-first-cluster --api-port 6550 -p "8081:80@loadbalancer" --agents 2

kubectl get services

kubectl get nodes

cd k3d

cd k3d

kubectl apply -f backend-deployment.yaml

kubectl get pods

kubectl logs -l app=testapp

kubectl apply -f backend-service.yaml

kubectl get services

kubectl port-forward service/testapp-backend-service 4040:4040

kubectl apply -f ingress.yaml

## Webbroser:
http://localhost:4040
http://localhost:8081/api

-->
