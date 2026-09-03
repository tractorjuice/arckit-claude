# Stakeholder Drivers & Goals Analysis: Housing Benefits Portal

> **Template Origin**: Official | **ArcKit Version**: 6.13.0 | **Command**: `/arckit:stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Housing Benefits Portal (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-09-03 |
| **Last Modified** | 2026-09-03 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-12-03 |
| **Owner** | Priya Nandakumar, Head of Digital |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Benefits Transformation Board, Design Authority, Information Governance Group, Housing Benefits Portal project team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-09-03 | ArcKit AI | Initial creation from `/arckit:stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders, their underlying drivers (motivations, concerns, needs), how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to project success metrics.

### Key Findings

The Housing Benefits Portal replaces a paper and telephone claims process at Ashcombe District Council with a citizen-facing online service. Three decision-making bodies govern it: the Design Authority (architecture and suppliers), the Benefits Transformation Board (scope, budget, go-live) and the Information Governance Group (DPIA sign-off and retention) [OS-C6]. The dominant driver is the Director of Resources' savings target of £180k a year from the benefits service by 2027-28 [OS-C7], which collides directly with the caseworkers' experience of the last system change, rolled out without training and followed by three months of increased overtime [OS-C8]. The Data Protection Officer holds a hard gate: no processing of claimant data may go live without her sign-off [OS-C5]. Claimants, who are largely pensioners and people in supported or temporary accommodation now that working-age claims have moved to Universal Credit, need an accessible online route with an assisted alternative, and the 14-day decision commitment in BR-002 is the single goal that satisfies the most stakeholders at once.

### Critical Success Factors

- **Savings delivered without a workforce shock**: the £180k target is met through natural attrition, redeployment and avoided contact, with a no-compulsory-redundancy position agreed with the union representative before go-live.
- **Governance gates respected, not bypassed**: DPIA signed off by the Information Governance Group and architecture and supplier choices approved by the Design Authority before the Benefits Transformation Board takes the go-live decision.
- **Training before go-live, measured afterwards**: every caseworker trained at least two weeks before go-live, with overtime and backlog tracked weekly for the first three months.
- **Assisted digital route from day one**: telephone and face-to-face support remain available so that the online channel does not exclude the claimants least able to use it.

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Senior stakeholders agree on the destination (online claims, decisions within 14 days, lower running costs) but not on the path. The Director of Resources needs savings to land in the 2027-28 financial year, while the DPO, the Service Manager and the union representative each hold reasons to slow the timetable. The Head of Digital's Design Authority controls supplier and architecture choices, which the service side may see as friction. Alignment will rise to HIGH if the Benefits Transformation Board agrees a phased savings profile and a no-compulsory-redundancy commitment in its first meeting after this document is issued.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Margaret Ellery | Chief Executive, accountable to Full Council [OS-C1] | HIGH | MEDIUM | Quarterly briefing, escalation point, Full Council narrative |
| Daniel Quist | Director of Resources, Section 151 officer, owns Revenues and Benefits service and budget [OS-C2], chairs Benefits Transformation Board [OS-C6] | HIGH | HIGH | Senior Responsible Owner, monthly board, savings tracker |
| Priya Nandakumar | Head of Digital, chairs Design Authority [OS-C3] | HIGH | HIGH | Architecture and supplier decisions, fortnightly Design Authority |
| Tom Okafor | Benefits Service Manager, Service Owner, line-manages 22 caseworkers across two offices [OS-C4] | HIGH | HIGH | Day-to-day product direction, requirements prioritisation, training plan owner |
| Lena Marsh | Data Protection Officer, chairs Information Governance Group [OS-C5] | HIGH | MEDIUM | DPIA co-design from discovery, monthly Information Governance Group |
| Housing Benefit caseworkers | 22 staff across two offices [OS-C4] | LOW | HIGH | User research, design sprints, training champions, weekly stand-up during rollout |
| Union branch representative | Represents caseworkers; raised the last rollout's training and overtime problems [OS-C8] | MEDIUM | HIGH | Early consultation on workforce impact, agreed training and overtime commitments |
| Customer Services Manager | Runs contact centre and reception for both offices (assumed role) | MEDIUM | HIGH | Avoidable contact metrics, assisted digital design |
| ICT Operations and Platform team | Operates the council's PostgreSQL platform service (DR-001) | MEDIUM | MEDIUM | Non-functional requirements, runbooks, support model |
| Transformation Office | Programme management; author of the governance extract | MEDIUM | HIGH | Delivery management, board papers, benefits tracking |
| Cabinet Member for Finance and Resources | Portfolio holder; answers to Full Council and residents (assumed role) | HIGH | MEDIUM | Quarterly portfolio briefing, resident-facing messaging |

### External Stakeholders

| Stakeholder | Organization | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Housing Benefit claimants | Residents of Ashcombe district (mainly pensioners and residents of supported or temporary accommodation) | Beneficiary | LOW | HIGH |
| Private landlords and housing associations | Receive direct payments for many claimants | Beneficiary | LOW | MEDIUM |
| Department for Work and Pensions (DWP) | Funds Housing Benefit subsidy, collects performance statistics, sets policy | Oversight and funder | HIGH | LOW |
| Information Commissioner's Office (ICO) | Data protection regulator | Oversight | HIGH | LOW |
| Local Government and Social Care Ombudsman | Complaints about maladministration | Oversight | MEDIUM | LOW |
| External auditor | Audits subsidy claim and accounts | Oversight | MEDIUM | LOW |
| Citizens Advice and local advice agencies | Help claimants complete claims | Partner | LOW | MEDIUM |

### UK Government Digital Roles (GovS 005)

