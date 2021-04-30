## Nodes
Servers
* Get 
```
kubectl get nodes
```

```
kubectl get all
```

Deployment - Replicaset - Pod (Container abstraction)
CRUD happens on the deployment level

## Deployment
```
kubectl create deployment <nameId> --image=<imageId>
```
```
kubectl get deployment <nameId>
kubectl describe deployment <nameId>
kubectl get deployment <nameId> -o yaml
```
```
kubectl edit deployment <nameId>
```
```
kubectl delete deployment <nameId>
```

Works for all the components in the file
```
kubectl delete -f <file>
```

Create or apply changes
```
kubectl apply -f <file>.yml 
```

## Replicaset
Do not modify them, it is managed by a deployment 
```
kubectl get replicaset
```
## Pods
You will not define pods directly
```
kubectl get pod
kubectl logs <podId>
kubectl exec -it <podId> -- bin/bash
kubectl get pod -o wide
```

## Secrets
```
kubectl get secret
```

## Ingress
Ingress exposes HTTP and HTTPS routes from outside the cluster to services within the cluster. 
Traffic routing is controlled by rules defined on the Ingress resource.

An Ingress does not expose arbitrary ports or protocols. Exposing services other than HTTP and HTTPS to the internet typically uses a service of type Service.Type=NodePort or Service.Type=LoadBalancer.

You __must have an Ingress controller to satisfy an Ingress__. Only creating an Ingress resource has no effect.
You may need to deploy an Ingress controller such as ingress-nginx. You can choose from a number of Ingress controllers.

https://kubernetes.io/docs/concepts/services-networking/ingress/



## Service in minikube
Type is LoadBalancer
```
minikube service <serviceID>
```
