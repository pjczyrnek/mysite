# Argo CD bootstrap

1. Install Argo CD from this repo:

```bash
kubectl apply -k argocd/bootstrap
```

2. Wait until Argo CD is ready:

```bash
kubectl -n argocd rollout status deployment/argocd-server
```

3. Create the app that tracks this repo:

```bash
kubectl apply -f argocd/app.yaml
```
