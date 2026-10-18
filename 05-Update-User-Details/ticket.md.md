# Ticket 005: Update User Details

## Documentation Status
Draft lab worksheet. Planned steps are not a record of completed work. Document actual actions and verification before marking resolved.

## Ticket Details
- Ticket ID: AD-005
- Technician: Rohullah Hussaini
- Date performed: 10-17-2026
- Type: Service request — lab user details update
- Priority: Medium — proposed for this lab exercise
- Status: Draft — pending execution
- Environment: Isolated Active Directory home lab
- Domain: Not yet documented
- Server: DC01 — Windows Server 2022 Standard
- Client: CLIENT01 — Windows 11 Pro, version 24H2
- Target account: Not yet confirmed for this ticket
- Account OU: Not yet documented
- Requested updates: Not yet documented
- Authorization: Self-authorized practice using a test account in my own isolated home lab. No real user request or identity verification is involved.

## Scenario
Update selected profile details for an existing Active Directory test user. Possible lab fields include display name, description, office, telephone number, email address, job title, department, and company. Only explicitly selected fields are in scope.

Changing the sign-in name, moving the account, changing group memberships, and resetting the password are outside this ticket unless separately authorized and documented.

## Actual Symptoms and Initial Findings
This ticket is a request for updating the information for the user.

## Planned Steps
1. Confirm the lab domain, intended test account, and authorization to update its details.
2. Identify the account by its sign-in name and OU rather than relying only on the display name.
3. Define the exact fields and replacement values in the Requested Changes table.
4. Open Active Directory Users and Computers on DC01.
5. Locate the account, open Properties, and record the existing values of every field to be changed.
6. Update only the agreed profile fields using fictional lab data.
7. Apply and save the changes.
8. Close and reopen the account properties, then compare the saved values with the request.
9. Confirm that no unrelated settings were intentionally changed, including sign-in name, account status, group memberships, and password settings.
10. Record actual results and capture sanitized evidence.

## Actual Work Performed
Some information pertaining to the user account was updated based on the request from the ticket shown in the screenshots.

## Verification
- Test: Close and reopen the same account properties in ADUC. Compare each saved field with the requested value and record the result in the table.
- Expected result: All requested profile fields contain the intended values, and unrelated account settings remain unchanged.
- Actual result: user details were updated.
- Outcome: tested.
- Scope note: A sign-in test alone does not verify profile-field updates. If a sign-in test is separately performed, record it as an additional check rather than a substitute for field verification.

## Resolution / Current Outcome
The requested updates were successfully updated.

## Rollback / Recovery
- This is just a virtual lab environment, so no rollbacks were performed.

## Screenshots
Add real screenshots after completing the checks:
- 01-double-left-click-on-the-user — Double click on the user account.
- 02-go-to-organization — Go to organization.
- 03-go-to-telephone — Go to telephone.
- 04-go-to-address — go to address.


## Lessons Learned / Follow-up
- Lessons learned: Add one or two observations from actual practice after completing the lab.
- Confirm the target account and exact requested updates.
- Record previous values before editing.
- Apply only the agreed changes.
- Reopen the account properties and verify each saved value.
- Complete the change table, add sanitized screenshots, and update the ticket status.
