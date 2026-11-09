# Lab 02 – User and Group Management

## Objective
Organize identities into security groups so access can be assigned consistently and reviewed centrally.

## Scenario
The organization has four teams: Cloud Administrators, Security Analysts, Network Engineers, and Cloud Developers.

## Prerequisites
- Complete Lab 01.
- A lab tenant and permission to manage users and groups.

## Tasks
1. In Microsoft Entra admin center, navigate to Identity > Groups > All groups.
2. Create these Security groups: Cloud-Administrators, Security-Analysts, Network-Engineers, and Cloud-Developers.
3. Add fictional test users to the appropriate groups.
4. Use each group's Members page to verify membership.
5. Review group owners and membership type. Prefer assigned membership for this introductory exercise.
6. Do not grant directory or subscription-wide administrative roles simply because a user belongs to a department group.

## Example membership
| User | Group |
|---|---|
| Alex Morgan | Security-Analysts |
| Jordan Lee | Network-Engineers |
| Taylor Reed | Cloud-Developers |
| Casey Quinn | Cloud-Administrators |

These are illustrative identities. Use the accounts created in your own lab.

## Validation
- All four security groups exist.
- Each test user is in the intended group.
- No user has been added to an unrelated group without a documented reason.

## Zero Trust connection
Groups make access administration manageable, but membership alone should not grant broad access. The next lab assigns narrowly scoped permissions and verifies the actual result.

## Cleanup
Remove test memberships and delete temporary groups when the exercise is complete.

## Evidence
Capture the group list and membership pages with sensitive information hidden.
