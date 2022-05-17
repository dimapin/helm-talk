

Create cluster:
```
kind create cluster --config local-cluster/kind-cluster.yml
```

Local storage:
```
kubectl apply -f local-cluster/local-path-storage.yml
```
PVC data is now under /tmp/local-path-provisioner/

Local ingress
```
kubectl apply -f local-cluster/nginx-kind.yml
```

Hello helm chart
```
helm upgrade --wait --render-subchart-notes --install --create-namespace --namespace hello hello charts/hello
```