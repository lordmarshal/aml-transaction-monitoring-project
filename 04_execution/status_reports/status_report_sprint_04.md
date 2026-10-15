# Project Status Report: Sprint 4
## AML Transaction Monitoring System Implementation

| Item | Detail |
|---|---|
| Reporting period | May 26 to June 6, 2025 |
| Prepared by | Blessing Adeniyi, PMP |
| Distribution | Steering Committee, Internal Audit |

## Overall status: 🟠 AMBER

A gap in scope was found: Interac e-Transfers are not in the core banking extract. A change request (CR001) has been raised. Schedule and budget are currently on track, but the project is amber until the Change Control Board decides on CR001.

| Area | Status | Comment |
|---|---|---|
| Scope | 🟠 Amber | Interac e-Transfers missing from data feed. CR001 raised June 4. |
| Schedule | 🟢 Green | All milestones on track. Sprint 4 goal met. |
| Budget | 🟢 Green | Spend $905,000 vs plan $910,000. |
| Risks | 🟠 Amber | R04 (missing data) has occurred. |
| Quality | 🟢 Green | Structuring and large cash scenarios passed all test cases. |
| Stakeholders | 🟢 Green | AML Ops Manager now actively championing the project. |

## Completed this sprint

* Structuring scenario (US10) configured and passed test cases TC01 to TC04
* Large cash scenario (US11) configured and passed TC05 to TC07
* Scenario test data set (US33) built
* Threshold change screen with CCO approval (US34) delivered
* 23 of 23 committed story points completed

## Planned next sprint (Sprint 5, June 9 to 20)

* High risk jurisdiction wires (US12) and rapid movement of funds (US13)
* Alert risk scoring (US36) and high risk country list (US35)
* Change Control Board decision on CR001

## Key issue

**I03: Interac e-Transfers not monitored.** While testing the structuring scenario, analysts noticed that customers who split cash often moved it on by Interac e-Transfer. These transactions sit in the online banking platform, not core banking, so they are not in the feed. About 180,000 e-Transfers a month (15% of volume) would go unmonitored, which would not meet the objective of 100% coverage. See [CR001](../change_request_CR001.md).

## Decisions needed

| Decision | From | By |
|---|---|---|
| Approve CR001: add Interac e-Transfer feed ($80,000 from contingency) | Change Control Board | June 11, 2025 |

## Top risks

| ID | Risk | Score | Trend | Action this period |
|---|---|---|---|---|
| R01 | Data quality | 20 | ⬇ Falling | Cleansing complete; records missing data down from 3.2% to 0.4% |
| R05 | False positive volume | 16 | ➡ Stable | Tuning plan agreed for parallel run |
| R04 | Missing data source | 12 | Occurred | Converted to issue I03 and CR001 |
| R02 | Vendor delays | 15 | ⬇ Falling | Vendor has met every sprint commitment so far |
