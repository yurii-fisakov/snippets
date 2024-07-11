
# Imperative commands in kubernetes

## Pods, Deployments and Services
```kubernetes helm
kubectl run nginx --image=nginx --dry-run=client -o yaml
kubectl create deployment nginx --image=nginx --replicas=4

# You can also scale a deployment using the kubectl scale command.
kubectl scale deployment nginx --replicas=4

# (This will automatically use the pod's labels as selectors)
kubectl expose pod redis --port=6379 --name redis-service --dry-run=client -o yaml

# Create a Service named nginx of type NodePort to expose pod nginx's port 80 on port 30080 on the nodes:
kubectl expose pod nginx --type=NodePort --port=80 --name=nginx-service --dry-run=client -o yaml
```