# Lab 01 – Microsoft Entra ID Identity Basics

## Objective
Understand how identities are represented in Microsoft Entra ID and create dedicated test identities for later Zero Trust exercises.

## Scenario
A fictional organization is preparing a cloud environment. The administrator needs separate test identities rather than shared administrator accounts.

## Prerequisites
- A Microsoft Entra ID lab tenant.
- An account authorized to manage users.
- A dedicated lab environment; do not use production identities.

## Tasks
1. Open the Microsoft Entra admin center: https://entra.microsoft.com/
2. Navigate to Identity > Users > All users.
3. Review the user list and inspect a test user's profile.
4. Create two fictional cloud-only test users, such as Alex Morgan (alex.morgan) and Jordan Lee (jordan.lee).
5. Use the tenant's approved password setup process. Do not put passwords in this repository or screenshots.
6. Review each user's properties, sign-in status, and available identity details.
7. Confirm that the identities are separate and have no unnecessary administrative roles.

## Validation
- Both test identities appear in the user list.
- Each identity has a distinct username.
- Neither account has unnecessary administrative roles.

## Zero Trust connection
Identity is the starting point for an access decision, not proof that access should automatically be granted. Later labs add authentication strength, group membership, device context, and scoped authorization.

## Cleanup
Delete temporary users when no longer needed, or retain them for later labs with non-privileged access only.

## Evidence
Capture the user list and user profiles with personal data and tenant-sensitive details hidden.
