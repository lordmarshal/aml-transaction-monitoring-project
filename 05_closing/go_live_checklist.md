# Go Live Readiness Checklist
## AML Transaction Monitoring System Implementation

Go/no go meeting: **November 7, 2025**, 2:00 p.m. CST · Go live: **Monday, November 10, 2025**

## Readiness criteria

| # | Area | Criterion | Evidence | Owner | Status |
|---|---|---|---|---|---|
| 1 | Testing | UAT signed off, no open critical or high defects | [UAT results](../04_execution/uat_plan.md) | Test Lead | ✔ Ready |
| 2 | Testing | Parallel run complete, results reviewed | Parallel run report, issue I06 | AML Ops Manager | ✔ Ready |
| 3 | Data | Daily load reconciled 100% for 20 consecutive business days | Reconciliation reports | IT Integration Lead | ✔ Ready |
| 4 | Scenarios | Final thresholds approved by CCO | Threshold approval memo | AML Ops Manager | ✔ Ready |
| 5 | Security | Penetration test findings fixed; security approval granted | Security sign off | Information Security | ✔ Ready |
| 6 | Access | All 27 users set up with correct roles; access review done | Access review report | Information Security | ✔ Ready |
| 7 | Controls | Internal Audit confirms maker/checker, audit log and retention | Audit memo | Internal Audit | ✔ Ready |
| 8 | People | 24 analysts and 3 team leads trained and passed proficiency check | Training records | Training Lead | ✔ Ready |
| 9 | Process | Updated AML procedures approved and published | Procedure v3.0 | Compliance Policy Lead | ✔ Ready |
| 10 | Support | Hypercare rota agreed (vendor, IT, super users); escalation contacts published | Hypercare plan | Project Manager | ✔ Ready |
| 11 | Rollback | Rollback plan tested: return to manual sampling within 1 business day if needed | Rollback test record | Head of IT | ✔ Ready |
| 12 | Comms | Go live announcement approved and scheduled | Email and intranet draft | Sponsor | ✔ Ready |
| 13 | Calendar | Go live is outside the December 15 to January 5 change freeze | Change calendar | Head of IT | ✔ Ready |

## Cutover plan

| When | Step | Owner |
|---|---|---|
| Fri Nov 7, 5:00 p.m. | Final parallel run review complete; manual sampling continues as backup | AML Ops Manager |
| Sat Nov 8 | Production configuration frozen; final threshold settings loaded | Vendor |
| Sun Nov 9, 10:00 p.m. | First production load runs | IT Integration Lead |
| Mon Nov 10, 6:00 a.m. | Load and reconciliation confirmed | IT Integration Lead |
| Mon Nov 10, 8:00 a.m. | Analysts start working alerts in the new system | AML Ops Manager |
| Mon Nov 10, 4:00 p.m. | Day 1 checkpoint with sponsor | Project Manager |
| Nov 10 to Dec 5 | Hypercare: daily 15 minute check in | Project Manager |

## Decision

| Name | Role | Vote |
|---|---|---|
| Linda Okafor | Sponsor | Go |
| Marcus Chen | Head of IT | Go |
| Priya Sharma | AML Operations Manager | Go |
| Tom Reyes | Information Security | Go |
| David Thompson | Chief Risk Officer | Go |

**Outcome: GO.** Recorded by Blessing Adeniyi, PMP.
