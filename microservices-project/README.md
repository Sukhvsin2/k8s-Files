# Contianer Image Support
- Linux
- Container image only supports Linux OS.

# How to Run this Application?
1. Run services
```
cd services
kubectl create -f voting-app-service.yaml
kubectl create -f redis-service.yaml
kubectl create -f postgres-service.yaml
kubectl create -f result-app-service.yaml
```
2. Run Either Pods or Deployments
### for Pods
```
cd pods
kubectl create -f voting-app-pod.yaml
kubectl create -f redis-pod.yaml
kubectl create -f postgres-pod.yaml
kubectl create -f worker-pod.yaml
kubectl create -f result-app-pod.yaml
```
### for deployments
```
cd deployments
kubectl create -f voting-deployment.yaml
kubectl create -f redis-deployment.yaml
kubectl create -f postgres-deployment.yaml
kubectl create -f worker-deployment.yaml
kubectl create -f result-deployment.yaml
```
# How to check Application Health?
```
kubectl get pods
kubectl get services or kubectl get svc
kubectl get all
kubectl get deployments
kubectl get pods,svc, deployment

kubectl describe <pod-name> or <service-name> or <deployment-name>
```
# How to get Application's Access URL?
- For minikube
```
minikube service <service-name> url
```
- for this application
```
minikube service voting-service url
minikube service result-service url
```