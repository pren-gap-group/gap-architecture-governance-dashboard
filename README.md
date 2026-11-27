# GAP Architecture Governance Dashboard (AGD)

A single view of architecture governance across GAP's top digital delivery projects: reviews, decisions, risks, waivers and compliance with standards. Built for the CTO Office.

This project is also GAP's **reference SDLC delivered jointly by a human and an AI**. Lessons learned here will form the GAP SDLC Standard, which will live in a separate repository.

| What | Where |
|---|---|
| Documentation (charter, requirements, design, ADRs, test plans, release notes) | [Confluence – AGD space](https://gap-group.atlassian.net/wiki/spaces/AGD) |
| Backlog, sprints, releases | [Jira – AGD project](https://gap-group.atlassian.net/jira/software/projects/AGD) |
| Code | This repository |

> **All documentation lives in Confluence.** This repo contains only code, tests, synthetic sample data, and the files that make the repo work (this README, `CLAUDE.md`, `CONTRIBUTING.md`).

## Getting started

### Option A – Dev container (recommended)
1. Install [VS Code](https://code.visualstudio.com/), [Docker Desktop](https://www.docker.com/products/docker-desktop/) and the **Dev Containers** extension.
2. Clone this repo and open it in VS Code.
3. When prompted, choose **Reopen in Container**. Git, Node.js, Python, GitHub CLI, Azure CLI and Claude Code are pre-installed.

### Option B – GitHub Codespaces
Click **Code → Codespaces → Create codespace on main**. Same environment, nothing to install.

### Option C – Local
Install the tools listed in `.devcontainer/devcontainer.json` yourself. Not recommended, as versions can drift.

## Repository layout

```
.devcontainer/   Shared dev environment (human, AI, CI)
.vscode/         Recommended extensions and editor settings
.github/         Pull request template, issue routing, code owners, workflows
src/             Dashboard source code (technology chosen in Phase 2)
tests/           Automated tests
data/sample/     Synthetic test data ONLY – never real project data
CLAUDE.md        Working agreement for the AI (Claude Code)
CONTRIBUTING.md  How we work: branches, commits, pull requests, Definition of Done
```

## How humans and AI work together

Either a human or Claude can pick up any piece of work. Handover always happens through Git:

1. Every change starts from a Jira ticket (`AGD-<n>`).
2. Work happens on a branch `feature/AGD-<n>-short-description`.
3. Whoever stops work leaves a **handover note** in the pull request description.
4. Every pull request needs CI to pass **and a human approval**, whoever wrote it.

See [CONTRIBUTING.md](CONTRIBUTING.md) and [CLAUDE.md](CLAUDE.md).

## Status

Phase 0 – Initiation. See the [Project Charter](https://gap-group.atlassian.net/wiki/spaces/AGD/pages/83623938).
