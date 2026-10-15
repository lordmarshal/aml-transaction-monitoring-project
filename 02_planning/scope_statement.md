# Project Scope Statement
## AML Transaction Monitoring System Implementation

Version 1.0, baselined April 11, 2025

## 1. Product scope description

A cloud hosted (SaaS) AML transaction monitoring system, hosted in Canada, that receives daily transaction and customer data from Prairie Trust Bank's core banking system, runs detection scenarios against every transaction, generates alerts, and lets AML analysts investigate, decide and document each alert in one case management tool. The system supports preparation of Suspicious Transaction Reports (STRs) and Large Cash Transaction Reports (LCTRs) for submission to FINTRAC.

## 2. Deliverables

| ID | Deliverable | Acceptance criteria |
|---|---|---|
| D1 | Vendor selection report and signed contract | Contract signed; vendor meets all mandatory RFP requirements including Canadian data residency |
| D2 | Daily data integration (transactions and customers) | Daily load completes by 6:00 a.m. CST; record counts reconcile to core banking at 100% |
| D3 | Six configured detection scenarios | Each scenario passes its UAT test cases; thresholds approved by the CCO |
| D4 | Alert case management workflow | Analyst review and team lead approval (maker/checker) enforced; every decision requires a written rationale |
| D5 | Regulatory reporting support | STR and LCTR drafts generated from case data with all mandatory fields populated |
| D6 | Security and audit controls | Role based access approved by Information Security; full audit log; five year retention |
| D7 | Operating procedures | Updated AML procedures approved by the CCO |
| D8 | Trained users | 24 analysts and 3 team leads complete training and pass a proficiency check |
| D9 | Parallel run report | Four weeks of parallel running with results reviewed and signed off |
| D10 | Production system live | Go live approved by Steering Committee; hypercare complete |

## 3. Exclusions

* Credit card transactions (phase 2)
* Sanctions screening
* Changes to customer onboarding and KYC collection
* Core banking system upgrades
* Automatic electronic filing to FINTRAC (reports are prepared in the system and submitted by Compliance through FINTRAC's existing channel)

## 4. Constraints

* Go live no later than November 2025
* Budget of $1.8 million including contingency
* Customer data must remain in Canada
* No production releases during the December 15 to January 5 freeze

## 5. Assumptions

* Core banking can produce reliable daily extracts
* Analysts are available for UAT and training as planned
* The vendor platform supports Canadian regulatory report formats

## 6. Scope change control

Any change to deliverables, exclusions or acceptance criteria goes through the change request process described in the [change request template](../04_execution/change_request_CR001.md) and is decided by the Change Control Board.
