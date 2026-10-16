# Module 15: Metrics, Traces, Logs, and KQL

## Lesson Notes

Metrics support trends/alerts, logs provide event details, and distributed traces correlate requests across dependencies. Use operation/trace IDs and consistent service/environment dimensions. Compare CPU, memory, disk, and network indicators with application usage, latency, and errors. Kusto Query Language (KQL) queries Azure Monitor Logs. Application Insights table names vary between classic and workspace-based resources; inspect the actual schema.

## Lab Notes

Generate a successful request and a controlled failing request. In the Log Analytics/Application Insights query editor, use the available schema. Example classic-schema query:

```kusto
requests
| where timestamp > ago(24h)
| summarize requestCount=count(), failures=countif(success == false) by bin(timestamp, 1h)
| order by timestamp desc
```

Find failed dependencies and trace correlation:

```kusto
dependencies
| where timestamp > ago(1h) and success == false
| project timestamp, name, target, resultCode, duration, operation_Id
| order by timestamp desc
```

Use `operation_Id` to inspect related requests, exceptions, and traces. Compare timestamps with infrastructure charts and the deployment timeline; create a linked incident/work item.

## Exercises

1. Query slow requests above a chosen duration and group by operation.
2. Count failures by result code over time.
3. Write a short incident report using metrics, trace evidence, logs, impact, mitigation, and follow-up.
4. Explain high-cardinality dimensions and retention cost.

## Verification

- Queries are time-bounded and match the workspace schema.
- Trace correlation identifies the failing operation/dependency.
- Incident links to deployment, source revision, and follow-up work.
