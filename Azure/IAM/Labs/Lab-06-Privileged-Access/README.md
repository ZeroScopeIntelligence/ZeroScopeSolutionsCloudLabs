# Lab 06 – Privileged Identity and Just-in-Time Access

## Objective
Understand how privileged access can be limited, approved, time-bound, and reviewed.

## Scenario
Administrators should not keep elevated permissions permanently when they only need them for occasional tasks.

## Prerequisites
- A dedicated Microsoft Entra lab tenant.
- A separate test administrator identity.
- Review current licensing and availability for Microsoft Entra Privileged Identity Management (PIM).

## Tasks
1. Open **Identity Governance > Privileged Identity Management** if the feature is available in your tenant.
2. Review the difference between permanent active assignments and eligible assignments.
3. Review role settings such as activation duration, approval, MFA, and justification.
4. If supported, configure a narrowly scoped eligible assignment for a test role and test identity.
5. Activate the eligible role through the approved lab workflow.
6. Verify that the role is active only for the configured duration.
7. Review PIM audit history and role activation events.
8. If PIM is unavailable, document the licensing limitation. In an isolated resource group, demonstrate the principle by adding a narrowly scoped temporary role assignment and removing it immediately after testing.

## Validation
- The test identity does not hold unnecessary permanent privileges.
- The activation process applies the configured controls, where PIM is available.
- Temporary access is removed or expires as expected.
- The activity is visible in available audit records.

## Zero Trust connection
Just-in-time access supports least privilege and the assume-breach mindset by reducing standing administrative permissions.

## Safety notes
- Never experiment with your only Global Administrator account.
- Avoid permanent Global Administrator or subscription Owner permissions.
- Confirm a recovery path before changing privileged-role settings.
- Keep the exercise limited to a dedicated test identity and isolated scope.

## Cleanup
Remove temporary eligible or active assignments and confirm that the test identity no longer has elevated access.

## Evidence
Capture redacted assignment details, activation requirements, duration, and audit records.
