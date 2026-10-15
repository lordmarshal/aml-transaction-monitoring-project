# Project Charter
## AML Transaction Monitoring System Implementation

| Item | Detail |
|---|---|
| Project ID | PTB-COMP-2025-01 |
| Sponsor | Linda Okafor, Chief Compliance Officer |
| Project Manager | Blessing Adeniyi, PMP |
| Date approved | January 24, 2025 |
| Version | 1.0 |

## 1. Purpose

Replace manual, sample based transaction reviews with an automated AML transaction monitoring system, closing the deficiency raised in the bank's last FINTRAC examination. See the [business case](business_case.md).

## 2. Objectives (SMART)

1. Monitor **100%** of retail and business banking transactions daily by **November 10, 2025**.
2. Deliver the project within the approved budget of **$1.8 million CAD**.
3. Reach an average alert triage time of **5 business days or less** within 3 months of go live.
4. File **100%** of LCTRs within 15 calendar days and STRs as soon as practicable, from go live onward.
5. Train **all 24 AML analysts** and their 3 team leads before go live.

## 3. High level scope

**In scope**
* Selection of a SaaS transaction monitoring vendor through an RFP
* Daily data feeds from core banking: cash, cheques, electronic funds transfers (EFTs) and wire transfers
* Customer KYC and risk rating data feed
* Configuration of six detection scenarios (structuring, rapid movement of funds, high risk jurisdictions, large cash, activity inconsistent with profile, dormant account reactivation)
* Alert case management workflow with maker/checker review
* STR and LCTR preparation support
* User access controls, audit logging and five year record retention
* Training, procedures and a four week parallel run

**Out of scope**
* Credit card transaction monitoring (planned phase 2)
* Sanctions screening (existing tool remains in place)
* Replacement of the core banking system
* Changes to customer onboarding (KYC) processes

## 4. Key milestones

| Milestone | Target date |
|---|---|
| Charter approved | January 24, 2025 |
| Vendor selected and contract signed | March 28, 2025 |
| Project management plan baselined | April 11, 2025 |
| Configuration and integration complete (Sprint 10) | August 29, 2025 |
| UAT sign off | October 10, 2025 |
| Parallel run complete | November 7, 2025 |
| **Go live** | **November 10, 2025** |
| Hypercare ends | December 5, 2025 |
| Project closed | December 19, 2025 |

## 5. Budget

**$1,800,000 CAD** total, made up of a $1,620,000 cost baseline and a $180,000 contingency reserve. Contingency is released by the PM up to $25,000 per item; anything above that needs sponsor approval.

## 6. Success criteria

* All objectives in section 2 met
* UAT completed with zero open critical or high defects
* Internal Audit confirms the audit trail and access controls are adequate
* Sponsor formally accepts the system at project close

## 7. Assumptions

* Core banking can produce a daily transaction extract
* AML Operations can release analysts for UAT (about 30% of their time for 5 weeks)
* A suitable SaaS vendor is available that meets Canadian data residency requirements

## 8. Constraints

* Hard deadline: go live before the end of November 2025 (board commitment to FINTRAC)
* Budget capped at $1.8 million
* Customer data must be stored in Canada
* No production change freeze windows may be breached (December 15 to January 5)

## 9. High level risks

* Data quality issues in core banking
* Vendor delivery delays
* Analyst resistance to change
* Legacy system integration complexity

## 10. Project approach

Hybrid. Initiation, vendor selection and planning follow a predictive approach. Configuration and integration run as ten two week Agile sprints. Testing, parallel run and go live follow a predictive approach with formal sign offs.

## 11. Project manager authority

* Manage the day to day project team and assign work
* Approve spending within the cost baseline and release contingency up to $25,000 per item
* Approve schedule changes that do not move a milestone
* Escalate to the sponsor any change affecting scope, a milestone, or more than $25,000

## 12. Governance

* **Steering Committee** (monthly): CCO (chair), CRO, Head of IT, AML Operations Manager, Project Manager
* **Change Control Board** (as needed): Sponsor, Head of IT, Project Manager
* **Internal Audit:** independent observer with access to all project documents

## 13. Approval

| Name | Role | Decision | Date |
|---|---|---|---|
| Linda Okafor | Chief Compliance Officer, Sponsor | Approved | Jan 24, 2025 |
| David Thompson | Chief Risk Officer | Approved | Jan 24, 2025 |
| Marcus Chen | Head of IT | Approved | Jan 24, 2025 |
| Blessing Adeniyi | Project Manager | Accepted | Jan 24, 2025 |
