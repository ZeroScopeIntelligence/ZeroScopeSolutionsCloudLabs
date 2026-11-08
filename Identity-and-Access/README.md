# Microsoft Entra ID and Azure RBAC

## Purpose

Learn how identities are created, organized into groups, assigned permissions, and tested using least privilege.

## How This Provider Works

Microsoft Entra ID manages users and security groups. Azure RBAC assigns resource roles to groups at a defined scope. Group members inherit the resource access. Entra directory roles are separate from Azure resource RBAC roles.

## Lab Sequence

| Lab | Topic | Status |
| --- | --- | --- |
| 01 | [Create users, groups, and membership](./LAB-01-users-and-groups.md) | Ready |
| 02 | [Assign different policies or roles to groups](./LAB-02-group-permissions.md) | Ready |
| 03 | [Test, audit, and clean up access](./LAB-03-test-and-cleanup.md) | Ready |

## Permission Design

| Group | Permission | Scope |
| --- | --- | --- |
| ZS-Resource-Readers | Reader | Dedicated lab resource group |
| ZS-Storage-Contributors | Storage Blob Data Contributor | Dedicated test storage resource |

## Safety Checklist

- Use disposable lab identities in a non-production environment.
- Do not use root or primary administrator accounts for routine tests.
- Enable MFA for privileged identities.
- Avoid broad administrator permissions.
- Review every role's effective permissions and scope.
- Remove temporary access after testing.

## References

- [Lab template](../LAB-TEMPLATE.md)
- [Notes](../NOTES.md)
- [Official documentation](https://learn.microsoft.com/entra/identity/)
