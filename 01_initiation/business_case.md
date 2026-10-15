# Business Case
## AML Transaction Monitoring System Implementation

| Item | Detail |
|---|---|
| Organization | Prairie Trust Bank (fictional), Regina, Saskatchewan |
| Sponsor | Linda Okafor, Chief Compliance Officer |
| Prepared by | Blessing Adeniyi, PMP, Project Manager |
| Date | January 13, 2025 |
| Version | 1.0 (Approved) |

## 1. Executive summary

Prairie Trust Bank monitors only about 5% of its transactions for money laundering and terrorist financing, using manual spreadsheet reviews. A recent FINTRAC examination identified this as a deficiency. This business case recommends buying and implementing a cloud based automated transaction monitoring system that will review 100% of transactions, route alerts to analysts through a single case management tool, and keep a complete audit trail. The recommended option costs $1.62 million plus a $180,000 contingency, within the $1.8 million approved by the board, and can be live within 11 months.

## 2. Problem statement

* **Coverage gap:** the bank processes about 1.2 million transactions a month for 220,000 customers across 38 branches. Analysts sample roughly 60,000 a month. About 95% of activity is never reviewed.
* **Regulatory finding:** FINTRAC's examination found the bank's transaction monitoring was not adequate for its size and risk profile. The bank must submit and deliver a remediation plan.
* **Inconsistency:** each analyst applies their own judgement in spreadsheets. Two analysts can reach different decisions on the same pattern.
* **Weak audit trail:** decisions sit in emails and spreadsheet comments. Reconstructing why an alert was closed takes hours.
* **Reporting risk:** Suspicious Transaction Reports (STRs) depend on analysts noticing patterns manually, so some may be late or missed.

## 3. Why it matters

| Area | Impact if nothing changes |
|---|---|
| Regulatory | Administrative monetary penalties under the PCMLTFA, follow up examinations, and public naming of the penalty |
| Financial | Penalties, remediation consulting costs, and growing analyst headcount to keep up manually |
| Reputational | Loss of customer and correspondent bank trust if the bank is linked to laundered funds |
| Operational | Analyst burnout, high turnover, and slow investigations |

## 4. Options considered

| Option | Description | Cost (est.) | Time to value | Assessment |
|---|---|---|---|---|
| A. Do nothing | Keep manual sampling | $0 upfront | None | Rejected. Does not fix the FINTRAC finding. |
| B. Hire more analysts | Add 15 analysts to raise sampling to about 20% | $1.2M per year, ongoing | 6 months | Rejected. Still not full coverage, high ongoing cost, still inconsistent. |
| C. Build in house | Bank IT builds a rules engine and case tool | $2.4M | 18 to 24 months | Rejected. Over budget, misses the 12 month deadline, high delivery risk. |
| **D. Buy a SaaS monitoring system** | **Configure a proven vendor platform and integrate it with core banking** | **$1.62M + $180K contingency** | **11 months** | **Recommended** |

## 5. Recommended option: D

**Benefits**
* 100% of transactions screened against defined detection scenarios every day
* Consistent, rules based alerts and a standard investigation workflow
* Full audit trail kept for at least five years, as required under the PCMLTFA
* Faster, more reliable STR and Large Cash Transaction Report (LCTR) filing
* Vendor maintains the platform and updates typologies, so the bank keeps pace with new risks

**Measurable success targets**

| Measure | Today | Target within 3 months of go live |
|---|---|---|
| Transactions monitored | about 5% | 100% |
| Average alert triage time | not measured | 5 business days or less |
| LCTRs filed within 15 calendar days | about 91% | 100% |
| False positive rate | not measured | below 85% after tuning |
| Investigation decisions with documented rationale | partial | 100% |

## 6. Costs

| Category | Cost (CAD) |
|---|---|
| Vendor licence (year 1) and implementation services | $620,000 |
| Internal staff (IT, compliance, PMO) | $540,000 |
| Data integration and migration | $210,000 |
| Testing (including UAT and parallel run) | $70,000 |
| Infrastructure and security | $90,000 |
| Training and change management | $60,000 |
| Project management tools and quality assurance | $30,000 |
| **Subtotal** | **$1,620,000** |
| Contingency reserve (about 11%) | $180,000 |
| **Total requested** | **$1,800,000** |

Ongoing cost after year 1 is about $310,000 per year in licence and support. This compares favourably with option B at $1.2 million per year.

## 7. High level risks

* Poor data quality in core banking may create false alerts
* Vendor delivery delays
* Analysts may resist new tools and processes
* Integration with legacy systems may be harder than expected

Each is tracked in the [risk register](../02_planning/risk_register.md).

## 8. Recommendation

Approve option D, appoint a project manager, and release the $1.8 million budget so the project can begin vendor selection in February 2025 and go live by November 2025, meeting the board's 12 month commitment to FINTRAC.

**Decision:** Approved by the Executive Committee on January 20, 2025.
