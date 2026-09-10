# Lab 2 – Malicious Command Detection

## Objective

Detect suspicious command execution on an Ubuntu endpoint using Wazuh.

## Tools

- Wazuh SIEM
- Ubuntu Linux
- Auditd
- Wazuh custom rules

## Detection Rule

Custom Wazuh Rule ID:

100100

The rule was configured to detect `curl` command execution.

## Test Activity

The following command was executed in the lab:

curl http://example.com

Auditd captured the command execution through EXECVE/SYSCALL events.

## Investigation

The event was investigated through Wazuh Threat Hunting.

The resulting Wazuh alert showed:

- Rule ID: 100100
- Rule Level: 10
- Agent: ubuntuu
- Description: Suspicious command execution: curl detected

## Evidence

### Auditd Event

![Auditd Event](./screenshots/auditd-curl-event.png),(./screenshots/auditd-curl-rule.png)

### Custom Wazuh Rule

![Wazuh Rule](./screenshots/wazuh-rule-100100.png)

### Wazuh Alert

![Wazuh Alert](./screenshots/wazuh-alert.png)

## SOC Skills Demonstrated

- Command execution monitoring
- Linux log analysis
- Auditd investigation
- Custom detection rule creation
- SIEM alert investigation