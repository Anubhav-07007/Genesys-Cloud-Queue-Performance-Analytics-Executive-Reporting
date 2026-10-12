# Genesys Cloud Queue Performance Analytics

## Overview

This project automates the extraction and reporting of contact center performance metrics from Genesys Cloud.

The solution retrieves queue, agent, and hourly analytics data using Genesys Cloud Analytics APIs and generates a consolidated Excel report for operational and management review.

## Features

### Queue Daily KPI Reporting

Provides daily queue-level performance metrics:

- Offered Calls
- Answered Calls
- Abandoned Calls
- Service Level %
- SLA Target
- Over SLA
- Average Wait Time
- Average Talk Time
- Average ACW
- Average Handle Time

### Agent Performance Reporting

Provides agent-level productivity metrics:

- Agent Name
- Queue Name
- Answered Interactions
- Average Talk Time
- Average ACW
- Average Handle Time

### Hourly Trend Analysis

Provides hourly queue activity data:

- Date
- Hour
- Queue Name
- Offered Calls

Used for:

- Peak Hour Identification
- Workforce Planning
- Capacity Management

---

## Technology Stack

### Programming

- Python 3.x

### Libraries

- requests
- pandas
- openpyxl
- python-dotenv
- pytz

### Data Sources

- Genesys Cloud Analytics API
- Genesys Cloud Users API

### Reporting

- Microsoft Excel
- Power BI (Optional)

---

## Project Structure

```text
Queue_Performance_Analytics
│
├── .env
├── queue_performance.py
├── Queue_Performance_Report.xlsx
├── config
├── logs
├── output
├── reports
└── run_queue_performance.bat
```
### Sheet 1 – Queue_Daily_KPI

| Column |
|----------|
| Queue_Name |
| Date |
| Offered |
| Answered |
| Abandoned |
| Over_SLA |
| SLA_Percent |
| SLA_Target |
| Avg_Wait_Sec |
| Avg_Talk_Sec |
| Avg_ACW_Sec |
| Avg_Handle_Sec |

---

### Sheet 2 – Agent_Performance

| Column |
|----------|
| Date |
| Queue_Name |
| Agent_Name |
| Answered |
| Avg_Talk_Sec |
| Avg_ACW_Sec |
| Avg_Handle_Sec |

---

### Sheet 3 – Hourly_Trend

| Column |
|----------|
| Date |
| Hour |
| Queue_Name |
| Offered |

---

## Installation

Install required packages:

```bash
pip install requests pandas openpyxl python-dotenv pytz
```

---

## Execution

Run the solution:

```bash
python queue_performance.py
```

or

```bash
run_queue_performance.bat
```

---

## Business Benefits

### Operational Visibility

Provides managers with a consolidated view of:

- Queue workload
- Service Level Performance
- Agent productivity
- Hourly demand patterns

### Workforce Planning

Identifies:

- Peak traffic periods
- Staffing requirements
- Queue bottlenecks

### Reporting Automation

Eliminates manual reporting activities and provides a repeatable reporting process.

---

## Future Roadmap

Planned enhancements:

### Phase 2

- Automated Dashboard Generation
- Power BI Integration
- Scheduled Report Execution
- Email Distribution

### Phase 3

- Forecasting Models
- Predictive Staffing Analytics
- Queue Health Scoring
- Real-Time Dashboard Integration
