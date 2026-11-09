# Lab 07 – Zero Trust IAM Assessment

## Objective
Combine the previous labs into a small identity security assessment and verify that access is justified, limited, and monitored.

## Scenario
You are reviewing the identity configuration for a fictional organization before it moves a workload into the cloud.

## Prerequisites
- Complete Labs 01–06, or document any unavailable features.
- A dedicated lab tenant and test identities.
- Redacted evidence from earlier labs.

## Assessment checklist
| Control | Verification question | Evidence |
|---|---|---|
| Identity inventory | Are test identities named, owned, and documented? | User inventory |
| Group governance | Does each group have a clear purpose and membership? | Group membership |
| Least privilege | Are roles assigned at the narrowest practical scope? | RBAC assignments |
| MFA | Is strong authentication required for test identities? | Authentication settings and sign-in result |
| Conditional Access | Are access conditions scoped and tested safely? | Policy and sign-in evaluation |
| Privileged access | Are elevated permissions limited and reviewed? | PIM or temporary assignment record |
| Monitoring | Are sign-ins and administrative changes reviewed? | Audit and sign-in logs |
| Cleanup | Were temporary permissions and resources removed? | Final role and resource review |

## Test cases
1. Sign in as a standard test user and verify only intended access is available.
2. Attempt an action outside the user's assigned role and record whether it is denied.
3. Sign in as a user targeted by the MFA policy and verify the expected challenge.
4. Review a privileged activation or temporary role assignment and verify its duration.
5. Review sign-in and audit logs for the test activity.
6. Check for inherited roles or other assignments that could change the expected result.

## Findings template
For each finding, record:
- Finding ID and title
- Affected identity, group, resource, or policy
- Expected control
- Observed behavior
- Risk and business impact
- Recommended remediation
- Validation after remediation

## Zero Trust conclusion
Summarize how the lab applies:
- **Verify explicitly:** identity and sign-in context are evaluated.
- **Use least privilege:** permissions are scoped and privileged access is limited.
- **Assume breach:** activity is monitored and standing access is minimized.

## Cleanup
Remove temporary policies, role assignments, users, groups, and resource groups that are no longer required. Confirm no test configuration can affect unrelated users.

## Final deliverables
- Completed assessment checklist.
- Access test matrix with expected and actual results.
- Redacted screenshots or log excerpts.
- Findings and remediation recommendations.
- Short conclusion describing remaining gaps and limitations.
