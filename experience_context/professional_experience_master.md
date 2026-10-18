# Professional Experience Context — Master

This file is the single source of truth for professional experience context. It includes role details and relevant historical-resume claims; placeholders and unconfirmed details remain explicitly unresolved. This is a source of experience context, not a resume. Resolve placeholders and verify claims before using them in a resume.

## Cloud Engineer

**Company:** U.S. Bank  
**Duration:** 2023–Present  
**Title Tags:** `AWS Engineer`, `Automation Engineer`, `Cloud Engineer`, `Software Developer`, `Software Engineer`, `DevOps Engineer`, `DevSecOps Engineer`

### Cloud engineering work

- Built AWS quota monitoring across 2,100+ service quotas in 18+ accounts using DynamoDB-backed stateful alerting. Reduced PagerDuty events from 1.12 million published events to 37 actionable incidents, cutting alert noise by more than 99% and helping prevent quota-driven outages.
- Built a reusable IAM-user provisioning and delivery solution using Python, boto3, Docker, Spinnaker, Kubernetes, and Terraform. The module recorded 32,000+ total downloads and 1,024 weekly downloads.
- Built multi-region NAT infrastructure observability with Terraform, CloudWatch, EventBridge, and SNS-to-PagerDuty alerting across Development, QA, and Production. Provided 100% visibility and incident-response coverage for NAT instances supporting U.S. Bank services.
- Redesigned a reusable Terraform module for IAM service-user provisioning to attach policies directly to users, enforce a standard permission boundary by default, and generate IP restrictions from account-, region-, and datacenter-specific allowlists. Built end-to-end Go/Terratest checks in GitHub Actions to verify user creation, metadata, and security controls, preventing changes from weakening the intended least-privilege and network-security posture.
- Developed reusable Terraform IAM modules with application teams; implemented cross-account connectivity using Route 53 private zones, VPC endpoints, and PrivateLink; configured custom network ACLs and security groups; and troubleshot application connectivity.
- Centralized AWS Certificate Manager lifecycle automation in a GitHub repository across accounts and regions. Developed a 10-step migration from imported certificates to DNS-validated certificates, including service-registry owner resolution and bulk Jira-ticket creation.

### Cloud skills and technologies

- AWS, Azure, Terraform, EC2, S3, RDS, DynamoDB, VPC, Route 53, PrivateLink, CloudWatch, EventBridge, SNS, Docker, Kubernetes, Spinnaker, boto3, Terratest, and GitHub Actions.

## Cloud Engineer (Master's Project)

