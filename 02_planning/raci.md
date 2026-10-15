# RACI Chart
## AML Transaction Monitoring System Implementation

**R** = Responsible (does the work) · **A** = Accountable (one owner, final approval) · **C** = Consulted · **I** = Informed

| Activity | Sponsor (CCO) | Project Manager | Head of IT | AML Ops Manager (Product Owner) | Info Security | Internal Audit | Vendor | AML Analysts |
|---|---|---|---|---|---|---|---|---|
| Approve business case and charter | A | R | C | C | I | I | | |
| Write RFP and select vendor | A | R | C | C | C | I | | C |
| Approve contract | A | C | C | I | C | I | C | |
| Project plan and baselines | I | A/R | C | C | C | I | C | |
| Data mapping and integration | I | A | R | C | C | | R | |
| Design detection scenarios and thresholds | A | C | I | R | | C | R | C |
| Prioritize product backlog | I | C | C | A/R | | | C | C |
| Configure system | | A | C | C | | | R | |
| Access controls and audit logging | I | C | C | C | A/R | C | R | |
| Security assessment | I | I | C | | A/R | I | C | |
| User acceptance testing | I | A | C | R | C | C | C | R |
| Update AML procedures | A | C | | R | | C | | C |
| Training | I | A | | C | | | R | R |
| Parallel run and results review | A | R | C | R | | C | C | R |
| Go live decision | A | R | C | C | C | I | I | I |
| Status reporting | I | A/R | I | I | I | I | C | |
| Change requests | A | R | C | C | C | I | C | |
| Lessons learned and closure | A | R | C | C | C | C | C | C |

**Rule check:** every row has exactly one **A**, so accountability is never shared or missing.
