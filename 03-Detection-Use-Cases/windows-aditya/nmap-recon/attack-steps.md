# Attack Simulation – Nmap Network Scanning

## Objective
To simulate Nmap-based reconnaissance against a Windows endpoint and validate
Wazuh’s ability to detect suspicious network scanning behavior.

## Attack Steps
1. Attacker system (Kali Linux) performs Nmap scans against the Windows host.
2. Nmap generates multiple connection attempts across various ports.
3. Windows records network and service-related activity.
4. Wazuh agent collects relevant Windows events and logs.
5. Wazuh Manager correlates scanning patterns.
6. Alerts are generated for suspicious reconnaissance behavior.

## Tools Used
- Kali Linux
- Nmap
