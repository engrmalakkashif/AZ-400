# Module 08: Deployment Strategies and Application Releases

## Lesson Notes

Blue-green switches between parallel environments; canary/ring/progressive exposure gradually expands traffic; rolling updates instances in place; slots permit pre-swap validation. Feature flags separate deployment from feature release. A/B testing compares variants against an outcome. Select strategy by capacity, blast radius, rollback speed, and data compatibility. Order dependent deployments. Use expand/migrate/contract database changes so old and new application versions coexist. Include database tasks, containers, binaries, scripts, load balancing, hotfix paths, and resiliency controls in the deployment design.

## Lab Notes

Create a deployment decision record for the sample service: artifact ID, target, dependency order, health checks, rollout stages, approval, stop thresholds, rollback/roll-forward, database plan, and owner. Add a feature flag controlled by configuration; verify it can be turned off without rebuilding. For Azure App Configuration Feature Manager, connect the supported SDK and test a controlled cohort.

If using Azure App Service, check plan cost and create only disposable resources. Validate a staging slot, health settings, and swap/rollback using the current Azure portal or CLI. For a container, deploy by immutable image digest. Test only in a non-production environment.

Write a hotfix runbook with priority criteria, named approver, minimum checks, artifact provenance, post-deployment verification, merge-back to main/release branches, and audit evidence.

## Exercises

1. Choose a strategy for a single-instance service and for a multi-region service; explain capacity and downtime trade-offs.
2. Define health/telemetry thresholds that stop canary/ring expansion.
3. Design backward-compatible database migration and rollback steps.
4. Compare feature flags with deployment slots and A/B testing; include flag expiry and ownership.

## Verification

- The same immutable artifact is promoted across environments.
- Failed health checks stop rollout and trigger documented recovery.
- Database changes are compatible with both deployed and next versions.
- Hotfix remains traceable and is merged back to supported branches.
