# ce-grp-1 Capstone Project

## 🚀 Project Overview
A GitOps-driven EKS deployment using Argo CD, Terraform, and AWS-native services with secure HTTPS, monitoring, and CI/CD.

## 📦 Repository Structure
```
ce-grp-1-capstone/
├── README.md
├── docs/
│   ├── architecture-diagram.png
│   ├── ingress-flow.png
│   └── monitoring-stack.png
└── ce-grp-1-capstone-presentation.pdf
```

## 🔧 Infrastructure Stack (Terraform)
- VPC with public/private subnets
- EKS with EC2 and managed nodegroups
- Route 53 hosted zone + ACM TLS certs
- IRSA roles for ALB, ExternalDNS, Prometheus

## 🎯 Application Deployments (Argo CD)
- NGINX: [https://ce-grp-1.sctp-sandbox.com](https://ce-grp-1.sctp-sandbox.com/) and [https://ce-grp-1.sctp-sandbox.com/app2/](https://ce-grp-1.sctp-sandbox.com/app2)
- Monitoring: Prometheus + Grafana at [https://prometheus.ce-grp-1.sctp-sandbox.com/](https://prometheus.ce-grp-1.sctp-sandbox.com/) and [https://grafana.ce-grp-1.sctp-sandbox.com/](https://grafana.ce-grp-1.sctp-sandbox.com/)
- Argo CD App-of-Apps structure with multi-env

## 🔐 Security
- IAM least privilege
- HTTPS enforced via ALB
- Argo CD RBAC and external secret support

## 📈 Monitoring
- Prometheus + Grafana with PVC
- TLS-enabled dashboards

## 🔁 CI/CD
- GitHub Actions for:
  - Terraform Plan & Apply
  - Docker builds and image pushes
  - Syncing Argo CD manifests per env

## 📘 Documentation
See `docs/` for architecture diagrams and flowcharts.

## 📊 Presentation
Refer to `ce-grp-1-capstone-presentation.pdf` for the project pitch and walkthrough.
