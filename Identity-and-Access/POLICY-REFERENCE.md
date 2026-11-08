# Azure Role Reference

| Group | Azure role | Scope / Purpose |
| --- | --- | --- |
| `ZS-Resource-Readers` | `Reader` | View management-plane resources in the lab resource group |
| `ZS-Storage-Contributors` | `Storage Blob Data Contributor` | Read, write, and delete blob data in the test storage account |

## Important Distinctions

- Azure RBAC roles control access to Azure resources and data at a defined scope.
- Microsoft Entra directory roles control directory tasks, such as managing users and groups.
- Reader is a management-plane role; it does not automatically provide access to underlying data.
- Storage Blob Data Contributor is a data-plane role for blob data.

Role assignments can be made at management-group, subscription, resource-group, or resource scope. Permissions may inherit from parent scopes. Use the narrowest practical scope.

References: [Built-in roles](https://learn.microsoft.com/azure/role-based-access-control/built-in-roles) · [Scope overview](https://learn.microsoft.com/azure/role-based-access-control/scope-overview)
