# Website Production System

A repository-level engineering standard for delivering premium corporate websites through specification-driven, agent-executed work.

## Purpose

This repository defines how a website project is structured, designed, implemented, tested, reviewed, and released. It is an engineering baseline, not a claim that external agents or deployment infrastructure are already connected.

## Operating model

- **Principal:** supplies business intent, approves material product and release decisions.
- **Architecture/orchestration:** converts requirements into bounded tasks, selects dependencies, coordinates work, and verifies evidence.
- **Codex execution:** implements assigned repository tasks and reports changed files, commands, test results, and blockers.
- **Claude review:** provides independent review of architecture, implementation, risks, and acceptance criteria when an execution channel is available.
- **Runtime provider:** hosts the approved application. Cloudflare is a candidate runtime, not an assumed dependency.
- **Repository host:** stores versioned source and review artifacts. It is not designated as enterprise-wide authority by this document.

## Delivery lifecycle

1. Discovery and requirements.
2. Information architecture and content model.
3. Brand and design-system specification.
4. Page and interaction design.
5. Implementation task decomposition.
6. Agent implementation in isolated branches.
7. Automated and independent verification.
8. Staging deployment and acceptance.
9. Production release, rollback readiness, and operations.

## Repository map

- `AGENTS.md` — execution rules for coding agents.
- `docs/architecture/system-overview.md` — system boundaries and project structure.
- `docs/engineering/task-contract.md` — required task input/output contract.
- `docs/quality/release-gates.md` — verification and release criteria.
- `docs/website/delivery-standard.md` — website-specific quality standard.
- `.github/PULL_REQUEST_TEMPLATE.md` — change evidence template.

## Current state

This commit establishes documentation and workflow contracts only. It does not create an application, connect Codex or Claude, configure CI, provision Cloudflare resources, or deploy a website.
