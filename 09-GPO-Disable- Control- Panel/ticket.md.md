# Ticket 009: GPO — Disable Control Panel

## Documentation Status
In progress

## Ticket Details
- Ticket ID: AD-009
- Technician: Rohullah Hussaini
- Date performed: 10-17-2026
- Type: Change — lab Control Panel and Settings restriction
- Priority: Medium — proposed for this lab exercise
- Status: Draft — pending execution
- Environment: Isolated Active Directory home lab
- Domain: Not yet documented
- Server: DC01 — Windows Server 2022 Standard
- Test client: CLIENT01 — Windows 11 Pro, version 24H2
- Target test user: Not yet confirmed
- Target user OU: Not yet documented
- Proposed GPO name: LAB-Disable-Control-Panel
- Authorization: Self-authorized practice using a test user in my own isolated home lab. No production systems or real user requests are involved.

## Scenario
Apply a user-scoped Group Policy to restrict access to Control Panel and the Windows Settings app for the intended test user.

The selected policy targets both Control Panel and Settings, not Control Panel alone. Confirm that this broader scope is intended before applying it. This is an interface restriction, not a replacement for appropriate permissions or other security controls.

## Actual Symptoms and Initial Findings
The user was verified, and the control panel was disabled for the user successfully.

## Proposed Configuration
- Policy path: User Configuration > Policies > Administrative Templates > Control Panel
- Policy: Prohibit access to Control Panel and PC settings
- Proposed setting: Enabled
- Previous effective setting: Not yet recorded
- GPO link location: Intended test user OU — not yet confirmed
- Security filtering: Not yet documented

## Planned Steps
1. Confirm authorization and that restricting both Control Panel and Settings is intended.
2. Verify the lab domain, target user, and OU containing that user. Preserve a separate authorized administrative account for recovery.
3. Sign in to CLIENT01 as the target user. Record baseline results when opening Control Panel using control.exe and Settings using Windows + I.
4. Record existing relevant policies, links, filtering, and effective settings. Back up any existing GPO before editing it.
5. On DC01, open Group Policy Management and create a dedicated GPO named LAB-Disable-Control-Panel, or record the actual name used.
6. Link the GPO only to the intended test user OU. Confirm that filtering permits the intended user to apply the policy and that required GPO read permissions are retained.
7. Edit the GPO and navigate to User Configuration > Policies > Administrative Templates > Control Panel.
8. Set Prohibit access to Control Panel and PC settings to Enabled and save.
9. On CLIENT01, refresh policy in the target user's session using gpupdate /force. Record the output and complete any requested sign-out. Sign out and back in for the final test if needed.
10. In the target user's session, generate a user policy report using gpresult /scope user /h "%TEMP%\control-panel-policy.html". Review the applied GPO and relevant effective setting. Do not substitute a different administrator's user-policy report.
11. Attempt to open Control Panel and Settings again. Record exact behavior and messages for each separately.
12. If a non-target account is available and testing is authorized, check that it is not unintentionally restricted by this GPO.
13. Capture sanitized evidence and document the actual outcome.

## Actual Work Performed
The user was verified, GPO was created and applied to the selected OU, and gpupdate/force was applied to the user.

## Verification
| Check | Expected result | Actual result |
| --- | --- | --- |
| Baseline Control Panel access | Record actual pre-change behavior | Not tested |
| Baseline Settings access | Record actual pre-change behavior | Not tested |
| Target user's effective policy | Intended GPO applies and policy is Enabled | Not tested |
| Control Panel after change | Access is restricted for the target user | Not tested |
| Settings after change | Access is restricted for the target user | Not tested |
| Non-target user, if in scope | Not unintentionally restricted by this GPO | Not tested |

- Exact messages: Not yet recorded.
- Outcome: Control panel was disabled successfully.
- Scope note: A successful policy refresh alone does not prove enforcement. Record effective-policy evidence and actual application behavior separately.

## Resolution / Current Outcome
GPO was applied successfully, the user's request to access control panel was successfully disabled.

## Rollback / Recovery
- Previous policy values, links, and filtering: Not yet captured.
- Changes made: None documented.
- Recovery plan: If reversal is authorized and this ticket created a dedicated GPO, disable its specific test-OU link. If an existing GPO was edited, restore only the recorded changes or use its authorized backup.
- Refresh policy for the affected user and sign out and back in as needed.
- Verify effective policy and retest both Control Panel and Settings. Other GPOs may still impose restrictions.
- Do not change domain-wide policies, remove unrelated controls, or delete evidence during recovery.

## Screenshots
- 01-edit-GPO — Select edit GPO.
- 02-select-enable — Enabled policy and intended user-OU link.
- 03-select-user — select user.
- 04-link-the-GPO — link the GPO.
- 05-select-GPO — select GPO.
- 06-click-refresh — Click refresh.
- 07-apply-GPO — apply GPO.
- 08-result-of-GPO — result showing GPO.
- 09-result-of-GPO- result of GPO

## Lessons Learned / Follow-up
- Confirm the test user, user OU, and intended restriction scope.
- Record baseline access and previous policy settings.
- Verify user-policy application in the correct user's session.
- Test Control Panel and Settings separately.
- Add sanitized screenshots and update the ticket status.

