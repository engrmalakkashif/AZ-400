# Module 10: Pipeline Operations, Optimization, and Migration

## Lesson Notes

Monitor failure rate, duration, queue time, flaky tests, agent utilization, and cost per successful delivery. Use diagnostic logs to find the first causal failure. Optimize safe caching, duplicate work, path selection, agent sizing, and parallelism without weakening reproducibility/isolation. Tune concurrency to capacity and cost. Retain logs, tests, artifacts, packages, and dependencies to policy. Migrate classic pipelines to YAML by inventorying behavior, running parallel validation, comparing outputs, and cutting over with rollback.

## Lab Notes

Record queue time, duration, success/failure, flaky reruns, artifact size, and tool versions for five runs. Inspect a failed run's diagnostic logs. Change one bottleneck (cache dependencies, parallelize independent jobs, or right-size an agent), collect five more runs, and compare median/p95 duration and failure rate. Never cache secrets or share writable cache state across untrusted jobs.

Create a retention matrix for logs, test results, release artifacts, packages, and dependency caches. For a classic Azure Pipeline, inventory triggers, variables, service connections, tasks, agent demands, approvals, and retention; recreate in YAML, run both, compare permissions/outputs, then plan cutover.

## Exercises

1. Diagnose a pipeline with long queue time, repeated downloads, and flaky end-to-end tests.
2. Rank optimization ideas by expected performance/cost improvement and operational risk.
3. Define retention for a regulated release and a short-lived PR build.

## Verification

- Optimization has measured benefit without reducing test/security coverage.
- Concurrency matches agent capacity/cost limits.
- YAML migration matches triggers, permissions, approvals, and outputs before retirement.
