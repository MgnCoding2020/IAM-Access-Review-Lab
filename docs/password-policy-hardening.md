# Password Policy Hardening
Burn and Churn Coffee IAM Access Review Lab

## Purpose
This document describes password policy improvements made on the Windows lab VM to address weaknesses identified during the IAM access review process.

## Background
During local access validation, the following password policy weaknesses were observed:

- Minimum password length was set to 0
- Password history was not enforced
- Maximum password age was set to 42 days

These settings were determined to be weak for a business environment and inconsistent with stronger access control practices.

## Changes Implemented
The following password policy settings were updated through Local Security Policy (`secpol.msc`):

| Setting | Before | After |
|---|---:|---:|
| Enforce password history | None | 10 |
| Maximum password age | 42 days | 90 days |
| Minimum password age | 0 days | 1 day |
| Minimum password length | 0 | 12 |
| Password complexity | Disabled / Not enforced | Enabled |

## Validation Method
Configuration changes were validated using the built-in Windows command:

```powershell
net accounts

## Evidence

The following evidence files document the configuration change:

- evidence/vm-password-policy-before.txt

- evidence/vm-password-policy-after.txt

## Security Value

These changes improve the strength of local account authentication controls by:

-requiring longer passwords

-reducing reuse through password history

-enforcing complexity requirements

-establishing a more defensible baseline for access control

## Notes

This activity demonstrates how IAM review findings can lead to practical control improvements and configuration validation on a live Windows system.