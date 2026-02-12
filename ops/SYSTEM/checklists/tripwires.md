# Tripwires (hard stops / escalation)

If any of these conditions are true, the agent must **stop and ask** (or produce an Approval Pack update) before proceeding.

## High-risk actions
- Spending money / creating paid resources
- Sending/posting externally (email, Slack, Discord, social)
- Changing auth, billing, DNS
- Modifying production env vars/secrets
- Applying migrations to production
- Any destructive data action (delete/drop/revoke)

## Quality / uncertainty
- Confidence < 0.7
- Any critical assumption without evidence
- Conflicting sources or inability to verify a key claim
- Output deviates from required format / missing required fields

## Safety / access
- Credentials requested in plain text
- Tool access exceeds what was approved

## Publish-ready gate
- If QA fails, nothing is published.
