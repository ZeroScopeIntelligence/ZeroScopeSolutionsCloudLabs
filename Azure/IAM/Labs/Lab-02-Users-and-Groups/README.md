# Lab 02 – User and Group Management

## Objective
Organize test identities into security groups so access can be assigned consistently and reviewed centrally.

## Scenario
A fictional organization has four teams: Cloud Administrators, Security Analysts, Network Engineers, and Cloud Developers.

## Prerequisites
- Complete Lab 01.
- A lab tenant and permission to manage users and groups.

## Tasks
1. Open the [Microsoft Entra admin center](https://entra.microsoft.com/).
2. Navigate to **Identity > Groups > All groups**.
3. Create the following groups with **Group type: Security** and **Membership type: Assigned**:
   - `Cloud-Administrators`
   - `Security-Analysts`
   - `Network-Engineers`
   - `Cloud-Developers`
4. Add fictional test users to the appropriate groups.
5. Open each group's **Members** page and verify membership.
6. Review group owners and document who is responsible for membership changes.
7. Do not assign directory-wide or subscription-wide administrator roles simply because a user belongs to a department group.

## Example membership plan

| Example user | Security group |
|---|---|
| Alex Morgan | Security-Analysts |
| Jordan Lee | Network-Engineers |
| Taylor Reed | Cloud-Developers |
| Casey Quinn | Cloud-Administrators |

These names are examples. Use the test accounts created in your own tenant.

## Validation
- All four security groups exist.
- Each test user is in the intended group.
- Group owners and membership purposes are documented.
- No user has unrelated group membership without a documented reason.

## Zero Trust connection
Groups simplify access administration, but membership should not grant broad access by default. Each group's permissions must be justified and scoped to the work its members perform.

## Cleanup
Remove temporary memberships and delete test groups when the exercise is complete.

## Evidence
Capture the group list, group type, membership type, and member lists. Redact tenant-sensitive information.
