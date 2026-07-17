# PowerShell Monitoring

## Objective

Detect PowerShell activity and suspicious script execution using Wazuh.

## Description

PowerShell is a legitimate Windows administration tool, but attackers frequently abuse it for malware execution, persistence, credential theft, and lateral movement.

Wazuh can monitor PowerShell Operational logs and generate alerts when suspicious PowerShell activity is detected. :contentReference[oaicite:0]{index=0}

## Detection Capabilities

- PowerShell Script Execution
- Encoded Commands
- Registry Modifications
- Malware Download Activity
- Suspicious Administrative Actions

## Important Event IDs

- 4104 – PowerShell Script Block Logging
- 4103 – PowerShell Module Logging

## SOC Investigation Questions

- Who executed PowerShell?
- What command was executed?
- Was the command encoded or obfuscated?
- Did it download a file?
- Did it create a new user or modify privileges?

## Example Scenario

A user opens a phishing attachment.

The document launches PowerShell and downloads a malicious payload from the internet.

Wazuh detects the PowerShell activity and generates an alert for investigation. :contentReference[oaicite:1]{index=1}

## MITRE ATT&CK

- T1059.001 - PowerShell
- T1105 - Ingress Tool Transfer
- T1055 - Process Injection
- T1547 - Boot or Logon Autostart Execution

## Analyst Response

1. Review PowerShell logs.
2. Identify executed commands.
3. Check for downloaded files.
4. Investigate account creation activity.
5. Isolate the endpoint if compromise is confirmed.
