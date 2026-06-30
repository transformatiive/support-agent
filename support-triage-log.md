# Support Triage Log

Tracks emails processed from `suporte@transformatiive.com` into JIRA tickets.
Maintained by the automated support-agent routine to prevent duplicate ticket creation.

---

## 2026-06-28 — Buenavista Equity (TRNSF-429)

**Email:** "Alterações e melhorias CRM"
**From:** Francisco Lino Marques &lt;flm@buenavistaequity.pt&gt; (Partner, Buenavista Equity)
**Received:** 2026-06-28T21:43:36Z
**Client Domain:** buenavistaequity.pt → Epic **TRNSF-429** (Buenavista)

**Summary of request:**
Comprehensive batch of CRM improvement and correction requests covering:

- **Pipeline / Accounts / Contacts:**
  - Private notes on Accounts
  - Auto-fill description field using bio-generator skill (copy-paste from Perplexity → automatic)
  - Linking Board Team (contacts) and Service Providers (accounts) to Portfolio accounts
  - Cap table missing on Portfolio + Active accounts
  - KYC segment should only appear when Contact Type = Investor
  - Account type = BV: simplify layout to show only Identification fields; remove Address and Description sections
  - Unknown "e" field appearing in Identification segment and Related List
  - Automatic pipeline summaries not running; documents not saved correctly when stage advances
  - Source data file upload (cleaned historical DB, capture current stage + pipeline progress)
  - Source Type "Others" → should trigger a free-text field (like Events already does)
  - "Watch+" stage: history not visible
  - Button harmonisation across all pipeline stages (fast Track available at every stage for owner profile)
  - Private Accounts → all Activities (Tasks, Meetings, Calls) should be private by default
  - Private tasks: ability to create private task on a public account
  - Agreements Key Terms section missing (replicate Term Sheet logic)
  - Memo generator integration at Sourcing and Pre-IC stages

- **Portfolio:**
  - Portfolio + Active company accounts: add Permanent Cert. Code, Cert. Validity, Beneficial Ownership Register, BOR date, One Drive Investor URL fields
  - Source Type: align with Pipeline options; add conditional text field for event-type sources
  - Remove SIFIDE field from Portfolio accounts

**JIRA Tickets Created:**

| Ticket | Summary | Status | Labels | Created |
|--------|---------|--------|--------|---------|
| [TRNSF-1221](https://transformatiive.atlassian.net/browse/TRNSF-1221) | Support Triage \| BV: CRM — Alterações e melhorias (email FLM 28-Jun-2026) | Done | Support-Triage | 2026-06-28 |
| [TRNSF-1223](https://transformatiive.atlassian.net/browse/TRNSF-1223) | BV \| Support Triage — Batch de Alterações e Melhorias CRM (28 Jun 2026, Francisco Marques) | Done | Support_Triage | 2026-06-29 |
| [TRNSF-1226](https://transformatiive.atlassian.net/browse/TRNSF-1226) | Buenavista CRM — Backlog de melhorias e correcções (Pipeline, Accounts, Contacts, Portfolio) | INBOX | Support-Triage | 2026-06-29 |

**Action taken:** Email already fully triaged into JIRA by the time of this routine run (2026-06-30). No new tickets needed.

---

## Routine Run Log

| Run Date | Window Checked | Emails Found | Tickets Created | Notes |
|----------|---------------|--------------|-----------------|-------|
| 2026-06-30 ~16:50 UTC | Last 1h15m (≥15:35 UTC) | 0 | 0 | No new emails to suporte@ in window. BV email from 2026-06-28 already processed into TRNSF-1221, TRNSF-1223, TRNSF-1226. |
