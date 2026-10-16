# Module 11: Identity, Authentication, Permissions, and Teams

## Lesson Notes

Managed identities avoid stored Azure credentials: system-assigned identity follows one resource's lifecycle; user-assigned identity can be shared and has an independent lifecycle. Service principals/app registrations serve other workloads; prefer workload identity federation/OIDC over long-lived secrets. GitHub Apps provide fine-grained integration permissions; `GITHUB_TOKEN` is workflow-scoped; PATs are user-bound and should be narrow and short-lived. Azure DevOps service connections should be scoped and pipeline-authorized; PATs are not preferred for unattended automation.

Apply least privilege with GitHub roles, teams, outside-collaborator access, and rulesets; Azure DevOps permissions, security groups, teams, projects, and access levels (including stakeholder access). Separate admin duties, restrict bypass, and periodically review access.

## Lab Notes

Configure a test Azure workload identity federation/OIDC connection for GitHub Actions or Azure Pipelines. In GitHub, use minimal permissions and set `id-token: write` only for the job requesting an OIDC token. Configure the matching federated credential and grant only the resource role required. In Azure Pipelines, authorize a workload-identity service connection only for the test pipeline. Attempt intended and unrelated resource operations; the latter should be denied.

Create a test GitHub team/repository permission and Azure DevOps group/project permission. Connect a test Teams channel to pipeline notifications and confirm access/routing is appropriate.

## Exercises

1. Choose system-assigned vs user-assigned identity for two workloads.
2. Compare GitHub App, `GITHUB_TOKEN`, and PAT for an integration.
3. Create an access matrix for developers, release managers, auditors, administrators, and outside collaborators; include Azure DevOps stakeholder access.

## Verification

- Intended access works; unrelated access is denied.
- Service connection, GitHub token, role, and group scopes are minimal.
- Ownership, review, audit, and revocation are documented.
