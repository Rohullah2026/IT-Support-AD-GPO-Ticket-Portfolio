# Ticket 004: Create New User Account

## Documentation Status
Draft lab worksheet. Planned steps are not a record of completed work. Document actual actions and verification before marking resolved.

## Ticket Details
- Ticket ID: AD-004
- Technician: Rohullah Hussaini
- Date performed: 10-17-2026
- Type: Service request — lab user account creation
- Priority: Medium — proposed for this lab exercise
- Status: Draft — pending execution
- Environment: Isolated Active Directory home lab
- Domain: Not yet documented
- Server: DC01 — Windows Server 2022 Standard
- Client: CLIENT01 — Windows 11 Pro, version 24H2
- New account name: Not yet selected
- User sign-in name: Not yet documented
- Target organizational unit (OU): Not yet documented
- Required group memberships: Not yet documented
- Authorization: Self-authorized practice using a test account in my own isolated home lab. No real user request or identity verification is involved.

## Scenario
Create a new Active Directory test user in the intended lab OU, assign only the access required for the exercise, and verify the account configuration and sign-in.

## Actual Symptoms and Initial Findings
There is a ticket from the IT department for creating a new user account with the information provided.

## Planned Steps
1. Confirm the lab domain, target OU, and authorization to create the test account.
2. Choose a fictional test identity and record the intended display name and sign-in name. Do not use production personal information.
3. Check whether the proposed account already exists to avoid creating a duplicate.
4. Open Active Directory Users and Computers on DC01.
5. Navigate to the intended OU and select New > User.
6. Enter the approved test identity and user sign-in name.
7. Set an initial password that meets the applicable lab password policy. Do not record the password in the ticket or screenshots.
8. Configure the password options required by the exercise and record those choices. Require a password change at next logon if appropriate for the test.
9. Review the details and create the account.
10. Confirm the account location, enabled state, and group memberships. Add only explicitly required groups; do not grant administrative access for convenience.
11. Test a fresh domain sign-in on CLIENT01. Complete any required password change.
12. Record actual results without exposing credentials.

## Actual Work Performed
Account information was successfully verified and created based the information from the ticket from IT department.

## Verification
- Test: Locate the new account in the intended OU and review its sign-in name, enabled state, password options, and group memberships. Attempt a fresh domain sign-in on CLIENT01.
- Expected result: The account exists in the correct OU with the intended settings and access. Sign-in succeeds, and any required password change completes, provided no other access restrictions exist.
- Actual result: Account created.
- Outcome: The user is able to login.

## Resolution / Current Outcome
Account was created successfully.
## Rollback / Recovery
- There is no rollback needed because it is just a virtual lab environment.

## Screenshots
Add real screenshots after completing the checks:
- 01-right-click-and-select-new-user — Creating the new user.
- 02-selecting-user-info — Putting the user information.
- 03-selecting-password — Selecting a password
- 04-user-created — Additional verification evidence.

## Lessons Learned / Follow-up
- Check for an existing account before creating a new one.
- Document actual password options and group memberships without recording passwords.
- Verify account creation and fresh sign-in.
- Add sanitized screenshots and update the ticket status.
