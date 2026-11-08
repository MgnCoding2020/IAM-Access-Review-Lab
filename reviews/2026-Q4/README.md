# Q4 2026 Access Review (planned)

The first access review run in **Microsoft Entra ID**, after the Microsoft 365 cutover (hub CR-001, 2026-11-15). It is also the **post-implementation review** for CR-001 and CR-003.

**Status:** Planned. Nothing here is evidence yet.

---

## Scope

Everything in the [procedure's scope](../../procedure/quarterly-access-review-procedure.md), plus the [planned additions](../../procedure/quarterly-access-review-procedure.md#planned-additions-to-scope-first-review-after-2026-11-15): admin and break-glass accounts, the vendor guest, the password manager, network device admin accounts, and connected-device vendor portals.

## What this review must do

1. **Confirm the Q1 findings are closed** (IAM:F-001 to F-004), with evidence, or record them as still open.
2. **Raise what Q1 missed:** the generic shared vendor accounts ("Vertex IT Support", "NorthPeak Systems") that P-001 §5.7 doesn't allow (program finding AL-13). Record it as a new finding with its closure evidence from the CR-003 handover.
3. **Check the new design:** admin roles exactly as in the hub's `admin-accounts.csv`, `grp-bc-*` group membership against `people.csv`, the website's `bc-website-staff` app-role assignments against `people.csv` (and that Entra ID itself refuses an account with no role), break-glass sign-ins explained, no personal accounts on vendor portals.
4. **Separation of duties:** the IT Technician exports the data; the Owner and Store Manager review and **sign off** (the sign-off missing from Q1).

## Planned files

| File | Contents |
|---|---|
| `evidence/` | Redacted Entra exports (users, groups, admin roles, guests, sign-ins), from the hub's live tenant evidence |
| `evidence/user-access-matrix.csv` | The review matrix for every in-scope account |
| `findings/access-review-findings.md` | Findings, cited outside this repository as `IAM-Q4:F-###` |
| `remediation/remediation-tracker.csv` | Same columns as Q1; read automatically by the hub's monthly monitor |
| `review-summary/quarterly-access-review-summary.md` | Date, reviewers, results and the management sign-off |

Findings roll up to the hub POA&M under **POAM-014** (AC-2, AC-6).

---

*This document is a simulation for educational and portfolio purposes only.*
