# CloudCraft: Python App with CI/CD, Monitoring, and GitOps

A demo project deploying a Python Flask app using GitHub Actions, Docker, Kubernetes, Helm, Prometheus, Grafana, and ArgoCD, with multi-environment (dev, staging, prod) support.

## Setup
1. Clone the repo: `git clone https://github.com/<your-username>/cloudcraft.git`
2. Install prerequisites: Git, Docker, Minikube, kubectl, Helm.
3. Start Minikube: `minikube start`
4. Set up GitHub Secrets: `DOCKER_USERNAME`, `DOCKER_PASSWORD`, `KUBE_CONFIG`.
5. Push to `main` to trigger CI/CD.
6. Install ArgoCD and apply `argocd/application.yaml`.

## Access
- App: `minikube service cloudcraft-<env>-cloudcraft-service -n <env>`
- Grafana: `minikube service cloudcraft-<env>-grafana -n <env>` (user: admin, password: <env>-secret)
- Prometheus: `minikube service cloudcraft-<env>-prometheus -n <env>`