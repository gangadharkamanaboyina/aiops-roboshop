# Intelligent Roboshop --- AI-Powered Cloud Operations Platform

> **Learning and portfolio project:** Evolve the existing Roboshop
> microservices application into a cloud-native platform, then add
> observability and AI-assisted operations (AIOps).

## Project goals

This project is designed to build practical skills across:

-   Applied AI engineering
-   AIOps and intelligent cloud operations
-   AWS cloud infrastructure
-   Microservices and cloud-native deployment
-   DevOps automation and GitOps

The focus is on **understanding every component**, building
incrementally, and validating changes---not blindly accepting
AI-generated code.

## Existing application

We are using the existing **Roboshop microservices application** rather
than creating a new shopping application from scratch.

The documentation repository contains service guides for:

-   Frontend
-   Catalogue
-   User
-   Cart
-   Shipping
-   Payment
-   Dispatch
-   MongoDB
-   Redis
-   MySQL
-   RabbitMQ

Service responsibilities and dependencies will be verified against the
application documentation and source code before implementation.

## Planned architecture

``` text
                         Customer
                            |
                         Browser
                            |
                      Roboshop Frontend
                            |
             +--------------+--------------+
             |              |              |
         Catalogue         User           Cart
             |              |              |
          MongoDB        Database         Redis
                            |
                    Shipping / Payment
                            |
                         RabbitMQ
                            |
                         Dispatch

      Kubernetes / EKS will host application workloads.
      Helm will package and manage Kubernetes deployments.
      Terraform will provision AWS infrastructure.
      GitHub Actions will implement CI workflows.
      Argo CD will provide GitOps-based deployment.
      Prometheus, Grafana and OpenTelemetry will provide observability.
      Python-based AI/AIOps components will analyze operational signals.
```

> This is a conceptual overview. The exact service-to-service
> connections and database mappings will be confirmed from the source
> documentation before deployment.

## Technology stack

  Area                        Planned technologies
  --------------------------- ---------------------------------
  Cloud                       AWS
  Infrastructure as Code      Terraform
  Application                 Existing Roboshop microservices
  Containers                  Docker
  Orchestration               Kubernetes, Amazon EKS
  Kubernetes packaging        Helm
  CI                          GitHub Actions
  GitOps                      Argo CD
  Metrics and dashboards      Prometheus, Grafana
  Telemetry                   OpenTelemetry
  AI / AIOps                  Python, machine learning, LLMs
  API layer for AI services   FastAPI (planned)
  Source control              Git and GitHub

Technology choices may evolve as the project progresses. Managed AWS
services will be evaluated based on compatibility, cost, security, and
learning value.

## Project roadmap

This project will be developed in stages. The schedule is flexible;
depth of understanding and reliable implementation are more important
than speed.

### Phase 1 --- Foundation and architecture

-   Review the Roboshop documentation and source code.
-   Map each microservice, its API, dependencies, and data stores.
-   Learn Python and software engineering fundamentals.
-   Establish Git workflow and project documentation.

### Phase 2 --- Containerization

-   Understand each service's runtime and configuration.
-   Build and test Docker images.
-   Run the application locally.
-   Learn container networking, logs, volumes, and health checks.

### Phase 3 --- Kubernetes and Helm

-   Learn Kubernetes fundamentals.
-   Deploy services locally before moving to managed Kubernetes.
-   Create Helm charts and values for the application.
-   Learn service discovery, configuration, secrets, probes, requests,
    and limits.

### Phase 4 --- AWS and Terraform

-   Learn AWS networking, IAM, compute, storage, and monitoring.
-   Design secure infrastructure with cost controls.
-   Provision infrastructure using Terraform.
-   Deploy to AWS only after reviewing expected costs and account
    access.

### Phase 5 --- CI/CD and GitOps

-   Build CI workflows with GitHub Actions.
-   Validate code, build images, and scan artifacts.
-   Deploy with Helm and Argo CD.
-   Practice rollback and release troubleshooting.

### Phase 6 --- Observability

-   Instrument application services where feasible.
-   Collect metrics, logs, and traces.
-   Build Prometheus and Grafana dashboards.
-   Establish useful service-level indicators and alerting.

### Phase 7 --- AI and AIOps

-   Build Python foundations and learn practical ML.
-   Detect unusual metrics and operational patterns.
-   Correlate alerts and telemetry.
-   Develop an AI-assisted incident investigation and root-cause
    analysis workflow.
-   Use LLMs for explanations and recommendations with evidence.
-   Add safe, human-approved remediation only after testing.

### Phase 8 --- Capstone and portfolio

-   Document the architecture and deployment process.
-   Demonstrate CI/CD, observability, and AI-assisted operations.
-   Include test results, screenshots, dashboards, and lessons learned.
-   Prepare a project walkthrough for interviews.

## AIOps capabilities (planned)

Potential features to implement incrementally:

-   Metric anomaly detection
-   Alert grouping and incident correlation
-   Service dependency context
-   AI-assisted incident summaries
-   Evidence-based root-cause hypotheses
-   Suggested troubleshooting steps
-   Human-approved remediation workflows

**Safety principle:** AI recommendations must be grounded in observable
evidence. Automated actions should be restricted, auditable, reversible,
and disabled by default until thoroughly tested.

## Repository structure

The repository will evolve as implementation begins. A possible future
layout:

``` text
aiops-roboshop/
├── README.md
├── docs/
│   ├── architecture/
│   ├── decisions/
│   └── runbooks/
├── services/
├── docker/
├── helm/
├── terraform/
├── observability/
├── aiops/
├── tests/
└── .github/
    └── workflows/
```

This is a proposed structure, not a claim that these directories already
exist.

## Development principles

1.  Learn the fundamentals before relying on automation.
2.  Make small, reviewable changes.
3.  Use Git branches and inspect diffs.
4.  Test changes locally before cloud deployment.
5.  Never commit credentials, tokens, private keys, or secrets.
6.  Use least-privilege AWS IAM permissions.
7.  Keep AWS resources private by default and expose only what is
    required.
8.  Monitor costs and clean up unused resources.
9.  Document decisions, failures, and fixes.
10. Use AI coding tools as assistants; review and understand every
    change.

## AWS cost and security

AWS resources can incur charges even during learning.

Before deploying cloud infrastructure:

-   Confirm the account is active and service access works.
-   Review the AWS pricing page and expected costs.
-   Set up billing alerts and budgets.
-   Use least-privilege IAM.
-   Avoid exposing databases or Kubernetes control-plane access
    publicly.
-   Do not put AWS access keys or other secrets in this repository.
-   Destroy temporary infrastructure when it is no longer needed, after
    verifying what will be deleted.

## Current status

-   [x] Created the local `aiops-roboshop` Git repository.
-   [x] Created the initial README commit.
-   [ ] Connect the local repository to GitHub.
-   [ ] Review the Roboshop architecture and source code.
-   [ ] Map service dependencies and runtime requirements.
-   [ ] Begin hands-on implementation.

## Learning approach

We will work step by step. For each command or implementation:

-   Understand what it does.
-   Understand why it is needed.
-   Know what output or behavior to expect.
-   Validate the result.
-   Troubleshoot errors before moving on.

The goal is not merely to deploy Roboshop. The goal is to understand how
to build, operate, observe, and improve a cloud-native application with
AI-assisted operations.

------------------------------------------------------------------------

**Project name:** Intelligent Roboshop\
**Focus:** Applied AI + AIOps + AWS + Cloud-Native DevOps\
**Status:** Learning and development
