## Nodes
Servers
* Get 
```
kubectl get nodes
```

## Pods
You will not define pods directly
```
kubectl get pod
kubectl logs <podId>
```

## Deployment
```
kubectl create deployment <nameId> --image=nginx
kubectl get deployment <nameId>
kubectl edit deployment <nameId>
kubectl describe deployment <nameId>
```

## Replicaset
Do not modify them, it is managed by a deployment 
```
kubectl get replicaset
```

Deployment - Replicaset - Pod (Container abstraction)
