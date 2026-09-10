# Lab 4 – Malicious File Detection

## Objective

Simulate malware detection using the safe EICAR test file and investigate the resulting security event.

## Tools

- Wazuh SIEM
- Ubuntu Linux
- File Integrity Monitoring
- EICAR test file

## Investigation

The EICAR test file was introduced into the monitored environment.

Wazuh detected the file activity through File Integrity Monitoring.

## Evidence

![EICAR Test](./screenshots/eicar-file.png)

![Wazuh Alert](./screenshots/wazuh-file-alert.png)

## SOC Skills Demonstrated

- Malware detection simulation
- File Integrity Monitoring
- Alert investigation
- Endpoint monitoring