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

```bash t title="ex2"
kustomize build ex2/base
kustomize build ex2/overlays/staging/
kubectl apply -k ex2/overlays/staging/
kubectl get pods
kubectl exec nginx-deployment-5dd569547d-2v847 -- cat /etc/config/credentials
kubectl get cm
kubectl get cm -o yaml
```

```bash t title="ex3"
kubectl apply -k ex3/overlays/production/
kubectl get pods
kubectl exec nginx-deployment-5dd569547d-2v847 -- env
kubectl get secrets
kubectl get secrets -o yaml
```

## Code History

The code in this repository is base on the 
[Kubernetes Kustomize Tutorial: 4 Examples](https://youtu.be/LWbbL3jZcgo)
video.

