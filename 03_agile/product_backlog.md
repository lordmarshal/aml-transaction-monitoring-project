# Product Backlog
## AML Transaction Monitoring System Implementation

Product Owner: Priya Sharma, AML Operations Manager · Scrum Master: Blessing Adeniyi, PMP

Stories follow the format **As a [role], I want [feature], so that [benefit].** Points use the Fibonacci scale (1, 2, 3, 5, 8, 13).

A Jira ready version of this backlog is in [jira_backlog_import.csv](jira_backlog_import.csv) (Jira: Settings > System > External System Import > CSV).

## Epics

| Epic | Name | Stories | Points |
|---|---|---|---|
| E1 | Data Integration | 13 | 84 |
| E2 | Detection Scenarios | 11 | 68 |
| E3 | Alert Case Management | 5 | 26 |
| E4 | Regulatory Reporting | 2 | 16 |
| E5 | Security and Access | 5 | 26 |
| E6 | Dashboards and Readiness | 3 | 21 |
| | **Total** | **39** | **241** |

## Definition of Done

* Acceptance criteria met and demonstrated at sprint review
* Tested in the test environment with test cases recorded in Jira
* No open critical or high defects
* Audit logging confirmed for any new user action
* Product Owner accepts the story

## E1: Data Integration

| ID | User story | Acceptance criteria | Points | Priority | Sprint |
|---|---|---|---|---|---|
| US01 | As the IT Integration Lead, I want a secure file transfer connection to the vendor, so that customer data is protected in transit. | Encrypted SFTP connection tested both ways; keys stored in the bank vault; Information Security approves. | 5 | Highest | 1 |
| US02 | As an AML analyst, I want every daily transaction extracted from core banking, so that nothing escapes monitoring. | Extract covers cash, cheques, EFTs and wires; runs nightly; file lands by 4:00 a.m. CST. | 8 | Highest | 1 |
| US03 | As the vendor, I want transaction fields mapped to our data model, so that scenarios read the right values. | Mapping document signed off by IT and AML Ops; all mandatory fields mapped. | 8 | Highest | 1 |
| US04 | As an AML analyst, I want customer KYC and risk rating data loaded, so that alerts reflect who the customer is. | Customer type, occupation, risk rating and expected activity loaded daily. | 8 | Highest | 2 |
| US05 | As the AML Ops Manager, I want a data quality profiling report, so that we know where data gaps will cause false alerts. | Report shows completeness for every mandatory field; gaps over 1% flagged. | 5 | High | 2 |
| US06 | As Internal Audit, I want record counts reconciled on every load, so that I can prove all transactions were monitored. | Counts and totals match core banking at 100%; any break raises an alert to IT. | 5 | Highest | 2 |
| US07 | As an AML analyst, I want the daily load fully automated, so that alerts are ready when I start work. | Load completes by 6:00 a.m. CST on 10 consecutive test days. | 8 | Highest | 3 |
| US30 | As IT Support, I want failed loads to retry and notify us, so that problems are fixed before analysts arrive. | Automatic retry once; on second failure email and page on call support. | 5 | High | 3 |
| US31 | As IT Support, I want a load monitoring view, so that I can see each day's status at a glance. | Shows load time, record count and status for the last 30 days. | 3 | Medium | 3 |
| US32 | As the KYC team, I want incomplete customer records cleansed, so that profile based scenarios work. | Records missing occupation or risk rating reduced from 3.2% to under 0.5%. | 8 | High | 3 |
| US08a | As an AML analyst, I want Interac e-Transfer data designed into the feed (CR001), so that e-Transfers are monitored. | Data source, mapping and extract design approved. | 5 | Highest | 6 |
| US08b | As an AML analyst, I want Interac e-Transfer data loaded daily (CR001), so that no transaction type is missed. | e-Transfers included in daily load and reconciliation at 100%. | 8 | Highest | 7 |
| US09 | As an AML analyst, I want 13 months of history loaded, so that profile and dormancy scenarios work from day one. | 13 months loaded and reconciled. | 8 | High | 10 |

## E2: Detection Scenarios

