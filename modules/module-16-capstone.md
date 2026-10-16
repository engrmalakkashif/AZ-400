# Module 16: End-to-End Capstone

## Lesson Notes

The capstone combines the five exam domains: processes/communications, source control, build/release pipelines, security/compliance, and instrumentation. Deliver the same immutable artifact through controlled stages and preserve traceability from requirement to production and operational feedback.

## Lab Notes

Deliver a version endpoint to a monitored test service. Demonstrate:

1. Issue/work item linked to branch, PR, commit, checks, artifact, deployment, and incident.
2. Protected branch, reviews, required test/security status, and merge restrictions.
3. Markdown/Mermaid diagram, runbook, API notes, and curated release notes.
4. CI build, tests, coverage/results, immutable package/artifact, and retention.
5. Dependency/code/secret/license/container/IaC scanning as appropriate.
6. YAML multi-stage deployment, approvals, health gate, rollout, database compatibility, rollback, and hotfix path.
7. IaC validation/what-if and disposable environment cleanup.
8. Managed identity or OIDC; Key Vault only for unavoidable secrets.
9. Azure Monitor/Application Insights telemetry, alert, and KQL investigation.
10. Dashboard with lead/cycle time, deployment health, security remediation, and recovery measures.

## Exercises

Demonstrate one failure (rejected PR, failing test, security gate, denied identity, or unhealthy deployment), its evidence, recovery, and linked follow-up. Score 0–2 for traceability, source control, tests, release, IaC, security, monitoring, and operations. Remediate every zero and repeat without relying on the previous runbook.

## Verification

- The same artifact is promoted and tied to source revision.
- No secret reaches source, logs, artifacts, or untrusted code.
- Release is gated, observable, and recoverable.
- Azure resources and temporary permissions are removed.
