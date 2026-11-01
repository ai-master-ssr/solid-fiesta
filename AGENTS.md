# Agent Execution Contract

## Mandatory rules

1. Read this file and the relevant documents under `docs/` before changing code.
2. Work only on the assigned task and stated repository/branch.
3. Inspect the existing implementation before proposing replacement architecture.
4. Preserve existing behavior unless the task explicitly changes it.
5. Do not invent credentials, endpoints, environment variables, APIs, deployments, test results, or completed work.
6. Do not commit secrets, tokens, private keys, personal data, or production configuration values.
7. Do not introduce dependencies without explaining why they are required.
8. Do not perform destructive data, infrastructure, or history operations without explicit authorization.
9. Keep changes small, reviewable, and reversible.
10. If blocked, stop at the boundary, report the exact blocker, and do not fabricate a workaround.

## Required implementation report

Every completed task must report:

- Task identifier and objective.
- Base branch and working branch.
- Files created, modified, or deleted.
- Design and implementation decisions.
- Commands executed.
- Test results, including failures and skipped checks.
- Security, accessibility, performance, and compatibility implications.
- Remaining risks and follow-up tasks.
- Commit SHA or pull-request reference, if one actually exists.

## Agent responsibilities

### Implementation agent (Codex)

Implement the assigned scope, add or update tests, run available checks, and provide reproducible evidence. Do not self-approve a release.

### Independent reviewer (Claude or designated reviewer)

Review the diff against the task contract, architecture, correctness, security, accessibility, and maintainability. Report findings with file paths and severity. Do not claim to have run tests unless execution evidence is available.

### Orchestrator

Own task decomposition and dependency ordering, ensure acceptance criteria are testable, reconcile implementation and review findings, and report verified status. An orchestration plan is not evidence of execution.

## Definition of done

A task is done only when its acceptance criteria pass, relevant checks have been run, review findings are resolved or explicitly accepted, and the implementation report is complete. Deployment requires a separate release approval and deployment evidence.
