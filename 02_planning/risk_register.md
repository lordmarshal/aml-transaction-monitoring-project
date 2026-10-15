# Risk Register
## AML Transaction Monitoring System Implementation

Scoring: Probability (P) and Impact (I) rated 1 (very low) to 5 (very high). **Score = P × I.** High: 15 or more · Medium: 8 to 14 · Low: 7 or less.

Status shown as at project closure (December 19, 2025).

| ID | Risk (cause → event → effect) | Category | P | I | Score | Response | Response plan | Owner | Status |
|---|---|---|---|---|---|---|---|---|---|
| R01 | Incomplete customer data in core banking → poor alert quality → high false positives and missed risk | Data | 4 | 5 | **20** | Mitigate | Data profiling in Sprint 2; data cleansing with KYC team; reconciliation controls on every load | IT Integration Lead | Occurred (see issue I02). Closed. |
| R02 | Vendor misses delivery dates → sprint goals slip → go live delayed | Vendor | 3 | 5 | **15** | Mitigate | Delivery milestones and penalties in contract; vendor attends all sprint ceremonies; weekly delivery review | Project Manager | Closed. Did not occur. |
| R03 | Analysts fear the new system or alert volumes → low adoption, workarounds | People | 4 | 4 | **16** | Mitigate | AML Ops Manager as Product Owner; super user group; early demos; alert tuning workstream | AML Ops Manager | Closed. Adoption 100%. |
| R04 | Legacy core banking cannot produce some data → missing transaction types | Technical | 3 | 4 | 12 | Mitigate | Full data source inventory in Sprint 1; spike on extract feasibility | Head of IT | Occurred (Interac e-Transfers, see CR001). Closed. |
| R05 | Too many false positive alerts at go live → backlog builds, triage target missed | Operational | 4 | 4 | **16** | Mitigate | Threshold tuning during 4 week parallel run; CCO approves thresholds; temporary overtime budget | AML Ops Manager | Closed. FP fell from 96% to 82%. |
| R06 | Data residency rules not met → security approval refused | Compliance | 2 | 5 | 10 | Avoid | Canadian hosting made a mandatory RFP requirement | Information Security | Closed. |
| R07 | Analysts unavailable for UAT due to normal workload → UAT delayed | Resource | 3 | 3 | 9 | Mitigate | UAT time agreed with AML Ops Manager in advance; temporary backfill from Compliance | Project Manager | Closed. |
| R08 | Key project staff leave → knowledge loss | Resource | 2 | 4 | 8 | Mitigate | Documentation in Confluence; pair working on integration | Project Manager | Closed. |
| R09 | Security weakness found late → go live delayed | Security | 2 | 4 | 8 | Mitigate | Penetration test scheduled in Sprint 9, leaving time to fix | Information Security | Closed. 2 medium findings fixed. |
| R10 | Regulatory guidance changes during the project → rework | Regulatory | 2 | 3 | 6 | Accept | Compliance monitors FINTRAC updates; contingency covers small changes | Sponsor | Closed. |
| R11 | Go live clashes with December change freeze → forced delay to January | Schedule | 2 | 5 | 10 | Avoid | Go live set for November 10, five weeks before freeze | Project Manager | Closed. |
| R12 | Vendor platform outperforms expectations → capacity to add credit cards early | Opportunity | 2 | 3 | 6 | Exploit | Assess during hypercare for phase 2 business case | Sponsor | Passed to phase 2. |

## Top risks at baseline (April 2025)

1. **R01** Data quality (20)
2. **R03** Analyst adoption (16)
3. **R05** False positive volume (16)
4. **R02** Vendor delays (15)

These four were reviewed at every sprint review and every Steering Committee meeting.
