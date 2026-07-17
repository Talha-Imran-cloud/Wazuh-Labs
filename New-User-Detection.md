# New User Detection

## Objective

Detect newly created user accounts using Wazuh and Windows Security Logs.

## Description

Wazuh monitors Windows Security Events and can generate alerts when a new user account is created.

Attackers commonly create new accounts to maintain persistence and regain access after remediation.

## Important Event IDs

- 4720 – User Account Created
- 4728 – User Added to Privileged Group
- 4732 – User Added to Local Group

## Detection Capabilities

- Unauthorized User Creation
- Backdoor Account Detection
- Persistence Detection
- Privileged Account Monitoring

## SOC Investigation Questions

- Who created the account?
- What is the name of the new account?
- Was the account added to Administrators or Domain Admins?
- Has the account logged in?
- Is the account legitimate?

## Example Scenario

An attacker compromises a workstation and creates a new account named backup_admin.

The attacker then adds the account to the Administrators group for long-term access.

Wazuh generates alerts for account creation and privilege assignment.

## MITRE ATT&CK

- T1136 - Create Account
- T1098 - Account Manipulation
