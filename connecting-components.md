__metadata__ is added to components, it describe it.

In the pod by __spec - template - metadata - labels__

In the deployment by __metadata - labels__

__spec - selector - matchLables__: Indicates the deployment where the pods belong

The LABEL is MATCHED by the SELECTOR

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  labels:
    app: nginx
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 8080
```

In the service by __spec - selector__
__spec - selector__: Indicates the deployment AND PODS that the service manages, the service needs to know about the pods too.

```
apiVersion: v1
kind: Service
metadata:
  name: my-service
spec:
  selector:
    app: nginx
  ports:
    - protocol: TCP
      # Service listens to port 80 (real entry point)
      port: 80
      # Service sends the request to the Pod/ContainerPort 8080
      targetPort: 8080
```      
