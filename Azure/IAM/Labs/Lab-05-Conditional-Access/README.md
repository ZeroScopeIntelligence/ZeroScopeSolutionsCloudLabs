# Lab 05 – Conditional Access

## Objective
Create a carefully scoped Conditional Access policy that evaluates sign-in context rather than relying only on a valid password.

## Scenario
The organization wants to require MFA for a selected test group when members access a designated cloud application.

## Prerequisites
- Complete Labs 01, 02, and 04.
- Microsoft Entra licensing that supports Conditional Access.
- A dedicated test group and test account.
- A separately protected emergency-access account.
- A safe way to review sign-in logs.

## Tasks
1. Open **Protection > Conditional Access > Policies** in the Microsoft Entra admin center.
2. Create a policy named `CA-Lab-Require-MFA-Test-Users`.
3. Under **Users**, include only the dedicated test group.
4. Exclude the protected emergency-access account according to your organization's emergency-access design.
5. Under **Target resources**, select an appropriate test cloud application.
6. Under **Grant**, require multifactor authentication.
7. Set the policy to **Report-only** initially.
8. Review sign-in logs and available Conditional Access insights to understand the policy's expected impact.
9. Validate the scope and test behavior with the dedicated test identity.
10. Enable enforcement only after confirming the policy will not disrupt unrelated users or emergency access.

## Validation
- The policy targets only the intended test group and application.
- Report-only results match the expected policy behavior.
- The test user is required to complete MFA when enforcement is enabled.
- Emergency access remains available and is monitored.

## Zero Trust connection
Conditional Access can evaluate signals such as user, application, device, location, and risk when supported and configured. This is an implementation of **verify explicitly**.

## Safety notes
- Never test broad policies against all users in a production tenant.
- Keep emergency-access exclusions narrow, documented, protected, and monitored.
- Use Report-only mode first.
- Change one condition at a time and maintain a recovery path.

## Cleanup
Disable and delete the test policy after recording results, unless you intentionally retain it in the isolated lab tenant.

## Evidence
Capture redacted policy settings, Report-only results, and sign-in outcomes for the test identity.
