# Lab 06 – Privileged Identity and Just-in-Time Access

## Objective
Understand how privileged access can be limited, approved, time-bound, and reviewed.

## Scenario
Administrators should not keep elevated permissions permanently when they only need them for occasional tasks.

## Prerequisites
- A dedicated Microsoft Entra lab tenant.
- Review current Microsoft Entra ID Governance / Privileged Identity Management licensing and availability.
- A separate test administrator identity. Do not use your everyday account.

## Tasks
1. Open Identity Governance > Privileged Identity Management if available in your tenant.
2. Review the difference between permanent active assignments and eligible assignments.
3. Review role settings such as activation duration, approval, MFA, and justification.
4. If supported, configure a narrowly scoped eligible assignment for a test role and test identity.
5. Activate the eligible role using the approved lab workflow.
6. Verify that the role is active only for the configured duration.
7. Review PIM audit history and role activation events.
8. If PIM is unavailable, document the licensing limitation and demonstrate the principle with a time-limited, manually added and removed role assignment in an isolated lab scope.

## Validation
- The test identity does not hold unnecessary permanent privileges.
- The activation process applies configured controls.
- The role assignment is removed or expires as expected.
- The activity is visible in available audit records.

## Zero Trust connection
Just-in-time access supports least privilege and the assume-breach mindset by reducing standing administrative permissions.

## Safety notes
Never experiment with your only Global Administrator account. Avoid permanent Global Administrator or subscription Owner permissions. Have a tested recovery path before changing privileged-role settings.

## Cleanup
Remove all temporary eligible or active assignments and confirm the test identity no longer has elevated access.

## Evidence
Capture redacted eligible/active assignment views, activation requirements, and activation/audit records.