| ID | User story | Acceptance criteria | Points | Priority | Sprint |
|---|---|---|---|---|---|
| US10 | As an AML analyst, I want structuring detected, so that I can spot customers splitting cash to avoid reporting. | Alert when 2 or more cash deposits of $9,000 to $9,999 each occur within 5 days; passes test cases TC01 to TC04. | 8 | Highest | 4 |
| US11 | As a compliance reporting officer, I want large cash transactions flagged, so that LCTRs are never missed. | Flags $10,000 or more in cash within a 24 hour period, single or combined; passes TC05 to TC07. | 5 | Highest | 4 |
| US33 | As the test lead, I want a scenario test data set, so that every scenario can be tested repeatably. | Synthetic data set with known expected alerts for every scenario. | 5 | High | 4 |
| US34 | As the AML Ops Manager, I want scenario thresholds editable with approval, so that we can tune without vendor help. | Threshold change needs CCO approval in system; every change logged. | 5 | High | 4 |
| US12 | As an AML analyst, I want wires to or from high risk jurisdictions flagged, so that I can review cross border risk. | Flags wires involving countries on the bank's high risk list; passes TC08 to TC10. | 8 | Highest | 5 |
| US13 | As an AML analyst, I want rapid movement of funds detected, so that I can spot pass through accounts. | Flags when 80% or more of incoming funds leave within 48 hours, over $5,000; passes TC11 to TC13. | 8 | High | 5 |
| US35 | As the AML Ops Manager, I want to maintain the high risk country list, so that it stays current. | List editable by authorized users only; changes logged. | 3 | Medium | 5 |
| US36 | As an AML analyst, I want each alert risk scored, so that I work the riskiest alerts first. | Score from 1 to 100 based on scenario, amount and customer risk rating. | 8 | High | 5 |
| US14 | As an AML analyst, I want activity inconsistent with the customer profile flagged, so that unusual behaviour stands out. | Flags monthly activity over 3 times expected activity; passes TC14 to TC16. | 8 | High | 6 |
| US15 | As an AML analyst, I want dormant accounts that suddenly reactivate flagged, so that I can check for account takeover or misuse. | Flags accounts inactive 12 months or more with over $5,000 activity in 30 days; passes TC17 to TC18. | 5 | High | 6 |
| US37 | As an AML analyst, I want expected activity fields from KYC used in scoring, so that profile alerts are accurate. | Expected monthly volume and value loaded and used by US14. | 5 | High | 6 |

## E3: Alert Case Management

| ID | User story | Acceptance criteria | Points | Priority | Sprint |
|---|---|---|---|---|---|
| US16 | As an AML analyst, I want an alert queue sorted by risk score, so that I always know what to work next. | Queue filters by scenario, score, age and analyst. | 5 | Highest | 7 |
| US17 | As an AML analyst, I want to investigate and close alerts with a written rationale, so that every decision is documented. | Alert cannot close without rationale of at least 50 characters and a disposition code. | 8 | Highest | 7 |
| US18 | As a team lead, I want to approve analyst decisions (maker/checker), so that no alert is closed by one person alone. | Analyst cannot approve own work; team lead approval required for every closure. | 5 | Highest | 7 |
| US19 | As an AML analyst, I want to attach documents and notes to a case, so that all evidence is in one place. | Upload PDF, image and email files up to 20 MB each. | 3 | Medium | 8 |
| US20 | As an AML analyst, I want to escalate an alert to an STR case, so that suspicious activity is reported. | Escalation creates STR case linked to all related alerts. | 5 | Highest | 8 |

## E4: Regulatory Reporting

| ID | User story | Acceptance criteria | Points | Priority | Sprint |
|---|---|---|---|---|---|
| US21 | As a compliance reporting officer, I want an STR draft generated from case data, so that reports are fast and complete. | All mandatory FINTRAC STR fields populated or flagged as missing. | 8 | Highest | 8 |
| US22 | As a compliance reporting officer, I want LCTR drafts with a due date tracker, so that every LCTR is filed within 15 calendar days. | Draft generated next day; tracker warns at day 10 and day 13. | 8 | Highest | 8 |

## E5: Security and Access

| ID | User story | Acceptance criteria | Points | Priority | Sprint |
|---|---|---|---|---|---|
| US23 | As Information Security, I want role based access, so that people see only what their job needs. | Roles: analyst, team lead, manager, auditor (read only), admin; approved by InfoSec. | 8 | Highest | 9 |
| US24 | As Internal Audit, I want every user action logged, so that I can reconstruct any decision. | Log shows who, what, when for every view, edit, approval; cannot be edited. | 5 | Highest | 9 |
| US25 | As the CCO, I want records kept for at least five years, so that we meet PCMLTFA record keeping rules. | Retention rule set to 5 years from case closure; deletion only after expiry. | 5 | Highest | 9 |
| US38 | As Information Security, I want vendor support during the penetration test, so that findings are understood quickly. | Test completed; findings logged in Jira. | 3 | High | 9 |
| US26 | As Information Security, I want penetration test findings fixed, so that the system is safe to go live. | Both medium findings fixed and retested. | 5 | Highest | 10 |

## E6: Dashboards and Readiness

| ID | User story | Acceptance criteria | Points | Priority | Sprint |
|---|---|---|---|---|---|
| US27 | As the AML Ops Manager, I want a dashboard of alert volumes, ageing and false positive rate, so that I can manage workload. | Dashboard refreshes daily; drill down by scenario and analyst. | 8 | High | 10 |
| US29 | As the Training Lead, I want a training sandbox with sample data, so that analysts can practise safely. | Sandbox with masked data available to all 27 users. | 5 | High | 10 |
| US28 | As the CCO, I want board level trend reports, so that I can report AML performance to the board. | Monthly trend report by scenario. Deferred to post go live under CR001. | 8 | Medium | Deferred |
