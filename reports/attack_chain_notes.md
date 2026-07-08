# Attack Chain Detection Project

## Goal

Detect suspicious PowerShell activity using Sysmon and Sigma.

## Detection Rules

1. PowerShell Execution Policy Bypass
   - Detects PowerShell started with ExecutionPolicy Bypass.

2. Encoded PowerShell
   - Detects PowerShell using -EncodedCommand.

3. CMD to PowerShell
   - Detects PowerShell launched by cmd.exe.

4. PowerShell Network Connection
   - Detects outbound network connections from PowerShell.

5. PowerShell File Creation
   - Detects files created by PowerShell.

6. Registry Persistence
   - Detects suspicious registry modifications related to persistence.

## Detection Philosophy

No single event confirms an attack.

Multiple related events occurring on the same host within a short period provide higher confidence and should be investigated as a single incident.
