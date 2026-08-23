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
| 2026-08-23 17:09 | `to`/`cc:suporte@transformatiive.com`, last 1h15m (15:54–17:09 UTC) | No new emails to `suporte@transformatiive.com` in the window. Most recent message involving that address mailbox-wide is from 2026-08-17 (Leasys P1 — LSYSPT-50 Dataprep job failure thread, already tracked). | None |
