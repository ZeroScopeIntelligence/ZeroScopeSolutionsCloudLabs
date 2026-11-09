# Google Cloud IAM Role Reference

## Group Permission Design

| Group | Role | Scope | Purpose |
| --- | --- | --- | --- |
| `cloud-project-viewers` | `roles/viewer` | Lab project | Broad read-only visibility |
| `cloud-storage-operators` | `roles/storage.objectUser` | Test bucket | Object operations in one bucket |

## How Google Cloud IAM Works
Google Cloud IAM grants roles to principals through policy bindings on resources. A binding associates a group principal with a role. The role is not attached to the Google Group object itself.

- **Viewer (`roles/viewer`):** Broad read-only access across supported project resources. Use only in a dedicated lab project.
- **Storage Object User (`roles/storage.objectUser`):** Allows object operations such as creating, reading, updating, and deleting objects. Grant at the test bucket scope.
- Prefer narrowly scoped predefined roles in real environments.
- Avoid Owner and Editor for routine lab identities.

## References
- [Google Cloud predefined roles](https://cloud.google.com/iam/docs/understanding-roles)
- [Grant roles to groups](https://cloud.google.com/iam/docs/grant-role-to-group)
- [Cloud Storage IAM roles](https://cloud.google.com/storage/docs/access-control/iam-roles)
