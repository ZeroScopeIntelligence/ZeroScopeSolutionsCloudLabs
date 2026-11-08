# Microsoft Azure Notes

Quick reference for concepts, commands, service comparisons, and verified troubleshooting.

> Never store passwords, access keys, private keys, tokens, recovery codes, or personal data here.

## IAM Concepts

- Identity: a user, group, service account, or other principal.
- Group: a collection of identities used to manage access collectively.
- Policy or role: a permission definition or named set of permissions.
- Scope: the resource or hierarchy level where permissions apply.
- Least privilege: grant only the access required for a task.

## Provider IAM Model

Microsoft Entra ID manages users and security groups. Azure RBAC role assignments grant resource access to groups at management-group, subscription, resource-group, or resource scope. Entra directory roles and Azure resource roles are different.

## Reference Notes

| Topic | Notes |
| --- | --- |
| Identity | Microsoft Entra ID users |
| Groups | Microsoft Entra ID security groups |
| Permissions | Azure RBAC role assignments |
| MFA | Enable for privileged identities |
| Scope | Use the narrowest practical resource scope |

## Commands and Troubleshooting

Record safe commands and verified fixes. Redact account numbers, project IDs, tenant IDs, and email addresses where appropriate. Never include credentials.

## Official Documentation

- [Microsoft Azure IAM documentation](https://learn.microsoft.com/entra/identity/)
