# Azure Identity and Access Management (IAM)

This section covers Microsoft Entra ID identity administration and Azure role-based access control (RBAC), using Zero Trust principles throughout the labs.

## Learning objectives
- Create and manage cloud identities.
- Organize users with security groups.
- Assign permissions using least privilege and appropriate scopes.
- Understand multifactor authentication (MFA).
- Evaluate sign-ins with Conditional Access.
- Reduce standing administrative privileges.
- Review identity activity and assess access controls.

## Zero Trust foundations
1. **Verify explicitly:** evaluate identity and available sign-in context before granting access.
2. **Use least privilege:** grant only the permissions required, at the narrowest practical scope and for the shortest practical duration.
3. **Assume breach:** minimize standing access, monitor activity, and regularly review permissions.

## Lab sequence

| Lab | Topic | Outcome |
|---|---|---|
| [01 – Identity Basics](./Labs/Lab-01-Identity-Basics/README.md) | Microsoft Entra ID identities | Create dedicated test identities |
| [02 – Users and Groups](./Labs/Lab-02-Users-and-Groups/README.md) | Identity organization | Create security groups and manage membership |
| [03 – Least Privilege and RBAC](./Labs/Lab-03-Least-Privilege-RBAC/README.md) | Authorization | Assign and test scoped Azure roles |
| [04 – MFA](./Labs/Lab-04-MFA/README.md) | Authentication | Configure and validate MFA |
| [05 – Conditional Access](./Labs/Lab-05-Conditional-Access/README.md) | Context-aware access | Test a safely scoped Conditional Access policy |
| [06 – Privileged Access](./Labs/Lab-06-Privileged-Access/README.md) | Administrative access | Explore just-in-time privileged access |
| [07 – Zero Trust Assessment](./Labs/Lab-07-Zero-Trust-Assessment/README.md) | Security assessment | Evaluate controls and document findings |

## Example lab groups
- Cloud-Administrators
- Security-Analysts
- Network-Engineers
- Cloud-Developers

These are example security groups for organizing test identities. Group membership does not automatically require or justify an administrative role.

## Lab conventions
- Use neutral resource names such as `rg-cloudlabs`, `app-cloudlabs-demo`, and `vm-cloudlabs-test`.
- Use fictional test identities and non-production data.
- Never include passwords, recovery codes, access tokens, tenant secrets, or personal information in this repository.
- Record the role, scope, reason, and owner for every role assignment.
- Capture redacted screenshots and logs as evidence.

## Safety and prerequisites
- Perform the exercises in a dedicated lab tenant and non-production subscription.
- Confirm feature availability and licensing. Conditional Access and Privileged Identity Management capabilities can require specific Microsoft Entra licensing.
- Maintain a separately protected emergency-access account, exclude it from experimental policies where appropriate, and monitor its use.
- Begin Conditional Access exercises in Report-only mode when available.
- Never apply broad policies or administrative roles to production users for a learning exercise.
- Review inherited role assignments before testing access.
- Remove temporary users, groups, role assignments, policies, and resources during cleanup.

## Documentation standard
Each lab includes an objective, scenario, prerequisites, implementation tasks, validation, Zero Trust connection, cleanup, and evidence requirements.
