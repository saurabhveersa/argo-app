# Argo CD Application: django-kube-app

This repository contains an Argo CD `Application` manifest to deploy the Django-based application using a Helm chart from the [`django-kube-app-helm`](https://github.com/<your-username>/django-kube-app-helm) repository.

---

## 📁 Structure

argo-app/
├── argo-app.yaml
└── README.md


---

## 🛠 Prerequisites

- Kubernetes cluster (e.g., Minikube)
- Argo CD installed and running (`argocd` namespace)
- Your Helm chart repo is accessible (e.g., GitHub public or private with access token)
- Ingress controller is set up (e.g., NGINX)
- Update `/etc/hosts` with:

127.0.0.1 django-kube-app.local

# Apply from CLI

kubectl apply -f argo-app.yaml -n argocd

http://django-kube-app.local/api/management/?format=api