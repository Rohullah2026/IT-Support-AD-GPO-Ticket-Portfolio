# Ticket 007: GPO — Disable USB Storage

## Documentation Status
in progress
## Ticket Details
- Ticket ID: AD-007
- Technician: Rohullah Hussaini
- Date performed: 10-17-2026
- Type: Change — lab removable-storage restriction
- Priority: Medium — proposed for this lab exercise
- Status: Draft — pending execution
- Environment: Isolated Active Directory home lab
- Domain: Not yet documented
- Server: DC01 — Windows Server 2022 Standard
- Test client: CLIENT01 — Windows 11 Pro, version 24H2
- Target computer OU: Not yet documented
- Proposed GPO name: LAB-Disable-USB-Storage
- Test USB storage device: Not yet documented
- Authorization: Self-authorized practice in my own isolated home lab using a test computer and disposable test files. No production systems are in scope.

## Scenario
Use a computer-scoped Group Policy Object to restrict access to removable-disk storage on the test client. Verify both policy application and actual storage access.

The proposed method uses Removable Disks policies. It is not a USB-port disablement policy or a guarantee that every USB-connected storage device will be blocked. Device classification affects coverage. USB keyboards and mice are not the target of this exercise.

## Actual Symptoms and Initial Findings
There is a request for disabling the user access to usb storage, a GPO was created and the user access was disabled to usb storage.

Do not claim that USB storage was initially accessible or later blocked without testing. If CLIENT01 is a virtual machine, confirm that the test USB device is passed through and accessible before attributing any failure to Group Policy.

## Proposed Configuration
Computer Configuration > Policies > Administrative Templates > System > Removable Storage Access

Do not enable All Removable Storage classes: Deny all access merely as a substitute. That setting has broader scope and takes precedence over individual removable-storage settings. Use it only if a broader restriction is explicitly intended and documented.

## Planned Steps
1. Confirm authorization, the target computer OU, and the intended storage restriction.
2. Confirm that CLIENT01 is domain joined and can communicate with the lab domain controller.
3. Use a known-working test USB device with disposable files. Record baseline read and write behavior. Test execution only with a trusted harmless test file if execution testing is in scope.
4. Record existing effective policies, relevant GPO links, filtering, and policy values. Back up any existing GPO before editing it.
5. On DC01, open Group Policy Management and create a dedicated lab GPO named LAB-Disable-USB-Storage, or record the actual name used.
6. Link the GPO only to the intended test computer OU. Confirm that security filtering permits the intended computer to read and apply it. Do not link it to the domain root or Domain Controllers OU for convenience.
7. Edit the GPO and configure the three Removable Disks settings listed above under Computer Configuration.
8. On CLIENT01, run gpupdate /force from an elevated command prompt. Record the output and complete any requested restart. Reconnect the test device as needed.
9. Generate an effective-policy report on CLIENT01 using gpresult /h "%TEMP%\usb-policy-report.html" from an elevated command prompt. Verify computer-policy application and the relevant settings; do not assume that a successful refresh proves enforcement.
10. Retest the same device and operations used for the baseline. Record exact errors and whether read, write, and any in-scope execution attempts are denied.
11. Check that expected non-storage USB peripherals still function, if available. Record any device classes or devices not covered by the test.
12. Capture sanitized evidence and document the actual outcome.

## Actual Work Performed
GPO was created, applied to the specific domain or OU, then it was verified with the user.

## Verification
- Baseline: tested.
- Policy application test: Review the computer's effective-policy report for the intended GPO and settings.
- Functional test: Repeat read, write, and any in-scope execution tests using the same known-working USB device.
- Expected result: The intended policy applies and the configured operations are denied for the tested removable-disk device.
- Actual result: Not yet documented.
- Exact error messages: Not yet recorded.
- Outcome: result verified.
- Limitation: Denied access alone does not prove the GPO caused it. Compare baseline behavior, effective policy, and post-change behavior. Do not generalize one device's result to every USB storage class.

## Resolution / Current Outcome
-GPO was created and the user access was disabled to the user.
## Rollback / Recovery
- Previous policy values and links: Not yet captured.
- Changes made: None documented.
- Recovery plan: If reversal is authorized and a dedicated GPO was newly created for this ticket, disable its specific test-OU link. If an existing GPO was edited, restore only the recorded settings changed by this ticket or use its authorized backup.
- Refresh policy on CLIENT01, complete any required restart, and retest the same device.
- Verify the resulting effective policy; other GPOs may still impose storage restrictions.
- Do not remove unrelated security controls, change domain-wide policies, or delete evidence during recovery.

## Screenshots
- 01-selecting-GPO — Selecting GPO.
- 02-naming-GPO — Naming the GPO.
- 03-editing-GPO — editing the GPO.
- 04-selecting-removable-storage — selecting the removable storage.
- 05-selecting-all-removable-storage — selecting all removable storage.
- 06-select-enable — select enable.
- 07-select-refresh — select refresh.

## Lessons Learned / Follow-up
- Lessons learned: Add one or two observations from actual practice after completing the lab.
- Confirm the target computer OU, GPO scope, and device classification.
- Record baseline behavior and previous policy settings.
- Apply the dedicated lab policy and verify effective settings.
- Test actual storage operations and record exact results.
- Document device coverage and any untested operations.
- Add sanitized screenshots and update the ticket status.

## Technical Sources
- Microsoft: Managing removable devices through Group Policy — troubleshooting guidance.
  https://learn.microsoft.com/en-us/troubleshoot/windows-server/group-policy/removable-devices-group-policy-troubleshooting-guidance
- Microsoft: Create a GPO to disable USB storage devices — Q&A procedure for the Removable Disks settings.
  https://learn.microsoft.com/en-us/answers/questions/2198881/create-a-gpo-to-disable-usb-storage-devices
- Microsoft: ADMX_RemovableStorage policy documentation — all-class restriction scope and precedence.
  https://learn.microsoft.com/en-us/windows/client-management/mdm/policy-csp-admx-removablestorage
