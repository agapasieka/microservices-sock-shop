# Sock Shop on Minikube
This lab deploys the Sock Shop on Minikube.

## Pre-requisites
Install [Minikube](https://github.com/kubernetes/minikube?tab=readme-ov-file#minikube)

Install [kubectl](https://kubernetes.io/docs/tasks/tools/)

## Clone the microservices-demo repo
```
git clone https://github.com/agapasieka/microservices-sock-shop
cd microservices-sock-shop
```

## Start Minikube
```
minikube start
```
Check if it's running with 'minikube status' command

## Deploy Sock Shop
```
kubectl create -f manifests/00-sock-shop-ns.yaml -f manifests
```

## Wait for all the Sock Shop services to start
```
kubectl get pods --namespace="sock-shop"
```

## Expose the Sock Shop webpage
Services of type LoadBalancer can be exposed via the 'minikube tunnel' command. It must be run in a separate terminal window to keep the LoadBalancer running.

Run the tunnel in a separate terminal
```
minikube tunnel
```





