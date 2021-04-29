## Nodes
Servers
* Get 
```
kubectl get nodes
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

