# Support Triage Log

Tracks automated runs that scan `suporte@transformatiive.com` for new client emails and
create JIRA tickets (label: `Support Triage`) under the matching client Epic in the
`TRNSF` project. **Check this log before creating a new ticket to avoid duplicates** —
if a request from the same thread/customer already has an entry below, do not
re-create it; update the existing ticket instead.

Process follows `inbox-jira-review.skill` / `jira-task-manager.skill` (domain → Epic
mapping in `references/config.json` of `inbox-jira-review.skill`), cloud ID
`d508f45a-2b02-4988-a34a-057d4ff2860d`, project `TRNSF`.

## ⚠️ Known issue: run log not landing on `main`

Each scheduled run opens its own branch + PR (`claude/busy-dirac-*`) with a log entry,
but as of 2026-08-30 **none of PR #23 through #52 (2026-07-31 through 2026-08-29) have
been merged**. This file on `main` is still missing ~30 days of run history that only
exists in those open, unmerged PRs. The PR backlog needs a merge pass (or the
schedule needs to commit straight to `main`) to keep this log — and its
duplicate-prevention purpose — actually reliable.

## Domain → Epic reference (from skill config)

| Domain | Epic |
|---|---|
| alfaseguros.pt | TRNSF-1 |
| leasys.com (Luxembourg) | TRNSF-6 |
| leasys.com (Portugal) | TRNSF-14 |
| auditconsult.pt | TRNSF-73 |
| frotcom.com / pt.frotcom.com | TRNSF-274 |
| cjseguros.pt | TRNSF-330 |
| oficialseguros.pt | TRNSF-425 |
| buenavistaequity.pt | TRNSF-429 |
| fittestequipment.com | TRNSF-461 |
| institutounicenter.com | TRNSF-56 |
| teresabranco.com | TRNSF-9 |
| stelic.com | TRNSF-589 |
| simplybus.pt | TRNSF-585 |
| sie.pt | TRNSF-439 |
| estrategor.pt | TRNSF-601 |

## Run Log

| Run (UTC) | Email window checked | Result | Tickets created |
|---|---|---|---|
| 2026-07-13 17:00 | `to:suporte@transformatiive.com` / `cc:suporte@transformatiive.com`, last 1h15m (15:45–17:00 UTC) | No new emails to `suporte@transformatiive.com` in the window. Mailbox's only messages to that address are from 2026-06-28 (already answered, internal CRM change list) and August 2025 (AuditConsult / TRNSF-73, already answered). | None |
| 2026-08-30 17:09 | `to:suporte@transformatiive.com`, last 1h15m (15:54–17:09 UTC), re-checked back to 14:00 UTC | No new emails to `suporte@transformatiive.com` in the window. Most recent message to that address is the ongoing Leasys PT "Surveys Leasys" thread (TRNSF-14) from 2026-08-28 11:02 UTC — already tracked, outside the window. `n8n` MCP connector was unauthenticated this run; epic mapping resolved from the static table below instead of live vault data. | None |
