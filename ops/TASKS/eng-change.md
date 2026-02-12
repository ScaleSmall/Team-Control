# Task Playbook: Engineering Change

## Output (publish-ready)
- PR link (or patch) + summary
- `ops/RUNS/<run-id>/06_qa_report.md` with evidence

## Required artifacts per run
- `00_intake.md`
- `01_context.md`
- `02_plan.md` (with acceptance criteria)
- `03_risk_and_approvals.md` (Approval Pack)
- `04_worklog.md`
- `06_qa_report.md`

## QA checklist (minimum)
- [ ] No destructive changes without explicit approval
- [ ] Idempotent steps (safe to re-run)
- [ ] Tests/lint pass (list commands)
- [ ] Diff reviewed: no accidental deletions
- [ ] Env/config changes documented

## Approval Pack template
Include checkboxes:
- [ ] Create branch + PR
- [ ] Merge PR
- [ ] Apply migrations (dev/staging)
- [ ] Apply migrations (production)
- [ ] Modify env vars
- [ ] Deploy to production
