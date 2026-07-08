# Support Triage Log

This file tracks JIRA tickets created by the automated support-triage routine
so future runs don't create duplicates for the same customer request.

**Process (per `inbox-jira-review.skill` / `jira-task-manager.skill`):**
1. Scan Gmail for messages sent to `suporte@transformatiive.com` in the lookback window.
2. Identify the customer from the sender domain / email signature using the
   `epic_mapping` table below (see `inbox-jira-review/references/config.json`,
   also available via the n8n credential vault at
   `https://trnsf.up.railway.app/webhook/credential-vault`).
3. Search JIRA (and Confluence) for prior related tickets under the customer's Epic.
4. Draft a description + action plan for the request.
5. Create a JIRA ticket under the customer's Epic, labeled `Support Triage`.
6. Log the ticket below.

## Customer → Epic mapping (reference)

| Domain | Epic |
|---|---|
| alfaseguros.pt | TRNSF-1 |
| leasys.com | TRNSF-6 (Luxembourg) / TRNSF-14 (Portugal) |
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
| scalarly.com / scafz.com / gimm.pt / nbiz.pt / cobaialisboa.pt | unmapped — flag for manual epic assignment |

## Tickets created

| Date (UTC) | Customer | Epic | JIRA Ticket | Summary | Source Email |
|---|---|---|---|---|---|
| _none yet_ | | | | | |

## Run history (no action needed)

| Date (UTC) | Window checked | Result |
|---|---|---|
| 2026-07-08 | Emails to suporte@transformatiive.com, last 1h15m | No new emails found. Most recent email to that address was 2026-06-28 (outbound, from nbarreto, 10 days prior) — no client support request in window. No tickets created. |
