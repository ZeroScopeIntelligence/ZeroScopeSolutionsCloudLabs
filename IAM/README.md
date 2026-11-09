# AWS IAM

## Purpose

Learn how identities are created, organized into groups, assigned permissions, and tested using least privilege.

## How This Provider Works

AWS IAM supports IAM users and IAM groups. Add users to groups, then attach identity-based policies to groups. Group members inherit those permissions. For workforce access in production, prefer IAM Identity Center and federation rather than long-lived IAM users.

## Lab Sequence

| Lab | Topic | Status |
| --- | --- | --- |
| 01 | [Create users, groups, and membership](./LAB-01-users-and-groups.md) | Ready |
| 02 | [Assign different policies or roles to groups](./LAB-02-group-permissions.md) | Ready |
| 03 | [Test, audit, and clean up access](./LAB-03-test-and-cleanup.md) | Ready |

## Permission Design

| Group | Permission | Scope |
| --- | --- | --- |
| Cloud-Audit-Readers | ReadOnlyAccess | Dedicated lab environment |
| Cloud-S3-Operators | Custom S3 object policy | Dedicated test storage resource |

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
- [Official documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
