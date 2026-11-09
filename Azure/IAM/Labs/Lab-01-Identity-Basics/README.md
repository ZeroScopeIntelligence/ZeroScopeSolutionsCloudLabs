# Lab 01 – Microsoft Entra ID Identity Basics

## Objective
Understand cloud identities in Microsoft Entra ID and create dedicated test accounts for the remaining IAM labs.

## Scenario
A fictional organization is preparing a cloud environment. Administrators need separate, individually assigned identities rather than shared accounts.

## Prerequisites
- Access to a Microsoft Entra ID lab tenant.
- An account authorized to create users.
- A dedicated lab environment; do not use production identities.

## Tasks
1. Open the [Microsoft Entra admin center](https://entra.microsoft.com/).
2. Navigate to **Identity > Users > All users**.
3. Review the user list and inspect a test user's profile.
4. Create two fictional cloud-only test users, for example:
   - Alex Morgan – username: `alex.morgan`
   - Jordan Lee – username: `jordan.lee`
5. Follow your tenant's approved password setup process. Do not save passwords in this repository or screenshots.
6. Review each user's account status, user type, and assigned directory roles.
7. Confirm that neither test identity has unnecessary administrative privileges.

## Validation
- Both test identities appear in the user list.
- Each identity has a distinct username.
- The accounts are enabled for the intended lab activities.
- Neither account has an unnecessary directory role.

## Zero Trust connection
An identity is only one input to an access decision. A successful sign-in does not automatically mean the user should be authorized to access every resource.

## Cleanup
Keep the accounts for the following labs with non-privileged access, or delete them when the exercise is complete.

## Evidence
Capture the user list and relevant profile details. Hide personal data, tenant identifiers, and other sensitive information before publishing screenshots.
