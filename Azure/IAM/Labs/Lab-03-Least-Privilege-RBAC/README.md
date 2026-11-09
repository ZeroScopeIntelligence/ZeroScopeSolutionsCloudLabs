# Lab 03 – Least Privilege and Azure RBAC

## Objective
Assign permissions based on job responsibilities, using the smallest practical scope.

## Scenario
Each team needs access to perform its work, but no team should receive subscription-wide administrator access by default.

## Prerequisites
- Complete Labs 01 and 02.
- A non-production Azure subscription.
- Permission to create resource groups and role assignments.

## Tasks
1. Create a resource group named rg-zs-cloudlabs for the exercise.
2. Open Access control (IAM) for that resource group.
3. Review built-in roles and distinguish Azure resource roles from Microsoft Entra directory roles.
4. Assign a suitable built-in role to a test group at the resource-group scope. For example, use Reader for a group that only needs to inspect resources.
5. For a write-permission demonstration, use a separate test resource group and a narrowly scoped role such as Contributor only for the exercise.
6. Do not assign Owner or User Access Administrator unless a specific exercise requires it and the scope is isolated.
7. Review Role assignments and record the principal, role, scope, and reason.
8. Sign in as a test user and verify what the user can and cannot do.

## Validation matrix
| Test | Expected result |
|---|---|
| Reader views resources in assigned scope | Allowed |
| Reader changes resource configuration | Denied |
| User accesses an unrelated resource group | Denied, unless another assignment grants access |
| Authorized administrator reviews role assignments | Visible |

Actual results depend on inherited assignments and other permissions. Check for inherited access before concluding that a denial or allowance is caused by this lab.

## Zero Trust connection
Least privilege reduces the impact of compromised accounts. Scope permissions to the resource group or individual resource instead of the entire subscription whenever practical.

## Cleanup
Remove temporary role assignments and delete the test resource group after confirming it contains no needed data.

## Evidence
Capture role assignment details and successful read-only and denied write tests. Redact secrets and tenant identifiers.
