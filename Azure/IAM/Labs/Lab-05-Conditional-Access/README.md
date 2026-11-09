# Lab 05 – Conditional Access

## Objective
Build a Conditional Access policy that evaluates sign-in context instead of granting access based only on a valid password.

## Scenario
The organization wants to require MFA for a selected test group when accessing a cloud application.

## Prerequisites
- Complete Labs 01, 02, and 04.
- Microsoft Entra ID licensing that supports Conditional Access.
- A dedicated test group and test account.
- A protected emergency-access account excluded from the test policy.

## Tasks
1. Open Protection > Conditional Access > Policies in the Microsoft Entra admin center.
2. Create a policy named CA-Lab-Require-MFA-Test-Users.
3. Under Users, include only the dedicated test group.
4. Exclude the protected emergency-access account.
5. Under Target resources, select an appropriate test cloud application.
6. Under Grant, require multifactor authentication.
7. Start with Report-only mode.
8. Review policy impact using sign-in logs and Conditional Access insights available in your tenant.
9. After confirming scope and expected behavior, enable enforcement only if safe to do so.
10. Test with an included user and confirm that an excluded account is not unexpectedly affected.

## Validation
- The policy targets only the intended test group and application.
- Report-only results match expected policy behavior.
- The test user is prompted for MFA when the policy is enforced.
- Emergency access remains available and is not accidentally blocked.

## Zero Trust connection
Conditional Access evaluates signals such as user, application, device, location, and risk where licensed and configured. It helps implement verify explicitly.

## Safety notes
Never test broad policies against All users in a production tenant. Keep emergency-access exclusions narrow, documented, strongly protected, and monitored. Use Report-only mode first and change one condition at a time.

## Cleanup
Disable and delete the test policy after recording results, unless you intentionally retain it in the lab tenant.

## Evidence
Capture redacted policy configuration, Report-only results or sign-in logs, and test outcomes for included and excluded identities.
