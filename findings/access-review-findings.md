# Quarterly Access Review Findings

Burn and Churn Coffee
Review Period: Q1 2026

---

## 1. Review Overview

A quarterly access review was conducted for Burn and Churn Coffee to verify that system access aligns with employee job responsibilities and the organization's access control policy.

The review included access data from the following systems:

* Google Workspace
* Toast POS
* xtraCHEF
* QuickBooks Online
* Network administration interfaces

The access matrix and supporting evidence are stored in the **evidence** directory of this repository.

---

## 2. Summary of Findings

| Finding ID | Issue                                                       | Risk Level | Status |
| ---------- | ----------------------------------------------------------- | ---------- | ------ |
| F-001      | Terminated employee account still active                    | High       | Open   |
| F-002      | Shift leader assigned unnecessary administrative privileges | Medium     | Open   |
| F-003      | Inactive vendor account still enabled                       | Medium     | Open   |
| F-004      | Multi-factor authentication not enabled for one user        | Low        | Open   |
| F-005      | Weak password configuration                                 | Medium     | Completed   |
---

## 3. Detailed Findings

### F-001 — Terminated Employee Account Still Active

**User:** Aiden Scott
**System(s):** Google Workspace, Toast POS

**Observation**

The access review identified that a user account belonging to a terminated employee remains active in multiple systems.

**Risk**

Former employees retaining system access creates a risk of unauthorized access, potential data exposure, or malicious activity.

**Recommended Action**

Immediately disable or remove all accounts associated with the former employee and verify that no additional access remains active.

---

### F-002 — Unnecessary Administrative Privileges

**User:** Marcus Hill
**System:** Toast POS

**Observation**

The access review identified that a shift leader account currently holds administrative privileges in the POS system.

**Risk**

Administrative privileges should be restricted to authorized management personnel. Excessive privileges increase the risk of configuration changes, fraud, or operational disruption.

**Recommended Action**

Downgrade the user's permissions to the standard Shift Leader role.

---

### F-003 — Inactive Vendor Account Still Enabled

**Account:** NorthPeak Systems
**System:** Network administration interface

**Observation**

An inactive vendor account remains enabled despite no active support engagement.

**Risk**

Vendor accounts can present a security risk if left enabled when not actively required.

**Recommended Action**

Disable the vendor account immediately. If vendor support is required in the future, access should be provisioned temporarily and removed after the engagement.

---

### F-004 — Missing Multi-Factor Authentication

**User:** Ethan Brooks
**System:** Google Workspace

**Observation**

The access review identified a user account without multi-factor authentication enabled.

**Risk**

Accounts without MFA are more vulnerable to credential compromise.

**Recommended Action**

Require MFA enrollment for the user and verify MFA enforcement for all accounts.

---

### F-005 — Weak Password Policy Configuration

System: Windows Lab VM

Observation

Local system password policy settings were reviewed using the `net accounts` command.

The following weak configuration settings were identified:

- Minimum password length set to 0
- Password history not enforced
- Password complexity not enabled

Risk

Weak password policies increase the likelihood of password guessing attacks, credential reuse, and unauthorized system access.

Recommended Action

Implement stronger password policy settings including:

- Minimum password length of 12 characters
- Password history enforcement
- Password complexity requirements
- Reasonable password expiration settings

Remediation Update

Password policy settings were updated using Local Security Policy (`secpol.msc`) and validated using the `net accounts` command.

Status: **Remediated**

---

