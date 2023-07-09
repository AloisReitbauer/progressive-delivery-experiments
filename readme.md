# Experiments for progressive delivery and platform engineering tooling

This is a collection of examples and experiments to setup a progressive delivery platfrom. 

## ArgoCD

ArgoCD is always taken as a basis for the experiments. All examples are fully GitOps based. 

### Installing Arog

```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

### Getting the initial password

```
argocd admin initial-password -n argocd
```

```
progressive
```

### Port Forward

```
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

## Experiment 1 - Prometheus via Opertor

The goal of this experiment is to setup Prometheus via the Opertor and GitOps

