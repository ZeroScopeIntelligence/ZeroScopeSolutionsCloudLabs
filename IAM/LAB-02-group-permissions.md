# Lab 02: Attach Different IAM Policies to Groups

## Objective
Attach different policies to the two groups. Group membership then gives each test user the permissions assigned to that group.

## Permission Design

| Group | Policy | Intended access |
| --- | --- | --- |
| `Cloud-Audit-Readers` | AWS managed `ReadOnlyAccess` | Read-only visibility across supported AWS services |
| `Cloud-S3-Operators` | Customer-managed `Cloud-LabS3ObjectOperator` | List a named lab bucket and read/write objects, without deleting them |

## Part A: Attach ReadOnlyAccess

1. Open **IAM → User groups → Cloud-Audit-Readers**.
2. Open **Permissions → Add permissions → Attach policies**.
3. Search for and select `ReadOnlyAccess`.
4. Review and attach the policy.

This AWS managed policy is broad read-only access. Use it only in an isolated lab account and review its current permissions before use.

## Part B: Create a Limited S3 Policy

1. Open **IAM → Policies → Create policy → JSON**.
2. Replace `YOUR-LAB-BUCKET-NAME` with the exact name of a dedicated test bucket you own.
3. Enter this policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "ListOnlyLabBucket",
      "Effect": "Allow",
      "Action": ["s3:ListBucket"],
      "Resource": "arn:aws:s3:::YOUR-LAB-BUCKET-NAME"
    },
    {
      "Sid": "ReadWriteLabObjects",
      "Effect": "Allow",
      "Action": ["s3:GetObject", "s3:PutObject"],
      "Resource": "arn:aws:s3:::YOUR-LAB-BUCKET-NAME/*"
    }
  ]
}
```

4. Choose **Next**, name it `Cloud-LabS3ObjectOperator`, review, and create the policy.
5. Open **IAM → User groups → Cloud-S3-Operators → Permissions → Add permissions → Attach policies**.
6. Find and attach `Cloud-LabS3ObjectOperator`.

## Part C: Review

- `cloud-audit-user` inherits `ReadOnlyAccess` through its group.
- `cloud-storage-user` inherits the custom S3 policy through its group.
- The custom policy grants no object deletion or bucket administration.
- Other controls, including resource policies, permissions boundaries, and service control policies, can further restrict effective access.

## Validation
Use Lab 03 to test both identities. Do not test with the administrator identity.

## References
- [Attach policies to IAM groups](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_groups_manage_attach-policy.html)
- [Managed and inline policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_managed-vs-inline.html)
