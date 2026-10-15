# User Acceptance Testing (UAT) Plan and Results
## AML Transaction Monitoring System Implementation

| Item | Detail |
|---|---|
| UAT window | September 8 to October 10, 2025 (5 weeks) |
| Test lead | Bank test analyst |
| Testers | 8 AML analysts, 3 team leads, 1 compliance reporting officer |
| Observer | Internal Audit |
| Sign off | Linda Okafor (CCO) and Priya Sharma (AML Ops Manager) |

## 1. Objective

Confirm that the system works the way AML analysts and Compliance need it to in day to day work, using realistic data, before it is trusted with live monitoring.

## 2. Entry criteria

* All Sprint 1 to 10 stories accepted by the Product Owner ✔
* System and integration testing complete with no open critical defects ✔
* Test environment loaded with masked production data and the scenario test data set ✔
* Testers trained on the system and the test process ✔
* Test cases approved by the Product Owner ✔

## 3. Exit criteria

* 100% of test cases executed
* Zero open critical or high defects
* Medium defects either fixed or accepted with a workaround by the Product Owner
* Internal Audit confirms controls (maker/checker, audit log, access) work as designed
* Formal sign off by CCO and AML Ops Manager

## 4. Defect severity

| Severity | Meaning | Must be fixed before go live? |
|---|---|---|
| Critical | System unusable or a regulatory requirement fails | Yes |
| High | A key function or control fails, no workaround | Yes |
| Medium | Function works with a workaround | Product Owner decides |
| Low | Cosmetic or minor | No, goes to backlog |

## 5. Test cases

| ID | Area | Test case | Expected result | Result |
|---|---|---|---|---|
| TC01 to TC04 | Structuring | Several cash deposits of $9,000 to $9,999 within 5 days, at one and at several branches | Alert generated with all linked deposits | Pass |
| TC05 to TC07 | Large cash | Single and combined cash of $10,000 or more within 24 hours | LCTR draft created next day | Pass |
| TC08 to TC10 | High risk jurisdictions | Incoming and outgoing wires with listed countries | Alert generated, country shown | Pass |
| TC11 to TC13 | Rapid movement | 80% or more of incoming funds out within 48 hours | Alert generated | Pass (TC12 passed after fix of a medium defect: e-Transfers counted twice) |
| TC14 to TC16 | Profile | Monthly activity over 3 times expected | Alert generated with expected vs actual | Pass |
| TC17 to TC18 | Dormancy | Account dormant 12 months then over $5,000 in 30 days | Alert generated | Pass |
| TC19 | Data | Daily load reconciles to core banking and online banking | Counts and totals match 100% | Pass |
| TC20 | Queue | Alerts sorted by risk score, filters work | Highest score first | Pass |
| TC21 | Investigation | Close alert without rationale | System blocks closure | Pass |
| TC22 | Maker/checker | Analyst tries to approve own closure | Blocked | Pass |
| TC23 | Maker/checker | Admin tries to approve own closure | Blocked | Pass after fix (high defect I05) |
| TC24 | Evidence | Attach PDF, image, email to case | Files saved and viewable | Pass |
| TC25 | STR | Escalate alert to STR and generate draft | All mandatory fields populated or flagged | Pass after fix (medium defect: one field mapped wrongly) |
| TC26 | LCTR | Due date tracker warns at day 10 and day 13 | Warnings shown | Pass |
| TC27 | Access | Each role sees only permitted screens | Matches access design | Pass |
| TC28 | Audit log | Reconstruct a closed alert from the log | Every action shown with user and time | Pass |
| TC29 | Retention | Attempt to delete record before 5 years | Blocked | Pass |
| TC30 | Dashboard | Alert volumes, ageing and false positive rate | Matches underlying data | Pass after fix (low defect: chart label) |

## 6. Results summary

| Measure | Result |
|---|---|
| Test cases executed | 30 of 30 (100%) |
| Passed first time | 26 (87%) |
| Passed after fix | 4 |
| Defects raised | 9 (0 critical, 2 high, 5 medium, 2 low) |
| Defects open at sign off | 1 low (moved to backlog, accepted by Product Owner) |
| Internal Audit controls review | Satisfactory, no findings |

## 7. Sign off

| Name | Role | Decision | Date |
|---|---|---|---|
| Priya Sharma | AML Operations Manager, Product Owner | Accepted | Oct 10, 2025 |
| Linda Okafor | Chief Compliance Officer, Sponsor | Accepted | Oct 10, 2025 |
| Grace Lefebvre | Director, Internal Audit | Observed, no objection | Oct 10, 2025 |
