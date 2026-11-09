# Azure Identity and Access Management (IAM)

This section teaches Microsoft Entra ID identity administration and applies Zero Trust principles to access decisions.

## Learning objectives
- Create and manage users and groups.
- Assign Azure RBAC roles at the correct scope.
- Apply least privilege and separate administrative duties.
- Understand MFA and Conditional Access.
- Explore privileged access and identity monitoring.
- Validate access with positive and negative tests.

## Zero Trust principles
1. **Verify explicitly:** evaluate identity, device, location, and sign-in risk where supported.
2. **Use least privilege:** grant only the permissions needed, for only the required scope and duration.
3. **Assume breach:** monitor activity, limit standing privileges, and review access continuously.

## Labs
| Lab | Topic |
|---|---|
| [01 – Identity Basics](./Labs/Lab-01-Identity-Basics/README.md) | Create test identities |
| [02 – Users and Groups](./Labs/Lab-02-Users-and-Groups/README.md) | Organize identities |
| [03 – Least Privilege and RBAC](./Labs/Lab-03-Least-Privilege-RBAC/README.md) | Scope permissions |
| [04 – MFA](./Labs/Lab-04-MFA/README.md) | Strengthen authentication |
| [05 – Conditional Access](./Labs/Lab-05-Conditional-Access/README.md) | Evaluate sign-in context |
| [06 – Privileged Access](./Labs/Lab-06-Privileged-Access/README.md) | Limit standing privileges |
| [07 – Zero Trust Assessment](./Labs/Lab-07-Zero-Trust-Assessment/README.md) | Test and document controls |

## Suggested test groups
- Cloud-Administrators
- Security-Analysts
- Network-Engineers
- Cloud-Developers

Use fictional test identities and non-production data. Do not use your everyday administrator account as a test user.

## Important safety notes
- Perform these exercises in a lab tenant or isolated subscription.
- Confirm licensing and feature availability. Conditional Access and Privileged Identity Management may require specific Microsoft Entra licensing.
- Keep a tested emergency-access account excluded from experimental Conditional Access policies, protect it strongly, and monitor its use.
- Start policies in Report-only mode when available. Validate sign-in behavior before enabling enforcement.
- Never apply broad admin roles or policies to a production tenant for a learning exercise.
- Remove temporary users, groups, role assignments, and policies during cleanup.

## Documentation standard
For each lab, record the objective, prerequisites, implementation, validation steps, screenshots with sensitive details hidden, results, and cleanup. Never publish passwords, access tokens, tenant secrets, or personal information.
