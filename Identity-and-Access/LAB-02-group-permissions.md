# Lab 02: Assign Different Azure RBAC Roles to Groups

## Objective
Assign different Azure resource roles to the Entra groups. One group gets read-only access to a dedicated resource group; the other gets blob data access on one test storage account.

## Permission Design

| Group | Role | Scope |
| --- | --- | --- |
| `ZS-Resource-Readers` | `Reader` | Dedicated lab resource group |
| `ZS-Storage-Contributors` | `Storage Blob Data Contributor` | Dedicated test storage account |

## Prerequisites
Complete Lab 01. Have a dedicated resource group and test storage account. Your administrator must have permission to create role assignments at those scopes.

## Part A: Assign Reader

1. Open [Azure portal](https://portal.azure.com/).
2. Navigate to **Resource groups** and select the dedicated lab resource group.
3. Open **Access control (IAM) → Add → Add role assignment**.
4. Select the **Reader** role and choose **Next**.
5. Under **Assign access to**, choose **User, group, or service principal**.
6. Select **ZS-Resource-Readers** as the member.
7. Review the role and resource-group scope, then choose **Review + assign**.

## Part B: Assign Storage Blob Data Contributor

1. Navigate to the dedicated test storage account.
2. Open **Access control (IAM) → Add → Add role assignment**.
3. Select **Storage Blob Data Contributor** and choose **Next**.
4. Choose **User, group, or service principal** and select `ZS-Storage-Contributors`.
5. Confirm the scope is the test storage account, not the subscription.
6. Choose **Review + assign**.

## Understand the Difference

- `Reader` allows viewing Azure management-plane resources at the selected scope. It does not automatically grant access to all data stored in those resources.
- `Storage Blob Data Contributor` grants read, write, and delete access to blob data at the selected scope.
- Azure RBAC assignments are made at resource scopes; they are not policies attached to Entra groups in the same way as AWS IAM.
- Role assignment changes can take several minutes to take effect.

## Validation
Use Lab 03 to test both users. Do not test using an administrator identity.

## References
- [Assign Azure roles in the portal](https://learn.microsoft.com/azure/role-based-access-control/role-assignments-portal)
- [Azure built-in roles](https://learn.microsoft.com/azure/role-based-access-control/built-in-roles)
