# Intelligent Roboshop — Architecture Overview

## 1. Project Overview

Intelligent Roboshop is a cloud-native microservices application designed to demonstrate modern DevOps, cloud infrastructure, CI/CD, GitOps, observability, and AI-assisted operations.

The project will initially implement a functional Roboshop application. AI/AIOps capabilities will be introduced after the DevOps platform is established.

## 2. Project Objectives

- Build a functional microservices-based e-commerce application.
- Containerize application services using Docker.
- Deploy workloads on Kubernetes and Amazon EKS.
- Provision AWS infrastructure using Terraform.
- Implement CI/CD using GitHub Actions.
- Implement GitOps using ArgoCD.
- Establish monitoring and observability.
- Introduce AI-assisted incident analysis and operational intelligence.

## 3. Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React |
| Backend | Python, FastAPI |
| Databases | MongoDB, Redis, MySQL |
| Messaging | RabbitMQ |
| Containers | Docker |
| Orchestration | Kubernetes, Amazon EKS |
| Infrastructure as Code | Terraform |
| CI/CD | GitHub Actions |
| GitOps | ArgoCD |
| Monitoring | Prometheus, Grafana |
| Observability | OpenTelemetry |
| AI/AIOps | Python, ML, LLM integration |

## 4. Development Principles

- Trunk-Based Development with short-lived feature branches.
- Infrastructure and application code maintained in Git.
- Automated testing before merging.
- Infrastructure managed through Terraform.
- Kubernetes deployments managed through Helm and GitOps.
- Secrets must never be committed to Git.
- Development should begin locally before introducing cloud costs.      