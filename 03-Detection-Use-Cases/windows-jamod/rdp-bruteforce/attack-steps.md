# Attack Simulation – RDP Brute Force

## Objective
To simulate an RDP brute-force attack against a Windows endpoint and
validate Wazuh’s ability to detect repeated authentication failures
over the RDP service.

## Attack Steps
1. Attacker system (Kali Linux) attempts multiple RDP login attempts
   using invalid credentials.
2. Windows generates authentication failure events for RDP logons.
3. Wazuh agent collects Windows Security Event Logs.
4. Events are forwarded to the Wazuh Manager.
5. Correlation rules trigger alerts for repeated RDP authentication failures.

## Tools Used
- Kali Linux
- RDP client / brute-force technique
