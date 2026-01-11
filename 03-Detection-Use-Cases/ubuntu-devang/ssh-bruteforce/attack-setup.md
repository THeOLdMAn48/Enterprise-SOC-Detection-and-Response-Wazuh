# Attack Simulation – SSH Brute Force

## Objective
To simulate an SSH brute-force attack against an Ubuntu system and validate
Wazuh’s ability to detect repeated authentication failures.

## Attack Steps
1. Attacker system (Kali Linux) attempts multiple SSH logins using invalid credentials.
2. Ubuntu system records failed authentication attempts in `auth.log`.
3. Wazuh agent on Ubuntu collects authentication logs.
4. Logs are forwarded to the Wazuh Manager.
5. Correlation rules trigger an alert for excessive failed SSH attempts.

## Tools Used
- Kali Linux
- SSH client / brute-force technique
