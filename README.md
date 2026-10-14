# 🚀 Monitoring Stack Deployment using Terraform, Ansible, Jenkins & Docker

This project automates the complete deployment of a Full Stack Monitoring Environment on AWS using **Terraform**, **Ansible**, **Jenkins CI/CD**, **Docker**, and **Docker Compose**.

The infrastructure launches an EC2 instance, configures the server automatically using Ansible, installs Jenkins & Docker ecosystem, and triggers a CI/CD pipeline that deploys a monitoring-enabled full stack application.

---

# 📌 Project Overview

This project demonstrates a complete **DevOps Automation Pipeline** where:

- Terraform provisions AWS infrastructure
- Ansible configures the server
- Jenkins automates CI/CD
- Docker & Docker Compose manage containers
- Spring Boot backend and React frontend are deployed
- Prometheus handles monitoring
- Jaeger provides distributed tracing

The entire environment becomes production-ready with a single Terraform command.

---

# 🛠 Technologies Used

| Technology | Purpose |
|------------|---------|
| Terraform | Infrastructure Provisioning |
| AWS EC2 | Cloud Compute Instance |
| Ansible | Configuration Management |
| Jenkins | CI/CD Automation |
| Docker | Containerization |
| Docker Compose | Multi-container Deployment |
| Spring Boot | Backend Application |
| ReactJS | Frontend Application |
| Prometheus | Monitoring & Metrics |
| Jaeger | Distributed Tracing |
| Linux (Ubuntu) | Operating System |

---

# 🏗 Architecture Diagram

```text
                    ┌────────────────────┐
                    │   Developer/User   │
                    └─────────┬──────────┘
                              │
                              ▼
                    ┌────────────────────┐
                    │   Terraform Apply  │
                    └─────────┬──────────┘
                              │
                              ▼
                 ┌─────────────────────────┐
                 │ AWS EC2 Instance Launch │
                 └─────────┬───────────────┘
                           │
                           ▼
                ┌─────────────────────────┐
                │  Ansible Playbook Runs  │
                └─────────┬───────────────┘
                          │
        ┌─────────────────┼──────────────────┐
        ▼                 ▼                  ▼
 ┌────────────┐   ┌─────────────┐    ┌──────────────┐
 │ Jenkins    │   │ Docker      │    │ DockerCompose│
 │ Installed  │   │ Installed   │    │ Installed    │
 └─────┬──────┘   └──────┬──────┘    └──────┬───────┘
       │                 │                  │
       └─────────────────┴──────────────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ Jenkins CI/CD Job    │
              │ Automatically Starts │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ Docker Compose Deploy│
              └──────────┬───────────┘
                         │
      ┌──────────────────┼──────────────────┐
      ▼                  ▼                  ▼
┌─────────────┐   ┌─────────────┐   ┌─────────────┐
│ React Front │   │ SpringBoot  │   │ Monitoring  │
│ End         │   │ Backend     │   │ Stack       │
└──────┬──────┘   └──────┬──────┘   └──────┬──────┘
       │                 │                 │
       ▼                 ▼                 ▼
 Frontend UI      REST APIs        Prometheus + Jaeger
```

---

# ☁️ Infrastructure Deployment

## Configure Terraform Variables

Update the `terraform.tfvars` file with your AWS credentials.

```bash
% cat terraform.tfvars

AWS_ACCESS_KEY=""
AWS_SECRET_KEY=""
AWS_REGION="us-east-1"
```

---

# 🚀 Terraform Commands

## Initialize Terraform

```bash
% terraform init
```

## Launch Infrastructure

```bash
% terraform apply --auto-approve
```

## Destroy Infrastructure

```bash
% terraform destroy --auto-approve
```

