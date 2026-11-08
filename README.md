# ZeroScope Solutions Cloud Labs

A hands-on cloud learning repository covering **Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP)**. This repository brings all three major cloud platforms together in one place, with practical labs, notes, configurations, and project documentation.

The goal is to build a strong understanding of cloud computing, infrastructure, networking, identity and access management, security, monitoring, and automation across different cloud environments.

---

## What Is Cloud Computing?

Cloud computing is the delivery of computing resources and technology services over the internet. Instead of purchasing and maintaining all the physical hardware yourself, you can use resources provided by a cloud provider, such as servers, storage, databases, networking, and software, when you need them.

Cloud services can be provisioned, configured, scaled, and managed through web consoles, command-line tools, APIs, and automation. Depending on the service and configuration, customers may pay for the resources they consume.

### Core Cloud Service Models

| Model | What It Provides | Example |
| --- | --- | --- |
| Infrastructure as a Service (IaaS) | Virtualized computing resources such as virtual machines, storage, and networks. | Cloud virtual machines |
| Platform as a Service (PaaS) | A managed platform for building, deploying, and running applications. | Managed application platforms |
| Software as a Service (SaaS) | Ready-to-use software delivered over the internet. | Web-based email and collaboration tools |

### Cloud Deployment Models

- **Public Cloud:** Services are provided over the internet by a cloud provider and shared across customers through logically separated environments.
- **Private Cloud:** Cloud infrastructure is dedicated to one organization.
- **Hybrid Cloud:** Combines private infrastructure with public cloud services.
- **Multi-Cloud:** Uses services from multiple cloud providers, such as AWS, Azure, and Google Cloud.

### Why Learn Cloud Computing?

Cloud computing is widely used to host applications, store and process data, connect systems, support business operations, and deliver technology services. Understanding cloud platforms helps develop practical skills in:

- Designing and managing cloud infrastructure.
- Building virtual networks and connecting systems.
- Managing identities, permissions, and access.
- Securing workloads, applications, and data.
- Monitoring systems, investigating events, and maintaining availability.
- Automating deployments and managing infrastructure consistently.
- Understanding cost, scalability, reliability, and shared security responsibilities.

### Shared Responsibility

Cloud security is a shared responsibility between the cloud provider and the customer. The provider is responsible for security of the cloud, while customers are responsible for securing the resources and configurations they manage. The exact division depends on the provider and service model. These labs will include security considerations as part of each exercise.

---

## Cloud Platforms

This repository uses separate branches to organize hands-on learning for each platform.

### Amazon Web Services (AWS)

Learn and practice cloud services and infrastructure using AWS.

- Compute: EC2
- Storage: S3
- Networking: VPC, subnets, route tables, security groups
- Identity and Access Management: IAM
- Monitoring and auditing: CloudWatch, CloudTrail
- Security: security groups, network ACLs, and security best practices

**Branch:** [aws](https://github.com/ZeroScopeIntelligence/ZeroScopeSolutionsCloudLabs/tree/aws)

### Microsoft Azure

Explore Microsoft's cloud platform and its infrastructure and security services.

- Compute: Azure Virtual Machines
- Storage: Azure Storage
- Networking: Virtual Networks, subnets, Network Security Groups
- Identity and Access Management: Microsoft Entra ID and Azure RBAC
- Monitoring: Azure Monitor
- Security: Microsoft Defender for Cloud

**Branch:** [azure](https://github.com/ZeroScopeIntelligence/ZeroScopeSolutionsCloudLabs/tree/azure)

### Google Cloud Platform (GCP)

Build practical experience with Google Cloud services and cloud infrastructure.

- Compute: Compute Engine
- Storage: Cloud Storage
- Networking: VPC networks, subnets, firewall rules
- Identity and Access Management: Cloud IAM
- Monitoring and logging: Cloud Monitoring and Cloud Logging
- Security: Security Command Center and cloud security controls

**Branch:** [google-cloud](https://github.com/ZeroScopeIntelligence/ZeroScopeSolutionsCloudLabs/tree/google-cloud)

---

## Learning Areas

Labs and projects will be organized around these core topics:

| Area | Focus |
| --- | --- |
| Cloud Fundamentals | Cloud concepts, service models, deployment models, regions, zones, and shared responsibility |
| Compute | Virtual machines, instances, and workloads |
| Storage | Object, block, and file storage |
| Networking | VPCs, virtual networks, subnets, routing, and firewalls |
| Identity and Access Management | Users, roles, policies, and permissions |
| Cloud Security | Secure configurations, access controls, and threat protection |
| Monitoring and Logging | Metrics, logs, alerts, and auditing |
| Automation | Infrastructure as Code, scripting, and repeatable deployments |
| Projects | Practical multi-service and cross-platform exercises |

---

## Repository Structure

Each cloud platform has its own branch, keeping its labs, notes, and projects organized independently.

```text
ZeroScopeSolutionsCloudLabs/
├── main
│   └── README.md
├── aws
│   ├── README.md
│   ├── LAB-TEMPLATE.md
│   ├── NOTES.md
│   ├── Fundamentals/
│   ├── Compute/
│   ├── Storage/
│   ├── Networking/
│   ├── IAM/
│   ├── Security/
│   ├── Monitoring-and-Logging/
│   ├── Automation/
│   └── Projects/
├── azure
│   └── [Azure learning structure]
└── google-cloud
    └── [Google Cloud learning structure]
```

Each lab will include its objective, prerequisites, setup steps, implementation, validation, screenshots or command output when useful, cleanup instructions, and lessons learned.

---

## Lab Progress

This is a growing, long-term learning repository. Labs will be added and updated as each topic is studied and practiced.

| Platform | Branch | Status |
| --- | --- | --- |
| AWS | [aws](https://github.com/ZeroScopeIntelligence/ZeroScopeSolutionsCloudLabs/tree/aws) | Starter structure created |
| Microsoft Azure | [azure](https://github.com/ZeroScopeIntelligence/ZeroScopeSolutionsCloudLabs/tree/azure) | Starter structure created |
| Google Cloud | [google-cloud](https://github.com/ZeroScopeIntelligence/ZeroScopeSolutionsCloudLabs/tree/google-cloud) | Starter structure created |

---

## Important Notes

- Follow each cloud provider's documentation and security recommendations.
- Use least-privilege permissions when configuring identities and access.
- Review pricing before deploying resources. Some cloud services can incur charges, even during experimentation.
- Remove or shut down resources when they are no longer needed.
- Never commit passwords, API keys, access tokens, private keys, or other secrets to this repository.
- Use these labs only in cloud accounts and environments you are authorized to manage.

## Official Documentation

- [AWS Documentation](https://docs.aws.amazon.com/)
- [Microsoft Azure Documentation](https://learn.microsoft.com/azure/)
- [Google Cloud Documentation](https://cloud.google.com/docs)

---

## About ZeroScope Solutions

ZeroScope Solutions is a technology-focused initiative exploring cybersecurity, cloud infrastructure, networking, and emerging technologies through hands-on projects and research.

**Stay Curious. Stay Sharp. Stay Secure.**
