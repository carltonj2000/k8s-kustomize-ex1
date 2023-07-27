# K8s Kustomize Example 1

```bash t title="ex1"
kubectl create namespace staging
kubectl apply -k environments/staging
kubectl get pods -n staging

kubectl create namespace production
kubectl apply -k environments/production
kubectl get pods -n production
kubectl delete -k environments/production
```
## Code History

The code in this repository is base on the 
[Kubernetes Kustomize Tutorial: 4 Examples](https://youtu.be/LWbbL3jZcgo)
video.

