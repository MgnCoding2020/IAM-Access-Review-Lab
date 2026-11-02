# Quarterly Access Review Summary  
Burn and Churn Coffee  
Review Period: Q1 2026  
Review Date: 2026-03-25  
Reviewers: Olivia Carter (Owner), Daniel Lopez (Store Manager)

---

## 1. Review Scope

A quarterly access review was performed for Burn and Churn Coffee to verify that logical access to business systems remains appropriate and aligned with job responsibilities.

Systems reviewed:

- Google Workspace
- Toast POS
- xtraCHEF
- QuickBooks Online
- Network administration interfaces

In-scope users included:

- 1 Business Owner
- 1 Store Manager
- 3 Shift Leaders
- 15 Employees (plus one terminated employee whose accounts were still active)
- 2 IT Vendors

---

## 2. Review Activities Performed

The review included the following activities:

- Collection of current access data from in-scope systems
- Validation of active users and assigned roles
- Review of privileged access assignments
- Review of vendor access
- Identification of terminated or inactive accounts
- Documentation of findings and remediation actions

---

## 3. Review Results

Total findings identified: **4** (F-005, a password-policy fix on a lab VM, is a technique demonstration outside the company's system boundary and is not counted here)

| Finding ID | Description | Risk Level | Status |
|------------|-------------|------------|--------|
| F-001 | Terminated employee account still active | High | Open |
| F-002 | Shift leader assigned unnecessary administrative privileges | Medium | Open |
| F-003 | Inactive vendor account still enabled | Medium | Open |
| F-004 | Multi-factor authentication not enabled for one user | Low | Open |

---

## 4. Conclusion

The quarterly review confirmed that Burn and Churn Coffee has an established access review process, but several access control issues require remediation.

The most significant issue identified was the presence of active accounts associated with a terminated employee. Additional improvements are required for privileged access control, vendor account management, and MFA enforcement.

Findings from this review have been documented and entered into the remediation tracker for follow-up.

---

## 5. Reviewer Statement

This review was performed as part of the Burn and Churn Coffee IAM governance process to support least privilege, timely deprovisioning, and periodic access validation.

---

## 6. Corrections and Status (added 2026-10-30)

- Review date, reviewers and the employee count were added or corrected from the program record (see [CORRECTIONS.md](../evidence/CORRECTIONS.md)).
- **No management sign-off is recorded** for this review. The checklist's approval step is left open, and sign-off is required for the Q4 2026 review.
- F-001 to F-004 were found **overdue** on 2026-10-30; see [status checks](../remediation/status-checks.md).
