# Ticket 002: Account Unlock

## Ticket Details
- Ticket ID: AD-002
- Technician: Rohullah Hussaini
- Date recorded: October 17, 2026
- Type: Incident
- Priority: Medium
- Status: In progress
- Environment: Isolated Active Directory home lab
- Domain: Not yet documented
- Server: DC01 — Windows Server 2022 Standard
- Client: CLIENT01 — Windows 11 Pro, version 24H2
- Account: SamiraJones
- Authorization: Self-authorized lab practice using a test account.

## Scenario
Investigate a suspected account lockout preventing the test user from signing in.

## Actual Symptoms and Initial Findings
The ticket concerns a sign-in issue for Samira Jones. The exact error message and account status have not yet been documented. Account lockout has not been confirmed.

## Planned Steps
1. Confirm the correct test account.
2. Record the sign-in error on CLIENT01.
3. Open Active Directory Users and Computers on DC01.
4. Check the account status and confirm whether it is locked.
5. If locked, select Unlock account on the Account tab and apply.
6. Test a fresh sign-in with the correct credentials.
7. Check whether the account locks again.

## Actual Work Performed
The lab details and ticket have been documented. Technical checks and account changes have not yet been recorded.

## Verification
- Test: Fresh domain sign-in on CLIENT01.
- Expected result: Sign-in succeeds and the account remains unlocked.
- Actual result: Not yet documented.
- Outcome: Not tested.

## Resolution / Current Outcome
In progress. The account issue and successful sign-in must be verified before closing the ticket.

## Rollback / Recovery
No account changes have been documented. Record previous settings before making additional changes. If lockout recurs, investigate the cause.

## Screenshots
Add real screenshots after completing the checks:
- 01-finding-user — Finding the user.
- 02-unlocking-the-user — Account unlock action.

## Lessons Learned / Follow-up
- None
