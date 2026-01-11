# Detection Logic

## Log Source
- Windows Security Event Logs
- Event ID: 4625 (Failed Logon)
- Logon Type: 10 (RemoteInteractive – RDP)

## Key Indicators
- Multiple failed RDP login attempts
- Repeated failures from the same source IP
- Short time interval between attempts

## Detection Method
Wazuh correlates Windows authentication events and generates alerts when:
- Logon failures with Logon Type 10 exceed a defined threshold
- Activity matches brute-force behavior patterns

## Severity
- High: RDP brute-force attacks pose a direct risk of system compromise

## SOC Analyst Actions
- Identify attacking IP address
- Check geolocation and reputation of IP
- Block IP at firewall or endpoint level
- Reset affected user credentials
- Escalate if successful login follows failures
