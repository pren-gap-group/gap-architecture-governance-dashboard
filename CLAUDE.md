# CLAUDE.md – AI working agreement

This file tells Claude (Claude Code in VS Code, or Claude in Cowork) how to work in this repository. Humans should read it too: it is the contract between the human and AI members of the team.

## Project context
- **Product:** GAP Architecture Governance Dashboard (AGD) for the CTO Office.
- **Sponsor / Product Owner / approver:** Pren Naidoo (Enterprise Architect).
- **Backlog:** Jira project `AGD` – https://gap-group.atlassian.net/jira/software/projects/AGD
- **Documentation:** Confluence space `AGD` – https://gap-group.atlassian.net/wiki/spaces/AGD
- **Phase:** see the Project Charter in Confluence (AGD-DOC-001). The technology stack is decided in Phase 2. Until then, do not add application frameworks.

## Golden rules
1. **Never commit to `main`.** Always work on `feature/AGD-<n>-<short-description>` (or `fix/…`, `chore/…`).
2. **No ticket, no work.** Every change must trace to a Jira key. If there isn't one, stop and ask.
3. **Never merge, release, tag or deploy.** A human approves and merges every pull request.
4. **No real data in the repo.** Project data is confidential. Use only synthetic data in `data/sample/`. Never commit secrets, tokens, connection strings or personal data.
5. **Documentation goes to Confluence, not the repo.** Do not create design docs, ADRs or other docs in this repo. Code comments, docstrings and this repo's operational files (README, CLAUDE.md, CONTRIBUTING.md) are the only exceptions.
6. **Ask, don't guess.** If requirements are unclear or a change touches architecture, propose options and wait for a decision.
7. **Comply with GAP AI policy IS-POL-038.** A human reviews all AI output before it is merged or released.

## How to work
- Keep changes small: one ticket per pull request.
- Write or update tests with every code change, and run them before saying the work is done.
- Follow the formatting in `.editorconfig` and the linters configured for the chosen stack.
- Commit message format (Conventional Commits with Jira key):
  ```
  feat(AGD-12): ingest Delivery Portfolio Workbook

  <what and why>

  Co-Authored-By: Claude <noreply@anthropic.com>
  ```
  Use `feat`, `fix`, `test`, `refactor`, `docs`, `chore`, `ci`. AI-authored commits must include the `Co-Authored-By` trailer.

## Handover protocol (human ⇄ AI)
When you stop working on a branch, whether you are the human or the AI, update the pull request description (or open a draft pull request) with:
- **Done:** what is complete.
- **Next:** the next concrete step.
- **Open questions / risks.**
- **How to test.**

When picking up a branch, read the handover note and the Jira ticket first, then run the tests before changing anything.

## Commands
_Populated once the stack is chosen in Phase 2._
- Install: `TBD`
- Test: `TBD`
- Lint: `TBD`
- Run locally: `TBD`
