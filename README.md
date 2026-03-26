# siem-lab-alienvault
SIEM implementation using AlienVault OSSIM for threat detection, correlation rules, and incident response

##Objective
Deploy AlienVault OSSIM, ingest Windows event logs, create correlation rules, and generate incident reports for simulated attack scenarios.


## Tools Used
- AlienVault OSSIM
- Windows Server 2019
- Kali Linux (Hydra for brute-force simulation)
- Wireshark


## Lab Environment
| Component | Configuration |
|-----------|--------------|
| SIEM Server | AlienVault OSSIM (Ubuntu) |
| Windows Endpoint | Windows Server 2019 (AD Controller) |
| Attack Machine | Kali Linux |


## Process
1. Installed OSSIM server and configured sensors
2. Added Windows endpoint as asset
3. Configured syslog forwarding for Windows Security Events
4. Generated brute-force attack using Hydra from Kali
5. Created correlation rule for multiple failed logins
6. Generated incident ticket and report

## Findings
- OSSIM successfully detected brute-force attempt within 2 minutes
- Correlation rule: 10 failed logins from same source within 60 seconds = Medium severity alert
- Incident report documented source IP, target account, and recommended remediation

## Incident Report Sample
```json
{
  "alert_id": "OSSIM-2026-001",
  "severity": "Medium",
  "source_ip": "192.168.1.105",
  "target": "Windows-SRV-01",
  "event": "Multiple failed logins detected",
  "recommendation": "Block source IP, enable account lockout"
}
