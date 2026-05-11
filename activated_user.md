# Activated User

This file contains information related to activated users.

## Overview

An activated user is an account that has been successfully enabled and granted access to systems, applications, or services. Activation marks the point at which a user can fully authenticate and interact with organizational resources.

## Common Triggers for Activation

- New employee onboarding
- Reinstatement after suspension
- Role change requiring new system access
- Completion of identity verification and MFA enrollment
- Administrator-initiated provisioning

## Activation Process

1. **Provisioning** – The user account is created in the identity provider (e.g., JumpCloud, Azure AD).
2. **Identity Verification** – The user's identity is confirmed via email, SSO, or admin approval.
3. **MFA Enrollment** – The user sets up multi-factor authentication.
4. **Access Assignment** – Roles, groups, and permissions are assigned based on the user's profile.
5. **Device Enrollment** – The user's device is enrolled in MDM/EDR if required.
6. **Notification** – The user is notified that their account is active and ready to use.

## Access Granted Upon Activation

- Single Sign-On (SSO) access to applications
- VPN and network access (if applicable)
- Email and collaboration tools
- Cloud storage and document management
- Device management policies applied (MDM/EDR)

## Best Practices

- Enforce MFA at the point of activation
- Apply least-privilege access principles
- Log and audit all activation events
- Set an access review schedule for newly activated accounts
- Ensure device compliance before granting full access (Zero Trust)

## Relation to Suspended Users

An activated user is the operational counterpart to a suspended user. Reactivation of a suspended account follows the same activation process with additional review steps to ensure the original issue has been resolved.