**Company:** Capella University (Master's Information Technology)  
**Duration:** 2022–2023  
**Title Tags:** `Infomation Security Engineer`, `Automation Engineer`, `IAM Engineer`, `Software Developer`, `Software Engineer`

### Capella University consulting project

- Solution-architected and platform-engineered a full-stack, cloud-based web application for a client as a Master's consulting project (2022–2023). Redesigned and migrated a LAMP stack and related digital assets to AWS using IAM policies, EC2, S3, RDS, and security groups. The client is not named in the source material.

### Academic Coursework (2021–2023)

- Completed coursework projects involving S3 cross-region replication; a highly available EC2/VPC website with S3 static assets, an Application Load Balancer, Auto Scaling, and network ACLs; cross-region replication and archiving with EC2 and a VPC-enabled Lambda function using a secure tunnel; IAM policies for secure S3 access; and EC2 health checks using EventBridge and Route 53 network monitoring.

## Linux Administrator

**Company:** U.S. Bank  
**Duration:** 06/2021-07/2022  
**Title Tags:** `Infomation Security Specialist`, `Linux Administrator`, `Linux Systems Administrator`, `IAM Engineer`, `Systems Admin`

• Personally resolved 99% of more than 60,000 ServiceNow catalog requests, change tasks, and incidents within their defined SLAs from 2021–2022 while adhering to GDPR, SOC 2, and SOX requirements.

• Acting as Unix/ Linux SME or Consultant for application and database teams. 
         - Work pertaining to human and non-human system access in all server environments (Development, IT, UAT, Production).

• Supported application and database teams with Linux server access design and provisioning across server environments.

• Authored and published enterprise service architecture documentation for U.S. Bank's CyberArk PAM implementation and service offerings, working with Solutions Architecture.

• Managed CyberArk PAM user onboarding and provisioning, privileged service-account vaulting, credential management, and password rotation.

• Daily work and collaboration with Application Engineers, Developers, and database teams.

• Frequent hands-on work with the continuous integration phase while assisting Application teams in their CI/CD pipelines.

In addition to my IAM Linux Admin role on the Unix / Linux Provisioning team, I aided in co-founding a small automation team within the greater IAM Security Access Operations group.

• Taking ownership in the improvement of older, manual access provisioning processes through various automation methods:
         - Using Python scripts to assist higher management in automating the flow of business SLA metrics through data pipelines.
         - Using PowerShell and Python to automate IAM provisioning across Active Directory, CyberArk, and local Unix/Linux servers, reducing manual workload by 90% and supporting LDAP/SAML compliance.

• Writing operation requirements, presenting requirements to ISS management, and performing quality assurance to ensure adherence to those requirements.

• Manage all internal Unix automation projects. Own and process Jira stories.

• Design and manage automation repositories in GitLab for the Unix Team.

## Senior Integration Engineer

**Company:** U.S. Bank  
**Duration:** 03/2024-03/2026  
**Title Tags:** `Senior Infomation Security Engineer`, `Senior Automation Engineer`, `Senior IAM Engineer`, `Senior Software Developer`, `Senior Software Engineer`, `Senior DevOps Engineer`, `Senior DevSecOps Engineer`

### Security API and Vault integration engineering

- Promoted from Software Engineer/Automation Engineer in March 2024, retaining automation-software-engineering responsibilities while taking ownership of security API integrations and HashiCorp Vault.
- Served as HashiCorp Vault Enterprise SME for platform management, configuration, maintenance, application-team consultation, provisioning guidance, and standards. Partnered with governance and audit teams on solutions to improve platform visibility and auditability across the enterprise.
- Supported Vault use cases and application integrations involving OAuth/OIDC, SSO and federated protocols, retrievable JWTs, Java clients, Kubernetes service accounts, AWS authentication, GitLab projects/groups/runners, and custom auto-auth for Windows and Linux VMs. Personally implemented the AWS authentication integration method.
- Resume versions report Vault scale of 28,000+ stored secrets across namespaces, approximately 150,000 authentication tokens generated per hour, and more than 70,000 security tokens per day; the token-throughput figures vary by source version.
- Led a large Vault-operations automation effort, building automations for recurring platform operations and leading training and support planning, execution, and delivery to shift integration support to Security Operations.
- Designed and launched a custom-web-app onboarding service for Vault AWS authentication using Python, Svelte, TypeScript, and PostgreSQL, enabling application teams to configure EC2 or IAM authentication.
- Led a large, phased migration of Active Directory secrets from Vault's deprecated AD engine to its LDAP engine after vendor support for the AD engine ended. Coordinated application teams' code-reference updates and maintained service continuity with no downtime.
- Maintained automations for Vault entity-alias policy assignment and customization, secrets-engine provisioning, and secret rotation and management. Managed Terraform for AWS IAM permissions and S3 backups retaining the previous 100 Vault versions.
- Built and maintained security automation API suites for Active Directory, HashiCorp Vault, CMDB and other databases, SailPoint IIQ, CyberArk, and related platforms; collaborated with application teams on API-integrated security designs.
- Owned customer onboarding and integration for IAM automation APIs using JSON-based least-privilege policies, with read/write operations across SailPoint IIQ, Active Directory, CyberArk PAM, Vault, SQL databases, and RHEL virtual machines.

## Senior Software Engineer

**Company:** U.S. Bank  
**Duration:** 03/2026-Present  
**Title Tags:** `Senior Infomation Security Engineer`, `Senior Automation Engineer`, `Senior IAM Engineer`, `Senior Software Developer`, `Senior Software Engineer`, `Senior Platform Engineer`, `Principal Engineer`, `Senior DevOps Engineer`, `SeniorDevSecOps Engineer`

### AI-enabled engineering and platform work

- Led development of an enterprise security-operations platform for automation, reporting, governance, and operational enablement. Designed reusable event-driven, scheduled, and API-based automation; established CI/CD and containerization practices, secure development practices, platform architecture, governance controls, and operating model.
- Designed and built an AI assistant for Cloud Automation Engineering that automates Jira ticket triage, documentation retrieval, IAM engineering, and operational workflows within AI coding IDEs without server infrastructure.
- Architected a four-agent system (Supervisor, Triage, Analytics, Engineer) with intent-based semantic routing, scoped context, and tool governance across 10+ CLI tools. Designed always-loaded and on-demand context layers and extracted workflows into reusable skills for certificate migration, Jira Definition of Ready validation, repository scaffolding, and IAM policy authoring; one resume reports reducing prompt size by 300+ lines.
- Designed repository discovery spanning 226+ repositories across multiple GitHub Enterprise hosts, with a single entry point that allows the discovery strategy to change without downstream changes. Evaluated per-repository, per-subject, and generalist agent designs and recommended a generalist-first approach with repository-level context and evidence-based criteria for splitting agents.
- Created structured agent identities, deterministic routing, confidence-based escalation, and entity disambiguation. Developed a Jira Definition of Ready system with nine blocking criteria, field-evaluation hierarchy, severity levels, and verdict rules.
- Designed pre- and post-triage orchestration with scope checks, multi-agent coordination, and human approval gates for write actions; added retrospective learning and source-hash drift detection for stale generated files and agent errors.
- Integrated 10+ platform CLIs, including Jira, Confluence, GitHub, service registry, Terraform Enterprise, Datadog, PagerDuty, infrastructure graph, Teams, and organization directory, using structured JSON, native authentication, and per-agent read/write governance.
- Led migration from dispatcher/wrapper conventions to native CLI use; added routing across five GitHub Enterprise hosts and a documented authentication cascade. Built a shared setup system for Kiro and Claude Code. Non-interactive CI, checksum verification, and temporary-directory cleanup were identified as planned improvements, not completed work.
- Integrated cross-repository code intelligence through an MCP server. Built AI-assisted IAM workflows across 6+ repositories and tooling for IAM resources across 20+ AWS accounts, including console roles, service users, permission boundaries, SCPs, and service-linked roles.
- Integrated Terraform Enterprise workspace inspection, plans, and apply verification with human confirmation for destructive actions. Built a 10-step ACM certificate-migration workflow with service-owner resolution and bulk Jira-ticket management.
- Built structured YAML inventories, a domain glossary, per-agent tool preferences, and operational retrospectives for people and agents. Added Datadog/PagerDuty visibility into service status, incidents, and on-call schedules.
- Reduced ticket-triage effort by checking Definition of Ready requirements, resolving account/service identifiers, and generating structured assessments and clarifying questions; no measured reduction amount is available.

## Software Engineer

**Company:** U.S. Bank  
**Duration:** 2022-03/2024  
**Title Tags:** `Infomation Security Engineer`, `Automation Engineer`, `IAM Engineer`, `Software Developer`, `Software Engineer`, `DevOps Engineer`, `DevSecOps Engineer`

### Security automation and software engineering

- Delivered automation across 60+ Jira stories for Information Security and application teams, including GDPR-compliant workflows and policy-as-code using RBAC, EBAC, and PBAC access frameworks.
- Designed 13 Swagger-documented REST APIs performing read/write operations with LDAP, MySQL, and CyberArk. Replaced manual server-access provisioning and supported new RHEL builds.
- Integrated identity-management solutions into application teams' infrastructure-as-code using Ansible, Terraform, and Helm.
- Built a Python self-service platform for Active Directory object management with Security Access Operations, reducing manual task workload by 100% and improving SOC 2 compliance.
- Developed Python automation to revoke access for employees overdue on required security training. Generated $5.75 million in realized 2023 savings, calculated from avoided noncompliance fees and FTE time saved; aligned the process with ISO 27001.
- Built a Linux administration GUI using TypeScript, React, MySQL, Python, Flask, and Django, with REST APIs for remote Linux CLI tasks.
- Refactored Open Identity Manager automations and REST APIs in preparation for migration to SailPoint, including access-management read, write, and delete workflows. Supported production automations for a PingFederate implementation enabling AD FS OpenID Connect for SSO.
- Built a Jenkins/Docker pipeline to validate that infrastructure-as-code permissions granted to IAM roles complied with existing security guardrails, improving project delivery timelines by 30% and reducing deployment errors by 40%.
- Used Terraform to manage IAM policies and PowerShell for solutions requiring Windows-native scripting.

## Education

- **Capella University:** M.S. in Information Technology, specialization in Enterprise Networks and Cloud Computing (awarded 2023).
- **University of Northwestern–St. Paul:** B.A. in Business Administration (awarded 2019).

## Certifications

- Software Security Practitioner (SSP), 2021.
- Microsoft Certified: Azure Fundamentals, 2021.
- Microsoft Certified: Azure Data Fundamentals, 2022.

## Military Service

- U.S. Army, Artilleryman and Joint Fires Observer, 2013–2019; served at various U.S.-based locations.

## Resume-Wide Positioning

- Target titles/headlines have included Software Engineer, IAM Engineer, DevSecOps Engineer, Senior DevSecOps Engineer, Senior Security Platform Engineer, and Security Platform Engineer.
- Historical summary positioning described an Army veteran with approximately seven years of combined education and hands-on experience across cloud, automation, DevSecOps, middleware, security operations, and software engineering. The duration is historical resume positioning, not a verified tenure calculation.
