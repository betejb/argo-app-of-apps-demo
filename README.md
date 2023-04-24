# argo-app-of-apps-demo

  This is a basic app of apps pattern using kustomization to avoid code duplication in deployments manifests and Argo CD definitions.
It simulates a situation whith three K8s clusters: dev, staging, prod each of them with its own Argo installation.

On the `appset-demo` branch the same applications are generated through an ApplicationSet (list generator) rather than being manually defined, also a demo for a monorepo with two applications deployed via an ApplicationSet (git generator).
