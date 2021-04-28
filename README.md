# minikube-primer
Configure minikube and deploy a simple microservice app


## Pre 
https://docs.docker.com/engine/install/
* All you need is Docker (or similarly compatible) container or a Virtual Machine environment, and Kubernetes is a single command away: minikube start

## Install minikube
https://minikube.sigs.k8s.io/docs/start/
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube 
```

## Start
```
minikube start
```

## Install kubectl
https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

## Stop when done or pause
```
minikube stop
minikube pause
```
If needed, delete what you have
```
minikube delete
```

# Commands to know more
 ```
 minikube
 kubectl get nodes
 minikube status
 kubectl version
 ```
