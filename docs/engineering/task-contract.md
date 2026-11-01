# Engineering Task Contract

All agent work must be expressed as a bounded, independently verifiable task.

## Required task fields

| Field | Requirement |
|---|---|
| ID | Stable unique task identifier |
| Objective | One outcome, stated in observable terms |
| Context | Relevant paths, constraints, and existing behavior |
| Inputs | Approved designs, content, schemas, API contracts |
| Scope | Explicit files, modules, or behaviors included |
| Out of scope | Adjacent work the agent must not change |
| Dependencies | Tasks or services that must exist first |
| Acceptance criteria | Binary or measurable pass conditions |
| Verification | Exact commands, tests, or manual checks |
| Risk | Security, data, compatibility, and release impact |
| Output | Diff, tests, implementation report, unresolved blockers |

## Task template

```yaml
id: WEB-000
title: Implement [bounded capability]
objective: "[Observable result]"
context:
  repository: "[owner/repository]"
  base_branch: "[branch]"
  target_branch: "[branch]"
inputs:
  - "[approved specification or asset]"
scope:
  include:
    - "[path or behavior]"
  exclude:
    - "[explicitly excluded area]"
dependencies: []
acceptance_criteria:
  - "[testable condition]"
verification:
  - "[exact command or test]"
risk_level: low
required_report:
  - changed_files
  - commands_run
  - test_results
  - risks_and_blockers
```

## Execution protocol

1. Orchestrator validates task completeness and dependency readiness.
2. Execution agent inspects the target branch and reports its starting state.
3. Agent implements only the defined scope on an isolated branch.
4. Agent runs the specified verification and reports raw outcomes.
5. Independent review checks the diff and evidence.
6. Orchestrator resolves findings and requests rework where needed.
7. Merge and deployment occur only under the project's configured approval policy.

## Parallelism

Parallelize only tasks with non-overlapping write scopes or explicit interface contracts. Shared files, global tokens, routing, package manifests, and deployment configuration require a designated owner or serialized changes.

## Failure handling

A failed command is evidence, not a reason to claim success. Preserve logs, classify the failure (environment, dependency, implementation, or specification), and create a follow-up task with a reproducible condition.
