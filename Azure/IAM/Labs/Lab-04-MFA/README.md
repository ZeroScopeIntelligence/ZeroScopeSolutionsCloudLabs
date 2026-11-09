# Lab 04 – Multifactor Authentication (MFA)

## Objective
Understand how MFA strengthens authentication and how authentication methods are managed in Microsoft Entra ID.

## Scenario
The organization wants stronger sign-in protection for workforce identities, especially accounts with elevated permissions.

## Prerequisites
- A lab tenant and dedicated test users.
- An administrator authorized to review authentication-method settings.
- Access to a supported MFA method.
- Awareness of the tenant's current security defaults and Conditional Access configuration.

## Tasks
1. Open the [Microsoft Entra admin center](https://entra.microsoft.com/).
2. Review **Protection > Authentication methods** and the methods available in the tenant.
3. Review whether security defaults or Conditional Access already enforce MFA. Avoid creating overlapping controls without understanding their interaction.
4. Choose the supported method for the lab tenant and verify feature availability and licensing.
5. Register an MFA method for a dedicated test user through Microsoft's official security-info registration process.
6. Sign in as the test user and verify that the expected MFA challenge is presented.
7. Review the sign-in logs and confirm the authentication details.
8. Document the result without recording authentication secrets or recovery codes.

## Validation
- The test identity has a registered authentication method.
- A new sign-in triggers the expected MFA requirement.
- The sign-in log records the authentication result.

## Zero Trust connection
A password alone should not be treated as sufficient proof of identity. MFA strengthens identity verification, but it does not replace authorization, device evaluation, or monitoring.

## Safety notes
- Do not experiment with MFA requirements on your only administrator account.
- Maintain a separately protected emergency-access account and monitor its use.
- Never publish recovery codes, QR codes, phone numbers, or authentication secrets.

## Cleanup
Remove test authentication methods only when the account is no longer needed and only after confirming the account's recovery requirements.

## Evidence
Capture authentication-method settings and a redacted sign-in log showing the MFA result.
