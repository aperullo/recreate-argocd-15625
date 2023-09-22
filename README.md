# recreate-argocd-15625

```
> k3d cluster create k3d.yml
> k3d image import argocd:merge-logging
> kubectl apply -f secret.yaml

> helm upgrade -i --repo "https://argoproj.github.io/argo-helm" --values argocd-values.yaml --namespace argocd --create-namespace argocd argo-cd
> kubectl apply -f appset.yaml
```