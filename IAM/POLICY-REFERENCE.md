# AWS IAM Policy Reference

| Group | Policy | Scope / Purpose |
| --- | --- | --- |
| `ZS-Audit-Readers` | AWS managed `ReadOnlyAccess` | Broad read-only visibility in the isolated lab account |
| `ZS-S3-Operators` | Customer-managed `ZS-LabS3ObjectOperator` | List one named bucket and read/write its objects |

## Policy Types

- AWS managed policies are maintained by AWS.
- Customer managed policies are created and maintained in your account.
- Inline policies are embedded in one identity or group and are less reusable.

The custom S3 policy in Lab 02 grants `s3:ListBucket` on the named bucket and `s3:GetObject` / `s3:PutObject` on objects in that bucket. It does not grant delete or bucket administration.

Effective access can also be affected by resource policies, permissions boundaries, session policies, service control policies, and explicit denies. An explicit deny overrides an allow.

References: [Managed policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_managed-vs-inline.html) · [Policy evaluation](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html)