> The [Government Functional Standard for Digital (GovS 005)](https://www.gov.uk/government/publications/government-functional-standard-govs-005-digital) defines mandatory digital governance roles. Ashcombe District Council is a local authority, so GovS 005 is not binding, but the roles are adopted here as good practice and mapped to the council's own structure.

| Role | Responsibility | Typical Power/Interest | Engagement Strategy |
|------|---------------|----------------------|---------------------|
| Senior Responsible Owner (SRO) | Daniel Quist, Director of Resources. Accountable for outcomes, budget and the savings target; chairs the Benefits Transformation Board | HIGH / HIGH | Manage Closely — monthly board, decision escalation, savings tracker |
| Service Owner | Tom Okafor, Benefits Service Manager. Owns the end-to-end housing benefit service and user outcomes [OS-C4] | HIGH / HIGH | Manage Closely — weekly service review, backlog and prioritisation |
| Product Manager | To be appointed from the Transformation Office; prioritises features against user needs and policy | MEDIUM / HIGH | Keep Informed — sprint reviews, roadmap input |
| Delivery Manager | Transformation Office; manages cadence, risks and dependencies | MEDIUM / HIGH | Keep Informed — stand-ups, risk log, board papers |
| Central assurance (CDDO equivalent) | Not applicable to a district council. The Local Digital Declaration and MHCLG Local Digital guidance are the reference points | LOW / LOW | Monitor — align to Local Digital Declaration principles |
| CDIO equivalent | Priya Nandakumar, Head of Digital. Council digital strategy and technology oversight; chairs Design Authority [OS-C3] | HIGH / HIGH | Manage Closely — fortnightly Design Authority |
| DDaT Profession Lead | Head of Digital (combined role in a council of this size) | LOW / MEDIUM | Monitor — capability and recruitment support |

### UK Government Security Roles (GovS 007)

> The [Government Functional Standard for Security (GovS 007)](https://www.gov.uk/government/publications/government-functional-standard-govs-007-security) defines mandatory protective security roles. Mapped to the council's structure on the assumptions stated; confirm at the first Information Governance Group meeting.

| Role | Responsibility | Typical Power/Interest | Engagement Strategy |
|------|---------------|----------------------|---------------------|
| Senior Security Risk Owner (SSRO) | Margaret Ellery, Chief Executive, as the officer accountable to Full Council [OS-C1] | HIGH / MEDIUM | Keep Satisfied — security risk escalation, quarterly review |
| Departmental Security Officer (DSO) | ICT security lead within the Digital service (assumed) | HIGH / MEDIUM | Keep Satisfied — security compliance gates, incident reporting |
| Senior Information Risk Owner (SIRO) | Daniel Quist, Director of Resources (assumed; councils typically place SIRO with a director) | HIGH / MEDIUM | Keep Satisfied — information risk acceptance, DPIA residual risk decisions alongside the DPO |
| Cyber Security Lead | Digital service security engineer (assumed) | MEDIUM / HIGH | Keep Informed — security architecture reviews, penetration test scheduling before go-live |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • Chief Executive  │  • Director of      │
        │  • Cabinet Member   │    Resources (SRO)  │
        │  • DPO / IG Group   │  • Head of Digital  │
 P      │  • DWP              │  • Benefits Service │
 O      │  • ICO              │    Manager          │
 W      ├─────────────────────┼─────────────────────┤
 E      │                     │                     │
 R      │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • Ombudsman        │  • Caseworkers      │
        │  • External auditor │  • Union rep        │
        │  • Landlords        │  • Claimants        │
        │  • Advice agencies  │  • Customer Services│
        │                     │  • ICT Operations   │
        │                     │  • Transformation   │
        │                     │    Office           │
        └─────────────────────┴─────────────────────┘
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| Daniel Quist, Director of Resources (SRO) | HIGH | HIGH | Manage Closely | Monthly Benefits Transformation Board, fortnightly savings and delivery update |
| Priya Nandakumar, Head of Digital | HIGH | HIGH | Manage Closely | Fortnightly Design Authority, ADR review |
| Tom Okafor, Benefits Service Manager | HIGH | HIGH | Manage Closely | Weekly service review, embedded in delivery team |
| Margaret Ellery, Chief Executive | HIGH | MEDIUM | Keep Satisfied | Quarterly briefing, exception escalation |
| Cabinet Member for Finance and Resources | HIGH | MEDIUM | Keep Satisfied | Quarterly portfolio briefing, resident-facing milestones |
| Lena Marsh, DPO | HIGH | MEDIUM | Keep Satisfied | Monthly Information Governance Group, DPIA workshops from discovery |
| DWP | HIGH | LOW | Keep Satisfied | Quarterly performance statistics return, subsidy claim accuracy |
| ICO | HIGH | LOW | Keep Satisfied | DPIA on file, breach reporting readiness, no proactive contact expected |
| Caseworkers | LOW | HIGH | Keep Informed | Fortnightly show-and-tell, training champions, weekly rollout stand-up |
| Union branch representative | MEDIUM | HIGH | Keep Informed | Monthly consultation, written workforce commitments |
| Claimants | LOW | HIGH | Keep Informed | User research rounds, beta feedback, plain-English service updates |
| Customer Services Manager | MEDIUM | HIGH | Keep Informed | Monthly avoidable-contact review, assisted digital design |
| ICT Operations and Platform team | MEDIUM | MEDIUM | Keep Informed | Design Authority attendance, release notes, runbook sign-off |
| Transformation Office | MEDIUM | HIGH | Keep Informed | Weekly delivery stand-up, board paper preparation |
| Local Government and Social Care Ombudsman | MEDIUM | LOW | Monitor | Complaint trend review each quarter |
| External auditor | MEDIUM | LOW | Monitor | Annual subsidy audit evidence pack |
| Private landlords and housing associations | LOW | MEDIUM | Monitor | Landlord forum update at beta and live |
| Citizens Advice and advice agencies | LOW | MEDIUM | Monitor | Briefing before public beta, assisted digital referral route |

**Quadrant Interpretation:**

- **Manage Closely** (High Power, High Interest): Key decision-makers requiring active engagement
- **Keep Satisfied** (High Power, Low Interest): Influential stakeholders needing periodic updates
- **Keep Informed** (Low Power, High Interest): Engaged stakeholders needing regular communication
- **Monitor** (Low Power, Low Interest): Minimal engagement required

---

## Stakeholder Drivers Analysis

### SD-1: Director of Resources - Deliver £180k recurring savings by 2027-28

**Stakeholder**: Daniel Quist, Director of Resources and Section 151 officer

**Driver Category**: FINANCIAL

**Driver Statement**: Take £180k a year out of the benefits service running cost by 2027-28 [OS-C7] without a visible drop in service to residents, so that the council's medium-term financial plan balances.

**Context & Background**:
The Director of Resources owns the Revenues and Benefits service and its budget [OS-C2]. As Section 151 officer he is personally responsible for the council's financial administration and would have to issue a Section 114 notice if the budget could not be balanced. The savings target has already been booked into the medium-term financial plan, so failure to deliver it creates a gap that must be found elsewhere. The portal is the main lever available: today's paper and telephone process consumes caseworker time on data entry, chasing evidence and handling status calls.

**Driver Intensity**: CRITICAL

**Enablers** (What would help):

- A benefits realisation plan that shows the savings profile month by month, with online uptake and avoidable-contact reduction as the leading indicators
- Natural attrition in the caseworker team (assumed two to three leavers a year across 22 posts) so that posts can be held vacant rather than made redundant
- Reduced print, postage and scanning costs from digital submission

**Blockers** (What would hinder):

- Go-live slipping past April 2027, which removes most of the 2027-28 in-year saving
- A training and overtime bill in the rollout months that eats the first year of savings, as happened last time [OS-C8]
- Low online uptake among an older claimant base, leaving the paper channel and its cost in place

**Related Stakeholders**:

- Caseworkers and union representative (SD-6) fear the savings will come from their jobs
- Cabinet Member for Finance (SD-11) shares the driver politically
- Benefits Service Manager (SD-4) must deliver the savings operationally

---

### SD-2: Director of Resources - Protect the Housing Benefit subsidy claim and audit opinion

**Stakeholder**: Daniel Quist, Director of Resources and Section 151 officer

**Driver Category**: RISK

**Driver Statement**: Ensure the new process does not increase local authority error, because subsidy from DWP is reduced when error overpayments exceed thresholds and the external auditor qualifies the subsidy claim.

**Context & Background**:
Housing Benefit expenditure is largely reimbursed by DWP subsidy, but subsidy on local authority error overpayments falls sharply once the error rate passes the lower and upper thresholds. A new intake channel changes the evidence trail. If the portal captures poorer evidence or the audit trail of decisions is weaker, the annual subsidy audit could find more errors, costing the council far more than the portal saves.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- Structured online evidence capture with validation at the point of entry, which usually reduces error compared with paper
- Full audit trail of every claim event and caseworker decision retained for six years (DR-002)
- Early involvement of the external auditor in the design of the evidence and audit trail

**Blockers** (What would hinder):

- Caseworkers working overtime and under pressure during rollout, which is when error rates spike
- Evidence request workflow (FR-002) delivered late, forcing manual workarounds

**Related Stakeholders**:

- DWP (SD-9) shares the interest in accuracy
- External auditor
- Benefits Service Manager (SD-4)

---

### SD-3: Head of Digital - Build on council standards and platforms, not a new silo

**Stakeholder**: Priya Nandakumar, Head of Digital and chair of the Design Authority

**Driver Category**: STRATEGIC

**Driver Statement**: Deliver the portal as a reusable, standards-based service on the council's existing platforms, with every architecture and supplier decision going through the Design Authority [OS-C3], so that the pattern can be repeated for Council Tax Support and other services.

**Context & Background**:
The Design Authority exists because the council has accumulated single-service systems from past procurements. The Head of Digital wants the portal to prove that a common approach (GOV.UK Design System patterns, the council PostgreSQL platform service named in DR-001, shared identity and notifications) is faster and cheaper over time. A successful portal is also the Head of Digital's strongest case for continued investment in the Digital service.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- Architecture Decision Records for each significant choice, reviewed at the fortnightly Design Authority
- Reuse of the PostgreSQL platform with point-in-time recovery already required by DR-001
- WCAG 2.2 AA compliance and GOV.UK Design System patterns adopted from the start

**Blockers** (What would hinder):

- Pressure from the service or the board to buy a proprietary benefits portal module quickly, bypassing the Design Authority
- A fortnightly Design Authority cadence [OS-C6] that becomes the critical path for supplier approval

**Related Stakeholders**:

- Director of Resources (SD-1) may see standards work as delay
- ICT Operations (SD-10) benefits from platform reuse
- Benefits Service Manager (SD-4) needs fast decisions

---

### SD-4: Benefits Service Manager - Meet the 14-day decision commitment with the team he has

**Stakeholder**: Tom Okafor, Benefits Service Manager and Service Owner

**Driver Category**: OPERATIONAL

**Driver Statement**: Decide every complete claim within 14 calendar days (BR-002) while running two offices with 22 caseworkers [OS-C4], by removing the data entry, evidence chasing and status calls that currently consume the team.

**Context & Background**:
The current paper and telephone process means caseworkers key claims from forms, write out for missing evidence and take calls from claimants asking where their claim is. Incomplete claims are the biggest source of delay. The Service Manager is measured on DWP speed-of-processing statistics and on complaints. Save-and-resume (FR-001) and evidence requests (FR-002) are the features that address his pain most directly.

**Driver Intensity**: CRITICAL

**Enablers** (What would help):

- Online validation that stops incomplete claims at source
- Caseworker-initiated evidence requests with a deadline and automatic reminders (FR-002)
- A single work queue across both offices so load can be balanced

**Blockers** (What would hinder):

- A rollout that repeats the last change, with no training and a three-month backlog [OS-C8]
- Savings taken from headcount before the process efficiencies are real

**Related Stakeholders**:

- Caseworkers (SD-6)
- Claimants (SD-7)
- DWP (SD-9) measures the same speed statistic

---

### SD-5: Benefits Service Manager - Do not repeat the last rollout

**Stakeholder**: Tom Okafor, Benefits Service Manager

**Driver Category**: PERSONAL

**Driver Statement**: Keep the confidence of the caseworker team by ensuring this change is trained, supported and paced, so that the manager is not again the person explaining three months of overtime to staff and to the union.

**Context & Background**:
The last system change was rolled out without training and increased overtime for three months [OS-C8]. The Service Manager carried the operational and personal cost of that. His credibility with the team, and his standing with the Director of Resources, depend on this project going differently. He will resist any go-live date that does not allow for training and a hypercare period.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- Training plan owned by the Service Manager, agreed with the union representative and funded in the project budget
- Caseworker champions in each office embedded in design and testing
- Overtime and backlog reported weekly to the Benefits Transformation Board for the first three months after go-live

**Blockers** (What would hinder):

- A fixed go-live date set by the savings profile rather than by readiness
- Training budget cut to protect the savings number

**Related Stakeholders**:

- Caseworkers and union representative (SD-6) share this driver entirely
- Director of Resources (SD-1) holds the competing timetable pressure

---

### SD-6: Caseworkers and Union Representative - Training, fair workload and job security

**Stakeholder**: 22 Housing Benefit caseworkers across two offices, represented by the union branch representative

**Driver Category**: PERSONAL

**Driver Statement**: Be trained before the system changes, not carry the change through unpaid pressure or unplanned overtime, and know whether the £180k saving means redundancies.

**Context & Background**:
Caseworkers raised through their union representative that the last change was rolled out without training and increased overtime for three months [OS-C8]. They now hear of a savings target [OS-C7] and a new system in the same breath. Without a clear statement on jobs, the rational response is caution and low engagement in design. Their knowledge of edge cases (supported accommodation, backdating, overpayment recovery) is essential to getting the portal's rules right.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- A written no-compulsory-redundancy commitment for the life of the project, with savings taken through attrition and redeployment
- Paid, rostered training time at least two weeks before go-live, with backfill
- Champions role recognised in workload and appraisal

**Blockers** (What would hinder):

- Silence from senior management on the savings plan
- Design sessions scheduled on top of full caseloads

**Related Stakeholders**:

- Benefits Service Manager (SD-4, SD-5) is their advocate
- Director of Resources (SD-1) is the source of the tension

---

### SD-7: Claimants - Apply once, online, and hear back quickly

**Stakeholder**: Housing Benefit claimants in Ashcombe district

**Driver Category**: CUSTOMER

**Driver Statement**: Make a claim without travelling to an office (BR-001), stop and come back to it (FR-001), understand what evidence is needed, and get a decision within 14 days (BR-002) because rent is due.

**Context & Background**:
Since working-age claims moved to Universal Credit, the Housing Benefit caseload is mostly pensioners and people in supported, sheltered or temporary accommodation. Many have low digital confidence, some rely on advice agencies or family to apply, and most are financially vulnerable, so delay in a decision means rent arrears. They did not ask for a portal; they want a decision and clear communication. An online service helps them only if it is accessible, works on a phone, and has a supported alternative.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- Assisted digital route through the contact centre, reception and advice agencies
- Plain-English evidence checklist and status updates
- WCAG 2.2 AA compliance and mobile-first design

**Blockers** (What would hinder):

- Digital-only rollout that closes the paper and telephone channels early
- Identity verification steps that pensioners cannot complete

**Related Stakeholders**:

- Benefits Service Manager (SD-4) needs the same 14-day outcome
- Customer Services Manager (SD-12)
- Advice agencies and landlords

---

### SD-8: Data Protection Officer - Lawful, minimised processing signed off before go-live

**Stakeholder**: Lena Marsh, Data Protection Officer and chair of the Information Governance Group

**Driver Category**: COMPLIANCE

**Driver Statement**: Sign off the processing of claimant data before go-live [OS-C5] on the basis of a completed DPIA, with retention (six years after closure, DR-002) justified against data minimisation and with no unresolved high residual risk.

**Context & Background**:
Housing Benefit data includes income, health-related evidence for some premiums, tenancy and household composition, which are special category or otherwise sensitive for a vulnerable population. UK GDPR Article 35 requires a DPIA for this kind of processing, and the ICO expects the DPO to be consulted early. The DPO has a statutory duty and personal professional exposure. She will not sign off a DPIA presented two weeks before go-live.

**Driver Intensity**: CRITICAL

**Enablers** (What would help):

- DPIA started in discovery and reviewed at each monthly Information Governance Group [OS-C6]
- Data model and retention schedule agreed before build
- Clear processor arrangements for any supplier or hosting service

**Blockers** (What would hinder):

- Late supplier selection, which leaves processor due diligence to the end
- Requirements that collect more data than needed to decide a claim

**Related Stakeholders**:

- ICO
- Head of Digital (SD-3) for security architecture
- Director of Resources as SIRO for residual risk acceptance

---

### SD-9: DWP - Accurate subsidy claims and timely performance statistics

**Stakeholder**: Department for Work and Pensions

**Driver Category**: COMPLIANCE

**Driver Statement**: Receive accurate quarterly Housing Benefit performance statistics (speed of processing new claims and changes) and an unqualified annual subsidy claim from the council.

**Context & Background**:
DWP funds Housing Benefit through subsidy and publishes local authority speed-of-processing statistics. It has limited interest in how a district council runs its intake, but it will act if error rises or returns are late. DWP also continues to move remaining working-age cases to Universal Credit, which shrinks the caseload the portal serves over time.

**Driver Intensity**: MEDIUM

**Enablers** (What would help):

- Portal data feeding the existing benefits processing system so statistical returns are unchanged
- Improved evidence quality reducing error

**Blockers** (What would hinder):

- Data quality problems in migration between portal and processing system

**Related Stakeholders**:

- Director of Resources (SD-2)
- External auditor

---

### SD-10: ICT Operations and Platform team - A service they can run at 3am

**Stakeholder**: ICT Operations and Platform team

**Driver Category**: OPERATIONAL

**Driver Statement**: Host the portal on the council's PostgreSQL platform service with point-in-time recovery (DR-001), with monitoring, runbooks and a support model agreed before go-live, so that it does not become another unsupported bespoke system.

**Context & Background**:
The team runs the shared platform and picks up out-of-hours incidents. They have inherited systems from past projects with no runbooks and no supplier support. Their interest is moderate until go-live approaches, when it becomes intense.

**Driver Intensity**: MEDIUM

**Enablers** (What would help):

- Early non-functional requirements and capacity estimates
- Operational readiness gate before go-live

**Blockers** (What would hinder):

- Non-functional requirements left until after functional build
- Supplier-hosted components outside the team's visibility

**Related Stakeholders**:

- Head of Digital (SD-3)
- Benefits Service Manager (SD-4) as the business owner of the service

---

### SD-11: Cabinet Member and Chief Executive - Visible improvement without a headline

**Stakeholder**: Cabinet Member for Finance and Resources; Margaret Ellery, Chief Executive

**Driver Category**: STRATEGIC

**Driver Statement**: Show Full Council and residents a modern, cheaper service, with no Ombudsman finding, no data breach and no press story about pensioners locked out of benefits.

**Context & Background**:
The Chief Executive is accountable to Full Council [OS-C1]. The Cabinet Member must defend the savings in budget scrutiny and answer members whose residents complain. Their interest is episodic: high at budget-setting, at go-live and whenever something goes wrong. A failed rollout would surface in scrutiny committee and local press; a smooth one is a line in the annual report.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- Quarterly briefing with three numbers: online uptake, days to decision, savings to date
- Assisted digital route that gives members an answer for excluded residents

**Blockers** (What would hinder):

- Surprises reaching members before officers brief them
- Complaints trend rising during rollout

**Related Stakeholders**:

- Director of Resources (SD-1) reports to both
- Local Government and Social Care Ombudsman

---

### SD-12: Customer Services Manager - Reduce avoidable contact, keep an assisted route

**Stakeholder**: Customer Services Manager

**Driver Category**: OPERATIONAL

**Driver Statement**: Cut the volume of "where is my claim" and "what evidence do you need" calls and visits, while equipping advisers to help claimants who cannot use the portal alone.

**Context & Background**:
Benefits enquiries are a large share of contact centre and reception demand at both offices. Each avoidable contact costs adviser time and often results in a transfer to a caseworker. The Customer Services Manager wants the portal to show claim status and evidence needs so advisers can answer at first contact, and wants assisted digital designed with the contact centre rather than imposed on it.

**Driver Intensity**: MEDIUM

**Enablers** (What would help):

- Claim status visible to advisers and to claimants
- Assisted digital scripts and training for advisers alongside caseworkers

**Blockers** (What would hinder):

- Portal launched without adviser view or training, shifting confusion to the front desk

**Related Stakeholders**:

- Claimants (SD-7)
- Benefits Service Manager (SD-4)
- Director of Resources (SD-1) benefits from contact savings

---

## Driver-to-Goal Mapping

### Goal G-1: Achieve 70% online submission of new claims and changes within 12 months of go-live

**Derived From Drivers**: SD-1, SD-4, SD-7, SD-12

**Goal Owner**: Tom Okafor, Benefits Service Manager

**Goal Statement**: By 30 April 2028 (12 months after public beta go-live on 1 April 2027), at least 70% of new Housing Benefit claims and reported changes of circumstance are submitted through the portal, with an assisted digital route accounting for no more than 15 percentage points of that figure.

**Why This Matters**: Savings, faster decisions and lower contact volumes all depend on claims arriving in structured digital form. Uptake is the leading indicator for SD-1 and SD-4, and the assisted digital cap protects SD-7.

**Success Metrics**:

- **Primary Metric**: Percentage of new claims and changes submitted via portal per month
- **Secondary Metrics**:
  - Percentage of portal submissions completed with assisted digital support
  - Completion rate of started online claims (target above 75%)

**Baseline**: 0% online. Estimated annual volume 1,800 new claims and 15,000 changes of circumstance (to be confirmed from the benefits processing system in discovery).

**Target**: 40% by month 3, 55% by month 6, 70% by month 12.

**Measurement Method**: Monthly channel report from the benefits processing system, distinguishing portal, paper, telephone and assisted digital sources.

**Dependencies**:

- Save-and-resume (FR-001) and mobile-first design delivered in public beta
- Assisted digital route live in both offices and the contact centre at go-live
- Advice agencies briefed before public beta

**Risks to Achievement**:

- Older claimant base with low digital confidence adopts slowly
- Paper channel retained without active promotion of online, so habit persists

---

### Goal G-2: Decide 90% of complete claims within 14 calendar days by six months after go-live

**Derived From Drivers**: SD-4, SD-7, SD-9, SD-11

**Goal Owner**: Tom Okafor, Benefits Service Manager

**Goal Statement**: By 30 September 2027, 90% of new claims that arrive complete are decided within 14 calendar days of submission (BR-002), and average days to decision for all new claims falls from an estimated 23 days to 16 days or fewer.

**Why This Matters**: This is the requirement with the widest stakeholder support. It satisfies the Service Manager's operational target, claimants' need for certainty on rent, DWP's speed statistics and members' desire for a visible improvement.

**Success Metrics**:

- **Primary Metric**: Percentage of complete new claims decided within 14 calendar days
- **Secondary Metrics**:
  - Average days to decision, new claims (DWP speed-of-processing measure)
  - Average days to action a change of circumstance
  - Percentage of claims requiring a further evidence request (FR-002)

**Baseline**: Estimated 23 days average for new claims and roughly 55% within 14 days. Baseline to be confirmed from the last four quarterly DWP performance returns during discovery.

**Target**: 90% within 14 days for complete claims; 16 days average for all new claims.

**Measurement Method**: Quarterly DWP speed-of-processing return plus a weekly internal report from the benefits processing system.

**Dependencies**:

- Online validation reducing incomplete claims
- Evidence request workflow (FR-002) in place, even if initially manual
- Caseworker capacity not depleted by rollout overtime or premature vacancy freezes

**Risks to Achievement**:

- Post-go-live backlog if training is inadequate (see SD-5, SD-6)
- Definition of "complete" disputed between service and claimants

---

### Goal G-3: Reach a £180k annual savings run-rate by 31 March 2028 with no compulsory redundancies

**Derived From Drivers**: SD-1, SD-6, SD-11

**Goal Owner**: Daniel Quist, Director of Resources

**Goal Statement**: By 31 March 2028, the benefits service is running at a cost £180k a year below its 2025-26 baseline [OS-C7], delivered through held vacancies and redeployment (approximately four caseworker posts, £145k), reduced print, post and scanning (£20k) and reduced contact centre handling (£15k), with no compulsory redundancies and an in-year 2027-28 saving of at least £90k.

**Why This Matters**: This is the Director of Resources' critical driver and the source of the main stakeholder conflict. Setting the target as a run-rate at the end of 2027-28, with a stated in-year figure, gives the Section 151 officer a defensible number while giving the service and union a realistic path.

**Success Metrics**:

- **Primary Metric**: Annualised run-rate saving against 2025-26 baseline, reported monthly
- **Secondary Metrics**:
  - In-year cash saving for 2027-28
  - Posts held vacant or redeployed
  - Overtime spend in the rollout period against the 2025-26 average

**Baseline**: 2025-26 benefits service budget (figure held by the Director of Resources; assumed to include 22 caseworker posts at an average loaded cost of about £36k).

**Target**: £180k annualised run-rate by 31 March 2028; at least £90k in-year 2027-28.

**Measurement Method**: Monthly budget monitoring report from Finance, with a benefits realisation line maintained by the Transformation Office.

**Dependencies**:

- G-1 online uptake and G-2 processing improvements materialising
- Natural attrition of two to three posts a year across the team, confirmed with HR
- Training and hypercare funded from project budget, not the service budget

**Risks to Achievement**:

- Go-live slips past April 2027
- Attrition lower than assumed, forcing a choice between redundancy and missed savings
- Rollout overtime consumes first-year savings

---

### Goal G-4: DPIA signed off by the Information Governance Group at least eight weeks before go-live

**Derived From Drivers**: SD-8, SD-3, SD-11

**Goal Owner**: Lena Marsh, Data Protection Officer

**Goal Statement**: By 5 February 2027, the Information Governance Group has approved the DPIA for the portal [OS-C5] with no unresolved high residual risk, the six-year retention rule (DR-002) is documented with its legal basis, and any processor arrangements are contracted.

**Why This Matters**: DPO sign-off is a hard gate. Eight weeks of margin before a 1 April 2027 go-live gives time for remediation without moving the date, which protects the savings profile as well as compliance.

**Success Metrics**:

- **Primary Metric**: Date of Information Governance Group DPIA approval
- **Secondary Metrics**:
  - Number of high residual risks open at each monthly review
  - Percentage of data items in the data model with a documented purpose and retention period

**Baseline**: No DPIA started. Requirements document exists with two data requirements.

**Target**: Approval minuted at the February 2027 Information Governance Group meeting.

**Measurement Method**: Information Governance Group minutes and DPIA risk log.

**Dependencies**:

- Data model produced early enough for review (recommend `/arckit:data-model` and `/arckit:dpia` in October 2026)
- Supplier or hosting decision made by the Design Authority by December 2026

**Risks to Achievement**:

- Late supplier decision leaves processor due diligence incomplete
- Special category data handling (health evidence for premiums) not identified until build

---

### Goal G-5: Every caseworker trained at least two weeks before go-live, with overtime held within 10% of baseline

**Derived From Drivers**: SD-5, SD-6, SD-4

**Goal Owner**: Tom Okafor, Benefits Service Manager

**Goal Statement**: By 18 March 2027, 100% of the 22 caseworkers and all frontline advisers handling benefits enquiries have completed role-based training on the portal and the new evidence workflow, and in each of the three months after go-live caseworker overtime does not exceed the 2025-26 monthly average by more than 10%.

**Why This Matters**: This directly answers the union's complaint about the last change [OS-C8], protects the Service Manager's credibility, and prevents the error and backlog spike that would undermine G-2 and G-3.

**Success Metrics**:

- **Primary Metric**: Percentage of caseworkers with training completion recorded before 18 March 2027
- **Secondary Metrics**:
  - Monthly overtime hours, April to June 2027, against baseline
  - Caseworker confidence score (five-point scale) before and after training
  - Backlog of unactioned items each week for 12 weeks after go-live

**Baseline**: Last change: no training, three months of elevated overtime [OS-C8]. 2025-26 monthly overtime average to be obtained from payroll.

**Target**: 100% trained; overtime within 110% of baseline in each of April, May and June 2027.

**Measurement Method**: Training completion log held by the Service Manager; payroll overtime report; weekly backlog report to the Benefits Transformation Board.

**Dependencies**:

- Training plan agreed with the union representative by December 2026
- Backfill funded so training happens in work time
- Test environment stable enough for hands-on training

**Risks to Achievement**:

- Build slips compress the training window
- Two-office split means one office trains later than the other

---

### Goal G-6: All architecture and supplier decisions approved through the Design Authority with recorded ADRs before build starts

**Derived From Drivers**: SD-3, SD-10, SD-8

**Goal Owner**: Priya Nandakumar, Head of Digital

**Goal Statement**: By 18 December 2026, the Design Authority has approved Architecture Decision Records covering hosting on the council PostgreSQL platform (DR-001), the build or buy approach, identity and authentication, notifications, and any supplier engagement [OS-C3], and the portal meets WCAG 2.2 AA at public beta.

**Why This Matters**: The Head of Digital's driver is that this project sets the pattern for future services. Getting decisions through the Design Authority before build also gives the DPO the information she needs for processor and security assessment, and ICT Operations the supportability assurance they need.

**Success Metrics**:

- **Primary Metric**: Number of significant architecture decisions with an approved ADR before build
- **Secondary Metrics**:
  - Accessibility audit result at public beta (WCAG 2.2 AA, zero critical issues)
  - Percentage of components reused from council platforms

**Baseline**: No ADRs. One requirements document.

**Target**: Five ADRs approved by 18 December 2026; accessibility audit passed by 1 April 2027.

**Measurement Method**: Design Authority minutes and ADR register (`/arckit:adr`).

**Dependencies**:

- Research on build, buy or reuse options completed by November 2026 (`/arckit:research`, `/arckit:gov-reuse`)
- Fortnightly Design Authority slots reserved for the project

**Risks to Achievement**:

- Board pressure to select a supplier before options are assessed
- Design Authority cadence becomes the bottleneck for time-critical decisions

---

### Goal G-7: Reduce benefits-related avoidable contact by 30% within 12 months of go-live

**Derived From Drivers**: SD-12, SD-1, SD-7

**Goal Owner**: Customer Services Manager

**Goal Statement**: By 30 April 2028, benefits-related telephone calls and reception visits about claim status or evidence requirements are 30% below the 2025-26 average, while first-contact resolution for the remaining benefits enquiries rises to 70%.

**Why This Matters**: Avoidable contact is a cost to the contact centre and a symptom of claimant anxiety. Reducing it contributes to G-3 and shows that claimants have the information they need.

**Success Metrics**:

- **Primary Metric**: Monthly benefits-related contacts (calls plus visits) against baseline
- **Secondary Metrics**:
  - First-contact resolution rate for benefits enquiries
  - Assisted digital sessions delivered per month

**Baseline**: Estimated 22,000 benefits-related contacts a year (to be confirmed from contact centre reporting in discovery).

**Target**: 15,400 or fewer contacts in the 12 months to April 2028; 70% first-contact resolution.

**Measurement Method**: Contact centre telephony and reception footfall reports, categorised by enquiry type.

**Dependencies**:

- Claim status and evidence checklist visible to claimants and advisers
- Adviser training delivered alongside caseworker training (G-5)

**Risks to Achievement**:

- Contact rises temporarily at go-live as claimants seek reassurance about the new channel
- Enquiry categorisation in the contact centre is inconsistent, weakening the baseline

---

### Goal G-8: Unqualified subsidy audit and no increase in local authority error for 2027-28

**Derived From Drivers**: SD-2, SD-9

**Goal Owner**: Daniel Quist, Director of Resources

**Goal Statement**: The 2027-28 Housing Benefit subsidy claim is certified without qualification relating to the portal, and the local authority error overpayment rate stays below the lower subsidy threshold, at or below the 2025-26 level.

**Why This Matters**: A subsidy penalty would dwarf the savings. Demonstrating that the portal improves rather than degrades accuracy protects the Section 151 officer and satisfies DWP.

**Success Metrics**:

- **Primary Metric**: External auditor's opinion on the 2027-28 subsidy claim
- **Secondary Metrics**:
  - Local authority error overpayments as a percentage of expenditure, quarterly
  - Quality assurance check pass rate on portal-originated claims against paper-originated claims

**Baseline**: 2025-26 local authority error rate (held by the service; assumed below the lower threshold).

**Target**: Unqualified opinion; error rate at or below baseline.

**Measurement Method**: Annual subsidy audit; quarterly internal quality assurance sampling of decided claims by channel.

**Dependencies**:

- Full audit trail of claim events and decisions
- Quality assurance sampling designed before go-live

**Risks to Achievement**:

- Rollout pressure increases error in the first quarter after go-live

---

### Goal G-9: Claimant satisfaction of 80% or higher with no upheld Ombudsman complaint about digital exclusion

**Derived From Drivers**: SD-7, SD-11, SD-12

**Goal Owner**: Tom Okafor, Benefits Service Manager

**Goal Statement**: From public beta onwards, at least 80% of claimants completing the portal feedback survey rate the service as satisfied or very satisfied, and in the 12 months after go-live no complaint about the portal or about being unable to claim is upheld by the Local Government and Social Care Ombudsman.

**Why This Matters**: Claimants are the beneficiaries with the least power. A satisfaction measure and an Ombudsman measure give them a voice in governance and give the Chief Executive and Cabinet Member the assurance they need.

**Success Metrics**:

- **Primary Metric**: Percentage satisfied or very satisfied on the end-of-transaction survey
- **Secondary Metrics**:
  - Stage 1 and Stage 2 complaints about the portal per quarter
  - Ombudsman complaints and findings

**Baseline**: No current survey. Complaints baseline from the corporate complaints system for 2025-26.

**Target**: 80% satisfaction; zero upheld Ombudsman findings.

**Measurement Method**: Portal feedback survey (GOV.UK pattern); corporate complaints system; Ombudsman annual letter.

**Dependencies**:

- Assisted digital route and paper fallback retained through the first year
- User research with pensioners and supported accommodation residents in alpha and beta

**Risks to Achievement**:

- Identity verification designed for working-age users excludes pensioners
- Survey response biased towards confident users

---

## Goal-to-Outcome Mapping

### Outcome O-1: Faster claims processing with the same team

**Supported Goals**: G-1, G-2, G-5

**Outcome Statement**: Average days to decision for new Housing Benefit claims falls from an estimated 23 days to 16 days or fewer, and claims decided per caseworker per week rise by 25%, within 12 months of go-live.

**Measurement Details**:

- **KPI**: Average days to decision, new claims; claims decided per caseworker FTE per week
- **Current Value**: 23 days (estimate, to be confirmed); productivity baseline to be taken from the benefits processing system in discovery
- **Target Value**: 16 days; productivity baseline plus 25%
- **Measurement Frequency**: Weekly internally, quarterly to DWP
- **Data Source**: Benefits processing system and DWP performance return
- **Report Owner**: Tom Okafor, Benefits Service Manager

**Business Value**:

- **Financial Impact**: Productivity gain is the basis for holding approximately four posts vacant, worth about £145k a year
- **Strategic Impact**: Demonstrates the council can modernise a statutory service on shared platforms
- **Operational Impact**: Fewer incomplete claims, less rework, single work queue across two offices
- **Customer Impact**: Claimants receive decisions a week earlier on average, reducing rent arrears

**Timeline**:

- **Phase 1 (Months 1-3)**: Private beta with caseworker champions; no productivity target, error and overtime monitored
- **Phase 2 (Months 4-6)**: Public beta; 55% online uptake; average days to decision 19 or fewer
- **Phase 3 (Months 7-12)**: Full live; 70% online; 16 days; productivity plus 25%
- **Sustainment (Year 2+)**: Targets held while caseload shrinks under Universal Credit migration

**Stakeholder Benefits**:

- **Benefits Service Manager**: Meets the 14-day commitment and DWP statistics without additional staff
- **Claimants**: Faster certainty on rent
- **Director of Resources**: Evidence base for the savings profile

**Leading Indicators** (early signals of success):

- Online completion rate above 75% in private beta
- Percentage of claims needing an evidence request falling month on month

**Lagging Indicators** (final proof of success):

- DWP quarterly speed-of-processing statistics for Q3 and Q4 2027-28
- Annual productivity comparison 2025-26 against 2027-28

---

### Outcome O-2: £180k recurring saving delivered through attrition and avoided cost

**Supported Goals**: G-3, G-1, G-7

**Outcome Statement**: The benefits service runs at £180k a year below the 2025-26 baseline from 1 April 2028, with an in-year 2027-28 saving of at least £90k and no compulsory redundancies.

**Measurement Details**:

- **KPI**: Annualised run-rate saving; in-year cash saving; compulsory redundancies
- **Current Value**: £0 saving; 22 caseworker posts filled
- **Target Value**: £180k run-rate; £90k in-year 2027-28; zero compulsory redundancies
- **Measurement Frequency**: Monthly
- **Data Source**: Finance budget monitoring; HR establishment report
- **Report Owner**: Daniel Quist, Director of Resources, with the Transformation Office benefits tracker

**Business Value**:

- **Financial Impact**: £180k a year recurring against the medium-term financial plan
- **Strategic Impact**: Savings without service cuts strengthens the case for digital investment elsewhere
- **Operational Impact**: Lower print, post and scanning volumes
- **Customer Impact**: Neutral to positive, provided assisted digital is retained

**Timeline**:

- **Phase 1 (Months 1-3)**: Costs rise slightly for training and hypercare, funded from project budget
- **Phase 2 (Months 4-6)**: First vacancy held; print and post reduction visible
- **Phase 3 (Months 7-12)**: £90k in-year achieved; £180k run-rate by month 12
- **Sustainment (Year 2+)**: Full £180k in 2028-29 budget

**Stakeholder Benefits**:

- **Director of Resources**: Section 151 target met with an auditable trail
- **Cabinet Member**: Savings defensible in scrutiny as efficiency rather than cuts
- **Caseworkers and union representative**: Written protection from compulsory redundancy

**Leading Indicators** (early signals of success):

- Online uptake tracking to the G-1 profile
- Overtime within 110% of baseline in the first three months

**Lagging Indicators** (final proof of success):

- 2027-28 outturn report
- 2028-29 base budget reflecting the reduced establishment

---

### Outcome O-3: An assured, compliant service that passes its gates first time

**Supported Goals**: G-4, G-6, G-8

**Outcome Statement**: The portal goes live with a DPIA approved eight weeks in advance, all architecture and supplier decisions approved by the Design Authority, and an unqualified 2027-28 subsidy audit.

**Measurement Details**:

- **KPI**: Gates passed on first submission; audit opinion; data breaches reportable to the ICO
- **Current Value**: No gates passed; no DPIA; no ADRs
- **Target Value**: DPIA approved by 5 February 2027; five ADRs approved by 18 December 2026; unqualified audit; zero reportable breaches
- **Measurement Frequency**: Monthly at each board until go-live, then annually
- **Data Source**: Information Governance Group minutes, Design Authority minutes, external audit report, breach log
- **Report Owner**: Lena Marsh, DPO (privacy); Priya Nandakumar, Head of Digital (architecture); Daniel Quist (audit)

**Business Value**:

- **Financial Impact**: Avoids subsidy penalties and ICO enforcement, each potentially exceeding the project's total savings
- **Strategic Impact**: Establishes a repeatable assurance path for future services
- **Operational Impact**: Supportable service on the council platform with runbooks
- **Customer Impact**: Claimant data handled lawfully and securely

**Timeline**:

- **Phase 1 (Months 1-3)**: Post go-live security monitoring; quality assurance sampling by channel starts
- **Phase 2 (Months 4-6)**: DPIA reviewed against live operation
- **Phase 3 (Months 7-12)**: Subsidy claim prepared with portal audit trail
- **Sustainment (Year 2+)**: Annual DPIA review; audit cycle

**Stakeholder Benefits**:

- **DPO**: Statutory duty discharged with time to remediate
- **Head of Digital**: Design Authority authority demonstrated, pattern reusable
- **Director of Resources**: Subsidy protected
- **Chief Executive**: No breach or audit headline

**Leading Indicators** (early signals of success):

- DPIA risk log high risks trending to zero by January 2027
- ADRs submitted to Design Authority on schedule

**Lagging Indicators** (final proof of success):

- Information Governance Group approval minute
- External auditor's certificate for 2027-28

---

### Outcome O-4: A stable, trained workforce through the change

**Supported Goals**: G-5, G-3

**Outcome Statement**: All caseworkers are trained before go-live, overtime stays within 10% of baseline in each of the first three months, sickness absence and voluntary turnover in the team do not rise above the 2025-26 rate, and the union representative confirms in writing that consultation commitments were met.

**Measurement Details**:

- **KPI**: Training completion; overtime against baseline; sickness absence; voluntary turnover; union confirmation
- **Current Value**: Last change: no training, three months of elevated overtime [OS-C8]
- **Target Value**: 100% trained by 18 March 2027; overtime within 110% of baseline April to June 2027; absence and turnover at or below 2025-26
- **Measurement Frequency**: Weekly during rollout, monthly thereafter
- **Data Source**: Training log; payroll; HR absence and turnover reports
- **Report Owner**: Tom Okafor, Benefits Service Manager

**Business Value**:

- **Financial Impact**: Avoids an estimated £25k to £40k of unplanned overtime based on the last change
- **Strategic Impact**: Rebuilds trust between the service, its staff and the Transformation Office, making future change easier
- **Operational Impact**: Caseworkers productive from day one, error rate stable
- **Customer Impact**: No backlog-driven delay for claimants at go-live

**Timeline**:

- **Phase 1 (Months 1-3)**: Hypercare; weekly overtime and backlog report to board
- **Phase 2 (Months 4-6)**: Refresher training; champions review
- **Phase 3 (Months 7-12)**: Team involved in continuous improvement backlog
- **Sustainment (Year 2+)**: Training embedded in induction

**Stakeholder Benefits**:

- **Caseworkers and union representative**: The last rollout's experience is not repeated
- **Benefits Service Manager**: Credibility with the team preserved
- **Director of Resources**: Overtime does not erode savings

**Leading Indicators** (early signals of success):

- Training plan agreed with union representative by December 2026
- Caseworker confidence score rising after each training session

**Lagging Indicators** (final proof of success):

- Overtime outturn April to June 2027
- Union representative's written confirmation at the three-month review

---

### Outcome O-5: Claimants get a service they can use and trust

**Supported Goals**: G-1, G-7, G-9

**Outcome Statement**: Within 12 months of go-live, 70% of claims arrive online, 80% of claimants report satisfaction, benefits-related avoidable contact falls by 30%, and no Ombudsman complaint about digital exclusion is upheld.

**Measurement Details**:

- **KPI**: Online uptake; satisfaction; avoidable contact; Ombudsman findings
- **Current Value**: 0% online; no survey; estimated 22,000 contacts a year; complaints baseline from 2025-26
- **Target Value**: 70%; 80%; 15,400 contacts or fewer; zero upheld findings
- **Measurement Frequency**: Monthly (uptake, contact, satisfaction); quarterly (complaints)
- **Data Source**: Benefits processing system; portal survey; contact centre reports; complaints system
- **Report Owner**: Tom Okafor, Benefits Service Manager, with the Customer Services Manager

**Business Value**:

- **Financial Impact**: Contact reduction contributes about £15k a year to G-3
- **Strategic Impact**: Evidence that digital services can serve a vulnerable population when assisted digital is designed in
- **Operational Impact**: Advisers resolve enquiries at first contact
- **Customer Impact**: Claimants apply from home or with help, know what is needed and when to expect a decision

**Timeline**:

- **Phase 1 (Months 1-3)**: Private beta with 50 invited claimants and advice agency partners
- **Phase 2 (Months 4-6)**: Public beta; satisfaction above 70%; assisted digital sessions running in both offices
- **Phase 3 (Months 7-12)**: Full targets
- **Sustainment (Year 2+)**: Annual accessibility audit and user research round

**Stakeholder Benefits**:

- **Claimants**: A usable service with a human alternative
- **Cabinet Member and Chief Executive**: A resident-facing success and an answer to members' casework
- **Customer Services Manager**: Lower demand and better first-contact resolution

**Leading Indicators** (early signals of success):

- Task completion rate in usability testing with pensioners above 80%
- Assisted digital referrals from advice agencies in private beta

**Lagging Indicators** (final proof of success):

- 12-month channel and satisfaction report
- Ombudsman annual review letter for 2027-28

---

## Complete Traceability Matrix

### Stakeholder → Driver → Goal → Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Director of Resources | SD-1 | £180k recurring savings by 2027-28 | G-3 | £180k run-rate by March 2028, no compulsory redundancies | O-2 | £180k recurring saving |
| Director of Resources | SD-1 | £180k recurring savings by 2027-28 | G-1 | 70% online submission | O-2 | £180k recurring saving |
| Director of Resources | SD-1 | £180k recurring savings by 2027-28 | G-7 | 30% less avoidable contact | O-2 | £180k recurring saving |
| Director of Resources | SD-2 | Protect subsidy and audit opinion | G-8 | Unqualified subsidy audit | O-3 | Assured, compliant service |
| Head of Digital | SD-3 | Standards-based, reusable platform | G-6 | ADRs approved via Design Authority | O-3 | Assured, compliant service |
| Benefits Service Manager | SD-4 | 14-day decisions with current team | G-2 | 90% within 14 days | O-1 | Faster processing, same team |
| Benefits Service Manager | SD-4 | 14-day decisions with current team | G-1 | 70% online submission | O-1 | Faster processing, same team |
| Benefits Service Manager | SD-5 | Do not repeat last rollout | G-5 | 100% trained, overtime within 10% | O-4 | Stable, trained workforce |
| Caseworkers and union rep | SD-6 | Training, workload, job security | G-5 | 100% trained, overtime within 10% | O-4 | Stable, trained workforce |
| Caseworkers and union rep | SD-6 | Training, workload, job security | G-3 | No compulsory redundancies | O-2 | £180k recurring saving |
| Claimants | SD-7 | Apply online, hear back quickly | G-2 | 90% within 14 days | O-1 | Faster processing, same team |
| Claimants | SD-7 | Apply online, hear back quickly | G-9 | 80% satisfaction, no upheld Ombudsman finding | O-5 | Usable, trusted service |
| Claimants | SD-7 | Apply online, hear back quickly | G-1 | 70% online submission | O-5 | Usable, trusted service |
| DPO | SD-8 | DPIA sign-off before go-live | G-4 | DPIA approved eight weeks before go-live | O-3 | Assured, compliant service |
| DWP | SD-9 | Accurate subsidy, timely statistics | G-8 | Unqualified subsidy audit | O-3 | Assured, compliant service |
| DWP | SD-9 | Accurate subsidy, timely statistics | G-2 | 90% within 14 days | O-1 | Faster processing, same team |
| ICT Operations | SD-10 | Supportable service on council platform | G-6 | ADRs approved via Design Authority | O-3 | Assured, compliant service |
| Cabinet Member and Chief Executive | SD-11 | Visible improvement, no headline | G-9 | 80% satisfaction, no upheld Ombudsman finding | O-5 | Usable, trusted service |
| Cabinet Member and Chief Executive | SD-11 | Visible improvement, no headline | G-3 | £180k run-rate | O-2 | £180k recurring saving |
| Customer Services Manager | SD-12 | Less avoidable contact, assisted route | G-7 | 30% less avoidable contact | O-5 | Usable, trusted service |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: The Director of Resources needs £180k of savings in 2027-28 [OS-C7], but caseworkers and their union representative fear job losses and remember the untrained rollout [OS-C8]. A savings plan built on headcount before efficiencies are real would repeat that experience and depress engagement in design.
  - **Resolution Strategy**: The Benefits Transformation Board adopts G-3 as a run-rate target by 31 March 2028 with a £90k in-year floor, commits in writing to no compulsory redundancies for the project's life, and funds training and hypercare from the project budget rather than the service budget. HR confirms the attrition assumption. The union representative is consulted on the training plan by December 2026.

- **Conflict 2**: The savings timetable pulls go-live earlier, while the DPO's sign-off gate [OS-C5] and the Service Manager's insistence on training before go-live push it later.
  - **Resolution Strategy**: Fix go-live at 1 April 2027 now and work backwards: ADRs by 18 December 2026, DPIA approval by 5 February 2027, training complete by 18 March 2027. The Board treats these as readiness criteria for the go-live decision and moves the date rather than skipping a gate if they slip. The savings profile is re-baselined if the date moves, so the Director of Resources is not surprised.

- **Conflict 3**: The Head of Digital requires every architecture and supplier decision to pass through the fortnightly Design Authority [OS-C3] [OS-C6], while the Service Manager and the Board want a fast route to a working product.
  - **Resolution Strategy**: Reserve a standing project slot at each Design Authority meeting, submit options papers a week ahead, and agree a delegated decision threshold so that only significant decisions (hosting, build or buy, identity, notifications, supplier) require a full ADR. Complete research on reuse and market options in October and November 2026 so the Design Authority is choosing between assessed options rather than blocking.

- **Conflict 4**: The 70% online target serves the savings case, but the claimant population is older and less digitally confident, and members will hear first from residents who cannot use the portal.
  - **Resolution Strategy**: Keep the paper and telephone channels for at least the first year, design assisted digital with the contact centre and advice agencies, cap assisted digital within the uptake measure so the service cannot hit the target by simply keying paper forms, and report Ombudsman and complaint trends to the Board alongside uptake.

- **Conflict 5**: DR-002 requires evidence documents to be retained for six years after closure, which the DPO must reconcile with data minimisation.
  - **Resolution Strategy**: Document the retention basis (subsidy audit and overpayment recovery limitation periods) in the DPIA, apply retention at document level so that evidence not needed for audit is deleted earlier, and have the Information Governance Group approve the retention schedule [OS-C6] before build.

**Synergies**:

- **Synergy 1**: The Service Manager's operational driver (SD-4), the claimants' customer driver (SD-7), DWP's statistical interest (SD-9) and the members' reputational driver (SD-11) all converge on G-2, the 14-day decision goal. It should be the headline measure on every board paper.
- **Synergy 2**: Training investment (SD-5, SD-6) and the savings target (SD-1) are complementary rather than opposed once overtime is counted: an untrained rollout would cost £25k to £40k in overtime and delay the productivity gain that funds the savings.
- **Synergy 3**: The Head of Digital's platform reuse (SD-3), ICT Operations' supportability (SD-10) and the DPO's need for early architecture visibility (SD-8) are all served by G-6, ADRs through the Design Authority before build.
- **Synergy 4**: Save-and-resume (FR-001) and evidence requests (FR-002) reduce incomplete claims, which reduces caseworker rework (SD-4), avoidable contact (SD-12) and days to decision for claimants (SD-7) at once.

---

## Communication & Engagement Plan

### Stakeholder-Specific Messaging

#### Daniel Quist, Director of Resources (SRO)

**Primary Message**: The £180k is deliverable as a run-rate by March 2028 through attrition and avoided cost, and the fastest way to lose it is an untrained rollout or a subsidy audit finding.

**Key Talking Points**:

- Monthly savings tracker showing run-rate, in-year cash and the leading indicators (uptake, contact, overtime)
- Go-live readiness criteria protect the savings profile by preventing a repeat of the last change
- Audit trail and quality assurance by channel protect the subsidy claim

**Communication Frequency**: Fortnightly written update; monthly Benefits Transformation Board

**Preferred Channel**: Board paper with one-page dashboard; short face-to-face briefing before each board

**Success Story**: The 2027-28 outturn shows £90k in-year saving, the establishment is four posts lighter through attrition, and the subsidy claim is certified without qualification.

---

#### Priya Nandakumar, Head of Digital

**Primary Message**: This project is the reference implementation for council services on shared platforms, and the Design Authority decides its architecture.

**Key Talking Points**:

- ADR pipeline with dates for each decision
- Reuse of the PostgreSQL platform, GOV.UK Design System and shared components
- Accessibility and security assurance built into the plan, not bolted on

**Communication Frequency**: Fortnightly Design Authority; weekly delivery stand-up attendance optional

**Preferred Channel**: Design Authority papers, ADR register, architecture diagrams

**Success Story**: Five ADRs approved on schedule, WCAG 2.2 AA passed at public beta, and the Council Tax Support team asks to reuse the pattern.

---

#### Tom Okafor, Benefits Service Manager (Service Owner)

**Primary Message**: You own the product direction and the training plan, the go-live date moves if readiness slips, and the team's overtime is reported to the Board.

**Key Talking Points**:

- 14-day decision target is the headline measure
- Caseworker champions in each office shape the evidence workflow
- Training complete two weeks before go-live with backfill funded

**Communication Frequency**: Weekly service review; daily contact with the delivery team during beta

**Preferred Channel**: Face to face, backlog tool, weekly one-page status

**Success Story**: Three months after go-live, overtime is within baseline, backlog is lower than before, and the team's confidence score has risen.

---

#### Lena Marsh, Data Protection Officer

**Primary Message**: The DPIA starts in discovery, you see the data model before build, and sign-off is scheduled eight weeks before go-live.

**Key Talking Points**:

- DPIA risk log reviewed at each monthly Information Governance Group
- Retention schedule for DR-002 justified at document level
- Processor arrangements settled when the Design Authority approves any supplier

**Communication Frequency**: Monthly Information Governance Group; DPIA workshops at discovery, alpha and beta

**Preferred Channel**: DPIA document and risk log; workshops

**Success Story**: DPIA approved in February 2027 with no high residual risks and no changes required after go-live.

---

#### Caseworkers and Union Representative

**Primary Message**: Nobody will be made compulsorily redundant because of this project, you will be trained in work time before anything changes, and your overtime will be reported to the Board every week after go-live.

**Key Talking Points**:

- Written workforce commitments agreed with the union representative
- Champions in each office paid and recognised for design and testing time
- Weekly rollout stand-up where issues are logged and answered

**Communication Frequency**: Fortnightly show-and-tell; monthly union consultation; weekly stand-up for three months after go-live

**Preferred Channel**: Face to face in both offices; team briefing notes; champions network

**Success Story**: The union representative confirms in writing at the three-month review that consultation and training commitments were met.

---

#### Claimants

**Primary Message**: You can now claim online from home or with help at the council offices, you can save and come back, and you will hear within 14 days.

**Key Talking Points**:

- Help is available by phone, in person and through advice agencies
- Clear list of evidence needed before you start
- Track your claim without calling

**Communication Frequency**: At each user research round; at public beta launch; on-service messaging

**Preferred Channel**: Plain-English letters and web content, advice agency briefings, landlord forum

**Success Story**: A pensioner in supported accommodation completes a claim with an adviser's help and receives a decision in nine days.

---

#### Margaret Ellery, Chief Executive, and Cabinet Member for Finance and Resources

**Primary Message**: Three numbers each quarter: online uptake, days to decision, savings to date, plus any risk that could reach members before you do.

**Key Talking Points**:

- Assisted digital route gives an answer to every casework enquiry about access
- Governance gates passed on schedule
- Complaints and Ombudsman trend

**Communication Frequency**: Quarterly briefing; immediate escalation for any incident

**Preferred Channel**: One-page briefing note from the Director of Resources

**Success Story**: The portal appears in the annual report as a saving achieved through efficiency, with no scrutiny committee referral.

---

#### DWP, ICO, External Auditor and Ombudsman

**Primary Message**: Statutory returns, subsidy evidence and data protection documentation are unchanged in format and improved in quality.

**Key Talking Points**:

- Portal feeds the existing benefits processing system, so returns continue as today
- DPIA on file and breach process tested before go-live
- Audit trail available by channel for subsidy testing

**Communication Frequency**: Quarterly returns to DWP; annual audit; ICO and Ombudsman only if required

**Preferred Channel**: Existing statutory channels

**Success Story**: No regulator contact is needed beyond routine returns.

---

#### ICT Operations, Customer Services Manager and Transformation Office

**Primary Message**: You are in the design from the start: non-functional requirements, assisted digital and benefits tracking are project deliverables with named owners.

**Key Talking Points**:

- Operational readiness gate before go-live with runbooks and monitoring
- Adviser view of claim status and assisted digital scripts
- Benefits realisation tracker owned by the Transformation Office

**Communication Frequency**: Weekly delivery stand-up; monthly avoidable-contact review

**Preferred Channel**: Delivery tooling, release notes, stand-up

**Success Story**: No out-of-hours incident in the first three months and first-contact resolution for benefits enquiries at 70%.

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Caseworkers | Key paper forms, write for evidence, take status calls across two offices | Work a shared digital queue, issue evidence requests in the portal, fewer status calls | HIGH | HIGH | Champions, training in work time, no-compulsory-redundancy commitment, weekly overtime reporting |
| Benefits Service Manager | Manages backlog and complaints reactively | Owns product backlog and performance dashboard | HIGH | LOW | Service Owner role with real authority, training plan ownership |
| Claimants | Paper form or telephone, visit office for evidence | Online claim with save and resume, assisted route available | HIGH | MEDIUM | Assisted digital, paper fallback for year one, plain-English content, user research with pensioners |
| Customer Services advisers | Take status calls and transfer to caseworkers | Answer from adviser view, deliver assisted digital sessions | MEDIUM | MEDIUM | Adviser training alongside caseworkers, scripts, workload review |
| ICT Operations | Support legacy systems with limited documentation | Run a new service on the shared PostgreSQL platform with runbooks | MEDIUM | LOW | Operational readiness gate, early non-functional requirements |
| Director of Resources | Savings target booked, no delivery mechanism | Savings tracked monthly against a phased profile | MEDIUM | LOW | Run-rate target with in-year floor, transparent tracker |
| Head of Digital | Design Authority approves decisions case by case | Design Authority steers a reference implementation | LOW | LOW | Standing agenda slot, ADR pipeline |
| DPO | Consulted late on projects | DPIA co-designed from discovery | MEDIUM | LOW | Monthly Information Governance Group review, workshops |
| Landlords | Receive letters and payment schedules | Same payments, potentially earlier decisions | LOW | LOW | Landlord forum update |
| Advice agencies | Help clients with paper forms | Help clients online, referral route for assisted digital | MEDIUM | LOW | Briefing before public beta, named contact |

### Change Readiness

**Champions** (Enthusiastic supporters):

- Priya Nandakumar, Head of Digital - the project proves the platform and standards approach she chairs the Design Authority to promote
- Daniel Quist, Director of Resources - the portal is his mechanism for the savings already booked
- Customer Services Manager - stands to lose a large volume of avoidable contact

**Fence-sitters** (Neutral, need convincing):

- Tom Okafor, Benefits Service Manager - supports the outcome but will withhold commitment until training, pacing and the go-live readiness criteria are agreed in writing
- Lena Marsh, DPO - neutral on the project, decisive on the gate; convinced by early DPIA engagement and a data model she can review
- ICT Operations - convinced by non-functional requirements and an operational readiness gate
- Margaret Ellery, Chief Executive - supportive if no surprises; convinced by the quarterly three-number briefing
- Advice agencies - convinced by an assisted digital referral route that helps their clients rather than adding work

**Resisters** (Opposed or skeptical):

- Caseworkers and union representative - skeptical because the last change was untrained and increased overtime for three months [OS-C8], and because the savings target implies job losses - address with a written no-compulsory-redundancy commitment, training in work time, champions, and weekly overtime reporting to the Board
- A minority of claimants and their advocates - may see online-first as exclusion - address by retaining paper and telephone channels for year one and publishing the assisted digital offer

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Savings taken from headcount before efficiencies are real

**Related Stakeholders**: Director of Resources, Benefits Service Manager, caseworkers, union representative

**Risk Description**: Budget pressure leads to vacancies being frozen or posts deleted in 2027-28 before online uptake and processing gains have reduced workload, producing a backlog, error and overtime spike and a breakdown in trust with the union.

**Impact on Goals**: G-2, G-3, G-5, G-8

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Board adopts the run-rate savings profile with leading indicators as the trigger for holding each vacancy; no-compulsory-redundancy commitment in writing; overtime and backlog reported weekly for three months after go-live.

**Contingency Plan**: If backlog exceeds two weeks of intake, release the held vacancy budget for agency cover and re-baseline the savings profile at the next Board.

---

### Risk R-2: Rollout repeats the last change: no training, three months of overtime

**Related Stakeholders**: Caseworkers, union representative, Benefits Service Manager

**Risk Description**: Build slips compress the training window and go-live proceeds with partial training, repeating the experience the union has already raised [OS-C8].

**Impact on Goals**: G-2, G-5, G-8

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Training completion by 18 March 2027 is a go-live readiness criterion; training plan agreed with the union representative by December 2026; backfill funded from the project budget.

**Contingency Plan**: Move go-live by the number of weeks needed to complete training; re-baseline savings; inform the Cabinet Member before the decision is public.

---

### Risk R-3: DPIA sign-off arrives late or with unresolved high risks

**Related Stakeholders**: DPO, Head of Digital, Director of Resources as SIRO

**Risk Description**: Supplier or hosting decisions are made late, processor due diligence and security assessment are incomplete, and the DPO cannot sign off [OS-C5] in time for a 1 April 2027 go-live.

**Impact on Goals**: G-4, G-3, G-6

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: DPIA started in discovery; data model produced in October 2026; supplier decision at Design Authority by 18 December 2026; monthly Information Governance Group review of the risk log.

**Contingency Plan**: Go live with a reduced data scope (for example, no online upload of health-related evidence) while the remaining risks are treated; residual risk decision escalated to the SIRO.

---

### Risk R-4: Digital exclusion of pensioners and vulnerable claimants

**Related Stakeholders**: Claimants, Cabinet Member, Chief Executive, Ombudsman, advice agencies

**Risk Description**: The portal's identity verification, evidence upload or language excludes claimants with low digital confidence; complaints rise; an Ombudsman finding of maladministration follows.

**Impact on Goals**: G-1, G-9, G-7

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: User research with pensioners and supported accommodation residents in alpha and beta; assisted digital in both offices and through advice agencies; paper and telephone retained for year one; WCAG 2.2 AA audit before public beta.

**Contingency Plan**: Extend assisted digital hours and paper channel; publish the assisted route to members for casework; review identity verification approach at the Design Authority.

---

### Risk R-5: Design Authority becomes the critical path

**Related Stakeholders**: Head of Digital, Benefits Service Manager, Director of Resources

**Risk Description**: Fortnightly cadence [OS-C6] and full ADR requirements for every decision delay supplier and architecture choices, pushing the DPIA and training windows later.

**Impact on Goals**: G-6, G-4, G-3

**Probability**: MEDIUM

**Impact**: MEDIUM

**Mitigation Strategy**: Standing project slot; papers circulated one week ahead; delegated threshold so only five significant decisions need full ADRs; options research completed before decisions are tabled.

**Contingency Plan**: Head of Digital convenes an extraordinary Design Authority session for time-critical decisions.

---

### Risk R-6: Members hear of problems from residents before officers brief them

**Related Stakeholders**: Cabinet Member, Chief Executive, Director of Resources

**Risk Description**: An incident, backlog or exclusion story reaches councillors or local press before the quarterly briefing, damaging confidence in the project and in the Director of Resources.

**Impact on Goals**: G-9, G-3

**Probability**: LOW

**Impact**: MEDIUM

**Mitigation Strategy**: Escalation protocol requiring the Director of Resources to brief the Chief Executive and Cabinet Member within one working day of any incident affecting claimants; member briefing note before public beta.

**Contingency Plan**: Prepared lines and an assisted digital offer that ward members can pass to residents.

---

### Risk R-7: Subsidy audit finds increased error in portal-originated claims

**Related Stakeholders**: Director of Resources, DWP, external auditor

**Risk Description**: A weaker evidence trail or rollout-period error raises local authority error overpayments above the subsidy threshold, costing more than the project saves.

**Impact on Goals**: G-8, G-3

**Probability**: LOW

**Impact**: HIGH

**Mitigation Strategy**: Full audit trail; quality assurance sampling by channel from private beta; external auditor consulted on evidence design.

**Contingency Plan**: Targeted quality checks on portal claims; corrective training; early engagement with the auditor on the claim.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval and savings profile | Transformation Office | Director of Resources via Benefits Transformation Board [OS-C6] | Benefits Service Manager, Head of Digital, union representative | Chief Executive, Cabinet Member, caseworkers |
| Scope changes | Product Manager | Benefits Transformation Board | Service Owner, Head of Digital, DPO | Delivery team, ICT Operations |
| Requirements prioritisation | Product Manager | Tom Okafor, Service Owner | Caseworker champions, Customer Services Manager, claimants (via research) | Design Authority, Transformation Office |
| Architecture decisions and technical standards | Delivery team architect | Priya Nandakumar via Design Authority [OS-C3] [OS-C6] | ICT Operations, DPO, security lead | Benefits Transformation Board |
| Supplier selection and engagement | Head of Digital | Design Authority [OS-C3] | Director of Resources, DPO, procurement | Benefits Transformation Board |
| DPIA sign-off and retention schedule | Delivery team with DPO support | Lena Marsh via Information Governance Group [OS-C5] [OS-C6] | Head of Digital, Service Owner, SIRO | Benefits Transformation Board |
| Training plan and workforce commitments | Benefits Service Manager | Director of Resources | Union representative, HR, caseworker champions | Benefits Transformation Board |
| Go-live decision | Transformation Office (readiness evidence) | Benefits Transformation Board [OS-C6] | DPO, Head of Digital, Service Owner, ICT Operations | Chief Executive, Cabinet Member, all staff, advice agencies |
| Operational readiness and support model | ICT Operations | Head of Digital | Service Owner, delivery team | Benefits Transformation Board |
| Assisted digital offer and channel retention | Customer Services Manager | Service Owner | Advice agencies, claimants (via research), Cabinet Member | Benefits Transformation Board |

### Escalation Path

1. **Level 1**: Product Manager and Service Owner (Tom Okafor) - day-to-day priority, backlog and operational decisions
2. **Level 2**: Design Authority (technical, supplier and standards issues, fortnightly) or Information Governance Group (data protection and retention issues, monthly) [OS-C6]
3. **Level 3**: Benefits Transformation Board chaired by the Director of Resources - scope, budget, timeline, workforce commitments and go-live [OS-C6]
4. **Level 4**: Chief Executive - unresolved conflicts between boards, matters likely to reach Full Council or the press [OS-C1]

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| Daniel Quist, Director of Resources | 2026-09-17 (scheduled) | Review at September Benefits Transformation Board | PENDING |
| Priya Nandakumar, Head of Digital | 2026-09-10 (scheduled) | Review at next Design Authority | PENDING |
| Tom Okafor, Benefits Service Manager | 2026-09-08 (scheduled) | Review with caseworker champions | PENDING |
| Lena Marsh, Data Protection Officer | 2026-09-24 (scheduled) | Review at September Information Governance Group | PENDING |
| Union branch representative | 2026-09-15 (scheduled) | Consultation on workforce commitments | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Project Sponsor (SRO) | Daniel Quist, Director of Resources | PENDING | PENDING |
| Business Owner (Service Owner) | Tom Okafor, Benefits Service Manager | PENDING | PENDING |
| Enterprise Architect | Priya Nandakumar, Head of Digital | PENDING | PENDING |

---

## Appendices

### Appendix A: Stakeholder Interview Summaries

No stakeholder interviews have been conducted yet. This analysis is derived from the governance extract prepared by the Transformation Office in August 2026, the requirements document ARC-001-REQ-v1.0, and sensible defaults for a district council administering Housing Benefit. Interviews are proposed as follows; findings should be added at version 1.1.

#### Proposed interview with Daniel Quist, Director of Resources - week of 2026-09-14

**Key Points** (to confirm):

- Composition of the £180k target and whether it is booked in-year for 2027-28 or as a run-rate
- Attrition assumptions and appetite for a no-compulsory-redundancy commitment
- Position as SIRO and residual risk acceptance

**Quotes**:

- To be captured at interview

**Follow-up Actions**:

- Obtain 2025-26 service budget baseline and monthly overtime figures

#### Proposed interview with Tom Okafor, Benefits Service Manager - week of 2026-09-07

**Key Points** (to confirm):

- Current days to decision, incomplete claim rate and backlog by office
- Lessons from the last system change and what training would have prevented
- Nomination of caseworker champions in each office

**Quotes**:

- To be captured at interview

**Follow-up Actions**:

- Obtain last four quarterly DWP performance returns

#### Proposed interview with Lena Marsh, Data Protection Officer - week of 2026-09-21

**Key Points** (to confirm):

- DPIA scope, timetable and Information Governance Group dates through to February 2027
- Position on six-year retention (DR-002) and document-level retention
- Processor due diligence expectations for any supplier

**Quotes**:

- To be captured at interview

**Follow-up Actions**:

- Schedule DPIA discovery workshop

#### Proposed consultation with union branch representative - week of 2026-09-14

**Key Points** (to confirm):

- Specific failings of the last rollout and what commitments would rebuild confidence
- Preferred consultation cadence and format

**Quotes**:

- To be captured at consultation

**Follow-up Actions**:

- Draft written workforce commitments for Board approval

---

### Appendix B: Survey Results

No stakeholder or claimant survey has been conducted. A caseworker confidence survey (five-point scale, before and after training) and an end-of-transaction claimant survey using the GOV.UK feedback pattern are defined under G-5 and G-9 and should be baselined in discovery.

---

### Appendix C: References

- ARC-001-REQ-v1.0 Requirements: Housing Benefits Portal (BR-001, BR-002, FR-001, FR-002, DR-001, DR-002)
- Ashcombe District Council: Digital and Benefits Governance (extract), Transformation Office, August 2026 (`external/org-structure.md`)
- Government Functional Standard GovS 005: Digital
- Government Functional Standard GovS 007: Security
- Local Digital Declaration (MHCLG)
- UK GDPR Article 35 and ICO DPIA guidance
- DWP Housing Benefit subsidy guidance and speed-of-processing statistics
- No architecture principles document exists yet in 000-global; recommend `/arckit:principles` before the first Design Authority ADR review

---

## External References

> This section provides traceability from generated content back to source documents.
> Follow citation instructions in the project's citation reference guide.

### Document Register

| Doc ID | Filename | Type | Source Location | Description |
|--------|----------|------|-----------------|-------------|
| OS | org-structure.md | Governance extract / organisation chart | 001-benefits-portal/external/ | Ashcombe District Council reporting lines, governance boards and known tensions for the Digital and Benefits functions, prepared by the Transformation Office, August 2026 |

### Citations

| Citation ID | Doc ID | Page/Section | Category | Quoted Passage |
|-------------|--------|--------------|----------|----------------|
| [OS-C1] | OS | Reporting lines | Stakeholder Need | "Chief Executive: Margaret Ellery. Accountable to Full Council." |
| [OS-C2] | OS | Reporting lines | Stakeholder Need | "Director of Resources: Daniel Quist. Owns the Revenues and Benefits service and its budget; the Section 151 officer." |
| [OS-C3] | OS | Reporting lines | Design Decision | "Head of Digital: Priya Nandakumar. Chairs the Design Authority, which approves architecture decisions and any new supplier." |
| [OS-C4] | OS | Reporting lines | Stakeholder Need | "Benefits Service Manager: Tom Okafor. Service Owner for housing benefits; line-manages 22 caseworkers across two offices." |
| [OS-C5] | OS | Reporting lines | Compliance Constraint | "Data Protection Officer: Lena Marsh. Must sign off any processing of claimant data before go-live." |
| [OS-C6] | OS | Boards | Design Decision | Table of three boards: Design Authority chaired by the Head of Digital, fortnightly, deciding architecture, suppliers and technical standards; Benefits Transformation Board chaired by the Director of Resources, monthly, deciding scope, budget and go-live; Information Governance Group chaired by the DPO, monthly, deciding DPIA sign-off and retention |
| [OS-C7] | OS | Known tensions | Business Requirement | "The Director of Resources has a savings target of £180k a year from the benefits service by 2027-28." |
| [OS-C8] | OS | Known tensions | Risk Factor | "Caseworkers have raised, through their union representative, that the last system change was rolled out without training and increased overtime for three months." |

### Unreferenced Documents

| Filename | Source Location | Reason |
|----------|-----------------|--------|
| README.md | 001-benefits-portal/external/ | Placeholder note describing the purpose of the external directory; no organisational content |

---

**Generated by**: ArcKit `/arckit:stakeholders` command
**Generated on**: 2026-09-03
**ArcKit Version**: 6.13.0
**Project**: Housing Benefits Portal (Project 001)
**AI Model**: Claude Fable 5.1 (claude-fable-5-1)

<!-- arckit-provenance:start -->

## Build Provenance

*Stamped automatically by the ArcKit plugin's `provenance-stamp.mjs` PostToolUse hook. Complements (does not replace) the human-authored footer above. Carries only fields the model can't authoritatively self-report: build context from `.arckit/state.json` and effort levels derived from command frontmatter + the silent-downgrade matrix.*

| Field | Value |
|-------|-------|
| Requested Effort | `high` |
| Effective Effort | _unknown — model not parsed from existing footer_ |
| Stamped at | 2026-09-03T08:09:15.241Z |

<!-- arckit-provenance:end -->
