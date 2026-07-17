# Failed Login Detection

## Objective

Detect failed authentication attempts and brute force activity using Wazuh.

## Description

Wazuh monitors Windows Security logs and can generate alerts when multiple failed login attempts occur. Failed logins are commonly associated with brute force attacks, password spraying, or unauthorized access attempts. :contentReference[oaicite:0]{index=0}

## Detection Capabilities

- Failed Login Attempts
- Brute Force Detection
- Username Enumeration
- Account Lockout Monitoring

## Important Event IDs

- 4625 – Failed Logon
- 4740 – Account Lockout

## SOC Investigation Questions

- Which account was targeted?
- What was the source IP?
- How many failed attempts occurred?
- Was a successful login observed afterward?
- Is this normal user behavior?

## Example Scenario

An attacker performs multiple RDP login attempts against a Windows endpoint.

Wazuh detects the failed authentication events and generates an alert for investigation. :contentReference[oaicite:1]{index=1}

## MITRE ATT&CK

- T1110 - Brute Force
- T1078 - Valid Accounts
```
