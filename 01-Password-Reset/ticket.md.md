# Ticket 001: Password Reset

## Documentation Status
in progress

## Ticket Details
- Ticket ID: AD-001
- Technician: Rohullah Hussaini
- Date performed: 10-17-2026
- Type: Service request — lab password reset
- Priority: Medium — proposed for this lab exercise
- Status: Draft — pending execution
- Environment: Isolated Active Directory home lab
- Domain: Not yet documented
- Server: DC01 — Windows Server 2022 Standard
- Client: CLIENT01 — Windows 11 Pro, version 24H2
- Account: Not yet confirmed for this ticket
- Authorization: Self-authorized practice using a test account in my own isolated home lab. No real user request or identity verification is involved.

## Scenario
Practice resetting a test account password and verifying that the account can sign in with the new credentials. A forgotten or invalid password is a proposed scenario, not a confirmed finding.

## Actual Symptoms and Initial Findings
The user has forgotten the password and require a password reset.
## Planned Steps
1. Confirm the lab domain and intended test account.
2. Confirm authorization to reset the test account password.
3. Record the initial sign-in behavior and exact error, if any.
4. Open Active Directory Users and Computers on DC01.
5. Locate the account and check its status before making changes.
6. If the reset is appropriate, right-click the account and select Reset Password.
7. Enter and confirm a temporary password that meets the applicable lab password policy. Do not record the password in the ticket or screenshots.
8. If required by the exercise, select User must change password at next logon. Record whether this option was selected.
9. Apply the reset. Do not unlock, enable, or otherwise modify the account unless separately required and documented.
10. Test a fresh domain sign-in on CLIENT01. If a password change is required, complete it and verify sign-in with the final password.
11. Record the results without exposing any credentials.

## Actual Work Performed
Password was successfully reset for the user.

## Verification
- Test: Attempt a fresh domain sign-in on CLIENT01 using the reset password; complete the required password change if configured.
- Expected result: The reset is accepted, any required password change completes, and sign-in succeeds with the final credentials, provided no other access restrictions exist.
- Actual result: User is able to login now with selecting a new password.
- Outcome: user login is successful.

## Resolution / Current Outcome
Pending execution. The password reset and successful 
## Rollback / Recovery
- There is no rollback needed because it is just a virtual lab environment.

## Screenshots
Add real screenshots after completing the checks:
- 01-Finding-user — finding the user.
- 02-resetting-password — Resetting password.
- 03-selecting-password — Selecting a password.
- 04-password-successfully-changed — Successful password change

## Lessons Learned / Follow-up
- Confirm the domain and target account.
- Record initial symptoms and relevant non-secret settings.
- Complete the authorized password reset.
- Document whether a password change at next logon was required.
- Test sign-in and record actual results.
- Add sanitized screenshots and update the ticket status.
