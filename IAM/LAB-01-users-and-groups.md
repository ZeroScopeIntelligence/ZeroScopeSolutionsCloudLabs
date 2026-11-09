# Lab 01: Prepare Google Cloud User Identities, Groups, and Membership

## Objective
Prepare two test user identities and two Google Groups, then add each user to the appropriate group.

## Important Identity Model
Google Cloud IAM does not create ordinary human user accounts inside a project. User identities and Google Groups are managed through Google Workspace or Cloud Identity. Cloud IAM grants roles to these group principals in Lab 02.

If you only have a personal Google account without a managed organization, group creation through the Admin console may not be available. Do not invent email addresses or create identities outside an account/domain you control.

## Design

| User identity | Google Group | Purpose |
| --- | --- | --- |
| `cloud-audit-user` | `cloud-project-viewers` | Read-only project access |
| `cloud-storage-user` | `cloud-storage-operators` | Object access to a test bucket |

## Steps

1. Sign in to the [Google Admin console](https://admin.google.com/) with an authorized administrator.
2. Open **Directory → Users** and create two dedicated lab users, or identify two existing test users you are authorized to manage.
3. Open **Directory → Groups → Create group**.
4. Create `cloud-project-viewers`.
5. Repeat to create `cloud-storage-operators`.
6. Open `cloud-project-viewers`, choose **Add members**, and add the `cloud-audit-user` identity.
7. Open `cloud-storage-operators` and add `cloud-storage-user`.
8. Review group visibility and posting settings. Do not make groups public for this exercise.

## Validation
Confirm both groups exist and each contains the intended test user. No Cloud IAM roles are granted yet; Lab 02 handles permissions.

## Cleanup
Keep users and groups for Labs 02 and 03. Delete only identities and groups created specifically for this lab when the series is complete.

## References
- [Create a user](https://cloud.google.com/identity/docs/how-to/create-user)
- [Google Groups administration](https://support.google.com/a/answer/33343)
