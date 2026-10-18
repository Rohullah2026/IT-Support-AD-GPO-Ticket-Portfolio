# Ticket 006: Update Security Group Membership

## Documentation Status
in progress
## Ticket Details
- Ticket ID: AD-006
- Technician: Rohullah Hussaini
- Date performed: 10-17-2026
- Type: Service request — lab security group membership update
- Priority: Medium — proposed for this lab exercise
- Status: Draft — pending execution
- Environment: Isolated Active Directory home lab
- Domain: Not yet documented
- Server: DC01 — Windows Server 2022 Standard
- Client: CLIENT01 — Windows 11 Pro, version 24H2
- Target account: Not yet confirmed for this ticket
- Target security groups: Not yet documented
- Requested action: Add or remove membership — not yet specified
- Authorization: Self-authorized practice using a test account and test groups in my own isolated home lab. No real user request or identity verification is involved.

## Scenario
Update an existing test user's direct membership in selected Active Directory security groups to match an explicitly defined lab access requirement. Add or remove only the authorized memberships.

Changing group permissions, group scope, group type, nested group relationships, or the user's primary group is outside this ticket unless separately authorized and documented. Do not grant privileged access for convenience.

## Actual Symptoms and Initial Findings
The user was added to the group successfully.

## Planned Steps
1. Confirm the lab domain, target test user, and authorization for each membership change.
2. Define the intended access and exact groups to add or remove in the Requested Changes table.
3. Open Active Directory Users and Computers on DC01.
4. Verify the user's sign-in name and account location. Verify each target group's identity and that it is a security group.
5. Record the user's existing direct membership in each target group before editing. Note any known nested membership relevant to the test.
6. Open the user's Properties and review the Member Of tab, or inspect the target group's Members tab.
7. Add or remove only the authorized direct memberships. Verify the selected object before applying each change.
8. Save the changes, close and reopen the relevant properties, and compare the saved memberships with the request.
9. If resource access is part of the lab, define the resource and expected allowed or denied action before testing. Use a fresh sign-in on CLIENT01 for the access test.
10. Record the actual membership results and any separate resource-access test results. Capture sanitized evidence.

## Actual Work Performed
Found the user, added the user to specific group and verified that the user is added to the group.

## Verification
- Membership test: Reopen the target groups' Members lists or the user's Member Of tab and confirm each requested direct membership change.
- Expected membership result: The user is directly included in or excluded from each target group as requested, with unrelated memberships unchanged.
- Actual membership result: verified.
- Outcome: group membership verified.
## Resolution / Current Outcome
-User selected and added to the group successfully.

## Rollback / Recovery
- Recovery plan: If reversal is authorized, undo only the membership changes introduced by this ticket. Remove memberships newly added by this ticket and restore memberships removed by this ticket, using the recorded previous state.
- Do not restore access removed for security or offboarding reasons without explicit approval.
- Verification after recovery: Reopen the relevant group properties and confirm the restored membership state. Repeat any in-scope resource-access test with a fresh sign-in.
- Do not change unrelated memberships or group permissions as part of recovery.

## Screenshots
Add real screenshots after completing the checks:
- 01-finding-the-user — Finding the user.
- 02-right-click-on-user — right click on the user.
- 03-finding-the-group — Finding the group.
- 04-user-was-added — The user was added.

## Lessons Learned / Follow-up
- Confirm the target user, groups, and authorized access requirement.
- Record existing direct memberships before editing.
- Apply only the requested membership changes.
- Verify saved memberships and separately test resource access if in scope.
- Complete the change table, add sanitized screenshots, and update the ticket status.
