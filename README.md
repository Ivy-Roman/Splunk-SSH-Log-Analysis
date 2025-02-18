# Splunk SSH Log Analysis & Threat Detection  
**Security Monitoring | Log Analysis | Brute-Force Detection**  

## Overview  
This project focuses on **log analysis, threat detection, and alerting** using **Splunk Cloud**. The objective was to **identify SSH brute-force attack patterns**, configure a **dashboard** and implement **automated alerts** to detect suspicious activity in the future.  

- **Log source:** OpenSSH authentication logs
- **Analysis tool:** Splunk Cloud
- **Threat detected:** Brute-force attack attempt
- **Key outcomes:** Configured alerts, extracted fields, and detected attacker IPs  

---

## Methodology  

### Adding Users to Splunk  
- Created users with **assigned security roles**  
- Configured time zones and enforced **password policies**  

### Log Upload & Security Analysis  
- **Uploaded OpenSSH logs** to Splunk  
- **Analyzed anomalies** such as:  
  - Multiple failed logins  
  - Unusual IPs attempting SSH access  
  - Unauthorized root login attempts  
- **Identified attacker IPs**:  
  - `103.99.0.122` – Repeated failed login attempts  
  - `183.62.140.253` – Authentication failures  

### Dashboard & Alert Configuration  
- Created a **Splunk dashboard** to visualize:  
  - Failed login attempts  
  - Source IPs of attack attempts  
- Configured **an alert** to:  
  - Run **daily at 8 AM**  
  - Trigger if **failed logins > 2**  
  - Send **email alerts** for quick response  

---

## Key Findings  

| Threat Type       | IP Address         | Attack Behavior         | Risk Level |
|------------------|-------------------|------------------------|-----------|
| Brute-Force Attack | 103.99.0.122      | Multiple failed SSH logins | High |
| Unauthorized Access Attempt | 183.62.140.253 | Authentication failures | Medium |
| Unknown Username Access | Various | Attempted login with non-existent user | High |

---

## Remediation & Security Recommendations  
- **Enforce Multi-Factor Authentication (MFA)** for SSH access
- **Restrict SSH access** to trusted IPs using firewall rules
- **Monitor & block suspicious IPs** in real-time
- **Automate security alerting** using SIEM tools (Splunk, Microsoft Defender)  

---
