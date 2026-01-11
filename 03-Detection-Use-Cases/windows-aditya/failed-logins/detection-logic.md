# Detection Logic

## Log Source
- Windows Security Event Logs
- Event ID: 4625 (An account failed to log on)

## Key Indicators
- Multiple failed login attempts
- Same user account targeted repeatedly
- Short time interval between attempts

## Detection Method
Wazuh monitors Windows authentication events and triggers alerts when:
- Failed login attempts exceed a defined threshold
- Events occur within a specific time window

## Severity
- Medium: Normal failed login behavior
- High: Brute-force or password spraying behavior

## SOC Analyst Actions
- Identify targeted user accounts
- Check source IP address
- Correlate with RDP or SMB alerts
- Escalate if attack pattern continues
