# Module 03: Branching and Repository Governance

## Lesson Notes

Choose trunk-based development for frequent integration, short-lived feature branches for reviewable changes, and release branches for independently supported versions. PR policies should require reviews, successful checks, conversation resolution, and limited bypass. GitHub branch protection/rulesets and Azure Repos branch policies implement related controls. Set repository permissions, tags, merge strategy, and hotfix rules deliberately.

## Lab Notes

Create and push a short-lived branch:

```bash
git switch -c feature/<name>
git add <files>
git commit -m "Describe the change"
git push -u origin feature/<name>
```

Protect the default branch: require PR review and CI/security checks; restrict force-push/deletion; define stale approval handling, merge method, and bypass roles. In Azure Repos, configure reviewer, build validation, linked-work-item, and comment-resolution policies. Test with a non-admin contributor and a deliberately failing check.

## Exercises

1. Design branch strategies for daily SaaS and quarterly on-prem release cadences.
2. Specify merge restrictions, release tags, hotfix flow, and merge-back requirements.
3. Write a permission matrix for maintainers, contributors, auditors, and external collaborators.

## Verification

- Direct push is denied for ordinary contributors.
- Failing required status blocks merge.
- Only restricted administrators can bypass policy, and bypass is audited.
