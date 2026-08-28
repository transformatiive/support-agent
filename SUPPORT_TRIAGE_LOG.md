# Support Triage Log

Tracks automated runs that scan `suporte@transformatiive.com` for new client emails and
create JIRA tickets (label: `Support Triage`) under the matching client Epic in the
`TRNSF` project. **Check this log before creating a new ticket to avoid duplicates** —
if a request from the same thread/customer already has an entry below, do not
re-create it; update the existing ticket instead.

Process follows `inbox-jira-review.skill` / `jira-task-manager.skill` (domain → Epic
mapping in `references/config.json` of `inbox-jira-review.skill`), cloud ID
`d508f45a-2b02-4988-a34a-057d4ff2860d`, project `TRNSF`.

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
| 2026-08-28 17:11 | `to:suporte@transformatiive.com` (covers to/cc/bcc), last 1h15m (15:56–17:11 UTC) | No new emails to `suporte@transformatiive.com` in the window. Only thread involving that address today is the ongoing Leasys PT "Surveys Leasys" CC thread (TRNSF-14), last message at 11:02 UTC — outside the window, already an active/known thread, not a new support request. n8n MCP connector is unauthenticated this run (auth required, cannot be completed non-interactively); epic mapping resolved instead from the static `epic_mapping` table in `inbox-jira-review.skill`'s `references/config.json` (cloud ID `d508f45a-2b02-4988-a34a-057d4ff2860d`, project `TRNSF`), same table reproduced above. | None |
