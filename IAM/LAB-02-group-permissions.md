# Lab 02: Grant Different Google Cloud IAM Roles to Groups

## Objective
Grant different IAM roles to the groups created in Lab 01. One group receives project-level Viewer access; the other receives object permissions on a dedicated test bucket.

## Permission Design

| Group | Role | Scope |
| --- | --- | --- |
| `zs-project-viewers` | `roles/viewer` | Dedicated lab project |
| `zs-storage-operators` | `roles/storage.objectUser` | Dedicated test bucket |

## Prerequisites
Complete Lab 01. Use a dedicated non-production project and a test Cloud Storage bucket. Have permission to change IAM policies on the project and bucket.

## Part A: Grant Viewer to the First Group

1. Open the [Google Cloud console](https://console.cloud.google.com/) and select the lab project.
2. Open **IAM & Admin → IAM → Grant access**.
3. Enter the group principal, for example `zs-project-viewers@YOUR-DOMAIN`.
4. Assign **Viewer** (`roles/viewer`).
5. Review the project scope and grant access.

Viewer is broad read-only access. Keep this role within a dedicated lab project and review its current permissions.

## Part B: Grant Storage Object User to the Second Group

1. Open **Cloud Storage → Buckets** and select the dedicated test bucket.
2. Open **Permissions → Grant access**.
3. Enter `zs-storage-operators@YOUR-DOMAIN`.
4. Assign **Storage Object User** (`roles/storage.objectUser`) at the bucket scope.
5. Confirm the principal and bucket scope, then save.

Storage Object User permits object operations such as creating, reading, updating, and deleting objects. It does not grant broad project administration.

## Understand the Difference

- A group is the principal in the IAM binding.
- The role is granted through a policy binding on the project or bucket; it is not attached to the Google Group object.
- Project-level Viewer is broader than bucket-level object access.
- Organization policies and inherited IAM bindings can affect effective permissions.

## Validation
Use Lab 03 to test both users. Do not test with an organization administrator identity.

## References
- [Grant roles to groups](https://cloud.google.com/iam/docs/grant-role-to-group)
- [Cloud Storage IAM roles](https://cloud.google.com/storage/docs/access-control/iam-roles)
- [Manage IAM access](https://cloud.google.com/iam/docs/manage-access)
