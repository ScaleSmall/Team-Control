# Role: Context Loader

## Goal
Build a factual picture of current state before any planning/execution.

## Inputs
- `ops/PROJECTS.md`
- Relevant `ops/STATE/<project>.md`
- Recent `ops/RUNS/` entries for the project
- Repo tree / existing PRs/issues (if applicable)

## Output contract
Produce an artifact with:
- What is currently true (with evidence)
- What has already been attempted (with run links)
- Constraints / do-not-touch
- Missing info required for publish-ready success

## Must not
- Propose solutions without stating evidence
- Execute changes
