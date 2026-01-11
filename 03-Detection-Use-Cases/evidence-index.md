# Evidence Index – SOC Detection Use Cases

## Purpose
This document provides a centralized index of all detection use cases,
mapped evidence, and affected endpoints within the Wazuh SOC lab.

The evidence index helps SOC analysts, auditors, and reviewers quickly
identify:
- Which attack occurred
- On which endpoint
- What evidence supports the detection
- Which MITRE ATT&CK techniques are involved

This approach mirrors real-world SOC documentation practices.

---

## Ubuntu – Devang (Linux Endpoint)

### 1. SSH Brute Force
- **Endpoint:** Ubuntu (Devang)
- **Attack Type:** SSH Brute Force
- **MITRE Technique:** T1110 – Brute Force
- **Tactic:** Credential Access
- **Evidence:**
  - Screenshots:  
    `ubuntu-devang/ssh-bruteforce/screenshots/`
  - Logs:  
    `ubuntu-devang/ssh-bruteforce/logs/devang-auth.log`
  - Videos:  
    `ubuntu-devang/ssh-bruteforce/videos/`
- **Outcome:**  
  Successful detection of repeated SSH authentication failures with
  correlated alerts in Wazuh.

---

### 2. Nmap Network Scan Detection
- **Endpoint:** Ubuntu (Devang)
- **Attack Type:** Network Reconnaissance (Nmap)
- **MITRE Techniques:**  
  - T1046 – Network Service Scanning  
  - T1595 – Active Scanning
- **Tactic:** Discovery / Reconnaissance
- **Evidence:**
  - Screenshots:  
    `ubuntu-devang/nmap-scan-detection/screenshots/`
  - Logs (OS-level):  
    `ubuntu-devang/nmap-scan-detection/logs/`
- **Outcome:**  
  Reconnaissance activity detected through abnormal network behavior and
  correlated vulnerability and threat detection logs.

---

## Windows – Aditya (Windows 10 Endpoint)

### 3. Failed Login Attempts
- **Endpoint:** Windows 10 (Aditya)
- **Attack Type:** Failed Authentication Attempts
- **MITRE Technique:** T1110 – Brute Force
- **Tactic:** Credential Access
- **Evidence:**
  - Screenshots:  
    `windows-aditya/failed-logins/screenshots/`
  - Videos:  
    `windows-aditya/failed-logins/videos/aditya-lock-attempts.mp4`
- **Outcome:**  
  Wazuh successfully detected repeated failed logins using Windows Event
  ID 4625 with alert thresholding.

---

### 4. Nmap Network Reconnaissance
- **Endpoint:** Windows 10 (Aditya)
- **Attack Type:** Network Reconnaissance
- **MITRE Techniques:**  
  - T1046 – Network Service Scanning  
  - T1595 – Active Scanning
- **Tactic:** Discovery / Reconnaissance
- **Evidence:**
  - Screenshots:  
    `windows-aditya/nmap-recon/screenshots/`
  - Videos:  
    `windows-aditya/nmap-recon/videos/`
- **Outcome:**  
  Port scanning and service enumeration activity detected and correlated
  with Wazuh threat detection rules.

---

### 5. RDP Brute Force
- **Endpoint:** Windows 10 (Aditya)
- **Attack Type:** RDP Brute Force
- **MITRE Techniques:**  
  - T1110 – Brute Force  
  - T1021.001 – Remote Services: RDP
- **Tactic:** Credential Access / Initial Access
- **Evidence:**
  - Screenshots:  
    `windows-aditya/rdp-bruteforce/screenshots/`
  - Videos:  
    `windows-aditya/rdp-bruteforce/videos/`
- **Outcome:**  
  High-severity alerts generated for repeated RDP authentication failures
  (Logon Type 10), indicating brute-force behavior.

---

## Windows – Jamod (Windows 10 Endpoint)

### 6. RDP Brute Force
- **Endpoint:** Windows 10 (Jamod)
- **Attack Type:** RDP Brute Force
- **MITRE Techniques:**  
  - T1110 – Brute Force  
  - T1021.001 – Remote Services: RDP
- **Tactic:** Credential Access / Initial Access
- **Evidence:**
  - Screenshots:  
    `windows-jamod/rdp-bruteforce/screenshots/`
  - Logs (OS-level):  
    `windows-jamod/rdp-bruteforce/logs/`
  - Reports:  
    `windows-jamod/rdp-bruteforce/reports/`
- **Outcome:**  
  RDP brute-force activity successfully detected and validated through
  correlated authentication failure events.

---

## Notes
- Logs and reports are maintained at the **endpoint (OS) level** and
  reused across detection use cases.
- Screenshots and videos are **attack-specific evidence**.
- This structure reflects real-world SOC investigation and audit workflows.
