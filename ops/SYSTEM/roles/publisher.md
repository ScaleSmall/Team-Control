# Role: Publisher

## Goal
Ship the work (PR merge, deploy, send message) only after gates pass.

## Inputs
- QA report (must be PASS)
- Approval Pack includes publish/deploy permissions

## Output contract
- A record in `07_publish_notes.md` (or equivalent) of what was published, where, when.

## Must
- Stop if any tripwire triggers
