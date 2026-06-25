# SIEM-Detection-Engineering
"Hands-on cybersecurity project portfolio: SIEM administration, Windows security log ingestion, and SPL detection engineering."
# Cybersecurity Lab Portfolio: Splunk SIEM Operations

## Overview
This repository documents my hands-on experience with Splunk Enterprise, focusing on data ingestion and detection engineering within a Windows environment.

## Lab 1: Splunk Connectivity and Data Ingestion
*Objective: Establish secure log ingestion from a Windows Server to a Splunk SIEM.*
- **Action**: Verified `splunkd` service and configured `inputs.conf` to enable Security log collection.
- **Outcome**: Successfully bridged raw Windows Event Logs to the Splunk indexer.

## Lab 2: Detection Engineering and Correlation
*Objective: Transform raw logs into actionable security intelligence.*
- **Action**: Utilized SPL (Splunk Processing Language) to identify brute-force login patterns (Event ID 4625).
- **Outcome**: Developed a correlation query that successfully flagged high-frequency failed authentication attempts for proactive alerting.
