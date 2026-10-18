# Ticket 010: Offboarding User Account

## Documentation Status
In progress
## Ticket Details
- Ticket ID: AD-010
- Technician: Rohullah Hussaini
- Date performed: 10-17-2026
- Type: Service request — simulated user offboarding
- Priority: Medium — proposed for this lab exercise
- Status: Draft — pending execution
- Environment: Isolated Active Directory home lab
- Domain: Not yet documented
- Server: DC01 — Windows Server 2022 Standard
- Test client: CLIENT01 — Windows 11 Pro, version 24H2
- Target account: Not yet confirmed
- Current account OU: Not yet documented
- Offboarding OU, if required: Not yet specified
- Authorized offboarding time: Not yet documented
- Authorization: Self-authorized practice using a test account in my own isolated home lab. No real employee, production account, or employment action is involved.

## Scenario
Simulate offboarding an Active Directory test user by disabling the account at the authorized time and completing explicitly approved access-removal tasks. Preserve the account and required lab data unless deletion is separately authorized.

This ticket covers the isolated on-premises lab only. Email, cloud accounts, VPN access, application sessions, device recovery, and other services are outside scope unless explicitly added and tested. Do not claim that disabling an AD account proves all existing sessions or external access have ended.

## Actual Symptoms and Initial Findings
This is a planned lifecycle request, not a confirmed incident. No account inspection or offboarding actions have been documented. The target account, current enabled state, group memberships, active sessions, data dependencies, and authorized offboarding time have not yet been verified.

## Approved Offboarding Checklist
Complete this table before making changes. Remove tasks that do not apply rather than reporting them as completed.

| Task | Authorized scope / previous state | Actual result |
| --- | --- | --- |
| Verify target account and offboarding time |documented | performed |
| Disable account | recorded | performed |
| Remove selected direct group memberships, if approved | Exact groups specified | performed |
| End identified lab sessions, if approved | Sessions identified |  performed |
| Move to an offboarding OU, if approved | Source and destination specified | performed |
| Preserve or transfer lab data, if required | Requirements specified |  performed |
| Verify final state and fresh sign-in behavior | Test plan below |  tested |

## Planned Steps
1. Confirm authorization, the intended test account, and the time at which access should end. Verify the sign-in name and OU to avoid acting on a similarly named user.
2. Record the original enabled state, OU, relevant expiration settings, and direct group memberships. Record any known session or data dependencies without exposing secrets.
3. Confirm the exact approved tasks and any preservation requirements. Do not delete the account, profile, or files as a routine part of this ticket.
4. On DC01, open Active Directory Users and Computers and locate the verified test account.
5. At the authorized time, right-click the account and select Disable Account.
6. Close and reopen the account properties to verify that the account is disabled.
7. If approved, remove only the specified direct group memberships and record each change. Do not attempt to remove or change the primary group as a routine offboarding step.
8. If approved, move the account to the specified offboarding OU. Record the source and destination, and consider the policy impact before moving it.
9. If identified lab sessions are in scope, end them through the relevant authorized management method and verify each result separately. Do not assume the account disable action ended them.
10. Preserve or transfer lab data only according to the documented requirement. Record the actual action and destination without publishing sensitive contents.
11. On CLIENT01, test a fresh domain sign-in while the client is connected to the lab domain controller. Record the actual error. Do not use an offline cached sign-in as proof of account disablement enforcement.
12. Verify final account status, approved group changes, and OU location. Document any untested or remaining access paths.
13. Capture sanitized evidence and update the ticket outcome.

## Actual Work Performed
Confirmed authorization, and the time which the access should end. performed the step by step process and disabled the account according to the policy.

- Exact sign-in message: recorded.
- Outcome:  tested.
- Scope limitation: A disabled account and denied fresh sign-in do not prove termination of every pre-existing session, cached credential, application token, or external service login. Record those as separate scope items if applicable.

## Resolution / Current Outcome
Pending execution. The account has  been verified as disabled, and offboarding tasks have  been demonstrated. 
## Rollback / Recovery
- Previous account state, OU, and memberships: 
- Changes made: None documented.
- Recovery authorization: Explicit approval is required before restoring offboarded access, even if a technical reversal is possible.
- Recovery plan: If an erroneous lab offboarding is confirmed and reversal is authorized, restore only the recorded settings changed by this ticket. Re-enable the account only if it was previously enabled and access restoration is approved.
- Restore removed memberships or the original OU only when specifically approved. Do not recreate access from memory.
- Ended sessions are not automatically restored. Data recovery depends on the preservation method used; no deletion is planned in this ticket.
- Verify the recovered state and perform only the authorized access tests.

## Screenshots
- 01-right-click-on-the-user— right click on the user.
- 02-account-disabled — Disabled account state after saving.
- 03-right-click-on-the-user — right click on the user.
- 04-Account-disabled — account disabled.
- 05-block-office-sign-in — block office sign in.
- 06-select-block-sign-in — select block sign in.

## Lessons Learned / Follow-up
- Confirm the exact account, authorized timing, and task scope.
- Record previous settings before making changes.
- Disable the account and verify a fresh online domain sign-in is denied.
- Verify additional access-removal and preservation tasks separately if in scope.
- Document exclusions, untested access paths, and remaining work.
- Add sanitized screenshots and update the ticket status.
