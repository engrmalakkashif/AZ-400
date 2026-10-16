# Module 07: YAML Pipelines, Triggers, Agents, and Reuse

## Lesson Notes

Choose GitHub Actions or Azure Pipelines based on source location, integrations, governance, tooling, and agent needs. YAML defines triggers, jobs/stages, conditions, dependencies, variables, artifacts, environments, checks, and approvals. Parallelize independent jobs and sequence dependent deployment stages. Reuse templates, task groups, variable/variable groups, and reusable workflows. Hosted agents reduce maintenance; self-hosted runners/agents support custom tools/private connectivity but require patching, isolation, cost planning, and controls for untrusted PRs. Hybrid pipelines and VM templates address specialized deployment/agent requirements.

## Lab Notes

Create `.github/workflows/ci.yml` with PR and main-branch triggers, minimal `contents: read` permission, checkout, Node setup, `npm ci`, tests, coverage, and artifact upload. Commit `package-lock.json`; pin third-party actions to reviewed full commit SHAs for production.

Create an equivalent `azure-pipelines.yml` with `trigger`/`pr`, hosted `pool`, NodeTool, install, test, and artifact publish. Connect Azure Pipelines to GitHub with minimum repository access and verify PR status reporting. Add a reusable YAML template and a second independent job, then a dependent packaging stage. Create an environment with required approval/checks and verify PRs cannot deploy to production.

For self-hosted runner/agent planning, document OS/tools, licensing, cost, concurrency, network reach, patching, secret state, isolation, and maintenance. Do not run untrusted PR code on a privileged persistent agent.

## Exercises

1. Add path/branch trigger rules and explain which changes should start each pipeline.
2. Design a hybrid GitHub-to-Azure Pipelines path and identify trust boundaries.
3. Compare parallel and sequential job plans for speed, cost, reliability, and dependencies.
4. Design a VM agent template and self-hosted runner lifecycle for a private-network build.

## Verification

- PR and main pushes trigger the intended jobs.
- A failing test blocks packaging/deployment.
- Artifact/report uploads still occur on failure where appropriate.
- Approvals and checks are enforced by the environment, not just YAML convention.
