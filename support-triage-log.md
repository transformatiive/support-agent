# Support Triage Log

Tracks JIRA tickets created by the automated support-inbox triage routine
(`suporte@transformatiive.com` → JIRA, tagged **Support Triage**), so future
runs don't create duplicates for the same request.

How this is used:
- Each run checks Gmail for new mail to `suporte@transformatiive.com` since the
  last run.
- For every genuine client request found, a JIRA ticket is created under the
  client's Epic (see `epic_mapping` in `inbox-jira-review/references/config.json`)
  and labeled `Support Triage`.
- Every ticket created is logged below with the source email so later runs can
  check "did we already file this?" before creating a new one.
- Before filing anything, also check JIRA directly: `labels = "Support Triage"`.

## Tickets created

| Date | Ticket | Client / Epic | Summary | Source email |
|------|--------|----------------|---------|---------------|
| _none yet_ | | | | |

## Run history

| Run (UTC) | Window checked | Emails to suporte@ found | Tickets created |
|-----------|----------------|---------------------------|------------------|
| 2026-07-01 17:08 | last 1h15m (15:53–17:08) | 0 | 0 |
