# Lab 3 – SSH Brute-Force Detection

📌 Project Overview

This project demonstrates how to detect repeated failed SSH login attempts on a Linux machine using Wazuh SIEM.

The objective was to simulate SSH password-guessing activity in a controlled home lab, monitor authentication logs, and verify that Wazuh detects suspicious login attempts.

🎯 Objective

Simulate failed SSH login attempts.

Monitor Linux authentication logs.

Detect SSH authentication failures using Wazuh.

Investigate security alerts and identify the source IP address.

Understand how SOC analysts investigate possible brute-force attacks.

🛠️ Tools & Technologies

Wazuh SIEM 4.14.7

Ubuntu Linux

Kali Linux

OpenSSH

Wazuh Agent

Wazuh Manager

Docker

🖥️ Lab Environment

Machine

Role

IP Address

Kali Linux

Attacker

192.168.177.139

Ubuntu Linux

Target

192.168.177.137

Target username: socuser

⚙️ Implementation

1. Prepared the Linux machines

Configured Kali Linux as the testing machine and Ubuntu Linux as the SSH target.

2. Connected through SSH

Used the following command from Kali Linux:

ssh socuser@192.168.177.137

3. Generated failed login attempts

Entered an incorrect password three times to simulate repeated SSH authentication failures.

4. Monitored authentication logs

Checked failed login attempts on Ubuntu:

sudo grep "Failed password" /var/log/auth.log

Monitored authentication events in real time:

sudo tail -f /var/log/auth.log

5. Verified Wazuh alerts

Checked the Wazuh Manager alert file:

sudo docker exec single-node-wazuh.manager-1 \
grep '"id":"5760"' /var/ossec/logs/alerts/alerts.json

🚨 Detection Results

Wazuh successfully detected the failed SSH authentication attempts.

Alert Field

Detected Value

Rule ID

5760

Rule Level

5

Description

sshd: authentication failed.

Agent Name

ubuntuu

Agent ID

001

Source IP

192.168.177.139

Target Username

socuser

## SOC Skills Demonstrated

- Authentication monitoring
- Brute-force detection
- Log analysis
- Alert investigation
- Threat hunting
