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
