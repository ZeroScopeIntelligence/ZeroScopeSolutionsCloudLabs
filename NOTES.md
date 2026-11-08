# Google Cloud Platform (GCP) Notes

Quick reference for concepts, commands, service comparisons, and verified troubleshooting.

> Never store passwords, access keys, private keys, tokens, recovery codes, or personal data here.

## IAM Concepts
- Identity: a user, group, service account, or other principal.
- Group: a collection of identities used to manage access collectively.
- Role: a named set of permissions.
- Policy binding: associates a principal with a role on a resource.
- Scope: the resource or hierarchy level where permissions apply.
- Least privilege: grant only access required for a task.

## Google Cloud IAM Model

Human user identities and Google Groups are managed through Google Workspace or Cloud Identity. Cloud IAM grants roles to group principals through allow-policy bindings on projects, folders, organizations, or supported resources. Ordinary human users are not created inside a Google Cloud project.

## Reference Notes

| Topic | Notes |
| --- | --- |
| User identities | Google Workspace or Cloud Identity |
| Groups | Google Groups |
| Permissions | Cloud IAM role bindings |
| MFA | Enable for privileged identities |
| Scope | Use the narrowest practical resource scope |

## Commands and Troubleshooting
Record safe commands and verified fixes. Redact project IDs, organization identifiers, and email addresses where appropriate. Never include credentials.

## Official Documentation
- [Google Cloud IAM documentation](https://cloud.google.com/iam/docs/overview)
