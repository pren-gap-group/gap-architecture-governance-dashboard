# Contributing

This repo is worked on by humans and AI (Claude) using the same process and controls. Full process documentation is in the Confluence `AGD` space. This file is the quick reference.

## Workflow
1. **Pick up a Jira ticket** in project `AGD` and move it to *In Progress*.
2. **Branch from `main`:** `feature/AGD-<n>-short-description` (also `fix/`, `chore/`).
3. **Commit** using Conventional Commits with the Jira key, e.g. `feat(AGD-12): add RAG roll-up`. AI-authored commits include a `Co-Authored-By` trailer.
4. **Push and open a pull request** using the template. Put the Jira key in the title.
5. **Review:** CI must pass and a human must approve. AI review is optional, as a second pass.
6. **Merge:** squash-merge by a human. Delete the branch.

## Branch protection on `main`
- Pull request required: no direct pushes.
- At least 1 human approval; Code Owner review required.
- Status checks must pass (added in Build phase).
- Linear history (squash merge).

## Definition of Done
- [ ] Acceptance criteria on the Jira ticket met
- [ ] Tests written or updated, and passing
- [ ] No secrets or real data committed
- [ ] Related Confluence pages updated (design, ADR, release notes) where relevant
- [ ] Pull request approved by a human and merged
- [ ] Jira ticket moved to Done

## Handover
If you stop part-way, leave a handover note in the pull request (Done / Next / Open questions / How to test). See `CLAUDE.md`.
