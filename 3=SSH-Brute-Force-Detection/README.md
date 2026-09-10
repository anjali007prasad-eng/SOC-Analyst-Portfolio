# Lab 3 – SSH Brute-Force Detection

## Objective

Detect and investigate repeated failed SSH authentication attempts.

## Tools

- Wazuh SIEM
- Ubuntu Linux
- SSH
- Audit/authentication logs

## Attack Simulation

Multiple unsuccessful SSH authentication attempts were generated against the Ubuntu test machine.

## Detection

Wazuh detected repeated authentication failures.

Relevant events included:

- Rule ID: 5710
- Rule ID: 5551
- PAM failed login events
- Multiple failed logins within a short period

## Investigation

The events were reviewed in Wazuh Threat Hunting to identify:

- Timestamp
- Agent
- Rule ID
- Event description
- Severity
- Repeated authentication failures

## Evidence

![SSH Brute Force Detection](./screenshots/wazuh-bruteforce-alert.png)

## SOC Skills Demonstrated

- Authentication monitoring
- Brute-force detection
- Log analysis
- Alert investigation
- Threat hunting