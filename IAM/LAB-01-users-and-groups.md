# Lab 01: Create IAM Users, Groups, and Membership

## Objective
Create two lab IAM users, two IAM groups, and add each user to the appropriate group.

## Design

| User | Group | Purpose |
| --- | --- | --- |
| `cloud-audit-user` | `Cloud-Audit-Readers` | Read-only review |
| `cloud-storage-user` | `Cloud-S3-Operators` | Limited access to a test S3 bucket |

## Steps

1. Sign in to the AWS Management Console using an authorized lab administrator. Do not use the root user for routine work.
2. Open **IAM → User groups → Create group**.
3. Create `Cloud-Audit-Readers`. Do not attach a policy yet.
4. Repeat to create `Cloud-S3-Operators`.
5. Open **IAM → Users → Create user**.
6. Create `cloud-audit-user`. Configure console access only if required for this lab and follow the account's password and MFA requirements.
7. Add the user to `Cloud-Audit-Readers` during creation, or open the group and add the user afterward.
8. Repeat for `cloud-storage-user`, adding it to `Cloud-S3-Operators`.
9. Require MFA for interactive test access where supported.

## Validation

- Confirm both groups exist.
- Open each group and verify its intended user is a member.
- Open each user and confirm group membership.
- No group policies are attached yet; Lab 02 adds them.

## Security Notes

These are disposable learning identities. For workforce access in real environments, study IAM Identity Center and federation. Never publish passwords, access keys, secret keys, or MFA recovery information.

## Cleanup
Keep the users and groups for Labs 02 and 03. Delete them when the exercise series is complete.

## References
- [Create IAM users](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html)
- [IAM user groups](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_groups.html)
