# Module 01: Flow, Feedback, Traceability, and Metrics

## Lesson Notes

GitHub Flow uses short-lived branches, PR review/checks, and a releasable default branch. Coordinate work with GitHub Issues/Projects or Azure Boards. Trace work item -> branch -> commit -> PR -> checks -> artifact -> deployment -> incident/feedback. Dashboards expose bottlenecks. Define cycle time, lead time, time to recovery, deployment frequency, change failure rate, and measures for planning, development, testing, security, delivery, and operations. Every metric needs source, calculation, window, owner, and action; avoid activity measures that reward gaming.

## Lab Notes

Create an issue and note its number, then branch and link a PR:

```bash
gh issue create --title "Add version endpoint" --body "Expose and test the app version."
git switch -c feature/version-endpoint
git add server.js server.test.js
git commit -m "Add version endpoint"
git push -u origin feature/version-endpoint
gh pr create --title "Add version endpoint" --body "Closes #<issue-number>"
```

For Azure Boards, install/configure the CLI extension and query unresolved bugs:

```bash
az extension add --name azure-devops
az devops configure --defaults organization=https://dev.azure.com/<organization> project=<project>
az boards query --wiql "SELECT [System.Id], [System.Title], [System.State] FROM WorkItems WHERE [System.WorkItemType] = 'Bug' AND [System.State] <> 'Closed'"
```

Create a view/dashboard with cycle time, lead time, aging work, build health, and time to recovery. Use GitHub Projects charts or Azure Boards Queries/Analytics where available.

## Exercises

1. Define one query/metric for planning, development, testing, security, delivery, and operations.
2. Map a bug from discovery through fix and production verification.
3. Identify a bias or missing event in each metric and document a caveat.

## Verification

- Issue/work item links to code and PR.
- Displayed metrics have definitions, sources, periods, owners, and actions.
- Feedback/notifications create actionable follow-up work.
