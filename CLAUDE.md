# support-agent

Automated support-triage repo. A scheduled routine periodically checks
`suporte@transformatiive.com` for new client emails and, when one requires
action, creates a JIRA ticket (label `Support Triage`) under the matching
client Epic in the `TRNSF` project. See `inbox-jira-review.skill` /
`jira-task-manager.skill` for the process, and `SUPPORT_TRIAGE_LOG.md` for
the run history (check it before creating a ticket to avoid duplicates).

## Git / PR policy for scheduled runs

All work happens on the designated `claude/...` branch for the session.

- **Log-only run (no new emails, or emails reviewed but no ticket needed):**
  commit the `SUPPORT_TRIAGE_LOG.md` entry and push the branch. **Do not**
  open a pull request for this alone — it's a no-op audit entry, not a
  change worth reviewing. Let it accumulate on the branch.
- **Real work happened (a JIRA ticket was created):** commit the log entry,
  push, and open a PR as usual (per the standard "always PR after pushing"
  rule) — this bundles any accumulated no-op log entries with the run that
  actually did something, so there's one PR per unit of real work instead
  of one per cron tick.

This exists because opening a PR every ~1h15m tick — even when the only
change is "checked, found nothing" — creates review noise with no
corresponding value. The log file itself is the audit trail; the PR is for
when there's an actual JIRA ticket to point to.
