# 🦠 WarmCookie Malware — Traffic Analysis Exercise
  - Date: 2024-08-15
  - Malware Family: WarmCookie (backdoor/downloader)
  - Source: [malware-traffic-analysis.net](https://malware-traffic-analysis.net)

## Repository Structure
```
 warmcookie-analysis/
├── README.md                   ← You are here
├── report/
│   └── incident-report.md      ← Final incident report (Executive Summary, Victim, IOCs)
├── analysis/
│   └── extracted-files.md
│   └── wireshark-filters.md
├── screeshots/
```

## Background

A Windows host was infected, and it seems to be from WarmCookie malware.

## Lab Scenario
 
| Field | Value |
|---|---|
| LAN Segment | `10.8.15.0/24` |
| Domain | `lafontainebleu.org` |
| AD Controller | `10.8.15.4` — WIN-JEGJIX7Q9RS |
| AD Environment | `LAFONTAINBLEU` |
| Gateway | `10.8.15.1` |

 ---
 
## ⚠️ Disclaimer
 
All files and analysis in this repository are for **educational purposes only**.  
The pcap is intentionally provided for malware traffic analysis training.  
Do **not** connect to any IPs or domains found in this analysis.
 
