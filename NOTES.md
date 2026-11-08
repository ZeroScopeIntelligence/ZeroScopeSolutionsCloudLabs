# Google Cloud Platform (GCP) Notes

Quick reference for concepts, commands, service comparisons, and verified troubleshooting.

> Never store passwords, access keys, private keys, tokens, recovery codes, or personal data here.

## IAM Concepts

- Identity: a user, group, service account, or other principal.
- Group: a collection of identities used to manage access collectively.
- Policy or role: a permission definition or named set of permissions.
- Scope: the resource or hierarchy level where permissions apply.
- Least privilege: grant only the access required for a task.

## Provider IAM Model

Human user identities and Google Groups are managed through Google Workspace or Cloud Identity. Cloud IAM grants roles to group principals through allow-policy bindings on projects, folders, organizations, or supported resources.

## Reference Notes

| Topic | Notes |
| --- | --- |
| Identity | Google Workspace or Cloud Identity users |
| Groups | Google Groups |
| Permissions | Google Cloud IAM role bindings |
| MFA | Enable for privileged identities |
| Scope | Use the narrowest practical resource scope |

## Commands and Troubleshooting

Record safe commands and verified fixes. Redact account numbers, project IDs, tenant IDs, and email addresses where appropriate. Never include credentials.

## Official Documentation

- [Google Cloud Platform (GCP) IAM documentation](https://cloud.google.com/iam/docs/overview)
