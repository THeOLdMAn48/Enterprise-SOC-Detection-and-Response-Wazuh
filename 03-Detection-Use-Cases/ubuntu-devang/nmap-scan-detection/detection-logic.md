# Detection Logic

## Log Sources
- Network-related system logs
- Service access logs
- Wazuh vulnerability detection and threat detection logs

## Key Indicators
- Multiple connection attempts to different ports
- Rapid scanning behavior from a single source
- Abnormal spike in network-related events

## Detection Method
Wazuh correlates multiple events indicating:
- High-frequency port access attempts
- Sequential probing of services
- Reconnaissance patterns consistent with Nmap scans

## Severity
- Medium → Initial reconnaissance activity
- High → Aggressive or repeated scanning attempts

## SOC Analyst Actions
- Identify scanning source IP
- Verify if scan is authorized or internal
- Block or rate-limit malicious IPs
- Monitor for follow-up exploitation attempts
