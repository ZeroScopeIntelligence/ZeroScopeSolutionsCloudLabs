# Amazon Web Services Notes

Quick reference for concepts, commands, service comparisons, and verified troubleshooting.

> Never store passwords, access keys, private keys, tokens, recovery codes, or personal data here.

## IAM Concepts

- Identity: a user, group, service account, or other principal.
- Group: a collection of identities used to manage access collectively.
- Policy or role: a permission definition or named set of permissions.
- Scope: the resource or hierarchy level where permissions apply.
- Least privilege: grant only the access required for a task.

## Provider IAM Model

IAM users can be added to IAM groups. Identity-based policies attached to a group apply to its members. For workforce production access, also study IAM Identity Center and federation.

## Reference Notes

| Topic | Notes |
| --- | --- |
| Identity | IAM users |
| Groups | IAM groups |
| Permissions | IAM policies |
| MFA | Enable for privileged identities |
| Scope | Use the narrowest practical resource scope |

## Commands and Troubleshooting

Record safe commands and verified fixes. Redact account numbers, project IDs, tenant IDs, and email addresses where appropriate. Never include credentials.

## Official Documentation

- [Amazon Web Services IAM documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
