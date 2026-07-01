# Linux-Log-Analysis-using-Splunk-SIEM
The objective of this project was to collect Linux system logs from a Kali Linux machine, ingest them into Splunk Enterprise, perform log analysis using SPL (Search Processing Language), and visualize security-related events.

## Overview

This project demonstrates the process of collecting Linux system logs from a Kali Linux machine, ingesting them into Splunk Enterprise, performing log analysis using Splunk Search Processing Language (SPL), and visualizing security-related events through interactive dashboards.

The primary objective was to understand how Security Information and Event Management (SIEM) platforms collect, index, search, and analyze log data for monitoring and investigation.

---

## Objectives

- Configure Splunk Enterprise for Linux log analysis.
- Collect system and security-related logs from a Kali Linux machine.
- Import Linux logs into a dedicated Splunk index.
- Analyze log data using SPL queries.
- Visualize important events using dashboards.
- Document findings and observations.

---

## Architecture

```text
        Kali Linux
             │
      Linux Log Files
             │
             ▼
     Splunk Enterprise
             │
      SPL Log Analysis

```

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Kali Linux | Log generation and collection |
| Splunk Enterprise | SIEM platform |
| Linux Journal | System logging |
| SPL | Log analysis |
| GitHub | Project documentation |

---

## Project Workflow

### Phase 1 – Environment Setup

- Installed Splunk Enterprise.
- Configured a dedicated Linux index.
- Verified Splunk web interface.

---

### Phase 2 – Linux Log Collection

Collected the following logs:

- journal.log
- authentication.log
- sudo.log
- passwd.log
- dpkg.log
- alternatives.log
- system_info.txt
- network_info.txt
- kernel_info.txt

---

### Phase 3 – Log Ingestion

Imported all collected logs into Splunk.

Configuration:

- **Index:** linux
- **Host:** kali

After successful ingestion, over **81,000 events** were indexed for analysis.

---

### Phase 4 – Log Analysis

Performed multiple searches using SPL to investigate:

- Authentication events
- Login activity
- Administrative (sudo) activity
- Password changes
- Package installation events
- Event distribution
- Timeline analysis

All queries are available in:

```
spl_queries/queries.md
```

---

### Phase 5 – Findings

Key observations include:

- Linux logs were successfully indexed and searchable.
- Authentication-related events were identified.
- Administrative (sudo) activity was visible.
- Package management events were successfully analyzed.


---

## Repository Structure

```text
Linux-Log-Analysis-Using-Splunk/
│
├── README.md
├── logs/
├── spl_queries/
└── screenshots/
```

---

## Skills Demonstrated

- SIEM Fundamentals
- Splunk Enterprise
- Linux Log Analysis
- Search Processing Language (SPL)
- Log Collection
- Security Event Analysis
- Dashboard Creation
- Cybersecurity Documentation

---

## Future Improvements

- Integrate live log forwarding using the Splunk Universal Forwarder.
- Monitor multiple Linux hosts.
- Create custom alerts for authentication failures.
- Build correlation searches.
- Integrate Windows Event Logs for cross-platform monitoring.

---

## Disclaimer

This project was performed in a personal lab environment using systems owned and managed by the author. It is intended solely for educational and portfolio purposes.
