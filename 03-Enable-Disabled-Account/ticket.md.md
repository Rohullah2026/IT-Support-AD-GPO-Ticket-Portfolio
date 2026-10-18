# Ticket 003: Enable Disabled Account

## Documentation Status
in progress

## Ticket Details
- Ticket ID: AD-003
- Technician: Rohullah Hussaini
- Date performed: 10-17-2026
- Type: Service request — lab account enablement
- Priority: Medium — proposed for this lab exercise
- Status: Draft — pending execution
- Environment: Isolated Active Directory home lab
- Domain: Not yet documented
- Server: DC01 — Windows Server 2022 Standard
- Client: CLIENT01 — Windows 11 Pro, version 24H2
- Account: Not yet confirmed for this ticket
- Authorization: Self-authorized practice using a test account in my own isolated home lab. No real user request or identity verification is involved.

## Scenario
Investigate a test account suspected to be disabled and enable it if appropriate for the lab exercise.

## Actual Symptoms and Initial Findings
No observations have been documented for this ticket. The exact sign-in error, target account, and initial account status have not yet been verified. Account disablement is a scenario to investigate, not a confirmed finding.

## Planned Steps
1. Confirm the lab domain and intended test account.
2. Confirm that enabling the test account is authorized and appropriate.
3. Record the initial sign-in behavior and exact error, if any.
4. Open Active Directory Users and Computers on DC01.
5. Locate the test account and inspect its current status.
6. If the account is disabled, right-click it and select Enable Account.
7. Do not change the password, group memberships, or other account settings unless separately required and documented.
8. Test a fresh domain sign-in on CLIENT01 using the correct credentials.
9. Record the final account state and sign-in result.

## Actual Work Performed
The disabled account was successfully enabled.

## Verification
- Test: Confirm the account is enabled and attempt a fresh domain sign-in on CLIENT01.
- Expected result: The account is enabled and sign-in succeeds, provided no other access restrictions exist.
- Actual result: Account enabled.
- Outcome: The user is able to login now.

## Resolution / Current Outcome
Account enabled and the user is able to login successfully.

## Rollback / Recovery
-There is no rollback, because it was performed on virtual lab only.

## Screenshots
- 01-finding-user — Finding the user.
- 02-right-click-on- the-user — Right click on the user.
- 03-user-successfully-enabled — Final enabled state.


## Lessons Learned / Follow-up
- Lessons learned: Add one or two observations from actual practice after completing the lab.
- Confirm the domain name and target account.
- Record the initial account state and exact error.
- Enable the account only if required and authorized.
- Verify the final account state and test sign-in.
- Add screenshots, document actual results, and update the ticket status.
