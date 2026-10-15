# AML Transaction Monitoring System Implementation

**Portfolio project by Blessing Adeniyi, PMP**

> This is a simulated project built for my professional portfolio. Prairie Trust Bank is a fictional organization, and all names, figures and data are invented. The documents show how I plan, run and close a technology project in an Anti Money Laundering (AML) compliance setting.

## The problem

Prairie Trust Bank, a mid sized Canadian bank with 220,000 customers, reviewed only about **5%** of its 1.2 million monthly transactions, using spreadsheets. A FINTRAC examination flagged this as a deficiency, and the board committed to fixing it within 12 months.

## The solution

Select and implement a Canadian hosted SaaS transaction monitoring system that screens every transaction daily, routes alerts to analysts through a maker/checker case workflow, supports STR and LCTR reporting, and keeps a five year audit trail.

## Results

| Measure | Target | Result |
|---|---|---|
| Transactions monitored | 100% | **100%** (from about 5%) |
| Budget | $1.8M | **$1.705M** (5.3% under) |
| Milestones on baseline date | All | **8 of 8** |
| Average alert triage time | 5 business days or less | **3.1 days** |
| LCTRs filed on time | 100% | **100%** |
| False positive rate | Below 85% | **82%** (from 96% in parallel run) |
| Users trained | 27 | **27** |

## My role

Project Manager and Scrum Master, from business case to closure. Hybrid approach: predictive for initiation, vendor selection, testing and go live; ten two week Agile sprints for configuration and integration.

## Project documents

| Phase | Documents |
|---|---|
| **1. Initiation** | [Business case](01_initiation/business_case.md) · [Project charter](01_initiation/project_charter.md) · [Stakeholder register](01_initiation/stakeholder_register.md) |
| **2. Planning** | [Scope statement](02_planning/scope_statement.md) · [WBS](02_planning/wbs.md) · [RACI](02_planning/raci.md) · [Schedule](02_planning/schedule.md) · [Budget and earned value](02_planning/budget.md) · [Risk register](02_planning/risk_register.md) · [Communications plan](02_planning/communications_plan.md) |
| **3. Agile delivery** | [Product backlog](03_agile/product_backlog.md) · [Jira import CSV](03_agile/jira_backlog_import.csv) · [Sprint plan and velocity](03_agile/sprint_plan.md) · [AML alert workflow](03_agile/aml_alert_workflow.md) · [draw.io source](03_agile/diagrams/aml_alert_workflow.drawio) |
| **4. Execution and control** | [Status report Sprint 4](04_execution/status_reports/status_report_sprint_04.md) · [Status report Sprint 8](04_execution/status_reports/status_report_sprint_08.md) · [Change request CR001](04_execution/change_request_CR001.md) · [Issue log](04_execution/issue_log.md) · [UAT plan and results](04_execution/uat_plan.md) |
| **5. Closing** | [Go live checklist](05_closing/go_live_checklist.md) · [Lessons learned](05_closing/lessons_learned.md) · [Closure report](05_closing/project_closure_report.md) |

## Highlights worth reading

* **Turning a resistant stakeholder into the Product Owner** ([stakeholder register](01_initiation/stakeholder_register.md))
* **Catching a 13% coverage gap mid project and fixing it from contingency with no milestone slip** ([CR001](04_execution/change_request_CR001.md))
* **Cutting false positives from 96% to 82% during the parallel run** ([issue log](04_execution/issue_log.md))
* **Every RACI row with exactly one accountable owner** ([RACI](02_planning/raci.md))

## Skills demonstrated

* Project management: PMI practices, hybrid predictive and Agile delivery, earned value, change control
* AML compliance: transaction monitoring scenarios, alert investigation, maker/checker controls, KYC data, STR and LCTR reporting, PCMLTFA record keeping
* Stakeholder, risk, issue and quality management
* Tools: Jira, Confluence, draw.io, Mermaid
