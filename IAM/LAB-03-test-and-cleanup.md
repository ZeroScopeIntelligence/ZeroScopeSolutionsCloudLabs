# Lab 03: Test, Audit, and Clean Up Google Cloud IAM Access

## Objective
Verify that Google Group membership and IAM role bindings provide the intended access, then remove temporary bindings and lab identities.

## Test Matrix

| Test identity | Expected access |
| --- | --- |
| Member of `cloud-project-viewers` | Can view supported resources in the dedicated lab project; cannot make changes |
| Member of `cloud-storage-operators` | Can perform object operations in the designated test bucket; does not receive project administration |

## Steps

1. Sign out of the administrator session.
2. Sign in as the test user who belongs to `cloud-project-viewers`.
3. Open the Google Cloud console and select the dedicated lab project.
4. Confirm supported project resources can be viewed.
5. Confirm modification operations are not allowed. Do not attempt destructive changes.
6. Sign out and sign in as the test user who belongs to `cloud-storage-operators`.
7. Open the dedicated test bucket.
8. Upload and download a harmless test file to validate object access.
9. Return to the administrator session and review **IAM & Admin → IAM** and the bucket's **Permissions** tab.
10. Confirm roles are granted to groups at the intended scopes, not directly to test users.

## Audit Checklist
- [ ] Viewer is assigned only to the dedicated lab project.
- [ ] Storage Object User is assigned only to the dedicated test bucket.
- [ ] No unnecessary direct grants to test users exist.
- [ ] Public principals are not granted access.
- [ ] Inherited organization and folder policies are understood.

## Cleanup

1. Remove the project-level Viewer binding for `cloud-project-viewers`.
2. Remove the bucket-level Storage Object User binding for `cloud-storage-operators`.
3. Delete test users and groups from Google Workspace or Cloud Identity only if they were created specifically for this lab and are not used elsewhere.
4. Delete the test bucket and its contents only if it was created exclusively for this lab and contains no needed data.
5. Verify temporary IAM bindings have been removed.

## Expected Outcome
Explain how Google Cloud identities and groups are managed separately from resource IAM, how roles are bound to group principals, and why scope matters.

## References
- [View and manage IAM policies](https://cloud.google.com/iam/docs/manage-access)
- [IAM best practices](https://cloud.google.com/iam/docs/using-iam-securely)
