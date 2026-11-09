# Lab 03 – Least Privilege and Azure RBAC

## Objective
Assign Azure resource permissions based on job responsibilities and at the smallest practical scope.

## Scenario
Different teams need different levels of access. A security analyst may need to view resources, while a developer may need to manage resources in a dedicated development resource group.

## Prerequisites
- Complete Labs 01 and 02.
- A non-production Azure subscription.
- Permission to create resource groups and role assignments.

## Tasks
1. In the Azure portal, create a resource group named `rg-cloudlabs`.
2. Open **Access control (IAM)** for that resource group.
3. Review built-in Azure roles and understand the difference between Azure resource roles and Microsoft Entra directory roles.
4. Assign the **Reader** role to a suitable test group at the `rg-cloudlabs` scope.
5. If demonstrating write access, create a separate test resource group and assign **Contributor** only to the group that needs it and only at that resource-group scope.
6. Avoid assigning **Owner** or **User Access Administrator** for this introductory exercise.
7. Open **Role assignments** and record the principal, role, scope, and business reason.
8. Sign in as a test user and verify both permitted and prohibited actions.
9. Review inherited assignments and other access paths before interpreting test results.

## Example access matrix

| Group | Example permission | Scope |
|---|---|---|
| Security-Analysts | Reader | `rg-cloudlabs` |
| Cloud-Developers | Contributor, only if needed for the exercise | Separate development resource group |
| Network-Engineers | No assignment until a specific network task requires one | Narrow network resource scope |
| Cloud-Administrators | No standing broad role for this exercise | Use a separately controlled admin workflow |

## Validation

| Test | Expected result |
|---|---|
| Reader views resources in the assigned scope | Allowed |
| Reader changes resource configuration | Denied |
| User accesses an unrelated resource group | Denied unless another assignment grants access |
| Authorized administrator reviews role assignments | Visible |

Actual results depend on inherited assignments and other permissions in the tenant.

## Zero Trust connection
Least privilege reduces the potential impact of account compromise. Assign roles at resource or resource-group scope instead of subscription scope whenever practical.

## Cleanup
Remove temporary role assignments. Delete the test resource group after confirming it contains no required data.

## Evidence
Capture the role, assigned group, scope, and results of read/write tests. Redact subscription IDs and other sensitive values.
