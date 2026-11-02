# VM Local Access Review Evidence (Sanitized)
Burn and Churn Coffee IAM Access Review Lab

## Purpose
This document provides sanitized evidence from a Windows lab VM used to validate local account and password policy settings relevant to access control review activities.

## Commands Performed
The following built-in Windows commands were used during the review:

- `Get-LocalUser`
- `Get-LocalGroup`
- `Get-LocalGroupMember Administrators`
- `net accounts`

## Sanitized Observations

### Local User Accounts
The VM contains the default built-in local accounts expected on a Windows system, along with one enabled local administrative user account used for lab administration.

Observed account conditions:
- Built-in Administrator account: Disabled
- Guest account: Disabled
- DefaultAccount: Disabled
- WDAGUtilityAccount: Disabled
- One named local administrative account: Enabled

### Local Group Review
The local groups available on the system include standard Windows built-in groups such as:
- Administrators
- Users
- Remote Desktop Users
- Backup Operators
- Event Log Readers
- Hyper-V Administrators

### Administrators Group Membership
Review of the local Administrators group identified:
- Built-in Administrator account
- One enabled local administrative user account

This indicates there are two local administrator memberships present, although only one named administrative account is actively enabled for use.

### Password Policy Review
The following password and lockout settings were identified:

- Minimum password age: 0 days
- Maximum password age: 42 days
- Minimum password length: 0
- Password history maintained: None
- Lockout threshold: 10 invalid logon attempts
- Lockout duration: 10 minutes
- Lockout observation window: 10 minutes

## Access Control Review Relevance
This evidence supports review of:
- local account management
- administrative privilege assignment
- password policy strength
- access control configuration validation

## Sanitization Note
Hostnames, account names, and other environment-specific details have been generalized for public portfolio use.