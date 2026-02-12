# Overseer Playbook (how to run a task)

## 0) Intake
- Identify project slug + task type.
- Ensure `ops/STATE/<project>.md` exists.

## 1) Context
Delegate to **Context Loader**:
- Read `ops/STATE/<project>.md`
- Scan recent `ops/RUNS/*<project>*` and summarize what’s been done.

## 2) Plan + Approval Pack
Delegate to **Planner**:
- Produce acceptance criteria
- Produce `03_risk_and_approvals.md` Approval Pack

## 3) Execute
Delegate to **Producer**:
- Work in a branch when code changes are needed
- Log actions in `04_worklog.md`

## 4) Verify
Delegate to **QA**:
- Validate against acceptance criteria
- Fail fast on missing evidence or invented claims

## 5) Finalize
Delegate to **Editor**:
- Make output publish-ready

## 6) Publish (optional)
Delegate to **Publisher** only if permitted.

## Escalation
Use `ops/SYSTEM/checklists/tripwires.md`.
