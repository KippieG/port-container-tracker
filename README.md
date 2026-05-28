# 🚢 Port Container Tracker

> A full-stack application for monitoring, analysing, and reporting on container terminal operations — built to demonstrate end-to-end IT Analyst–Developer skills.

---

## Why this project?

Container terminals like CSP Zeebrugge run on real-time data: vessel arrivals, container movements, gate transactions, and KPI dashboards for operations teams. This project simulates a **Terminal Operations Support System** — the kind of internal tooling that sits alongside a TOS (Terminal Operating System) like Navis N4.

It covers the full stack required for the role:

| Requirement (vacancy) | Demonstrated here |
|---|---|
| Java / Groovy development | REST API in Java + Groovy data transformer |
| JavaScript / HTML / CSS | Interactive dashboard frontend |
| Python | Data analysis & automated reporting scripts |
| SQL / Oracle | Schema design + analytical queries |
| Git | This repo — branching, commits, PRs |
| BI reporting | KPI dashboard with Chart.js |
| Process analysis | `/docs/process-analysis.md` |
| Data warehouse | Star schema design in `/sql/` |
| End-user focus | UI built around operations team workflows |

---

## Project structure

```
port-container-tracker/
│
├── frontend/               # Browser dashboard (HTML + JS + CSS)
│   ├── index.html          # Main KPI dashboard
│   ├── app.js              # Dashboard logic & Chart.js visualisations
│   └── style.css           # Terminal operations UI styling
│
├── backend/                # Java REST API (Spring Boot)
│   ├── ContainerService.java
│   ├── VesselController.java
│   └── GateTransactionGroovy.groovy   # Groovy data transformer
│
├── data-analysis/          # Python analysis scripts
│   ├── dwell_time_analysis.py         # Container dwell time stats
│   ├── throughput_forecast.py         # Weekly TEU forecasting
│   └── report_generator.py           # Automated PDF/CSV reporting
│
├── sql/                    # Oracle SQL — schema + queries
│   ├── schema.sql                     # Star schema (data warehouse)
│   ├── kpi_queries.sql                # Operational KPI queries
│   └── sample_data.sql                # Realistic test data
│
└── docs/
    ├── process-analysis.md            # AS-IS / TO-BE analysis
    ├── architecture.md                # System design decisions
    └── user-stories.md                # End-user requirements
```

---

## Tech stack

- **Backend:** Java 17, Spring Boot, Groovy
- **Frontend:** Vanilla JavaScript, HTML5, CSS3, Chart.js
- **Data analysis:** Python 3.11, pandas, matplotlib, reportlab
- **Database:** Oracle SQL (compatible with PostgreSQL for local dev)
- **Version control:** Git, GitHub Actions CI

---

## Getting started

### Frontend (no install needed)
```bash
# Just open in browser
open frontend/index.html
```

### Python analysis
```bash
pip install pandas matplotlib reportlab
python data-analysis/dwell_time_analysis.py
```

### Backend (Java)
```bash
# Requires Java 17 + Maven
mvn spring-boot:run
# API runs on http://localhost:8080
```

---

## Key features

### 1. Live KPI Dashboard
Real-time view of terminal performance: TEU throughput, vessel turnaround time, gate transaction volume, and yard occupancy — the metrics an operations team actually monitors.

### 2. Container Dwell Time Analysis
Python script that identifies containers exceeding target dwell times, flags them by priority, and generates an automated daily report — reducing manual follow-up work.

### 3. Vessel Turnaround Reporting
SQL queries against a star schema data warehouse to track port-call performance over time. Designed to feed directly into a BI tool (Power BI, Tableau, or similar).

### 4. Gate Transaction Processor (Groovy)
Groovy transformer that validates and normalises incoming truck gate data before it enters the TOS — the kind of integration work typical in a terminal IT environment.

---

## Process analysis example

See [`/docs/process-analysis.md`](/docs/process-analysis.md) for a full AS-IS → TO-BE analysis of a manual container release process — converted into an automated workflow, with requirements elicitation notes and a proposed data model.

---

## About

Built as a portfolio project demonstrating full-stack IT Analyst–Developer skills relevant to port terminal environments. The domain knowledge is based on publicly available information about container terminal operations, Navis TOS architecture, and standard port KPIs.

**Contact:** [your-email@example.com] | [linkedin.com/in/yourprofile]
