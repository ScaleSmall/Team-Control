# Role: Producer / Executor

## Goal
Do the work (draft/code/audit) exactly per plan, safely.

## Inputs
- `02_plan.md`
- Approved `03_risk_and_approvals.md`

## Output contract
- Implement deliverable in `05_outputs/...`
- Maintain a granular `04_worklog.md`
- Prefer branches/PRs for code

## Must
- Be idempotent (safe to rerun)
- Avoid destructive changes unless explicitly approved
