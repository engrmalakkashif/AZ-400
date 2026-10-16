# Module 06: Testing Strategy, Quality Gates, and Coverage

## Lesson Notes

Run local/static checks and unit tests early; use integration/contract tests at boundaries, focused end-to-end tests for critical journeys, and controlled load tests. Configure test tasks and agents with required SDKs, tools, services, data, network, and isolation. Publish standard test results and coverage. Coverage is diagnostic, not a substitute for meaningful behavioral tests. Gates can include security, governance, quality, and release approvals.

## Lab Notes

Run tests and coverage on the sample Node service:

```bash
npm test
npm install --save-dev c8
npm pkg set scripts.coverage="c8 --reporter=text --reporter=cobertura node --test"
npm run coverage
```

Add test and coverage commands to CI, publish reports as artifacts, and publish test results in the platform's supported format. Confirm the test agent has the right runtime. Add one intentionally failing assertion and verify the pipeline fails and downstream deployment is skipped; remove it afterward. Assign fast tests to PRs and integration/load suites to scheduled or pre-release runs.

## Exercises

1. Create a test matrix with test type, trigger, environment, agent requirements, runtime, and failure policy.
2. Define coverage and quality gates that do not encourage gaming.
3. Write a flaky-test triage and quarantine policy, including owner and repair deadline.

## Verification

- Failed test fails CI and blocks promotion.
- Test results and coverage link to the source revision.
- Parallel tests are isolated and test data is not shared unsafely.
