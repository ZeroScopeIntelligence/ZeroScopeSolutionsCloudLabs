# Lab 04 – Multifactor Authentication (MFA)

## Objective
Understand how MFA adds an authentication factor and how authentication methods are managed in Microsoft Entra ID.

## Scenario
The organization wants stronger sign-in protection for workforce identities, especially accounts with elevated permissions.

## Prerequisites
- A lab tenant and test users.
- An administrator authorized to manage authentication methods.
- Access to a supported MFA method.
- Confirm tenant licensing and current Microsoft Entra authentication-method settings.

## Tasks
1. Open the Microsoft Entra admin center.
2. Review Protection > Authentication methods and the methods available in your tenant.
3. Review security defaults and Conditional Access configuration before changing anything.
4. For a controlled lab, choose the supported method for requiring MFA. Avoid overlapping controls without understanding their interaction.
5. Register an MFA method for a dedicated test user using Microsoft's official sign-in and security-info flow.
6. Sign in as the test user and verify that the configured MFA challenge is presented.
7. Review sign-in logs to confirm the authentication details.

## Validation
- The test identity has a registered authentication method.
- A new sign-in triggers the expected MFA challenge.
- The sign-in log records the authentication result.

## Zero Trust connection
A password alone should not be treated as sufficient proof of identity. MFA strengthens verification, but does not replace authorization, device evaluation, or monitoring.

## Safety notes
Do not experiment with MFA requirements on your only administrator account. Maintain a separately protected emergency-access account and monitor it. Never share or publish recovery codes, QR codes, phone numbers, or authentication secrets.

## Cleanup
Remove test authentication methods only when the account is no longer needed, following the tenant's recovery and access procedures.

## Evidence
Capture authentication-method settings, the test user's registered method with personal details hidden, and a redacted sign-in log.
