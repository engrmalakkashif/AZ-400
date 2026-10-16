# Module 14: Monitoring and Telemetry Collection

## Lesson Notes

Azure Monitor is the monitoring platform; Azure Monitor Logs/Log Analytics store and query logs; Application Insights provides application performance monitoring and distributed traces. VM Insights, Container Insights, Azure Monitor for Storage, and Azure Monitor for Networks add workload-specific telemetry. Monitor GitHub insights/charts and Azure Pipelines/GitHub Actions failures, duration, and queue time. Alerts need actionable thresholds, owner, routing, and runbook. Consider privacy, sampling, retention, and cost.

## Lab Notes

Create disposable Log Analytics and Application Insights resources using the current Azure portal/CLI and instrument a test app with the supported SDK. Verify requests, dependencies, exceptions, and traces; scrub sensitive fields. Enable VM, Container, Storage, or Network Insights only for available test resources. Configure a test alert/action group for availability or elevated errors, cause a controlled failure, and confirm alert routing. Enable GitHub insights/charts and configure a test pipeline event alert in GitHub or Azure DevOps.

Discover CLI commands and resources:

```bash
az monitor --help
az monitor log-analytics workspace list --resource-group <rg> --output table
az monitor app-insights component list --resource-group <rg> --output table
```

## Exercises

1. Design a telemetry matrix: signal, source, dimensions, retention, sampling, alert threshold, owner, response.
2. Explain how CPU, memory, disk, network, and application usage/performance inform capacity planning.
3. Separate actionable alerts from informational charts and justify each.

## Verification

- Test telemetry arrives with correct service/environment dimensions.
- Alert reaches its test receiver and links to an actionable runbook.
- Unnecessary/sensitive telemetry is excluded and resource costs are considered.
