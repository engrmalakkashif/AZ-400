Study guide for Exam AZ-400: Designing and Implementing Microsoft DevOps Solutions

Summarize this article for me
Purpose of this document
This study guide should help you understand what to expect on the exam and includes a summary of the topics the exam might cover and links to additional resources. The information and materials in this document should help you focus your studies as you prepare for the exam.

Useful links	Description
Certification renewal	Microsoft associate, expert, and specialty certifications expire annually. You can renew by passing a free online assessment on Microsoft Learn.
Your Microsoft Learn profile	Connecting your certification profile to Microsoft Learn allows you to schedule and renew exams and share and print certificates.
Exam scoring and score reports	A score of 700 or greater is required to pass.
Exam sandbox	You can explore the exam environment by visiting our exam sandbox.
Request accommodations	If you use assistive devices, require extra time, or need modification to any part of the exam experience, you can request an accommodation.
Take a free Practice Assessment	Test your skills with practice questions to help you prepare for the exam.
Updates to the exam
Our exams are updated periodically to reflect skills that are required to perform a role. We have included two versions of the Skills Measured objectives depending on when you are taking the exam.

We always update the English language version of the exam first. Some exams are localized into other languages, and those are updated approximately eight weeks after the English version is updated. While Microsoft makes every effort to update localized versions of exams as noted, there may be times when localized versions of an exam are not updated on this schedule. Other available languages are listed in the Schedule Exam section of the Exam Details webpage. If the exam isn't available in your preferred language, you can request an additional 30 minutes to complete the exam.

Note
The bullets that follow each of the skills measured are intended to illustrate how we are assessing that skill. Related topics may be covered in the exam.

Note
Most questions cover features that are general availability (GA). The exam may contain questions on Preview features if those features are commonly used.

Skills measured as of July 27, 2026
Audience profile
As a DevOps engineer, you’re a developer or infrastructure administrator who also has subject matter expertise in working with people, processes, and products to enable continuous delivery of value in organizations.

Your responsibilities for this role include delivering Microsoft DevOps solutions that provide continuous security, integration, testing, delivery, deployment, monitoring, and feedback. You design and implement flow of work, collaboration, communication, source control, and automation.

As a DevOps engineer, you work on cross-functional teams that include:

Developers

Site reliability engineers

Azure administrators

Security engineers

You must have experience both administering and developing in Azure, with strong skills in at least one of these areas. You should also have experience implementing both GitHub and Azure DevOps solutions.

Skills at a glance
Design and implement processes and communications (10–15%)

Design and implement a source control strategy (10–15%)

Design and implement build and release pipelines (50–55%)

Develop a security and compliance plan (10–15%)

Implement an instrumentation strategy (5–10%)

Design and implement processes and communications (10–15%)
Design and implement traceability and flow of work
Design and implement a structure for the flow of work, including GitHub Flow

Design and implement a strategy for feedback cycles, including notifications and GitHub Issues

Design and implement integration for tracking work, including GitHub projects, Azure Boards, and repositories

Design and implement source, bug, and quality traceability

Design and implement appropriate metrics and queries for DevOps
Design and implement a dashboard, including flow of work, such as cycle times, time to recovery, and lead time

Design and implement appropriate metrics and queries for project planning

Design and implement appropriate metrics and queries for development

Design and implement appropriate metrics and queries for testing

Design and implement appropriate metrics and queries for security

Design and implement appropriate metrics and queries for delivery

Design and implement appropriate metrics and queries for operations

Configure collaboration and communication
Document a project by configuring wikis and process diagrams, including Markdown and Mermaid syntax

Configure release documentation, including release notes and API documentation

Automate creation of documentation from Git history

Configure integration by using webhooks

Configure integration between Azure Boards and GitHub repositories

Configure integration between GitHub or Azure DevOps and Microsoft Teams

Design and implement a source control strategy (10–15%)
Design and implement branching strategies for the source code
Design a branch strategy, including trunk-based, feature branch, and release branch

