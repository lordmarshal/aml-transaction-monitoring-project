# Change Request CR001
## Add Interac e-Transfer Data Feed

| Item | Detail |
|---|---|
| CR number | CR001 |
| Raised by | Blessing Adeniyi, PMP (on behalf of Priya Sharma, AML Ops Manager) |
| Date raised | June 4, 2025 |
| Priority | High |
| Decision body | Change Control Board (Sponsor, Head of IT, Project Manager) |
| Status | **Approved** June 11, 2025 · Delivered July 18, 2025 |

## 1. Description of change

Add a daily data feed from the online banking platform so that Interac e-Transfers are included in transaction monitoring, reconciliation and all relevant detection scenarios.

## 2. Reason for change

During Sprint 4 testing, analysts found that e-Transfers are processed in the online banking platform and are not part of the core banking extract. About 180,000 e-Transfers a month (about 13% of all transactions once included) would not be monitored. Without this change the project cannot meet its main objective of monitoring 100% of transactions, and the FINTRAC deficiency would remain partly open. e-Transfers are also a common channel for moving funds quickly after cash is deposited, which is exactly the pattern the structuring and rapid movement scenarios are designed to catch.

## 3. Impact analysis

| Area | Impact |
|---|---|
| Scope | Adds one data source and two user stories (US08a design, 5 points; US08b build, 8 points). Board level trend reports (US28, 8 points) move to the post go live backlog to make room. |
| Schedule | No milestone impact. Fits into Sprints 6 and 7 by deferring US28. |
| Cost | $80,000: vendor integration services $52,000, internal IT effort $21,000, extra testing $7,000. Funded from contingency ($180,000 available). |
| Quality | Improves coverage from about 87% to 100% of transactions. |
| Risk | New integration with the online banking platform. Mitigated by profiling the data first (Sprint 2 retrospective rule). |
| Resources | Online banking support team needed for about 6 days. Confirmed by Head of IT. |
| Stakeholders | CRO and Internal Audit informed. US28 deferral accepted by CCO. |

## 4. Options considered

| Option | Cost | Outcome |
|---|---|---|
| A. Reject: go live without e-Transfers | $0 | Objective not met; FINTRAC finding partly open. Not acceptable. |
| B. Add after go live as phase 2 | About $95,000 later | 13% of transactions unmonitored for several months; higher cost to remobilize vendor. |
| **C. Add now, defer US28** | **$80,000 from contingency** | **Full coverage at go live, no milestone change.** |

## 5. Recommendation

Option C.

## 6. Decision

| Name | Role | Decision | Date |
|---|---|---|---|
| Linda Okafor | Sponsor | Approved | June 11, 2025 |
| Marcus Chen | Head of IT | Approved | June 11, 2025 |
| Blessing Adeniyi | Project Manager | Recommended | June 11, 2025 |

## 7. Follow up actions

* Update scope statement, backlog, budget and risk register ✔
* Inform Steering Committee at June meeting ✔
* Contingency balance updated: $180,000 → $100,000 ✔
