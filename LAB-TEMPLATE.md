# Lab XX: [Lab Title]

## Platform
Google Cloud Platform (GCP)

## Objective
Describe the goal of this exercise.

## Learning Outcomes
- [ ] Create or identify test identities.
- [ ] Organize identities into groups.
- [ ] Assign permissions at the correct scope.
- [ ] Validate allowed and denied actions.

## Prerequisites
- Authorized organization and project.
- Permission to manage test identities and IAM policies.
- MFA enabled for privileged identities.
- Dedicated test resources and identities.
- Costs reviewed before creating billable resources.

## Architecture
Document identities, groups, roles, resources, and permission scopes.

## Implementation
Document each step. Never include passwords, keys, tokens, or recovery codes.

## Validation
Test using a dedicated non-administrator identity. Record permitted and denied actions.

## Security Considerations
- Apply least privilege.
- Use the narrowest practical scope.
- Protect privileged accounts with MFA.
- Avoid production identities for experiments.
- Never commit secrets.

## Cleanup
Remove temporary role bindings, memberships, test identities, and billable resources when no longer needed.

## Results and Lessons Learned
Summarize outcomes, issues, and improvements.

## References
- [Google Cloud documentation](https://cloud.google.com/docs)
