# Detection Logic

## Log Source
- File: `/var/log/auth.log`
- Platform: Ubuntu Linux

## Key Indicators
- Multiple failed SSH login attempts
- Repeated authentication failures
- Same source IP or rapid attempts across users

## Detection Method
Wazuh monitors Linux authentication logs and triggers alerts when:
- SSH authentication failures exceed a defined threshold
- Events occur within a short time window

## Severity
- Medium → Initial brute-force behavior
- High → Sustained or aggressive brute-force attempts

## SOC Analyst Actions
- Identify source IP address
- Check if IP is internal or external
- Block source if malicious
- Escalate if persistence is observed
