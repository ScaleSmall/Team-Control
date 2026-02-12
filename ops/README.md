# ops/

This folder is the **source of truth** for agent-driven work in this repo.

Principles:
- Every run creates an auditable artifact under `ops/RUNS/...`.
- Project state lives in `ops/STATE/...`.
- Task playbooks/templates live in `ops/TASKS/...`.
- Work should be **idempotent**: re-running a task should not undo prior correct work.

## Run lifecycle (high level)
1. **Context load**: read relevant `ops/STATE/*` and recent `ops/RUNS/*`.
2. **Plan**: produce a plan + acceptance criteria + risk classification.
3. **Approval Pack**: front-load approvals once (avoid constant questioning).
4. **Execute**: do the work in a branch/draft.
5. **QA**: verify against acceptance criteria; include evidence.
6. **Publish**: PR / final deliverable.

## Quick links
- Project index: `ops/PROJECTS.md`
- Approval policy: `ops/APPROVALS.md`
- Run history: `ops/RUNS/`
