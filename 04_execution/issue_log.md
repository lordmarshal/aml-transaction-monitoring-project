# Issue Log
## AML Transaction Monitoring System Implementation

An issue is something that **has happened** and needs action. Risks that occurred are linked to their risk ID.

| ID | Date raised | Issue | Linked risk | Impact | Severity | Owner | Action taken | Date closed | Status |
|---|---|---|---|---|---|---|---|---|---|
| I01 | Apr 15, 2025 | Vendor test environment ready 3 days late | R02 | Sprint 1 integration work started late | Medium | Vendor PM | Team worked on data mapping first; vendor added a consultant for 1 week. Sprint 1 goal still met. | Apr 25, 2025 | Closed |
| I02 | May 2, 2025 | 3.2% of customer records missing occupation or risk rating | R01 | Profile scenarios would generate false alerts; Sprint 2 goal only partly met | High | IT Integration Lead | Data cleansing story (US32) with KYC team in Sprint 3. Missing records reduced to 0.4%. Ongoing data quality check added to daily load. | May 23, 2025 | Closed |
| I03 | Jun 3, 2025 | Interac e-Transfers not in core banking extract | R04 | About 13% of transactions unmonitored | High | Project Manager | CR001 raised and approved. Feed delivered Sprint 7. | Jul 18, 2025 | Closed |
| I04 | Aug 14, 2025 | Penetration test found 2 medium findings (session timeout too long; verbose error messages) | R09 | Security approval for go live at risk | Medium | Information Security | Vendor fixed both in Sprint 10 (US26); retest passed. | Aug 28, 2025 | Closed |
| I05 | Sep 17, 2025 | UAT defect: an admin user could approve their own alert closure, bypassing maker/checker | | Control weakness; Internal Audit would not sign off | High | Vendor | Rule changed so nobody, including admins, can approve their own work. Retested and confirmed by Internal Audit. | Sep 24, 2025 | Closed |
| I06 | Oct 21, 2025 | Parallel run week 1: false positive rate 96%, about 210 alerts a day | R05 | Analysts could not keep up; triage target at risk | High | AML Ops Manager | Tuning in weeks 2 to 4: excluded payroll deposits and recurring bill payments from the profile scenario, and suppressed repeat alerts on the same customer and pattern within 30 days. Fell to 82%, about 105 alerts a day. All changes approved by CCO and logged. | Nov 7, 2025 | Closed |
| I07 | Nov 12, 2025 | Hypercare: daily load finished at 6:40 a.m. on two days after go live | | Analysts started late | Low | IT Integration Lead | Extract start moved 45 minutes earlier. Load completes by 5:30 a.m. since. | Nov 19, 2025 | Closed |

**Summary:** 7 issues raised, 7 closed. None affected a milestone.
