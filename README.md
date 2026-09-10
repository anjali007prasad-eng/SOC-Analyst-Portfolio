# Wazuh SOC Labs

Hands-on SOC monitoring and threat detection labs built using Wazuh SIEM and Ubuntu Linux.

## Objective

The goal of these labs was to practice real-world SOC Analyst L1 activities including:

- Security event monitoring
- Vulnerability detection
- File Integrity Monitoring
- SSH brute-force detection
- Suspicious command detection
- Threat hunting
- Linux audit log analysis
- Alert investigation

## Lab Environment

- Wazuh SIEM 4.14.7
- Ubuntu Linux
- Wazuh Agent
- Auditd
- SSH
- Docker
- VMware

## Labs

### Lab 1 – Vulnerability Detection

Identified vulnerabilities affecting installed Ubuntu packages using Wazuh Vulnerability Detection.

[View Lab 1](./1=Vulnerability-Detection/)

### Lab 2 – Malicious Command Detection

Created a custom Wazuh rule to detect suspicious `curl` command execution and investigated the resulting alert.

Custom Rule: `100100`

[View Lab 2](./2=Malicious-Command-Detection/)

### Lab 3 – SSH Brute-Force Detection

Generated multiple failed SSH authentication attempts and investigated Wazuh alerts associated with brute-force activity.

[View Lab 3](./3=SSH-Brute-Force-Detection/)

### Lab 4 – Malicious File Detection

Used a safe EICAR test file to simulate malware detection and investigated the resulting Wazuh file monitoring alert.

[View Lab 4](./4=Malicious-File-Detection/)

## Skills Demonstrated

Wazuh | SIEM | Threat Hunting | Log Analysis | File Integrity Monitoring | Vulnerability Management | SSH Monitoring | Linux | Auditd | Security Alert Investigation