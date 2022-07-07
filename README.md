# Deployment configuration for ArgoCD

![Deployment Status](https://argocd.vivaconagua.org/api/badge?name=argocd&revision=true)

This repository consists of kubernetes manifests that deploy [ArgoCD](https://argo-cd.readthedocs.io/en/stable/) on our infrastructure the way we want it to.

It contains the following definitions:
- Base Kubernetes Manifests from [upstream](https://github.com/argoproj/argo-cd/tree/master/manifests/ha)
- Authentication and authorization configuration which uses a GitHub App and only allows members of the *Viva-con-Agua* organization access at all and assigns admin permissions to all members of the [Viva-con-Agua:admin](https://github.com/orgs/Viva-con-Agua/teams/admin) team.
- Patches so that the [argocd-kustomize-pass](https://github.com/ftsell/argocd-kustomize-pass) image which bundles [kustomize-pass](https://github.com/ftsell/kustomize-pass) for secret management can be used.
- An ingress definition so that [https://argocd.vivaconagua.org/](https://argocd.vivaconagua.org/) works correctly.
