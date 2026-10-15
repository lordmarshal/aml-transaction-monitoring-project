# Lessons Learned
## AML Transaction Monitoring System Implementation

Workshop held December 12, 2025 with the sponsor, delivery team, AML Ops, Information Security, Internal Audit and the vendor.

## What went well (keep doing)

| # | Lesson | Why it mattered | Recommendation for future projects |
|---|---|---|---|
| 1 | Making the resistant AML Ops Manager the Product Owner | She shaped the tool, so her team trusted it. Adoption was 100% from day one. | Give the most affected business leader a real decision making role early. |
| 2 | Scheduling the riskiest work (data integration) first | Data problems surfaced in Sprint 2, not in UAT, leaving time to fix them. | Put the highest uncertainty work at the front of the plan. |
| 3 | Inviting Internal Audit to sprint reviews | Control design was challenged early; zero audit findings at UAT apart from one defect caught in testing. | Treat audit as a design partner, not a final gate. |
| 4 | A four week parallel run with tuning | False positives fell from 96% to 82% before go live, so analysts were not overwhelmed. | Always plan time for tuning when rules engines go live. |
| 5 | Holding a contingency reserve | CR001 was funded without asking the board for more money. | Size contingency from the risk register, not a flat guess. |

## What could be better (change next time)

| # | Lesson | What happened | Recommendation |
|---|---|---|---|
| 6 | Inventory every system that touches transactions, not just the main one | Interac e-Transfers were missed in Sprint 1 because they sit outside core banking (CR001, $80,000). | Ask "where else can money move?" with business users, not only IT, during discovery. |
| 7 | Test admin and super user roles as hard as normal users | An admin could bypass maker/checker (I05). | Include privileged roles in every control test case. |
| 8 | Profile data before building on it | Missing KYC data cost 8 points of Sprint 2. | Make data profiling a standard Sprint 1 story for any data heavy project. |
| 9 | Agree load timing with real user start times | Load finished late on two days in hypercare (I07). | Set and test performance targets against the first user's start time, with a buffer. |

## Questions for the next project team

* Have we found every source of data for this process?
* Who is most likely to resist, and how can we give them ownership?
* Which controls could a privileged user bypass?
* How much tuning time do we need after go live?
