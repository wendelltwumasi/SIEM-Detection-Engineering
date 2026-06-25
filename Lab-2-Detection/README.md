# Lab 2: Detection Engineering & Brute-Force Correlation

## Objective
To leverage SPL (Splunk Processing Language) to transform raw Windows Event Logs (Event ID 4625) into actionable security alerts.

## Technical Commands
- **Initial Verification Search**:
  `index=main source="WinEventLog:Security" EventCode=4625`
  
- **Brute-Force Detection Query**:
  Aggregated failed login attempts by username to detect high-frequency failure patterns:
```splunk
  index=main source="WinEventLog:Security" EventCode=4625 
  | stats count as FailedAttempts by Account_Name 
  | where FailedAttempts > 10
![Failed Login Statistics](lab2_stats.png)