Design and implement a pull request workflow by using branch policies and branch protection rules

Implement branch merging restrictions by using branch policies and branch protection rules

Configure and manage repositories
Design and implement a strategy for managing large files, including Git Large File Storage (LFS) and git-fat

Design a strategy for scaling and optimizing a Git repository, including Scalar and cross-repository sharing

Configure permissions in the source control repository

Configure tags to organize the source control repository

Recover specific data by using Git commands

Remove specific data from source control

Design and implement build and release pipelines (50–55%)
Design and implement a package management strategy
Recommend package management tools including GitHub Packages and Azure Artifacts

Design and implement package feeds and views for local and upstream packages

Design and implement a dependency versioning strategy for code assets and packages, including semantic versioning (SemVer) and date-based (CalVer)

Design and implement a versioning strategy for pipeline artifacts

Design and implement a testing strategy for pipelines
Design and implement quality and release gates, including security and governance

Design a comprehensive testing strategy, including local tests, unit tests, integration tests, and load tests

Implement tests in a pipeline, including configuring test tasks, configuring test agents, and integration of test results

Implement code coverage analysis

Design and implement pipelines
Select a deployment automation solution, including GitHub Actions and Azure Pipelines

Design and implement a GitHub runner or Azure DevOps agent infrastructure, including cost, tool selection, licenses, connectivity, and maintainability

Design and implement integration between GitHub repositories and Azure Pipelines

Develop and implement pipeline trigger rules

Develop pipelines by using YAML

Design and implement a strategy for job execution order, including parallelism and multi-stage pipelines

Develop and implement complex pipeline scenarios, such as hybrid pipelines, VM templates, and self-hosted runners or agents

Create reusable pipeline elements, including YAML templates, task groups, variables, and variable groups

Design and implement checks and approvals by using YAML-based environments

Design and implement deployments
Design a deployment strategy, including blue-green, canary, ring, progressive exposure, feature flags, and A/B testing

Design a pipeline to ensure that dependency deployments are reliably ordered

Plan for minimizing downtime during deployments by using load balancing, rolling deployments, and deployment slot usage and swap

Design a hotfix path plan for responding to high-priority code fixes

Design and implement a resiliency strategy for deployment

Implement feature flags by using Azure App Configuration Feature Manager

Implement application deployment by using containers, binaries, and scripts

Implement a deployment that includes database tasks

Design and implement infrastructure as code (IaC)
Recommend a configuration management technology for application infrastructure

Implement a configuration management strategy for application infrastructure

Define an IaC strategy, including source control and automation of testing and deployment

Design and implement desired state configuration for environments, including Azure Automation State Configuration, Azure Resource Manager, Bicep, and Azure Machine Configuration

Design and implement Azure Deployment Environments for on-demand self-deployment

Maintain pipelines
Monitor pipeline health, including failure rate, duration, and flaky tests

Optimize a pipeline for cost, time, performance, and reliability

Optimize pipeline concurrency for performance and cost

Design and implement a retention strategy for pipeline artifacts and dependencies

Migrate a pipeline from classic to YAML in Azure Pipelines

Develop a security and compliance plan (10–15%)
Design and implement authentication and authorization methods
Choose between Microsoft Entra service principals and managed identities for Azure resources (system-assigned and user-assigned)

Implement and manage GitHub authentication, including GitHub Apps, GITHUB_TOKEN, and personal access tokens

Implement and manage Azure DevOps service connections and personal access tokens

Design and implement permissions and roles in GitHub

Design and implement permissions and security groups in Azure DevOps

Recommend appropriate access levels, including stakeholder access in Azure DevOps and outside collaborator access in GitHub

Configure projects and teams in Azure DevOps

Design and implement a strategy for managing sensitive information in automation
Implement and manage secrets, keys, and certificates by using Azure Key Vault

