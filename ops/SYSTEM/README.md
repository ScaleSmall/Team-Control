# AI System Team (multi-agent)

This directory defines the **pipeline** that produces reliable, publish-ready outputs.

Core design:
- Pipeline, not a chatroom: work flows through roles with **explicit artifacts**.
- Every role has a strict **I/O contract** (structured output).
- High-impact actions are controlled by **gates** and an **Approval Pack**.
- Runs are logged under `ops/RUNS/<run-id>/...`.

## Roles
- Context Loader
- Planner / PM
- Producer / Executor
- Critic / QA
- Editor / Finalizer
- Publisher (optional; typically gated)

See role definitions in `ops/SYSTEM/roles/`.

## Contracts
- Shared output schema: `ops/SYSTEM/schemas/artifact.schema.json`
- Decision thresholds + tripwires: `ops/SYSTEM/checklists/tripwires.md`

## How to run
1) Create a run folder under `ops/RUNS/<run-id>/`.
2) Context Loader produces `01_context.md`.
3) Planner produces `02_plan.md` + `03_risk_and_approvals.md`.
4) Producer executes in a branch/draft and logs in `04_worklog.md`.
5) QA produces `06_qa_report.md`.
6) Editor finalizes the publish-ready output.

## Publish-ready gates
A run cannot be published unless QA passes and evidence is recorded.
