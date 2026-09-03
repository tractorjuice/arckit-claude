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
| **Distribution** | Benefits Transformation Board, Design Authority, Information Governance Group, project team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-09-03 | ArcKit AI | Initial creation from `/arckit:stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders, their underlying drivers (motivations, concerns, needs), how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to project success metrics.

### Key Findings

The Housing Benefits Portal replaces a paper and telephone claims process at Ashcombe District Council. The dominant driver is financial: the Director of Resources, who is also the Section 151 officer, must deliver £180k a year of savings from the benefits service by 2027-28 [OS-C7], and the portal is the main lever for that. The dominant risk is workforce: the 22 caseworkers who will operate the new service have a documented grievance that the last system change was rolled out without training and cost them three months of overtime [OS-C8]. These two facts pull in opposite directions. Savings that arrive through channel shift and reduced re-keying are compatible with caseworker support; savings that are read as headcount cuts, delivered on a rushed timeline, are not. A third hard constraint sits with the Data Protection Officer, who must sign off all claimant data processing before go-live [OS-C4] and therefore holds an effective veto on the launch date.

### Critical Success Factors

- **Savings are realised through channel shift and automation, not compulsory redundancy**, and the Director of Resources can evidence the £180k in the 2027-28 budget without a staffing dispute.
- **Caseworkers are trained and the service is stable before go-live**, so overtime in the three months after launch does not exceed the pre-launch baseline.
- **DPIA is signed off by the Information Governance Group with time to act on its findings**, so the go-live date is never held hostage to a late data protection objection.
- **Claim decisions reach the 14-day target** (BR-002) so that citizens, elected members and DWP performance reporting all see improvement in the same quarter.
- **All architecture and supplier decisions pass through the Design Authority** on its fortnightly cadence [OS-C6], so the portal lands on the council's PostgreSQL platform (DR-001) without a shadow procurement.

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Senior officers agree on the destination: an online claims channel that is cheaper to run and faster for claimants. They do not yet agree on the route. The savings target is fixed and time-bound, while the caseworkers' representative is asking for a slower, better-supported rollout and the DPO controls a gate that cannot be compressed. Alignment will rise to HIGH if the Benefits Transformation Board adopts a phased go-live (private beta, then public launch) with a published training plan and a savings profile that relies on attrition and non-staff costs. It will fall to LOW if savings are presented as a headcount reduction before the portal has proved it can absorb the workload.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Daniel Quist | Director of Resources, Section 151 officer; owns Revenues and Benefits service and budget [OS-C1]; chairs Benefits Transformation Board [OS-C6] | HIGH | HIGH | Senior Responsible Owner. Monthly board, savings tracker, go-live decision |
| Priya Nandakumar | Head of Digital; chairs Design Authority [OS-C2] | HIGH | HIGH | Architecture and supplier approval, fortnightly Design Authority, document owner |
| Tom Okafor | Benefits Service Manager; Service Owner for housing benefits; line-manages 22 caseworkers across two offices [OS-C3] | MEDIUM | HIGH | Service Owner. Weekly delivery contact, owns training and cut-over plan |
| Lena Marsh | Data Protection Officer; chairs Information Governance Group; must sign off claimant data processing before go-live [OS-C4] | HIGH | MEDIUM | DPIA drafted early, monthly IGG updates, no surprises |
| Margaret Ellery | Chief Executive; accountable to Full Council [OS-C5] | HIGH | LOW | Quarterly briefing, escalation point, reputational assurance |
| Housing benefit caseworkers (22 staff, two offices) | Benefits service operations [OS-C3] | LOW | HIGH | Co-design workshops, named champions per office, training before go-live |
| Union representative | Staff-side representation for caseworkers [OS-C8] | MEDIUM | HIGH | Early consultation, written training commitment, joint review after go-live |
| Transformation Office | Programme support, author of governance extract | MEDIUM | HIGH | Delivery management, board papers, benefits tracking |
| Platform and infrastructure team | Operates the council PostgreSQL platform service (DR-001) | MEDIUM | MEDIUM | Capacity and backup planning, runbooks, on-call arrangements |
| Customer services and reception staff | Front door for claimants who cannot use the portal | LOW | MEDIUM | Assisted digital training, scripts, feedback loop |
| Finance and audit team | Supports the Section 151 officer; DWP subsidy claim preparation | MEDIUM | MEDIUM | Savings validation, subsidy reconciliation checks |

### External Stakeholders

| Stakeholder | Organization | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Housing benefit claimants | Residents of Ashcombe district, mainly pension-age and supported or temporary accommodation cases | Beneficiary | LOW | HIGH |
| Landlords and housing associations | Payees for many housing benefit awards | Beneficiary | LOW | MEDIUM |
| Department for Work and Pensions (DWP) | Sets housing benefit rules, pays subsidy, publishes speed-of-processing statistics | Oversight and funder | HIGH | MEDIUM |
| Information Commissioner's Office (ICO) | UK GDPR regulator | Oversight | HIGH | LOW |
| Full Council and Portfolio Holder for Resources | Elected members | Governance and scrutiny | HIGH | MEDIUM |
| External auditor | Audits council accounts and housing benefit subsidy claim | Oversight | MEDIUM | LOW |
| Local Government and Social Care Ombudsman | Handles maladministration complaints | Oversight | MEDIUM | LOW |
| Citizens Advice and welfare rights advisers | Support claimants through applications | Partner | LOW | HIGH |
| Portal delivery supplier (if procured) | Software or services supplier approved by Design Authority | Supplier | MEDIUM | HIGH |

### UK Government Digital Roles (GovS 005)

> The [Government Functional Standard for Digital (GovS 005)](https://www.gov.uk/government/publications/government-functional-standard-govs-005-digital) defines mandatory digital governance roles. Ashcombe District Council is a local authority, so GovS 005 is not binding, but the roles are used here as a sensible default so that the council's structure maps cleanly onto recognised accountabilities.

| Role | Responsibility | Typical Power/Interest | Engagement Strategy |
|------|---------------|----------------------|---------------------|
| Senior Responsible Owner (SRO) | Daniel Quist, Director of Resources. Accountable for outcomes, budget and the £180k savings [OS-C1] [OS-C7] | HIGH / HIGH | Manage Closely. Chairs Benefits Transformation Board, owns go-live decision |
| Service Owner | Tom Okafor, Benefits Service Manager [OS-C3] | HIGH / HIGH | Manage Closely. Weekly service reviews, owns operational readiness |
| Product Manager | To be appointed from the Transformation Office; prioritises features against claimant and caseworker needs | MEDIUM / HIGH | Keep Informed. Sprint reviews, roadmap input |
| Delivery Manager | To be appointed from the Transformation Office; manages cadence, risks and board papers | MEDIUM / HIGH | Keep Informed. Stand-ups, risk log |
| CDDO (Central Digital & Data Office) | Not applicable to a district council; no spend control submission required | LOW / LOW | Monitor. Apply the Technology Code of Practice voluntarily |
| CDIO (Chief Digital Information Officer) | Priya Nandakumar, Head of Digital, fulfils this role [OS-C2] | HIGH / HIGH | Manage Closely. Design Authority chair |
| DDaT Profession Lead | Head of Digital, as the council's senior digital professional | LOW / MEDIUM | Monitor. Capability planning for in-house support of the portal |

### UK Government Security Roles (GovS 007)

> The [Government Functional Standard for Security (GovS 007)](https://www.gov.uk/government/publications/government-functional-standard-govs-007-security) defines mandatory protective security roles. Mapped to the council's structure as a sensible default.

| Role | Responsibility | Typical Power/Interest | Engagement Strategy |
|------|---------------|----------------------|---------------------|
| Senior Security Risk Owner (SSRO) | Margaret Ellery, Chief Executive, as the officer accountable to Full Council [OS-C5] | HIGH / LOW | Keep Satisfied. Quarterly risk summary |
| Departmental Security Officer (DSO) | Head of Digital, acting security lead for council systems | HIGH / MEDIUM | Keep Satisfied. Security gates at Design Authority |
| Senior Information Risk Owner (SIRO) | Director of Resources, as owner of the service and its data | HIGH / MEDIUM | Keep Satisfied. Signs risk acceptance alongside DPO sign-off |
| Cyber Security Lead | Platform and infrastructure team lead | MEDIUM / HIGH | Keep Informed. Penetration test scheduling, security architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • Chief Executive  │  • Director of      │
        │  • DPO / IGG        │    Resources (SRO)  │
        │  • Full Council /   │  • Head of Digital  │
 P      │    Portfolio Holder │    (Design Auth.)   │
 O      │  • DWP              │  • Benefits Service │
 W      │  • ICO              │    Manager          │
 E      │  • External auditor │  • Union rep        │
 R      ├─────────────────────┼─────────────────────┤
        │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
   Low  │                     │                     │
        │  • Ombudsman        │  • Caseworkers      │
        │  • Landlords        │  • Claimants        │
        │  • Customer services│  • Platform team    │
        │                     │  • Citizens Advice  │
        │                     │  • Delivery supplier│
        └─────────────────────┴─────────────────────┘
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| Director of Resources (SRO) | HIGH | HIGH | Manage Closely | Monthly Benefits Transformation Board, fortnightly written savings tracker |
| Head of Digital | HIGH | HIGH | Manage Closely | Fortnightly Design Authority, owns this document |
| Benefits Service Manager | MEDIUM | HIGH | Manage Closely | Weekly delivery check-in, owns training and cut-over |
| Union representative | MEDIUM | HIGH | Manage Closely | Monthly consultation, written commitments on training |
| Data Protection Officer | HIGH | MEDIUM | Keep Satisfied | Monthly Information Governance Group, DPIA drafted by end of discovery |
| Chief Executive | HIGH | LOW | Keep Satisfied | Quarterly one-page briefing, escalation only |
| Full Council / Portfolio Holder | HIGH | MEDIUM | Keep Satisfied | Portfolio Holder briefed before each board, member briefing at go-live |
| DWP | HIGH | MEDIUM | Keep Satisfied | Performance statistics returns, no bespoke engagement needed |
| ICO | HIGH | LOW | Keep Satisfied | Engage only if DPIA identifies residual high risk |
| External auditor | MEDIUM | LOW | Keep Satisfied | Subsidy claim audit trail preserved and demonstrated |
| Caseworkers | LOW | HIGH | Keep Informed | Fortnightly show-and-tell, champions in each office, training |
| Claimants | LOW | HIGH | Keep Informed | User research, private beta, plain-English guidance, assisted digital |
| Platform and infrastructure team | MEDIUM | MEDIUM | Keep Informed | Design Authority attendance, runbook reviews |
| Citizens Advice and welfare rights advisers | LOW | HIGH | Keep Informed | Briefing before public launch, feedback channel |
| Delivery supplier | MEDIUM | HIGH | Keep Informed | Sprint reviews, contract governance via Design Authority |
| Landlords | LOW | MEDIUM | Monitor | Letter at go-live, payment schedule unchanged |
| Ombudsman | MEDIUM | LOW | Monitor | Complaints process documented; no proactive engagement |
| Customer services staff | LOW | MEDIUM | Monitor | Assisted digital briefing one month before launch |

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

**Driver Statement**: Deliver a cashable saving of £180k a year from the benefits service in the 2027-28 budget, with the portal as the primary mechanism [OS-C7].

**Context & Background**:
The savings target is already in the council's medium-term financial plan. As Section 151 officer, the Director is personally responsible for the council's financial standing [OS-C1] and will have to explain to Full Council and the external auditor if the target slips. The current paper and telephone process carries print, postage, scanning, re-keying and call-handling costs that an online channel removes. The Director needs the saving to be recognisable in the 2027-28 base budget, which means the portal must be live and shifting volume by the start of that financial year.

**Driver Intensity**: CRITICAL

**Enablers** (What would help):

- A savings profile that itemises non-staff costs (print, post, scanning, telephony) and vacancy management separately, so the total is credible without compulsory redundancy
- Go-live before April 2027 so that a full year of channel shift lands in 2027-28
- A benefits tracker reviewed at every Benefits Transformation Board

**Blockers** (What would hinder):

- A staff-side dispute that delays go-live or forces a slower rollout
- DPIA sign-off arriving late and pushing launch into 2027-28
- Savings double-counted with other Resources directorate initiatives

**Related Stakeholders**:

- Benefits Service Manager (SD-4, SD-5): owns the operational changes that produce the saving
- Caseworkers and union (SD-6): perceive the saving as a threat to jobs
- Chief Executive (SD-8): shares accountability to Full Council for the financial plan

---

### SD-2: Director of Resources - Protect subsidy income and audit standing

**Stakeholder**: Daniel Quist, Director of Resources and Section 151 officer

**Driver Category**: RISK

**Driver Statement**: Ensure the new process does not introduce errors into housing benefit awards that would reduce DWP subsidy or attract audit qualification.

**Context & Background**:
Housing benefit is administered by the council but largely funded by DWP subsidy, which is reduced for local authority error overpayments. The external auditor tests the subsidy claim every year. A portal that captures incomplete or incorrect claim data, or that loses the evidence trail, creates financial exposure that could exceed the saving the portal is meant to deliver. The Section 151 role makes this a personal as well as corporate risk.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- Structured data capture with validation at the point of claim
- Immutable evidence store meeting the six-year retention requirement (DR-002)
- Point-in-time recovery on the PostgreSQL platform (DR-001)

**Blockers** (What would hinder):

- Free-text claim forms that need re-keying and reinterpretation
- Missing audit trail for caseworker decisions and evidence requests

**Related Stakeholders**:

- DWP (SD-10): the same data quality that protects subsidy also feeds DWP statistics
- Finance and audit team: prepares the subsidy claim
- DPO (SD-7): retention and evidence handling overlap with data protection controls

---

### SD-3: Head of Digital - Land the portal on council standards without a new supplier lock-in

**Stakeholder**: Priya Nandakumar, Head of Digital and Design Authority chair

**Driver Category**: STRATEGIC

**Driver Statement**: Deliver the portal as a reference implementation of the council's platform strategy, using the shared PostgreSQL platform service and reusable components, with every architecture and supplier decision approved by the Design Authority [OS-C2].

**Context & Background**:
The Design Authority approves architecture decisions and any new supplier [OS-C2]. The Head of Digital has invested in a shared platform (evidenced by DR-001 mandating the council's PostgreSQL service) and needs the first high-profile service on it to succeed. A benefits portal bought as a standalone SaaS product under budget pressure would bypass the platform, fragment support, and undermine the Design Authority's standing. Conversely a successful build on the platform gives the Head of Digital a template for the next services and a stronger case for in-house digital capability.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- Early architecture decision records presented at the fortnightly Design Authority
- Reuse of existing council components (identity, payments, document store) where they exist
- A delivery supplier, if needed, engaged under Design Authority terms rather than a service-line contract

**Blockers** (What would hinder):

- Budget pressure from SD-1 favouring the cheapest quick-to-deploy product
- Platform team capacity to support a new production workload
- Perception that the Design Authority slows delivery

**Related Stakeholders**:

- Director of Resources (SD-1): controls budget and may favour speed over standards
- Platform and infrastructure team: must be ready to operate the service
- Benefits Service Manager (SD-4): needs a product that works for caseworkers, whatever the platform

---

### SD-4: Benefits Service Manager - Hit the 14-day decision target and clear backlog

**Stakeholder**: Tom Okafor, Benefits Service Manager and Service Owner

**Driver Category**: OPERATIONAL

**Driver Statement**: Issue decisions on complete claims within 14 calendar days (BR-002) consistently across both offices, without a backlog building at peak times.

**Context & Background**:
The Service Owner is judged on speed of processing, both internally and through DWP's published statistics. Paper claims arrive incomplete, evidence has to be chased by letter, and every document is scanned and re-keyed. Two offices [OS-C3] mean inconsistent handling and uneven workloads. A portal that captures complete claims, lets caseworkers request evidence digitally (FR-002) and lets claimants save and resume (FR-001) removes the main causes of delay. The Service Owner wants a tool that makes the team's day easier, not a new source of rework.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- Caseworker involvement in designing the evidence request workflow
- Work allocation across both offices from a single queue
- Dashboard showing days-to-decision in real time

**Blockers** (What would hinder):

- Portal launched before caseworkers can process claims through it end to end
- Dual running of paper and portal claims without extra capacity
- Digital claims that still need manual verification of every field

**Related Stakeholders**:

- Caseworkers (SD-6): deliver the outcome day to day
- Claimants (SD-9): benefit directly from faster decisions
- Director of Resources (SD-1): faster processing underpins the savings case

---

### SD-5: Benefits Service Manager - Protect the team from a repeat of the last rollout

**Stakeholder**: Tom Okafor, Benefits Service Manager

**Driver Category**: PERSONAL

**Driver Statement**: Avoid another rollout that damages team morale, generates overtime and lands the manager between the union and senior officers.

**Context & Background**:
The last system change was rolled out without training and increased overtime for three months [OS-C8]. The Service Manager line-manages the 22 caseworkers who lived through that [OS-C3] and will be the first person the union representative approaches if it happens again. The manager's credibility with the team, and with the Director of Resources, depends on this rollout being visibly better managed. This is a personal driver as much as an operational one: a bad launch damages the manager's reputation in both directions.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- Authority to set the training plan and to say no to a go-live date the team is not ready for
- Budget for backfill during training and the first month of live running
- A phased launch (private beta with a small cohort of claims) before full switch-over

**Blockers** (What would hinder):

- Go-live date fixed by the savings profile before readiness is known
- Training treated as a supplier deliverable rather than a service activity

**Related Stakeholders**:

- Caseworkers and union representative (SD-6): the manager's primary constituency
- Director of Resources (SD-1): sets the timeline pressure
- Transformation Office: must plan training and cut-over, not just the build

---

### SD-6: Caseworkers and union representative - Training, workload and job security

**Stakeholder**: 22 housing benefit caseworkers across two offices, represented by their union representative

**Driver Category**: PERSONAL

**Driver Statement**: Be trained before the new system goes live, avoid unpaid or forced overtime, and have clarity on whether the savings target means fewer jobs.

**Context & Background**:
The union representative has already put on record that the last change was rolled out without training and increased overtime for three months [OS-C8]. Caseworkers now hear of a £180k savings target [OS-C7] and a portal that removes manual work, and will reasonably read that as a threat to posts. Their power is low individually but the union representative can escalate to elected members and can make go-live contentious. Their interest is high because the tool changes every working day. Left unaddressed this driver becomes the project's single largest delivery risk.

**Driver Intensity**: CRITICAL

**Enablers** (What would help):

- Written commitment from the Director of Resources on how savings will be realised (attrition, non-staff costs) and that no compulsory redundancies are planned as a result of the portal
- Training completed and signed off before go-live, with time protected from casework
- Caseworker champions in each office involved in design from discovery onward
- Overtime monitored and reported to the Benefits Transformation Board for three months after launch

**Blockers** (What would hinder):

- Silence from senior officers on the staffing implications
- Training scheduled during the peak claims period
- Portal designed only from the claimant's side, with the caseworker interface an afterthought

**Related Stakeholders**:

- Benefits Service Manager (SD-5): shares the objective, is the natural ally
- Director of Resources (SD-1): source of the perceived threat and the only person who can defuse it
- Portfolio Holder and Full Council (SD-11): potential escalation route for the union

---

### SD-7: Data Protection Officer - Lawful, proportionate processing signed off before go-live

**Stakeholder**: Lena Marsh, Data Protection Officer and Information Governance Group chair

**Driver Category**: COMPLIANCE

**Driver Statement**: Complete and sign off a Data Protection Impact Assessment covering claimant data processing, evidence storage and six-year retention, before any live claimant data enters the portal [OS-C4].

**Context & Background**:
Housing benefit claims contain financial details, tenancy information, household composition and often health or disability information, which is special category data under UK GDPR. A citizen-facing portal is a new processing activity at scale and requires a DPIA. The DPO must sign off any processing of claimant data before go-live [OS-C4] and chairs the monthly Information Governance Group that owns DPIA sign-off and retention decisions [OS-C6]. The DPO's professional exposure is direct: an ICO reprimand would name the DPO's function. The DPO's driver is not to block the project but to be consulted early enough that findings can be fixed rather than argued over at the launch gate.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- DPIA started in discovery and reviewed at each monthly IGG, not presented once at the end
- Retention and deletion designed in (DR-002) rather than bolted on
- Clear data flows including any supplier processing and hosting location

**Blockers** (What would hinder):

- Supplier or hosting decisions made before data flows are documented
- Go-live date announced publicly before DPIA sign-off
- Evidence documents stored outside the council's controlled platform

**Related Stakeholders**:

- Director of Resources as SIRO: co-signs risk acceptance
- Head of Digital (SD-3): architecture decisions define the data flows
- ICO: engaged only if residual high risk remains

---

### SD-8: Chief Executive - Corporate reputation and accountability to Full Council

**Stakeholder**: Margaret Ellery, Chief Executive

**Driver Category**: RISK

**Driver Statement**: Ensure the portal delivers a visible service improvement and the planned savings without a public failure, staff dispute or data incident that reaches Full Council or the local press.

**Context & Background**:
The Chief Executive is accountable to Full Council [OS-C5] for both the financial plan (which contains the £180k) and the council's operational reputation. Housing benefit claimants are among the district's most vulnerable residents, so a failed launch generates member casework, ombudsman complaints and press coverage quickly. The Chief Executive's interest in the detail is low but the power to stop, redirect or re-resource the project is absolute. The Chief Executive also wants a digital success story to point to when Full Council next debates the transformation programme.

**Driver Intensity**: MEDIUM

**Enablers** (What would help):

- A one-page quarterly briefing with savings, readiness and risk in plain terms
- Early warning of any staff-side escalation before it reaches members
- A launch communication plan agreed with the Portfolio Holder

**Blockers** (What would hinder):

- Surprises: a go-live slip or dispute the Chief Executive hears about from a member first
- Over-promising on timelines in public before readiness is known

**Related Stakeholders**:

- Director of Resources (SD-1, SD-2): direct report and SRO
- Full Council and Portfolio Holder (SD-11)
- Union representative (SD-6): potential source of escalation

---

### SD-9: Claimants - A claim that can be made from home, saved, and decided quickly

**Stakeholder**: Housing benefit claimants in Ashcombe district, and the advisers who support them

**Driver Category**: CUSTOMER

**Driver Statement**: Submit a claim online without visiting an office (BR-001), save and return to it (FR-001), understand what evidence is needed, and receive a decision within 14 days (BR-002), with an accessible alternative for those who cannot use the portal.

**Context & Background**:
Housing benefit today is mostly claimed by pension-age households and by people in supported or temporary accommodation, since working-age claimants have largely moved to Universal Credit. Many claimants have limited digital confidence, no printer or scanner, and are in rent arrears while they wait. A visit to the office is a cost in bus fares and time. Citizens Advice and welfare rights advisers often complete claims on their behalf. The driver is speed and simplicity, but the risk is digital exclusion: a portal that assumes a confident user with a smartphone will fail the people it is meant to help.

**Driver Intensity**: HIGH

**Enablers** (What would help):

- User research with pension-age claimants and advisers before design is fixed
- Photo upload of evidence from a phone; no requirement to scan
- Assisted digital route through customer services and advisers, with the same portal used on their behalf
- WCAG 2.2 AA accessibility and plain-English content

**Blockers** (What would hinder):

- Closing the paper channel before the assisted route is proven
- Identity verification steps that pension-age claimants cannot complete
- Evidence requests that are unclear about what is acceptable

**Related Stakeholders**:

- Benefits Service Manager (SD-4): faster decisions serve both
- Landlords (SD-12): receive payment sooner when decisions are quicker
- Citizens Advice and welfare rights advisers: intermediaries who need portal access on behalf of clients

---

### SD-10: DWP - Accurate awards and timely performance returns

**Stakeholder**: Department for Work and Pensions, as policy owner and subsidy funder

**Driver Category**: COMPLIANCE

**Driver Statement**: Receive accurate housing benefit performance data and a subsidy claim with low local authority error, and see the council process new claims and change events within published targets.

**Context & Background**:
DWP publishes quarterly speed-of-processing statistics for every local authority and reduces subsidy where local authority error overpayments exceed thresholds. DWP does not engage with individual council IT projects, but its statistics are how the council's performance becomes public and comparable. The portal's data quality and processing time directly determine what DWP reports about Ashcombe.

**Driver Intensity**: MEDIUM

**Enablers** (What would help):

- Structured claim data that maps cleanly to DWP reporting
- Change-of-circumstances captured through the same portal

**Blockers** (What would hinder):

- Data quality regressions during cut-over
- Manual workarounds that break the audit trail

**Related Stakeholders**:

- Director of Resources (SD-2): subsidy exposure
- Finance and audit team: prepares the return

---

### SD-11: Full Council and Portfolio Holder for Resources - Visible improvement, no casework spike

**Stakeholder**: Elected members, led by the Portfolio Holder for Resources

**Driver Category**: STRATEGIC

**Driver Statement**: Be able to tell residents that benefit claims are quicker and easier, that money has been saved, and that no vulnerable residents were left behind.

**Context & Background**:
Members hear about benefits through casework: residents who cannot get through on the phone or are waiting for a decision. The Portfolio Holder will be asked in council meetings about the savings and about digital exclusion. Members also carry the political consequences of any staff dispute the union chooses to escalate. Their power is high, exercised through Full Council, but their day-to-day interest is medium and episodic.

**Driver Intensity**: MEDIUM

**Enablers** (What would help):

- Portfolio Holder briefed before each Benefits Transformation Board so no decision surprises them
- A member briefing note at go-live with the assisted digital offer explained
- Casework volumes on benefits tracked before and after launch

**Blockers** (What would hinder):

- Launch during a pre-election period or in a month with high rent-arrears casework
- No answer ready on digital exclusion

**Related Stakeholders**:

- Chief Executive (SD-8)
- Union representative (SD-6): possible escalation route
- Claimants (SD-9)

---

### SD-12: Landlords and housing associations - Prompt and predictable payment

**Stakeholder**: Private landlords and housing associations receiving direct housing benefit payments

**Driver Category**: CUSTOMER

**Driver Statement**: Receive housing benefit payments promptly after a claim is decided, with no disruption to payment schedules during the change.

**Context & Background**:
Many awards are paid direct to the landlord. Delays in decisions translate into rent arrears, eviction risk and pressure on the council's homelessness service. Landlords are not users of the portal but are affected by its performance. Their interest is medium and their power low, exercised mainly through complaints to members.

**Driver Intensity**: LOW

**Enablers** (What would help):

- Payment runs unchanged by the portal launch
- Landlord notification of decisions continues in the current form

**Blockers** (What would hinder):

- Cut-over that pauses decisions for more than a week

**Related Stakeholders**:

- Claimants (SD-9)
- Benefits Service Manager (SD-4)

---

## Driver-to-Goal Mapping

### Goal G-1: Shift 70% of new housing benefit claims to the online channel within six months of public launch

**Derived From Drivers**: SD-1, SD-4, SD-9, SD-11

**Goal Owner**: Tom Okafor, Benefits Service Manager

**Goal Statement**: By 30 September 2027, at least 70% of new housing benefit claims and 60% of change-of-circumstances notifications are submitted through the portal (including assisted submissions by advisers or customer services on the claimant's behalf), up from 0% today.

**Why This Matters**: Channel shift is the mechanism that produces the non-staff savings in SD-1 and removes the scanning and re-keying that delays decisions in SD-4. Counting assisted submissions keeps the goal honest about digital exclusion (SD-9).

**Success Metrics**:

- **Primary Metric**: Percentage of new claims received via the portal, monthly
- **Secondary Metrics**:
  - Percentage of change-of-circumstances notifications received via the portal
  - Percentage of portal claims submitted with an assisted digital flag
  - Percentage of claims received complete on first submission

**Baseline**: 0% online. All claims by paper form or telephone, with a completeness rate on first submission to be measured in discovery and assumed at 55% pending measurement.

**Target**: 70% new claims online and 60% changes online by 30 September 2027; 85% of portal claims complete on first submission.

**Measurement Method**: Portal submission log and benefits case management system intake reports, reconciled monthly by the Transformation Office.

**Dependencies**:

- Public launch by 31 March 2027 (assumed date; see G-3)
- Assisted digital route live in customer services and with Citizens Advice before public launch
- Paper channel retained throughout 2027-28 as a fallback

**Risks to Achievement**:

- Pension-age claimants continue to prefer paper; assisted route undersized
- Identity verification design excludes claimants without photo ID or smartphone

---

### Goal G-2: Issue decisions on complete claims within 14 calendar days

**Derived From Drivers**: SD-4, SD-9, SD-10, SD-11, SD-12

**Goal Owner**: Tom Okafor, Benefits Service Manager

**Goal Statement**: By 30 September 2027, the average time from complete submission to decision is 14 calendar days or fewer (BR-002), and 90% of complete claims are decided within 14 days, across both offices.

**Why This Matters**: This is the single metric that claimants, landlords, members and DWP statistics all observe. It is the operational proof that the portal has removed the delays in the paper process.

**Success Metrics**:

- **Primary Metric**: Average calendar days from complete submission to decision
- **Secondary Metrics**:
  - Percentage of complete claims decided within 14 days
  - Average days from evidence request to evidence received
  - Variance in days-to-decision between the two offices

**Baseline**: To be measured in discovery from the case management system. Assumed at 24 calendar days average pending measurement, consistent with a paper process that chases evidence by post.

**Target**: 14 days average and 90% within 14 days by 30 September 2027; office variance under 2 days.

**Measurement Method**: Case management system timestamps for complete-submission and decision events, reported weekly to the Service Owner and monthly to the Benefits Transformation Board. DWP quarterly speed-of-processing return as external validation.

**Dependencies**:

- Digital evidence request workflow (FR-002) live at launch
- Single work queue across both offices
- Caseworkers trained on the new workflow before go-live (G-4)

**Risks to Achievement**:

- Dual running of paper and portal claims consumes capacity
- Backlog from cut-over masks the improvement for the first quarter

---

### Goal G-3: Realise £180k of recurring savings in the 2027-28 budget without compulsory redundancy

**Derived From Drivers**: SD-1, SD-2, SD-6, SD-8

**Goal Owner**: Daniel Quist, Director of Resources

**Goal Statement**: By 31 March 2028, the benefits service base budget for 2027-28 shows £180k of validated recurring savings attributable to the portal [OS-C7], with the saving composed of non-staff costs (print, postage, scanning, telephony, storage) and vacancy management, and no compulsory redundancies arising from the project.

**Why This Matters**: The saving is the Director's non-negotiable driver (SD-1). Composing it explicitly from non-staff costs and attrition is what converts the caseworkers' critical driver (SD-6) from a blocker into something they can live with, and protects the Chief Executive (SD-8) from a staff dispute reaching Full Council.

**Success Metrics**:

- **Primary Metric**: Validated recurring saving in 2027-28 base budget, pounds
- **Secondary Metrics**:
  - Non-staff cost lines reduced (print, post, scanning, telephony) versus 2025-26 outturn
  - Posts released through attrition, count
  - Compulsory redundancies attributable to the project (target zero)

**Baseline**: £0 saved. 2025-26 outturn for the benefits service to be extracted by the finance team as the reference year.

**Target**: £180k recurring by 31 March 2028, with an indicative composition of £70k non-staff costs and £110k vacancy management, to be confirmed by the finance team in the business case.

**Measurement Method**: Finance team savings tracker, reviewed monthly at the Benefits Transformation Board and validated by the Section 151 officer at year end.

**Dependencies**:

- Public launch by 31 March 2027 (assumed) so that channel shift affects the full 2027-28 year
- Savings profile agreed with the union representative before launch
- G-1 channel shift achieved

**Risks to Achievement**:

- Launch slips into 2027-28, leaving only a part-year saving
- Attrition does not occur on the assumed profile
- Portal running costs (hosting, licences, support) offset more of the saving than planned

---

### Goal G-4: Every caseworker trained and signed off before go-live, with overtime held at baseline

**Derived From Drivers**: SD-5, SD-6, SD-8

**Goal Owner**: Tom Okafor, Benefits Service Manager

**Goal Statement**: 100% of the 22 caseworkers [OS-C3] complete role-based training and a competency sign-off at least two weeks before private beta, and paid overtime in the benefits service for the three months after public launch does not exceed the average of the three months before it.

**Why This Matters**: This goal directly answers the union's complaint about the last rollout [OS-C8]. It is the measurable commitment that turns the caseworkers from resisters into participants and protects the Service Manager's standing (SD-5).

**Success Metrics**:

- **Primary Metric**: Percentage of caseworkers with signed-off training before private beta
- **Secondary Metrics**:
  - Overtime hours per month, three months pre-launch versus three months post-launch
  - Caseworker confidence score from a short pulse survey before and after launch
  - Number of caseworker champions per office (target two per office)

**Baseline**: No training delivered. Overtime baseline to be extracted from payroll for the three months preceding private beta.

**Target**: 100% trained before private beta; post-launch overtime at or below pre-launch average; confidence score improved by at least one point on a five-point scale.

**Measurement Method**: Training register held by the Service Manager; payroll overtime report; pulse survey run by the Transformation Office.

**Dependencies**:

- Backfill budget approved by the Benefits Transformation Board for training days
- Training environment with realistic test claims available six weeks before private beta

**Risks to Achievement**:

- Training scheduled into peak claims period
- Supplier delivers system late, compressing the training window

---

### Goal G-5: DPIA signed off by the Information Governance Group at least six weeks before public launch

**Derived From Drivers**: SD-7, SD-2, SD-8

**Goal Owner**: Lena Marsh, Data Protection Officer

**Goal Statement**: A DPIA covering claimant data capture, evidence storage, supplier processing and six-year retention (DR-002) is approved by the Information Governance Group [OS-C6] no later than six weeks before public launch, with all high residual risks either mitigated or formally accepted by the SIRO, and zero ICO-reportable incidents in the first year of operation.

**Why This Matters**: The DPO holds a mandatory sign-off before go-live [OS-C4]. Setting a six-week buffer converts that gate from a launch-date risk into a planned milestone and gives the Head of Digital time to change the architecture if findings require it.

**Success Metrics**:

- **Primary Metric**: Date of IGG approval relative to public launch date, weeks
- **Secondary Metrics**:
  - Number of DPIA iterations reviewed at IGG before approval (target three or more, showing early engagement)
  - Number of high residual risks at approval (target zero without SIRO acceptance)
  - ICO-reportable incidents in the first 12 months (target zero)

**Baseline**: No DPIA exists. No portal processing of claimant data.

**Target**: IGG approval by 15 February 2027 for a public launch assumed at 31 March 2027.

**Measurement Method**: IGG minutes; DPIA version history; council incident log.

**Dependencies**:

- Data flows documented by the end of discovery
- Hosting and any supplier decisions confirmed by the Design Authority before DPIA finalisation

**Risks to Achievement**:

- Supplier contract terms for processing not agreed in time
- Special category data handling (health, disability) requires design changes late

---

### Goal G-6: All architecture and supplier decisions approved by the Design Authority, with the portal running on the council PostgreSQL platform service

**Derived From Drivers**: SD-3, SD-2, SD-7

**Goal Owner**: Priya Nandakumar, Head of Digital

**Goal Statement**: By public launch, every architecture decision record and any supplier engagement for the portal has a recorded Design Authority approval [OS-C2], the portal's claim records are held in the council's PostgreSQL platform service with point-in-time recovery (DR-001), and at least two existing council components are reused rather than rebuilt.

**Why This Matters**: This is how the Head of Digital's strategic driver (SD-3) becomes verifiable, and it also delivers the recoverability and evidence integrity that the Section 151 officer (SD-2) and DPO (SD-7) need.

**Success Metrics**:

- **Primary Metric**: Percentage of architecture decision records with Design Authority approval before implementation
- **Secondary Metrics**:
  - Count of reused council components
  - Point-in-time recovery tested successfully before launch (yes/no)
  - Number of suppliers engaged without prior Design Authority approval (target zero)

**Baseline**: No decisions recorded; no components identified.

**Target**: 100% of decisions approved; two or more reused components; recovery test passed by 28 February 2027.

**Measurement Method**: Design Authority minutes and architecture decision record log; platform team recovery test report.

**Dependencies**:

- Design Authority fortnightly cadence [OS-C6] maintained through the delivery period
- Platform team capacity to onboard a new production workload

**Risks to Achievement**:

- Budget pressure leads to a standalone SaaS product being proposed outside the Design Authority
- Platform service lacks a feature the portal needs, forcing an exception

---

### Goal G-7: Accessible and inclusive service with a proven assisted digital route

**Derived From Drivers**: SD-9, SD-11, SD-8

**Goal Owner**: Product Manager (Transformation Office), on behalf of the Service Owner

**Goal Statement**: By public launch, the portal meets WCAG 2.2 AA, has been tested with at least 15 claimants including pension-age and supported-accommodation users, offers save-and-resume (FR-001) and phone-photo evidence upload, and an assisted digital route is live through customer services and at least one advice partner.

**Why This Matters**: Without this, the channel shift in G-1 excludes the very claimants the service exists for, and members (SD-11) and the Chief Executive (SD-8) face the digital exclusion question without an answer.

**Success Metrics**:

- **Primary Metric**: Accessibility audit result against WCAG 2.2 AA (pass/fail with issue count)
- **Secondary Metrics**:
  - Number of claimants in usability research, by group
  - Task completion rate in usability testing (target 80% or better)
  - Assisted digital submissions as a share of all portal submissions

**Baseline**: No portal. Paper form accessibility never assessed.

**Target**: WCAG 2.2 AA pass with no critical issues; 15 or more research participants; 80% task completion; assisted route live at launch.

**Measurement Method**: Third-party or in-house accessibility audit report; user research records; portal submission log.

**Dependencies**:

- User research budget and recruitment of pension-age participants through advice partners
- Customer services staff trained on the portal one month before launch

**Risks to Achievement**:

- Identity verification approach excludes users without photo ID
- Research skipped under timeline pressure

---

### Goal G-8: Digital evidence handling with automated six-year retention

**Derived From Drivers**: SD-4, SD-2, SD-7, SD-10

**Goal Owner**: Priya Nandakumar, Head of Digital, with the Service Owner

**Goal Statement**: By public launch, caseworkers can request further evidence against a claim through the portal (FR-002), claimants can upload it from a phone, and evidence documents are retained for six years after claim closure and then deleted automatically (DR-002), with an audit trail covering every request, upload and deletion.

**Why This Matters**: Evidence chasing by post is the largest single cause of delay in SD-4. Automated retention satisfies both the DPO's data minimisation concern (SD-7) and the auditor's need for a complete evidence trail (SD-2, SD-10).

**Success Metrics**:

- **Primary Metric**: Average days from evidence request to evidence received
- **Secondary Metrics**:
  - Percentage of evidence received through the portal rather than post or counter
  - Retention rule tested and verified (yes/no)
  - Audit trail completeness in sample audit (target 100%)

**Baseline**: Evidence requested by letter; assumed 12 days average turnaround pending measurement. No automated retention.

**Target**: 5 days average by 30 September 2027; 80% of evidence via portal; retention rule verified before launch.

**Measurement Method**: Case management system and portal event logs; retention test report from the platform team; finance team sample audit.

**Dependencies**:

- Document store on or integrated with the PostgreSQL platform (G-6)
- Retention policy confirmed by the IGG

**Risks to Achievement**:

- File size and format constraints frustrate phone uploads
- Retention start event (claim closure) ambiguously defined

---

## Goal-to-Outcome Mapping

### Outcome O-1: Online channel adopted and cheaper to run

**Supported Goals**: G-1, G-7, G-8

**Outcome Statement**: 70% of new housing benefit claims arrive online by 30 September 2027, and the cost per claim processed falls by at least 30% against the 2025-26 baseline.

**Measurement Details**:

- **KPI**: Percentage of claims received online; cost per claim processed
- **Current Value**: 0% online; cost per claim to be calculated by the finance team from 2025-26 outturn divided by claims received
- **Target Value**: 70% online; cost per claim reduced by 30%
- **Measurement Frequency**: Monthly
- **Data Source**: Portal submission log, case management intake report, finance team cost model
- **Report Owner**: Transformation Office, validated by finance team

**Business Value**:

- **Financial Impact**: Non-staff cost reduction feeding G-3; indicative £70k a year in print, post, scanning and telephony
- **Strategic Impact**: First citizen-facing service on the council platform, template for future services
- **Operational Impact**: Complete claims on first submission reduce rework and re-keying
- **Customer Impact**: Claimants apply from home at any time, with save-and-resume

**Timeline**:

- **Phase 1 (Months 1-3, to December 2026)**: Discovery complete, baselines measured, user research with claimants and advisers done
- **Phase 2 (Months 4-6, to March 2027)**: Private beta with a small cohort of claims; public launch by 31 March 2027
- **Phase 3 (Months 7-12, to September 2027)**: 70% online reached; assisted route embedded
- **Sustainment (Year 2+)**: Paper channel retained as fallback; online share monitored quarterly

**Stakeholder Benefits**:

- **Director of Resources**: Non-staff savings evidenced in the tracker
- **Claimants**: No office visit or postage required
- **Benefits Service Manager**: Fewer incomplete claims to chase

**Leading Indicators** (early signals of success):

- Task completion rate in usability testing above 80%
- Private beta claims submitted complete on first attempt
- Customer services staff confident in assisted route before launch

**Lagging Indicators** (final proof of success):

- Monthly online share at or above 70% for three consecutive months
- Cost per claim in 2027-28 outturn

---

### Outcome O-2: Decisions within 14 days, visible in DWP statistics

**Supported Goals**: G-2, G-4, G-8

**Outcome Statement**: Average time to decision on complete claims is 14 calendar days or fewer by 30 September 2027, and Ashcombe's published DWP speed-of-processing figures improve in the same period.

**Measurement Details**:

- **KPI**: Average calendar days to decision; percentage decided within 14 days
- **Current Value**: Assumed 24 days average pending discovery measurement
- **Target Value**: 14 days average; 90% within 14 days
- **Measurement Frequency**: Weekly internally, quarterly via DWP return
- **Data Source**: Case management system timestamps; DWP speed-of-processing statistics
- **Report Owner**: Benefits Service Manager

**Business Value**:

- **Financial Impact**: Fewer overpayments from late changes; reduced rent arrears pressure on the homelessness budget
- **Strategic Impact**: Public performance comparison improves the council's standing
- **Operational Impact**: Backlog eliminated; consistent handling across two offices
- **Customer Impact**: Claimants and landlords get money sooner

**Timeline**:

- **Phase 1 (Months 1-3)**: Baseline measured; evidence workflow designed with caseworkers
- **Phase 2 (Months 4-6)**: Private beta shows evidence turnaround under 7 days
- **Phase 3 (Months 7-12)**: 14-day average achieved and sustained for a quarter
- **Sustainment (Year 2+)**: Quarterly review against DWP statistics

**Stakeholder Benefits**:

- **Claimants and landlords**: Faster payment
- **Benefits Service Manager**: Performance target met
- **Portfolio Holder**: Fewer casework enquiries about delays
- **DWP**: Better published figures for the authority

**Leading Indicators** (early signals of success):

- Evidence request turnaround in private beta
- Percentage of claims complete on first submission

**Lagging Indicators** (final proof of success):

- Quarterly DWP speed-of-processing figures
- Member casework volumes on benefit delays

---

### Outcome O-3: £180k recurring saving validated by the Section 151 officer

**Supported Goals**: G-3, G-1

**Outcome Statement**: The 2027-28 outturn for the benefits service shows £180k of recurring savings attributable to the portal, validated by the Section 151 officer, with no compulsory redundancies arising from the project [OS-C7].

**Measurement Details**:

- **KPI**: Validated recurring saving, pounds; compulsory redundancies, count
- **Current Value**: £0; zero redundancies
- **Target Value**: £180k; zero redundancies
- **Measurement Frequency**: Monthly tracker, annual validation
- **Data Source**: Finance team savings tracker; HR records
- **Report Owner**: Finance team, signed by the Director of Resources

**Business Value**:

- **Financial Impact**: £180k a year recurring from 2027-28
- **Strategic Impact**: Medium-term financial plan commitment honoured
- **Operational Impact**: Service runs with a smaller non-staff cost base
- **Customer Impact**: None directly; savings protect other council services

**Timeline**:

- **Phase 1 (Months 1-3)**: Savings profile itemised and agreed with the union representative
- **Phase 2 (Months 4-6)**: Launch by 31 March 2027 so channel shift covers the full year
- **Phase 3 (Months 7-12)**: In-year tracking shows savings on profile
- **Sustainment (Year 2+)**: Saving embedded in base budget

**Stakeholder Benefits**:

- **Director of Resources**: Target met and auditable
- **Chief Executive**: Financial plan commitment delivered without dispute
- **Caseworkers**: Savings realised without compulsory redundancy

**Leading Indicators** (early signals of success):

- Print and postage spend falling month on month after launch
- Vacancies held rather than filled, in line with the agreed profile

**Lagging Indicators** (final proof of success):

- 2027-28 outturn validated by the Section 151 officer
- External auditor raises no concern on the subsidy claim

---

### Outcome O-4: Workforce ready and rollout without overtime spike

**Supported Goals**: G-4, G-7

**Outcome Statement**: All 22 caseworkers are trained and signed off before private beta, and overtime in the three months after public launch is at or below the pre-launch average, reversing the pattern of the last rollout [OS-C8].

**Measurement Details**:

- **KPI**: Percentage of caseworkers trained before beta; post-launch overtime versus pre-launch baseline; caseworker confidence score
- **Current Value**: 0% trained; overtime baseline to be extracted from payroll; confidence unmeasured
- **Target Value**: 100% trained; overtime at or below baseline; confidence up one point
- **Measurement Frequency**: Training register weekly during rollout; overtime monthly; survey pre and post launch
- **Data Source**: Training register, payroll, pulse survey
- **Report Owner**: Benefits Service Manager

**Business Value**:

- **Financial Impact**: Avoided overtime cost; avoided cost of a staff dispute
- **Strategic Impact**: Rebuilds trust for future transformation projects
- **Operational Impact**: Service stable through cut-over
- **Customer Impact**: No service dip during launch

**Timeline**:

- **Phase 1 (Months 1-3)**: Champions appointed; union consulted on training plan and savings profile
- **Phase 2 (Months 4-6)**: Training delivered; competency sign-off; private beta
- **Phase 3 (Months 7-12)**: Overtime monitored and reported to the board for three months post launch
- **Sustainment (Year 2+)**: Refresher training built into induction

**Stakeholder Benefits**:

- **Caseworkers**: Trained before being asked to use the system
- **Union representative**: Written commitment honoured and measured
- **Benefits Service Manager**: Team morale and credibility protected

**Leading Indicators** (early signals of success):

- Training attendance on schedule
- Champions reporting positive feedback from show-and-tells

**Lagging Indicators** (final proof of success):

- Overtime report three months after launch
- Post-launch pulse survey result

---

### Outcome O-5: Lawful processing with no data incidents

**Supported Goals**: G-5, G-6, G-8

**Outcome Statement**: The DPIA is approved by the Information Governance Group at least six weeks before public launch, retention is automated, and there are zero ICO-reportable incidents in the first 12 months of live operation.

**Measurement Details**:

- **KPI**: DPIA approval lead time in weeks; ICO-reportable incidents; retention rule verified
- **Current Value**: No DPIA; no portal incidents; no retention automation
- **Target Value**: Six weeks or more; zero incidents; verified
- **Measurement Frequency**: DPIA at each monthly IGG; incidents continuously
- **Data Source**: IGG minutes; council incident log; platform team test report
- **Report Owner**: Data Protection Officer

**Business Value**:

- **Financial Impact**: Avoided ICO enforcement and remediation costs
- **Strategic Impact**: Demonstrates the council can launch citizen data services safely
- **Operational Impact**: Retention handled without manual review
- **Customer Impact**: Claimant data handled proportionately and transparently

**Timeline**:

- **Phase 1 (Months 1-3)**: Data flows documented; DPIA first draft at IGG
- **Phase 2 (Months 4-6)**: DPIA approved by 15 February 2027; retention rule tested
- **Phase 3 (Months 7-12)**: No reportable incidents; first retention review
- **Sustainment (Year 2+)**: DPIA reviewed annually

**Stakeholder Benefits**:

- **Data Protection Officer**: Consulted early, sign-off on time
- **Director of Resources as SIRO**: Risk acceptance informed
- **Head of Digital**: No late architecture changes

**Leading Indicators** (early signals of success):

- DPIA draft reviewed at three or more IGG meetings before approval
- Supplier processing terms agreed before DPIA finalisation

**Lagging Indicators** (final proof of success):

- Twelve months without a reportable incident
- Retention deletions executed on schedule in year seven

---

### Outcome O-6: Claimants satisfied and no one left behind

**Supported Goals**: G-7, G-1, G-2

**Outcome Statement**: At least 80% of portal users rate the service as satisfactory or better in the first six months after launch, and complaints about the benefits service to members and the ombudsman do not increase in 2027-28.

**Measurement Details**:

- **KPI**: Post-submission satisfaction score; benefits complaints count
- **Current Value**: No satisfaction measure; complaints baseline to be extracted from the complaints system for 2025-26
- **Target Value**: 80% satisfied; complaints at or below baseline
- **Measurement Frequency**: Satisfaction continuously, reported monthly; complaints quarterly
- **Data Source**: Portal feedback prompt; corporate complaints system; member casework log
- **Report Owner**: Product Manager, Transformation Office

**Business Value**:

- **Financial Impact**: Avoided ombudsman remedies and complaint handling cost
- **Strategic Impact**: Evidence for members that digital did not exclude residents
- **Operational Impact**: Feedback loop drives continuous improvement
- **Customer Impact**: Simpler, faster claims with support available

**Timeline**:

- **Phase 1 (Months 1-3)**: Research with 15 or more claimants; complaints baseline set
- **Phase 2 (Months 4-6)**: Private beta feedback incorporated; assisted route live
- **Phase 3 (Months 7-12)**: 80% satisfaction reached; complaints monitored
- **Sustainment (Year 2+)**: Quarterly review of feedback themes

**Stakeholder Benefits**:

- **Claimants**: Service designed around their needs
- **Portfolio Holder**: Answer to the digital exclusion question
- **Citizens Advice**: Portal usable on clients' behalf

**Leading Indicators** (early signals of success):

- Usability task completion above 80% in research
- Assisted route used in private beta

**Lagging Indicators** (final proof of success):

- Six-month satisfaction average
- 2027-28 complaints outturn

---

## Complete Traceability Matrix

### Stakeholder → Driver → Goal → Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Director of Resources | SD-1 | £180k recurring savings by 2027-28 | G-3 | £180k saving without compulsory redundancy | O-3 | Saving validated by S151 officer |
| Director of Resources | SD-1 | £180k recurring savings by 2027-28 | G-1 | 70% claims online | O-1 | Online channel adopted, cost per claim down 30% |
| Director of Resources | SD-2 | Protect subsidy and audit standing | G-6 | Design Authority approval, PostgreSQL platform | O-5 | Lawful processing, no incidents |
| Director of Resources | SD-2 | Protect subsidy and audit standing | G-8 | Digital evidence and automated retention | O-5 | Lawful processing, no incidents |
| Head of Digital | SD-3 | Council standards, no supplier lock-in | G-6 | Design Authority approval, PostgreSQL platform | O-5 | Lawful processing, no incidents |
| Head of Digital | SD-3 | Council standards, no supplier lock-in | G-8 | Digital evidence and automated retention | O-1 | Online channel adopted |
| Benefits Service Manager | SD-4 | 14-day decisions, no backlog | G-2 | 14-day average decision time | O-2 | Decisions within 14 days |
| Benefits Service Manager | SD-4 | 14-day decisions, no backlog | G-8 | Digital evidence and automated retention | O-2 | Decisions within 14 days |
| Benefits Service Manager | SD-5 | Avoid repeat of last rollout | G-4 | All caseworkers trained, overtime at baseline | O-4 | Workforce ready, no overtime spike |
| Caseworkers and union | SD-6 | Training, workload, job security | G-4 | All caseworkers trained, overtime at baseline | O-4 | Workforce ready, no overtime spike |
| Caseworkers and union | SD-6 | Training, workload, job security | G-3 | £180k saving without compulsory redundancy | O-3 | Saving validated, zero redundancies |
| Data Protection Officer | SD-7 | DPIA sign-off before go-live | G-5 | DPIA approved six weeks before launch | O-5 | Lawful processing, no incidents |
| Data Protection Officer | SD-7 | DPIA sign-off before go-live | G-8 | Digital evidence and automated retention | O-5 | Lawful processing, no incidents |
| Chief Executive | SD-8 | Reputation and accountability to Full Council | G-3 | £180k saving without compulsory redundancy | O-3 | Saving validated, zero redundancies |
| Chief Executive | SD-8 | Reputation and accountability to Full Council | G-5 | DPIA approved six weeks before launch | O-5 | Lawful processing, no incidents |
| Chief Executive | SD-8 | Reputation and accountability to Full Council | G-7 | Accessible service with assisted route | O-6 | Claimants satisfied, no one left behind |
| Claimants | SD-9 | Claim from home, save, fast decision | G-1 | 70% claims online | O-1 | Online channel adopted |
| Claimants | SD-9 | Claim from home, save, fast decision | G-2 | 14-day average decision time | O-2 | Decisions within 14 days |
| Claimants | SD-9 | Claim from home, save, fast decision | G-7 | Accessible service with assisted route | O-6 | Claimants satisfied, no one left behind |
| DWP | SD-10 | Accurate awards, timely returns | G-2 | 14-day average decision time | O-2 | Decisions within 14 days, DWP figures improve |
| DWP | SD-10 | Accurate awards, timely returns | G-8 | Digital evidence and automated retention | O-5 | Lawful processing, audit trail complete |
| Full Council and Portfolio Holder | SD-11 | Visible improvement, no casework spike | G-1 | 70% claims online | O-1 | Online channel adopted |
| Full Council and Portfolio Holder | SD-11 | Visible improvement, no casework spike | G-2 | 14-day average decision time | O-2 | Decisions within 14 days |
| Full Council and Portfolio Holder | SD-11 | Visible improvement, no casework spike | G-7 | Accessible service with assisted route | O-6 | Claimants satisfied, no one left behind |
| Landlords | SD-12 | Prompt and predictable payment | G-2 | 14-day average decision time | O-2 | Decisions within 14 days |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: The Director of Resources (SD-1) needs £180k of savings recognised in 2027-28 [OS-C7], but caseworkers and their union (SD-6) read the savings target as a threat to posts and remember a rollout without training [OS-C8]. Savings that depend on headcount and an early launch date are incompatible with a well-supported rollout.
  - **Resolution Strategy**: The Director publishes, before design is fixed, a savings profile composed of non-staff costs and vacancy management with an explicit statement that no compulsory redundancies will arise from the portal. In return the union agrees the training plan and go-live criteria (G-4). The Benefits Transformation Board adopts training completion and DPIA sign-off as go-live gates. Any residual gap in the £180k is closed through attrition over 2027-28 and 2028-29 rather than by accelerating launch.

- **Conflict 2**: The Director of Resources (SD-1) wants public launch before April 2027 to secure a full year of savings, but the DPO (SD-7) holds a mandatory sign-off [OS-C4] that cannot be compressed, and the Service Manager (SD-5) wants a phased launch.
  - **Resolution Strategy**: Plan backwards from a 31 March 2027 public launch: DPIA approved by 15 February 2027, private beta from early February with training complete two weeks earlier. The DPIA starts in discovery and is reviewed at every monthly IGG so that findings are addressed incrementally. If the DPIA or readiness slips, the board delays launch rather than launching without sign-off, and the savings profile is re-phased with a part-year effect.

- **Conflict 3**: The Head of Digital (SD-3) requires all decisions and suppliers to go through the Design Authority and the portal to run on the council PostgreSQL platform (DR-001), while budget pressure from SD-1 may favour a standalone SaaS product that is cheaper up front.
  - **Resolution Strategy**: The Design Authority evaluates options on five-year total cost including exit, support and DPIA implications, not licence cost alone. Any SaaS option is assessed against DR-001 and the DPO's data flow requirements before it reaches the Benefits Transformation Board, so the board sees a single recommended option with the platform argument already made.

- **Conflict 4**: Channel shift (G-1) serves savings (SD-1) and speed (SD-4), but claimants (SD-9) include pension-age and vulnerable residents for whom a digital-only route is exclusionary, and members (SD-11) will be asked about this publicly.
  - **Resolution Strategy**: Set the online target at 70% rather than 100%, count assisted submissions toward it, retain the paper channel through 2027-28, and fund the assisted route through customer services and advice partners. Report assisted digital share alongside the online share so exclusion is visible.

**Synergies**:

- **Synergy 1**: The Service Manager's speed driver (SD-4) and the claimants' driver (SD-9) both resolve through the same goal (G-2): digital evidence requests and complete claims on first submission make caseworkers faster and claimants better off simultaneously.
- **Synergy 2**: The Head of Digital's platform driver (SD-3), the Section 151 officer's audit driver (SD-2) and the DPO's compliance driver (SD-7) all point to the same architecture: claim records on the council PostgreSQL platform with point-in-time recovery and automated retention (G-6, G-8). One design decision satisfies three high-power stakeholders.
- **Synergy 3**: The Service Manager (SD-5) and the union representative (SD-6) want the same thing, a trained team and no overtime spike (G-4). The manager is a natural bridge between the union and the Director of Resources.
- **Synergy 4**: A well-managed rollout that hits 14 days (O-2) gives the Chief Executive (SD-8) and Portfolio Holder (SD-11) a public success story and reduces member casework, which in turn lowers the political cost of the savings target.

---

## Communication & Engagement Plan

### Stakeholder-Specific Messaging

#### Daniel Quist, Director of Resources (SRO)

**Primary Message**: The portal will deliver the £180k in 2027-28 on a profile you can defend to the auditor, provided we launch by 31 March 2027 with the team trained and the DPIA signed.

**Key Talking Points**:

- Savings profile itemised as non-staff costs and vacancy management, tracked monthly at your board
- Training and DPIA gates protect you from a staff dispute or data incident that would cost more than the saving
- Structured claim data reduces local authority error and protects subsidy

**Communication Frequency**: Monthly at the Benefits Transformation Board; fortnightly written savings and readiness tracker

**Preferred Channel**: Board paper with a one-page dashboard; short in-person briefing before each board

**Success Story**: The 2027-28 budget shows the £180k, the auditor signs the subsidy claim without comment, and no member has asked about job losses.

---

#### Priya Nandakumar, Head of Digital (Design Authority chair)

**Primary Message**: This is the reference implementation for the council platform. Every decision goes through the Design Authority and lands on the PostgreSQL service.

**Key Talking Points**:

- Architecture decision records presented fortnightly, ahead of implementation
- Reuse targets and platform team readiness tracked as goals
- Total cost of ownership framing pre-empts a standalone SaaS bid

**Communication Frequency**: Fortnightly at the Design Authority; weekly delivery stand-up as document owner

**Preferred Channel**: Design Authority papers; architecture decision record log

**Success Story**: The portal launches on the platform with two reused components and becomes the template cited in the next service business case.

---

#### Tom Okafor, Benefits Service Manager (Service Owner)

**Primary Message**: You set the readiness criteria. The portal does not go live until your team is trained and signed off.

**Key Talking Points**:

- Training plan and go-live criteria owned by you and agreed with the union
- Overtime reported to the board for three months after launch
- Caseworker champions shape the evidence workflow and work queue

**Communication Frequency**: Weekly delivery check-in; monthly board attendance

**Preferred Channel**: In-person weekly meeting; shared readiness checklist

**Success Story**: Decisions average 14 days across both offices, overtime is flat, and the team says this rollout was nothing like the last one.

---

#### Lena Marsh, Data Protection Officer (IGG chair)

**Primary Message**: You will see the DPIA from the first draft in discovery and at every IGG, so sign-off by mid-February 2027 is a planned milestone, not a last-minute request.

**Key Talking Points**:

- Data flows and supplier processing documented before architecture is fixed
- Retention for six years designed in and tested
- SIRO co-signs any residual risk acceptance

**Communication Frequency**: Monthly at the Information Governance Group; ad hoc when architecture changes

**Preferred Channel**: DPIA working document with version history; IGG papers

**Success Story**: DPIA approved six weeks before launch with no high residual risks and no reportable incidents in year one.

---

#### Margaret Ellery, Chief Executive

**Primary Message**: The portal is on track to save £180k and improve a service for vulnerable residents, with staff and data protection risks actively managed.

**Key Talking Points**:

- Savings, readiness and risk on one page
- Early warning of any staff-side or member escalation
- Launch communications agreed with the Portfolio Holder

**Communication Frequency**: Quarterly; immediately on any red risk

**Preferred Channel**: One-page briefing note; short verbal update from the Director of Resources

**Success Story**: Full Council hears about the portal as a success rather than through a question about job cuts or a data breach.

---

#### Caseworkers and union representative

**Primary Message**: You will be trained before go-live, overtime will be watched and reported, and the savings do not depend on compulsory redundancies.

**Key Talking Points**:

- Written commitment from the Director of Resources on the savings profile
- Champions in each office involved from discovery
- Training in protected time with backfill

**Communication Frequency**: Fortnightly show-and-tell for caseworkers; monthly consultation with the union representative

**Preferred Channel**: In-person sessions in both offices; short written updates on the intranet

**Success Story**: The team uses the portal confidently from day one and the union representative confirms at the post-launch review that the commitments were kept.

---

#### Claimants, Citizens Advice and welfare rights advisers

**Primary Message**: Claiming housing benefit will be quicker and can be done from home, and help is available in person if you need it.

**Key Talking Points**:

- Save and return to a claim; upload evidence from a phone
- Paper and assisted routes remain
- Decisions targeted within 14 days

**Communication Frequency**: User research in discovery; briefing to advisers one month before launch; launch communications

**Preferred Channel**: Adviser briefing sessions; plain-English guidance on the council website; letters with awards

**Success Story**: Advisers report the portal is easier than the paper form for their clients and satisfaction is above 80%.

---

#### Full Council and Portfolio Holder for Resources

**Primary Message**: A faster, cheaper benefits service that keeps a paper and assisted route for residents who need it.

**Key Talking Points**:

- Savings delivered without compulsory redundancy
- Digital exclusion addressed through assisted digital and a retained paper channel
- Casework on benefit delays expected to fall

**Communication Frequency**: Portfolio Holder briefed before each monthly board; member briefing note at launch

**Preferred Channel**: Portfolio Holder briefing; member briefing note

**Success Story**: The Portfolio Holder answers a council question on the portal with the 14-day figure and the assisted digital numbers.

---

#### Platform and infrastructure team

**Primary Message**: The portal is a new production workload on your platform; you will be involved in design and have runbooks before launch.

**Key Talking Points**:

- Capacity, backup and point-in-time recovery tested before launch
- Runbooks and on-call arrangements agreed
- Retention automation implemented with you

**Communication Frequency**: Fortnightly at the Design Authority; weekly during cut-over

**Preferred Channel**: Design Authority; operational readiness checklist

**Success Story**: Recovery test passes in February 2027 and the first month of live running produces no platform incidents.

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Caseworkers | Paper claims, scanned and re-keyed; evidence chased by post; two office queues | Structured digital claims; evidence requested and received in portal; single queue | HIGH | HIGH | Champions, training in protected time, written savings commitment, overtime reporting |
| Benefits Service Manager | Manages backlog and two office workloads manually | Real-time days-to-decision dashboard; owns readiness gates | HIGH | LOW | Authority over go-live criteria; backfill budget |
| Claimants | Paper form or phone; office visits; postal evidence | Online claim, save and resume, phone-photo evidence; assisted route | HIGH | MEDIUM | User research, assisted digital, paper channel retained |
| Customer services and reception | Hand out and receive paper forms | Assist claimants to use the portal | MEDIUM | MEDIUM | Training one month before launch; scripts; feedback loop |
| Director of Resources | Savings target unfunded by a specific mechanism | Savings tracked monthly against portal channel shift | MEDIUM | LOW | Board dashboard; clear composition of savings |
| Head of Digital | Platform strategy untested by a citizen-facing service | Platform hosts a live citizen service | MEDIUM | LOW | Design Authority cadence; reuse targets |
| Data Protection Officer | No claimant portal processing | New large-scale processing under DPIA | MEDIUM | LOW | Early and iterative DPIA; retention designed in |
| Platform and infrastructure team | No benefits workload | Production support for the portal | MEDIUM | MEDIUM | Involvement at Design Authority; runbooks; on-call agreed |
| Finance and audit team | Subsidy claim from paper evidence | Subsidy claim from digital audit trail | LOW | LOW | Sample audit of audit trail before launch |
| Citizens Advice and advisers | Complete paper forms with clients | Use portal on clients' behalf | MEDIUM | LOW | Adviser briefing; assisted digital flag |
| Landlords | Receive payments and notifications by post | Unchanged | LOW | LOW | Letter at launch confirming no change |

### Change Readiness

**Champions** (Enthusiastic supporters):

- Priya Nandakumar, Head of Digital: the portal validates the platform strategy and the Design Authority
- Daniel Quist, Director of Resources: the portal is the route to the £180k target
- Citizens Advice and welfare rights advisers: a portal they can use on clients' behalf removes paper handling

**Fence-sitters** (Neutral, need convincing):

- Tom Okafor, Benefits Service Manager: supports the outcome but will withhold commitment until the training plan and go-live criteria are in the manager's control
- Lena Marsh, Data Protection Officer: neutral on the project, will support it if consulted early and will block it if presented with a finished design
- Platform and infrastructure team: supportive in principle, worried about capacity and on-call
- Portfolio Holder: supportive of savings, needs an answer on digital exclusion

**Resisters** (Opposed or skeptical):

- Caseworkers and union representative: sceptical because of the last rollout [OS-C8] and the savings target [OS-C7]. Strategy: written commitment on savings composition and no compulsory redundancy, training before go-live as a formal gate, champions in each office, overtime reported to the board, joint review three months after launch.

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Staff-side dispute delays or disrupts go-live

**Related Stakeholders**: Caseworkers, union representative, Benefits Service Manager, Director of Resources, Portfolio Holder

**Risk Description**: The union representative, citing the last rollout [OS-C8] and the savings target [OS-C7], escalates to members or refuses to cooperate with cut-over, forcing a delay or a launch without caseworker support.

**Impact on Goals**: G-3 (savings phased later), G-4 (training and overtime), G-2 (decision time during cut-over)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Director of Resources issues the savings composition and no-compulsory-redundancy statement in discovery; training and readiness adopted as go-live gates; monthly union consultation; overtime reported to the board.

**Contingency Plan**: Delay public launch by up to one quarter, re-phase savings with a part-year effect, and commission an independent readiness review jointly with the union.

---

### Risk R-2: DPIA sign-off arrives late and blocks launch

**Related Stakeholders**: Data Protection Officer, Head of Digital, Director of Resources as SIRO

**Risk Description**: Data flows, supplier processing or special category data handling are not documented in time, the IGG withholds approval [OS-C4], and the launch date slips.

**Impact on Goals**: G-5, G-3 (part-year savings), G-1

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: DPIA started in discovery and reviewed at every monthly IGG; supplier and hosting decisions taken at the Design Authority before DPIA finalisation; approval target 15 February 2027 with a six-week buffer.

**Contingency Plan**: Launch private beta with a restricted cohort under an interim risk acceptance signed by the SIRO only if the DPO agrees residual risk is low; otherwise hold launch.

---

### Risk R-3: Savings pressure drives a standalone product outside the Design Authority

**Related Stakeholders**: Director of Resources, Head of Digital, Platform team, DPO

**Risk Description**: A low-cost SaaS benefits portal is proposed directly to the Benefits Transformation Board on price, bypassing the Design Authority [OS-C2] and DR-001, fragmenting support and complicating the DPIA.

**Impact on Goals**: G-6, G-8, G-5

**Probability**: LOW

**Impact**: HIGH

**Mitigation Strategy**: Board terms of reference require Design Authority approval before any supplier option is tabled; options compared on five-year total cost including exit and support.

**Contingency Plan**: Design Authority issues a formal exception assessment; Chief Executive arbitrates if the two boards disagree.

---

### Risk R-4: Digital exclusion generates complaints and member pressure

**Related Stakeholders**: Claimants, Portfolio Holder, Chief Executive, customer services

**Risk Description**: Pension-age and vulnerable claimants cannot use the portal, the paper route is under-resourced, and complaints reach members and the ombudsman.

**Impact on Goals**: G-7, G-1, O-6

**Probability**: MEDIUM

**Impact**: MEDIUM

**Mitigation Strategy**: User research with 15 or more claimants including pension-age users; assisted digital route funded and live at launch; paper channel retained through 2027-28; assisted share reported.

**Contingency Plan**: Increase customer services capacity for assisted claims and extend adviser access; slow the paper channel retirement.

---

### Risk R-5: Platform team cannot support the new workload

**Related Stakeholders**: Platform and infrastructure team, Head of Digital, Service Owner

**Risk Description**: The PostgreSQL platform service lacks capacity, on-call cover or a feature the portal needs, causing outages or an exception to DR-001.

**Impact on Goals**: G-6, G-2

**Probability**: MEDIUM

**Impact**: MEDIUM

**Mitigation Strategy**: Platform team attends Design Authority from discovery; capacity and recovery tested by 28 February 2027; runbooks and on-call agreed before private beta.

**Contingency Plan**: Temporary enhanced supplier support for the first three months; Design Authority approves a time-limited exception if a platform feature is missing.

---

### Risk R-6: Senior stakeholder surprise erodes sponsorship

**Related Stakeholders**: Chief Executive, Portfolio Holder, Director of Resources

**Risk Description**: A slip, dispute or incident reaches the Chief Executive or a member before the project reports it, damaging trust and prompting intervention.

**Impact on Goals**: All, through loss of sponsorship

**Probability**: LOW

**Impact**: HIGH

**Mitigation Strategy**: Quarterly one-page briefing to the Chief Executive; Portfolio Holder briefed before each board; red risks escalated the same day.

**Contingency Plan**: Director of Resources briefs the Chief Executive and Portfolio Holder in person with a recovery plan within 48 hours.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Project scope and budget | Delivery Manager | Director of Resources (Benefits Transformation Board) [OS-C6] | Head of Digital, Service Owner, finance team | Chief Executive, Portfolio Holder |
| Savings profile and composition | Finance team | Director of Resources | Service Owner, union representative, HR | Caseworkers, Chief Executive |
| Requirements prioritisation | Product Manager | Service Owner | Caseworker champions, claimants via research, DPO | Design Authority, supplier |
| Architecture decisions and technical standards | Solution architect or delivery supplier | Head of Digital (Design Authority) [OS-C6] | Platform team, DPO, Service Owner | Benefits Transformation Board |
| Supplier selection and engagement | Delivery Manager | Head of Digital (Design Authority) [OS-C2] | Director of Resources, procurement, DPO | Benefits Transformation Board |
| DPIA approval and retention rules | Data Protection Officer | Information Governance Group [OS-C6] | Head of Digital, Service Owner, SIRO | Benefits Transformation Board |
| Training plan and readiness criteria | Service Owner | Service Owner | Union representative, caseworker champions, Transformation Office | Benefits Transformation Board |
| Go/no-go for private beta | Service Owner | Director of Resources | DPO, Head of Digital, platform team | Caseworkers, Chief Executive |
| Go/no-go for public launch | Delivery Manager | Director of Resources (Benefits Transformation Board) [OS-C6] | DPO (sign-off mandatory [OS-C4]), Head of Digital, Service Owner, union representative | Chief Executive, Portfolio Holder, claimants, advisers, landlords |
| Paper channel retirement | Service Owner | Director of Resources | Portfolio Holder, customer services, advisers | Claimants, members |
| Risk acceptance for residual data protection risk | Data Protection Officer | Director of Resources as SIRO | Head of Digital | Chief Executive |

### Escalation Path

1. **Level 1**: Delivery Manager and Product Manager with the Service Owner (day-to-day delivery, priority and readiness decisions)
2. **Level 2**: Design Authority, fortnightly, for architecture, supplier and technical standards [OS-C6]; Information Governance Group, monthly, for data protection and retention [OS-C6]
3. **Level 3**: Benefits Transformation Board, monthly, chaired by the Director of Resources, for scope, budget, go-live and conflicts between Level 2 boards [OS-C6]
4. **Level 4**: Chief Executive, for unresolved conflicts between the Director of Resources and the Head of Digital or DPO, staff-side escalation, and anything likely to reach Full Council [OS-C5]
5. **Level 5**: Full Council and Portfolio Holder, for decisions with political or budgetary consequence beyond officer delegation

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| Daniel Quist, Director of Resources | PENDING | Review requested at next Benefits Transformation Board | PENDING |
| Priya Nandakumar, Head of Digital | PENDING | Document owner; review at next Design Authority | PENDING |
| Tom Okafor, Benefits Service Manager | PENDING | Review of SD-4, SD-5, G-2, G-4 | PENDING |
| Lena Marsh, Data Protection Officer | PENDING | Review of SD-7, G-5 at next Information Governance Group | PENDING |
| Union representative | PENDING | Review of SD-6, G-3, G-4 and Conflict 1 resolution | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Project Sponsor | Daniel Quist, Director of Resources | PENDING | PENDING |
| Business Owner | Tom Okafor, Benefits Service Manager | PENDING | PENDING |
| Enterprise Architect | Priya Nandakumar, Head of Digital | PENDING | PENDING |

---

## Appendices

### Appendix A: Stakeholder Interview Summaries

No stakeholder interviews have been conducted for this version. The drivers above are inferred from the governance extract prepared by the Transformation Office [OS-C1] [OS-C6] [OS-C7] [OS-C8] and from the requirements document ARC-001-REQ-v1.0, applying sensible defaults for a district council housing benefit service. Interviews are recommended before this document moves to IN_REVIEW.

#### Planned interview: Daniel Quist, Director of Resources

**Key Points to confirm**:

- Composition of the £180k savings target and the reference year
- Appetite for a no-compulsory-redundancy commitment
- Preferred launch date relative to the 2027-28 budget

**Follow-up Actions**:

- Finance team to extract 2025-26 benefits service outturn

#### Planned interview: Tom Okafor, Benefits Service Manager

**Key Points to confirm**:

- Current average days to decision and evidence turnaround
- What went wrong in the last rollout and what the team needs this time
- Peak claims periods to avoid for training and cut-over

**Follow-up Actions**:

- Extract case management system timestamps for baseline

#### Planned interview: Union representative

**Key Points to confirm**:

- Specific commitments that would satisfy the training and overtime concern
- Position on savings through attrition

**Follow-up Actions**:

- Draft written commitment for the Director of Resources

#### Planned interview: Lena Marsh, Data Protection Officer

**Key Points to confirm**:

- DPIA template and IGG review cadence
- Position on special category data and supplier processing

**Follow-up Actions**:

- Schedule DPIA first draft for the next IGG

---

### Appendix B: Survey Results

No stakeholder survey has been conducted. A caseworker pulse survey (five questions, five-point scale, covering confidence, workload, training and trust in the rollout) is proposed for discovery and again three months after launch, to provide the baseline and post-launch measure for G-4 and O-4.

---

### Appendix C: References

- ARC-001-REQ-v1.0, Requirements: Housing Benefits Portal (BR-001, BR-002, FR-001, FR-002, DR-001, DR-002)
- Ashcombe District Council: Digital and Benefits Governance (extract), Transformation Office, August 2026 (`external/org-structure.md`)
- Government Functional Standard GovS 005: Digital
- Government Functional Standard GovS 007: Security
- Project README, Project 001 Housing Benefits Portal
- No architecture principles document exists in 000-global at the time of writing; this analysis should be re-checked once `/arckit:principles` has been run

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-09-03 | ArcKit AI | Initial draft from organisation structure extract and requirements |

## External References

> This section provides traceability from generated content back to source documents.
> Follow citation instructions in the project's citation reference guide.

### Document Register

| Doc ID | Filename | Type | Source Location | Description |
|--------|----------|------|-----------------|-------------|
| OS | org-structure.md | Governance extract | 001-benefits-portal/external/ | Ashcombe District Council digital and benefits governance: reporting lines, boards, known tensions. Prepared by the Transformation Office, August 2026 |

### Citations

| Citation ID | Doc ID | Page/Section | Category | Quoted Passage |
|-------------|--------|--------------|----------|----------------|
| OS-C1 | OS | Reporting lines | Stakeholder Need | "Director of Resources: Daniel Quist. Owns the Revenues and Benefits service and its budget; the Section 151 officer." |
| OS-C2 | OS | Reporting lines | Design Decision | "Head of Digital: Priya Nandakumar. Chairs the Design Authority, which approves architecture decisions and any new supplier." |
| OS-C3 | OS | Reporting lines | Stakeholder Need | "Benefits Service Manager: Tom Okafor. Service Owner for housing benefits; line-manages 22 caseworkers across two offices." |
| OS-C4 | OS | Reporting lines | Compliance Constraint | "Data Protection Officer: Lena Marsh. Must sign off any processing of claimant data before go-live." |
| OS-C5 | OS | Reporting lines | Stakeholder Need | "Chief Executive: Margaret Ellery. Accountable to Full Council." |
| OS-C6 | OS | Boards | Design Decision | Boards table: Design Authority chaired by the Head of Digital, fortnightly, decides architecture, suppliers and technical standards; Benefits Transformation Board chaired by the Director of Resources, monthly, decides scope, budget and go-live; Information Governance Group chaired by the DPO, monthly, decides DPIA sign-off and retention |
| OS-C7 | OS | Known tensions | Business Requirement | "The Director of Resources has a savings target of £180k a year from the benefits service by 2027-28." |
| OS-C8 | OS | Known tensions | Risk Factor | "Caseworkers have raised, through their union representative, that the last system change was rolled out without training and increased overtime for three months." |

### Unreferenced Documents

| Filename | Source Location | Reason |
|----------|-----------------|--------|
| None | — | All external documents consulted were cited |

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
| Stamped at | 2026-09-03T08:08:43.225Z |

<!-- arckit-provenance:end -->
