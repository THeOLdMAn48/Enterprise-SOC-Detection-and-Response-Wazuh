# Attack Simulation – Nmap Network Scanning

## Objective
To simulate Nmap-based reconnaissance against an Ubuntu system and validate
Wazuh’s ability to detect abnormal network scanning behavior.

## Attack Steps
1. Attacker system (Kali Linux) performs Nmap scans against the Ubuntu host.
2. Nmap generates multiple connection attempts across different ports.
3. Ubuntu system logs network and service activity.
4. Wazuh agent collects relevant logs and events.
5. Wazuh manager analyzes patterns indicating port scanning behavior.
6. Alerts are generated for suspicious scanning activity.

## Tools Used
- Kali Linux
- Nmap