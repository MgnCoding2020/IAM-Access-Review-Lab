# Quarterly Access Review Procedure

Burn and Churn Coffee

---

## 1. Purpose

The purpose of this procedure is to ensure that user access to company systems and data is periodically reviewed to confirm that access remains appropriate for each user's job responsibilities.

Regular access reviews reduce the risk of:

* Unauthorized access
* Excessive user permissions
* Former employee accounts remaining active
* Improper administrative privileges

This procedure demonstrates how Burn and Churn Coffee performs a **Quarterly Access Review** as part of its Identity and Access Management (IAM) governance program.

---

## 2. Scope

This review applies to systems used to operate the business and store company or operational data.

Systems included in this review:

* Google Workspace (email, Drive, administrative roles)
* Toast POS system
* xtraCHEF inventory and supplier platform
* QuickBooks Online accounting platform
* Store networking administration interfaces

This review includes all users with access to these systems, including:

* Business Owner
* Store Manager
* Shift Leaders
* Store Employees
* Authorized IT vendors

### Planned additions to scope (first review after 2026-11-15)

The program added accounts and systems after the Q1 2026 review. From the Q4 2026 review on, the review also covers:

| What | Check | Program source |
|---|---|---|
| Admin accounts (`adm-olivia.carter`, `adm-riley.morgan`) | Exactly the roles in `admin-accounts.csv`; members of `grp-bc-admins` only; the IT Technician exported the data but didn't sign off | [admin-accounts.csv](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/00-company-profile/org/admin-accounts.csv), [roles.md](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/00-company-profile/org/roles.md) |
| Break-glass accounts | Every sign-in since the last review explained | [roles.md](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/00-company-profile/org/roles.md) |
| Vendor guest (VC-001, once CR-004 is active) | Still needed, in `grp-bc-vendors` only, end date not passed | [CR-004](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/09-change-management/CR-004-vendor-guest-access.md) |
| Password manager organization | Exactly two members: the Owner and the IT Technician | [PR-009](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/05-procedures/PR-009-credential-vault.md) |
| Network device admin accounts (firewall, access points) | Named accounts only; no default or vendor accounts left | [P-005](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/04-policies/P-005-network-security.md) §5 |
| Connected-device and vendor portal accounts (cameras, espresso service, temperature monitoring, speaker app) | Company-owned; individual camera accounts for the Owner and Store Manager with MFA; no personal accounts | [PR-011](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/05-procedures/PR-011-connected-devices.md), connected device checklist |
| Generic vendor accounts | None remain (the Vertex generic account is removed in the CR-003 handover) | Finding AL-13 in the program plan |
| Website staff portal app roles (`bc-website-staff`, live since 2026-11-07) | Every app-role assignment matches the person's role in `people.csv` (Barista, Shift Lead, Manager, Owner); no assignment to `adm-`, break-glass or vendor accounts; leavers removed; per-user assignments now, `grp-bc-` groups once Entra ID P1 is available | [CR-002](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/09-change-management/CR-002-online-ordering-website.md) §8 |
| "Assignment required" on that app | A tenant account with no app role is refused **by Entra ID**, not only by the website (an account with no role was issued a token on 2026-11-07; the website refused it: open finding) | [CR-002](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/09-change-management/CR-002-online-ordering-website.md) §6, test 1 |
| Register sign-in and the payment dashboard (after CR-005) | Replaces the Toast PIN review | [CR-005](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/09-change-management/CR-005-toast-pos-replacement.md) |

Systems in the main list above change to Microsoft Entra ID at the Microsoft 365 cutover (CR-001).

---

## 3. Roles and Responsibilities

### Business Owner

* Reviews and approves access review results
* Confirms privileged access assignments
* Approves remediation actions

### Store Manager

* Assists with reviewing employee access
* Confirms access aligns with job responsibilities
* Identifies unnecessary permissions

### IT Administrator (Vertex IT Support until 2026-11-15, then the IT Technician)

* Generates access reports from company systems
* Implements access changes identified during review
* Documents account changes and remediation actions

---

## 4. Review Frequency

Access reviews are conducted **quarterly**.

Review schedule:

| Quarter | Review Window      |
| ------- | ------------------ |
| Q1      | January – March    |
| Q2      | April – June       |
| Q3      | July – September   |
| Q4      | October – December |

Reviews should occur near the end of each quarter.

---

## 5. Access Review Process

### Step 1 – Generate Access Reports

The administrator collects current user access lists from each system.

Examples:

* Google Workspace user list and administrative roles
* Toast POS employee accounts and permissions
* xtraCHEF user access list
* QuickBooks Online user access list

These reports form the **access review evidence package**.

---

### Step 2 – Manager Review

Management reviews the access lists to confirm:

* The user is still employed by the company
* The user’s system access matches their job responsibilities
* No unnecessary administrative privileges exist
* Vendor access remains required

Accounts requiring modification should be identified for remediation.

---

### Step 3 – Access Adjustments

If issues are identified, the administrator performs the appropriate corrective actions:

Examples include:

* Removing accounts for former employees
* Reducing excessive privileges
* Updating roles for employees who changed responsibilities
* Removing vendor access no longer required

---

### Step 4 – Documentation and Sign-off

The results of the review must be documented.

Documentation must include:

* Date of review
* Systems reviewed
* Reviewer name
* Summary of findings
* Actions taken or planned remediation
* **Sign-off by the Owner and Store Manager.** The IT administrator exports the data but does not certify their own access (separation of duties)

These records serve as evidence that periodic access reviews are performed.

---

## 6. Handling Inactive Accounts

Accounts belonging to former employees or inactive users must be disabled or removed promptly.

Inactive accounts should not remain enabled unless a documented business reason exists.

---

## 7. Record Retention

Access review documentation should be retained for **at least one year** for internal review or audit purposes.

---

## Source Reference

This procedure is the lab's operational copy of the program's [PR-003 Quarterly Access Review procedure](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/05-procedures/PR-003-quarterly-access-review.md), which implements the [Access Management Policy (P-001)](https://github.com/MgnCoding2020/grc-paper-project-coffee-shop/blob/main/04-policies/P-001-access-control.md). If the two differ, PR-003 wins. The system scope changes to Microsoft Entra ID with the program's change CR-001 (2026-11-15).

This repository demonstrates the **operational execution** of that access review process.
