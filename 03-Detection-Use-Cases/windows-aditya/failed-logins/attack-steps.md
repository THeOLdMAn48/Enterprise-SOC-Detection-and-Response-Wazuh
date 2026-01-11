# Attack Simulation – Windows Failed Login Attempts

## Objective
To simulate unauthorized login attempts on a Windows endpoint and validate
Wazuh’s ability to detect repeated authentication failures.

## Attack Steps
1. Attacker attempts multiple invalid logins on the Windows lock screen.
2. Windows generates failed authentication events.
3. Wazuh agent collects Windows Security Event Logs.
4. Events are forwarded to the Wazuh Manager.
5. Correlation rules generate alerts for repeated failed login attempts.

## Tools Used
- Windows 10 Lock Screen
- Kali Linux (optional for remote attempts)
