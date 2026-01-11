# Detection Logic

## Log Sources
- Windows system and security logs
- Network-related event logs
- Wazuh threat detection and vulnerability detection logs

## Key Indicators
- Multiple connection attempts to different ports
- Rapid sequential probing of services
- Abnormal spike in network-related events

## Detection Method
Wazuh detects reconnaissance behavior by correlating:
- High-frequency connection attempts
- Port enumeration patterns
- Known scanning signatures

## Severity
- Medium: Initial reconnaissance activity
- High: Aggressive or repeated scanning attempts

## SOC Analyst Actions
- Identify source IP performing scans
- Verify if scan is internal or authorized
- Block or rate-limit malicious IPs
- Monitor endpoint for follow-up exploitation attempts
