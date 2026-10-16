# Module 13: Security Scanning, Supply Chain, and Compliance

## Lesson Notes

Plan dependency, code/CodeQL, secret, license, container, and IaC scanning. Use Dependabot alerts/updates and lockfiles. Define thresholds, owners, remediation SLAs, waiver expiry, evidence retention, and pipeline behavior. Microsoft Defender for Cloud DevOps Security connects repository posture with cloud context. GitHub Advanced Security applies to GitHub and Azure DevOps subject to current licensing. Container images should be scanned and promoted by immutable digest. CodeQL can run in a container when the runner/image/build mode meets current requirements. Never expose privileged credentials or persistent self-hosted runners to untrusted PR code.

## Lab Notes

On a disposable repository, enable dependency graph/Dependabot alerts and configure CodeQL using current supported actions and the appropriate language/build mode. For containerized CodeQL, use a supported job container and verify runtime/runner compatibility. Build and scan a sample container using an approved scanner such as Trivy:

```bash
docker build --tag az400-lab:dev .
trivy image --severity HIGH,CRITICAL --exit-code 1 az400-lab:dev
```

If licensed, connect a test repo to Defender for Cloud DevOps Security and GitHub Advanced Security for GitHub/Azure DevOps; verify repository authorization, finding flow, and alert ownership. Record a sample finding, remediation date, and any expiring exception.

## Exercises

1. For dependency, code, secret, license, container, and IaC scanning, define trigger, scanner, threshold, owner, SLA, and evidence.
2. Threat-model an untrusted PR targeting a self-hosted runner.
3. Explain the difference between Dependabot alerts and automated update PRs, and when to block a release.

## Verification

- A defined threshold blocks CI as intended.
- Findings are assigned and exceptions have expiry/review.
- Container digest and provenance remain traceable through promotion.
