# Staged User

This file contains information related to staged users.

## Overview

A staged user is an account that has been created in the identity provider but has not yet been fully activated or granted access to systems and services. It represents a pre-onboarding state where the user exists in the directory but cannot yet authenticate or access resources.

## Common Triggers for Staging

- Pre-boarding a new employee before their start date
- Preparing accounts in advance of a system migration
- Awaiting completion of background checks or compliance requirements
- Pending manager or HR approval before access is granted
- Bulk user imports where accounts need review before activation

## Staged vs. Active vs. Suspended

| State     | Directory Exists | Can Authenticate | Access Granted |
|-----------|-----------------|-----------------|----------------|
| Staged    | ✅ Yes          | ❌ No           | ❌ No          |
| Active    | ✅ Yes          | ✅ Yes          | ✅ Yes         |
| Suspended | ✅ Yes          | ❌ No           | ❌ No          |

> **Note:** While staged and suspended users both lack access, staged users have never been activated, whereas suspended users had prior active access that was revoked.

## Staging Process

1. **Account Creation** – The user account is created in the identity provider with basic attributes (name, email, role).
2. **Profile Population** – Additional attributes such as department, manager, and group memberships are pre-assigned.
3. **Awaiting Trigger** – The account remains in a staged state until an activation condition is met (e.g., start date, approval).
4. **Activation** – Once the trigger condition is satisfied, the account moves to an active state and the user is notified.

## What Staged Users Can and Cannot Do

### Cannot:
- Authenticate via SSO or direct login
- Access any applications or services
- Enroll in MFA
- Connect devices to MDM/EDR

### Can (admin-side):
- Be assigned to groups and roles in advance
- Have policies pre-applied for when activation occurs
- Be included in directory reports and audits

## Best Practices

- Set a defined activation date or approval workflow to avoid accounts remaining staged indefinitely
- Audit staged accounts regularly to remove stale or cancelled entries
- Pre-assign the minimum required roles following least-privilege principles
- Automate the staging-to-active transition using HRIS or provisioning integrations (e.g., JumpCloud, Okta, Azure AD)

## Relation to the User Lifecycle

Staged users sit at the beginning of the user lifecycle, preceding activation. The full lifecycle typically follows:

**Staged → Active → (Suspended) → Deactivated/Deleted**
