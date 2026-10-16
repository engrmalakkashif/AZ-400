# Module 00: Lab Setup and Delivery Lifecycle

## Lesson Notes

The exam assumes Azure development/administration experience and practical familiarity with GitHub and Azure DevOps. A common delivery lifecycle is plan -> source -> build/test -> secure -> package -> deploy -> monitor -> feedback. Later labs use a small Node.js service, but the practices transfer to other stacks.

Tools: Git, Node.js/npm, GitHub and `gh`, Azure subscription and `az`; optional Azure DevOps CLI extension, Docker, Bicep, Git LFS, Scalar. Use a dedicated lab identity/resource group. Never use production data or real secrets.

## Lab Notes

Check tools and account context:

```bash
git --version
node --version
npm --version
gh --version
az version
gh auth status
az account show --output table
```

Create the shared service and tests using [Lab 0 of the consolidated workbook](../AZ-400-lab-workbook.md#lab-0-build-the-shared-sample-service), then initialize a local baseline:

```bash
npm init -y
npm install --package-lock-only
git init -b main
git add package.json package-lock.json server.js server.test.js
git commit -m "Create AZ-400 lab service"
```

Run `npm test`, start the service with `npm start`, and verify `curl http://localhost:3000/health`.

## Exercises

1. List which labs need GitHub, Azure DevOps, an Azure subscription, paid features, or local tools.
2. Draw the lifecycle and mark where source revision, artifact version, approval, deployment, and telemetry are recorded.
3. Make a cost and cleanup checklist for cloud resources, identities, and test artifacts.

## Verification

- Tests pass and `/health` returns healthy status.
- Git working tree is clean after the baseline commit.
- No credentials or production data appear in the repository or logs.
