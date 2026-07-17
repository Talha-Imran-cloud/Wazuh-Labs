# File Integrity Monitoring (FIM)

## Objective

Monitor critical files and directories for unauthorized changes.

## Description

Wazuh File Integrity Monitoring (FIM) detects file creation, modification, and deletion events.

It creates a baseline of monitored files and compares future changes against that baseline. Alerts are generated when unexpected changes are detected. :contentReference[oaicite:0]{index=0}

## Detection Capabilities

- File Creation
- File Modification
- File Deletion
- Permission Changes
- Configuration Changes

## SOC Investigation Questions

- Which file changed?
- Who changed it?
- When did the change occur?
- Was the change authorized?
- Does the change indicate malware or persistence?

## Example Scenario

An attacker modifies a critical configuration file to maintain persistence.

Wazuh detects the change and generates an alert for investigation. :contentReference[oaicite:1]{index=1}

## MITRE ATT&CK

- T1098 - Account Manipulation
- T1547 - Boot or Logon Autostart Execution