Implement and manage secrets and secretless authentication (for example, workload identity federation/OpenID Connect) in GitHub Actions and Azure Pipelines

Design and implement a strategy for managing sensitive files during deployment, including Azure Pipelines secure files

Design pipelines to prevent leakage of sensitive information

Automate security and compliance scanning
Design a strategy for security and compliance scanning, including dependency, code, secret, and licensing scanning

Configure Microsoft Defender for Cloud DevOps Security

Configure GitHub Advanced Security for GitHub and GitHub Advanced Security for Azure DevOps

Integrate GitHub Advanced Security with Microsoft Defender for Cloud

Automate container scanning, including scanning container images and configuring an action to run CodeQL analysis in a container

Automate analysis of vulnerabilities of open-source components by using Dependabot alerts

Implement an instrumentation strategy (5–10%)
Configure monitoring for a DevOps environment
Configure Azure Monitor and Azure Monitor Logs to integrate with DevOps tools

Configure collection of telemetry by using Azure Monitor Application Insights, Azure VM Insights, Azure Container Insights, Azure Monitor for Storage, and Azure Monitor for Networks

Configure monitoring in GitHub, including enabling insights and creating and configuring charts

Configure alerts for events in GitHub Actions and Azure Pipelines

Analyze metrics from instrumentation
Inspect infrastructure performance indicators, including CPU, memory, disk, and network

Analyze metrics by using collected telemetry, including usage and application performance

Inspect distributed tracing by using Azure Monitor Application Insights

Interrogate logs using basic Kusto Query Language (KQL) queries

Study resources
We recommend that you train and get hands-on experience before you take the exam. We offer self-study options and classroom training as well as links to documentation, community sites, and videos.

Study resources	Links to learning and documentation
Get trained	Choose from self-paced learning paths and modules or take an instructor-led course
Find documentation	DevOps resource center
Azure DevOps documentation
Azure Boards
Azure Key Vault Keys, Secrets, and Certificates Overview
Azure Monitor
Azure Pipelines
Azure Repos
Work with Azure DevOps and GitHub
Ask a question	Microsoft Q&A | Microsoft Docs
Get community support	Azure DevOps - Microsoft Tech Community
Follow Microsoft Learn	Microsoft Learn - Microsoft Tech Community
Find a video	Exam Readiness Zone
Microsoft Learn Shows
Change log
The table below summarizes the changes between the current and previous version of the skills measured. The functional groups are in bold typeface followed by the objectives within each group. The table is a comparison between the previous and current version of the exam skills measured and the third column describes the extent of the changes.

Skill area prior to July 27, 2026	Skill area as of July 27, 2026	Change
Audience profile		No change
Design and implement processes and communications	Design and implement processes and communications	No change
Design and implement traceability and flow of work	Design and implement traceability and flow of work	Minor
Develop a security and compliance plan	Develop a security and compliance plan	No change
Automate security and compliance scanning	Automate security and compliance scanning	Minor
Implement an instrumentation strategy	Implement an instrumentation strategy	No change
Configure monitoring for a DevOps environment	Configure monitoring for a DevOps environment	Minor
Analyze metrics from instrumentation	Analyze metrics from instrumentation	Minor
Additional resources
Documentation

CmdLine@2 - Command line v2 task

Run a command line script using Bash on Linux and macOS and cmd.exe on Windows.

Configure a branch policy for an external service - Azure Repos

Configure a branch policy to require status from a 3rd party pull request status server

Review logs to diagnose pipeline issues - Azure Pipelines

Learn how to review pipeline diagnostic logs to troubleshoot failures in Azure Pipelines.

Show 4 more
Training

Learning path

Solution Architect: Design Microsoft Power Platform solutions - Training

Learn how a solution architect designs solutions.

Certification

Microsoft Certified: DevOps Engineer Expert - Certifications

This certification measures your ability to accomplish the following technical tasks: Design and implement processes and communications, design and implement a source control strategy, design and implement build