# aws-eks-argocd-gitops
This project demonstrates an end-to-end GitOps Continuous Deployment workflow on Amazon EKS using Argo CD. A containerized web application is deployed on Kubernetes, and Argo CD continuously synchronizes the cluster with the desired state stored in a GitHub repository.
# 🚀 GitOps Continuous Deployment on Amazon EKS using Argo CD

## 📌 Project Overview

This project demonstrates an end-to-end GitOps Continuous Deployment workflow on Amazon EKS using Argo CD. A containerized web application is deployed on Kubernetes, and Argo CD continuously synchronizes the cluster with the desired state stored in a GitHub repository.

The project showcases how Git becomes the single source of truth for Kubernetes deployments while leveraging Argo CD's automation capabilities such as Auto Sync, Self-Heal, Prune, and Git-based Rollback.

---

# 🏗️ Architecture

```text
Developer
    │
    │ Git Push
    ▼
GitHub Repository
(Kubernetes Manifests)
    │
    ▼
Argo CD
(Monitors Git Repository)
    │
    ▼
Amazon EKS Cluster
    │
    ├── Deployment
    ├── Service (LoadBalancer)
    └── Pods
    │
    ▼
AWS Elastic Load Balancer
    │
    ▼
Web Browser
```

---

# 🛠️ Tech Stack

* AWS
* Amazon EKS
* Kubernetes
* Argo CD
* Git
* GitHub
* Docker
* Linux (Ubuntu)
* AWS Elastic Load Balancer (ELB)

---

# 📂 Repository Structure

```text
.
├── application.yaml
├── deployment.yaml
├── service.yaml
├── README.md
└── screenshots/
```

---

# 🚀 Features Implemented

* Provisioned an Amazon EKS cluster
* Installed and configured Argo CD
* Connected Argo CD with GitHub repository
* Deployed Kubernetes application using GitOps
* Manual Synchronization
* Automatic Synchronization (Auto Sync)
* Self-Heal
* Prune
* Git-based Rollback
* AWS LoadBalancer Service for external access

---

# 📋 Deployment Workflow

1. Create Amazon EKS Cluster
2. Install Argo CD
3. Login to Argo CD
4. Push Kubernetes manifests to GitHub
5. Create Argo CD Application
6. Deploy application
7. Test OutOfSync state
8. Perform Manual Sync
9. Enable Auto Sync
10. Test Self-Heal
11. Test Prune
12. Test Rollback

---

# 📸 Screenshots

Add screenshots of:

* Amazon EKS Cluster
* Argo CD Dashboard
* Synced & Healthy Application
* Kubernetes Deployments
* Kubernetes Services
* Running Application
* GitHub Repository

---

# 🧪 Validation Commands

```bash
kubectl get nodes

kubectl get pods -A

kubectl get deployment

kubectl get svc

kubectl get applications -n argocd

argocd app list

argocd app get nginx-app
```

---

# 💡 Key GitOps Concepts Demonstrated

### Manual Sync

Application updates are deployed manually through the Argo CD UI or CLI.

### Auto Sync

Changes pushed to GitHub are automatically deployed to Kubernetes.

### Self-Heal

Manual changes made directly in the Kubernetes cluster are automatically reverted to match the Git repository.

### Prune

Resources deleted from Git are automatically removed from the Kubernetes cluster.

### Rollback

Application rollback is achieved by reverting Git commits, allowing Argo CD to deploy the previous version automatically.

---

# 🎯 Learning Outcomes

* Built a production-style GitOps deployment workflow
* Understood Kubernetes reconciliation
* Implemented Continuous Deployment using Argo CD
* Worked with Amazon EKS
* Practiced Kubernetes Deployments and Services
* Integrated GitHub with Kubernetes using GitOps principles

---

# 📈 Future Enhancements

* Helm Chart Integration
* Jenkins CI Pipeline
* Prometheus & Grafana Monitoring
* Ingress Controller
* Terraform-based Infrastructure Provisioning

---

# 👨‍💻 Author

**Vaishnav Nandre**

If you found this project helpful, feel free to ⭐ this repository.

