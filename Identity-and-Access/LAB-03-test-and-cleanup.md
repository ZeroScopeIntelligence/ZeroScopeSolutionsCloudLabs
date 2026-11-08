# Lab 03: Test, Audit, and Clean Up Group-Based Access

## Objective
Verify that group membership and the assigned policies or roles produce the intended access. Record allowed and denied actions, then remove temporary access.

## Test Matrix

| Test identity | Expected access |
| --- | --- |
| Read-only test user | Can view the resources permitted by the read-only role; cannot make changes |
| Storage test user | Can perform the storage operations granted to its group; cannot administer unrelated resources |

## Steps

1. Sign out of the administrator session.
2. Sign in as the read-only test identity created in Lab 01.
3. Open the dedicated lab resource environment and confirm that permitted read-only information is visible.
4. Confirm that a modification operation is denied. Do not attempt destructive changes.
5. Sign out and sign in as the storage test identity.
6. Open the dedicated test storage resource.
7. Upload and download a harmless text file to validate the granted object or blob permissions.
8. Test only the expected boundaries. Do not delete data unless the lab specifically requires a disposable test object and the role permits it.
9. Return to the administrator session.
10. Review the group memberships and policy or role assignments. Confirm permissions are granted to the groups rather than directly to users.

## Audit Checklist

- [ ] Each test identity belongs to the intended group.
- [ ] Each group has only its intended policy or role.
- [ ] The storage permission is limited to the test storage resource.
- [ ] No broad administrator role was added.
- [ ] Privileged accounts use MFA.
- [ ] No secrets were saved in the repository.

## Cleanup

1. Remove temporary policy attachments or role assignments.
2. Remove test users from groups.
3. Delete test users and groups only if they were created for this exercise and are not used elsewhere.
4. Delete test storage resources only if they were created exclusively for this lab and contain no needed data.
5. Verify that temporary access has been removed.

## Expected Outcome

Explain how group membership affects effective access, how the provider's permission model differs from the other cloud platforms, and why role scope and least privilege matter.

## References

- [Review Azure role assignments](https://learn.microsoft.com/azure/role-based-access-control/role-assignments-list-portal)
