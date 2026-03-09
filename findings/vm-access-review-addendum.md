# VM Access Review Addendum
Burn and Churn Coffee IAM Access Review Lab

## Purpose
This addendum documents observations from a local Windows VM review performed to supplement the quarterly access review evidence in this repository.

## Review Method
The review was performed using built-in Windows administrative commands to inspect:
- local user accounts
- local groups
- local administrator membership
- local password policy settings

## Observations

### 1. Local Administrative Access Exists
The review confirmed that the local Administrators group contains the built-in Administrator account and one enabled local administrative account used for system administration.

**Assessment:** Acceptable for lab administration, but privileged access should remain limited and periodically reviewed.

### 2. Built-in Administrator Account Is Disabled
The built-in Administrator account was observed in a disabled state.

**Assessment:** This is a positive control condition and reduces unnecessary exposure of the default privileged account.

### 3. Password Policy Requires Improvement
The local password policy review identified weak baseline settings, including:
- minimum password length set to 0
- password history not enforced

**Assessment:** These settings do not reflect strong access control practices and would require remediation in a production environment.

### 4. Lockout Controls Are Present
The review confirmed that account lockout settings are configured, including:
- lockout threshold of 10 attempts
- lockout duration of 10 minutes

**Assessment:** This provides a basic protection mechanism against repeated failed logon attempts.

## Recommended Actions
- Configure a minimum password length greater than 0
- Enforce password history
- Review whether the active local administrative account should remain a permanent administrator
- Periodically review local group membership for privileged access

## Portfolio Value
This addendum demonstrates how access review activities can be supported with live system validation using native Windows administrative commands rather than documentation alone.