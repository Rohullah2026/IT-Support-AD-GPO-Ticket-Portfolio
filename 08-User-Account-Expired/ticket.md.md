# Ticket 008: User Account Expired

## Documentation Status

## Ticket Details
- Ticket ID: AD-008
- Technician: Rohullah Hussaini
- Date performed: 10-17-2026
- Type: Incident — simulated account access interruption
- Priority: Medium — proposed for this lab exercise
- Status: Draft — pending execution
- Environment: Isolated Active Directory home lab
- Domain: Not yet documented
- Server: DC01 — Windows Server 2022 Standard
- Client: CLIENT01 — Windows 11 Pro, version 24H2
- Target account: Not yet confirmed for this ticket
- Account OU: Not yet documented
- Approved new expiration: Not yet specified
- Authorization: Self-authorized practice using a test account in my own isolated home lab. No real user request or identity verification is involved.

## Scenario
Investigate a test user who is suspected to be unable to sign in because the account has expired. If account expiration is confirmed and an extension is authorized for the exercise, update the expiration setting and verify access.

Account expiration is the scenario to investigate, not a proven finding. Do not assume that the password has expired or that the account is disabled or locked out.

## Actual Symptoms and Initial Findings
The user was verified and is unable to sign in, based on the research, it seems that the account is expired and the issue was resolved.

## Requested Change
Complete this table before editing the account.

| Item | Recorded value |
| --- | --- |
| Verified account sign-in name | Not yet documented |
| Current account expiration setting | Not yet recorded |
| Date, time, and time zone at verification | Not yet recorded |
| Approved replacement expiration setting | Not yet specified |
| Actual saved expiration setting | Not yet verified |

## Planned Steps
1. Confirm the lab domain, intended test account, and authorization to investigate and extend access.
2. On CLIENT01, record the initial sign-in behavior and exact error using the correct domain account.
3. On DC01, open Active Directory Users and Computers.
4. Locate the account and verify its sign-in name and OU.
5. Open Properties > Account and record the Account expires setting before making changes.
6. Check whether the expiration setting supports the reported issue. Record relevant date and time context, and inspect other account restrictions if needed.
7. If expiration is confirmed, define the authorized replacement setting before editing. Use the agreed future date, or Never only if explicitly appropriate for the lab exercise. Do not remove expiration automatically.
8. Apply the authorized change and close and reopen the account properties to verify that it was saved.
9. Do not reset the password, unlock the account, enable it, or change group memberships unless separately required and documented.
10. Attempt a fresh domain sign-in on CLIENT01 with the correct credentials.
11. Record the final account setting, exact sign-in result, and any remaining issue. Capture sanitized evidence.

## Actual Work Performed
No account inspection, expiration change, or sign-in test has been documented. After completing the lab, record the verified account, previous expiration setting, approved new setting, actual actions, and any deviations from the plan.

## Verification
- Configuration test: Close and reopen the target account properties and compare Account expires with the authorized replacement setting.
- Sign-in test: Attempt a fresh domain sign-in on CLIENT01 using the correct credentials.
- Expected result: The intended expiration setting is saved, the account is no longer expired at the test time, and sign-in succeeds if no other access restrictions exist.
- Actual configuration result: Not yet documented.
- Actual sign-in result: Not yet documented.
- Exact error, if any: Not yet recorded.
- Outcome: The user was enabled.
## Resolution / Current Outcome
Pending execution. Account expiration has not been confirmed, and restored access has not been verified. Do not mark resolved until the actual finding, authorized change, and verification results are recorded.

## Rollback / Recovery
- Recovery plan: If reversal is authorized, restore only the recorded previous expiration setting and verify it after saving.
- Restoring an already elapsed expiration may prevent access again. Confirm that this is intended before proceeding.
- Do not extend an account expired for security or offboarding reasons without explicit approval.
- Do not guess the previous setting or change unrelated account controls.

## Screenshots
- 01-user-expired — User expired.
- 02-left-click-on-the-user — Left click on the user.
- 03-selecting-never — select never.
- 04-user-login-succesful — user login successful.

## Lessons Learned / Follow-up
- Confirm the domain, account identity, and exact sign-in error.
- Record the original expiration setting and verification time context.
- Confirm the authorized extension before changing access.
- Verify the saved setting and complete a fresh sign-in test.
- Document any remaining issue instead of assuming expiration was the only cause.
- Add sanitized screenshots and update the ticket status.
