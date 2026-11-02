# Evidence Corrections Log
Burn and Churn Coffee IAM Access Review Lab

---

## Purpose

The access matrix and findings are dated records of the Q1 2026 review and are not silently rewritten. When a correction is unavoidable, it is logged here with the reason and the program alignment item (`AL-##`) that required it. Review dates, decisions and finding statuses are unchanged unless an entry says otherwise.

---

## 2026-10-30: Program alignment, phase 2

The program's consistency checker compared this matrix with the hub's MFA evidence ([mfa-status.csv](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/07-evidence-pack/artifacts/access/mfa-status.csv)) and found three cells that contradicted the rest of the record.

| File | Row | Change | Reason | Item |
|---|---|---|---|---|
| [user-access-matrix.csv](user-access-matrix.csv) | Ethan Brooks, Google Workspace | MFA_Enabled `Yes` → `No`; note `Access appropriate` → `MFA not enabled` | Finding F-004, its remediation-tracker entry and the hub's MFA export all record that Ethan had no Google Workspace MFA; only this cell disagreed | AL-12 |
| [user-access-matrix.csv](user-access-matrix.csv) | Ethan Brooks, Toast POS | Note `MFA not enabled` → `Access appropriate` | Toast cashier PIN logins are outside MFA scope by design (personal PINs, one user signed in at a time, sign-out and no-sharing rules; see the program's [roles.md](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/00-company-profile/org/roles.md)). The note now matches the other 14 cashiers | AL-12 |
| [user-access-matrix.csv](user-access-matrix.csv) | Aiden Scott, Google Workspace | MFA_Enabled `Yes` → `No` | The hub's MFA export (as `barista2@`) records no MFA for this account; the hub record is kept as the source | AL-18 |

F-005 and the VM addendum gained a note labelling them as a lab demonstration outside the company's system boundary (AL-17).

---

## 2026-10-30: Program alignment, story review

| File | Change | Reason |
|---|---|---|
| [quarterly-access-review-summary.md](../review-summary/quarterly-access-review-summary.md) | Review date (2026-03-25) and reviewers (Owner, Store Manager) added; "14 Employees" → 15; note that F-005 isn't counted; corrections and status section | The procedure requires the date and reviewer names; both are recorded in the program's access review export. The matrix lists 15 active employees. Sign-off is noted as missing rather than invented |
| [access-review-checklist.md](access-review-checklist.md) | Eight steps ticked; management approval left unticked | Every ticked step is proven by an existing artifact; no Q1 sign-off exists |
| [remediation-tracker.csv](../remediation/remediation-tracker.csv) | F-001 to F-004 → Overdue; `Last_Status_Check` and `Closure_Plan` columns added | Status check on 2026-10-30 (see [status checks](../remediation/status-checks.md)). This is a status update, not a correction of the original record |

---

*This document is a simulation for educational and portfolio purposes only.*
