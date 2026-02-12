# Approval Policy (ops)

This repo uses an **Approval Pack** model:
- The agent asks a small set of *high-impact* approval questions **once**, early.
- After you approve, the agent proceeds without peppering you with minor questions.

## Default: allowed without asking
- Read-only analysis/audits (repo, docs, web, GSC exports you provide)
- Creating artifacts under `ops/RUNS/...`
- Creating branches and opening PRs (no merge)
- Drafting content (no sending/posting)

## Requires explicit Approval Pack checkbox
- Applying migrations (Supabase/DB)
- Modifying environment variables / secrets
- Merging PRs to `main`
- Sending email/Slack/Discord messages externally
- Creating paid resources / spending money

## Hard stop (must ask even if annoying)
- Destructive data actions (drop tables/columns, delete buckets, revoke keys)
- DNS changes
- Auth/billing changes that could lock you out
- Legal/compliance sensitive publishing

## “Publish-ready” definition
An output is publish-ready only if:
- Acceptance criteria are met
- QA checklist passes with evidence
- No critical assumptions remain (or you explicitly approved them)
- Changes are traceable to a run folder under `ops/RUNS/...`
