# Ashcombe District Council Enterprise Architecture Principles

> **Template Origin**: Official | **ArcKit Version**: 6.13.0 | **Command**: `/arckit:principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Architecture Principles |
| **Project** | Ashcombe District Council Digital Services (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-09-03 |
| **Last Modified** | 2026-09-03 |
| **Review Cycle** | Annual |
| **Next Review Date** | 2027-09-03 |
| **Owner** | Head of Digital, Ashcombe District Council |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Digital, Data and Technology teams; Digital Design Authority; Revenues and Benefits service; Senior Information Risk Owner (SIRO); Data Protection Officer (DPO); contracted suppliers under NDA |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-09-03 | ArcKit AI | Initial creation from `/arckit:principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the principles governing all technology architecture decisions at Ashcombe District Council, written first for the Housing Benefits digital service (Project 001) and applicable to every council digital service that follows it. These principles ensure that services are accessible, secure, lawful, resilient and affordable, and that they can absorb the annual change cycle that welfare administration demands.

**Scope**: All technology projects, systems, integrations and initiatives commissioned, built or operated by the council, including services delivered by suppliers on the council's behalf
**Authority**: Ashcombe Digital Design Authority, chaired by the Head of Digital
**Compliance**: Mandatory unless an exception is approved through the process in Section VI. Exceptions to security or data-protection principles additionally require SIRO or DPO sign-off

**Philosophy**: These principles are **technology-agnostic**. They describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles. Where a requirements document names a specific platform service (for example the council's existing database platform in ARC-001-REQ DR-001), that is a constraint to be tested against these principles and recorded in an Architecture Decision Record, not a principle in itself.

**Context that shapes these principles**:

- Housing Benefit is administered by the council on behalf of the Department for Work and Pensions (DWP) under the Social Security Contributions and Benefits Act 1992 and the Housing Benefit Regulations 2006. The council is reimbursed through an annually audited subsidy claim, so every award must be reconstructable.
- Working-age caseload is migrating to Universal Credit. The remaining caseload (pension-age claimants, supported and temporary accommodation) is smaller but more complex. The architecture must cope with a shrinking, changing service rather than a growing one.
- Council Tax Reduction and Discretionary Housing Payments are claimed alongside Housing Benefit and share evidence, identity and household data.
- Claimants are disproportionately likely to have low digital confidence, disabilities or limited English. Accessibility and assisted digital are not optional.
- Public-sector obligations apply: the Public Sector Bodies (Websites and Mobile Applications) Accessibility Regulations 2018, the Equality Act 2010 Public Sector Equality Duty, UK GDPR and the Data Protection Act 2018, the Technology Code of Practice, the Local Digital Declaration, the National Cyber Security Centre (NCSC) Cyber Assessment Framework and the Local Government Association's Cyber 360 expectations.

**Principle categories**:

| Category | Principles | Purpose |
|----------|------------|---------|
| I. Strategic (Business) | 1 to 8 | How the council chooses what to build and why |
| II. Data | 9 to 13 | How claimant and case data is protected, governed and trusted |
| III. Integration (Application) | 14 to 16 | How services talk to each other, to DWP and to citizens |
| IV. Quality Attributes (Technology) | 17 to 20 | What operational qualities every service must exhibit |
| V. Development Practices | 21 to 23 | How change is made safely and repeatably |

---

## I. Strategic Principles

### 1. User Needs First and Accessible by Default

**Principle Statement**:
All services MUST be designed from evidenced user needs and MUST meet WCAG 2.2 AA or later across every citizen-facing and staff-facing journey. Every digital journey MUST have an assisted-digital route that reaches the same outcome.

**Rationale**:
Housing Benefit claimants include older people, disabled people, people in temporary accommodation and people with limited English. A service that only works for confident, well-equipped users fails the people it exists for, breaches the 2018 accessibility regulations and exposes the council to Equality Act challenge.

**Implications**:

- User research with real claimants, landlords and caseworkers precedes design, and continues through live operation
- Accessibility is tested with assistive technology, not only automated tooling
- Content is written in plain English at a reading age appropriate to the audience, with translation and interpretation routes where needed
- Telephone, face-to-face and trusted-intermediary channels feed the same case, with no separate "paper" process that diverges from the digital one
- Journeys work on low-specification mobile devices and slow connections
- Delegated access exists for advocates, carers and appointees without sharing the claimant's credentials

**Validation Gates**:

- [ ] User research findings documented and traceable to design decisions
- [ ] Accessibility audit against WCAG 2.2 AA completed by an independent assessor before public beta
- [ ] Accessibility statement published and kept current
- [ ] Assisted-digital route tested end to end and produces the same case record
- [ ] Equality impact assessment completed and actions tracked

**Example Scenarios**:

- ✅ **Good**: A claimant with a screen reader completes the whole claim, saves and resumes it, and uploads evidence. A caseworker on the phone can pick up the same saved claim and finish it with the claimant.
- ❌ **Bad**: The online form is accessible but evidence upload is a separate portal that fails keyboard navigation, so screen-reader users are told to post documents.

**Common Violations**:

- Treating an automated accessibility scan as proof of compliance
- Launching a digital route while the assisted route still uses a different form and a different case record
- Content written for benefits officers rather than claimants

---

### 2. Reuse Before Buy Before Build, Open by Default

**Principle Statement**:
Teams MUST demonstrate that no existing council, cross-government or open-source capability meets the need before buying, and that no suitable commodity product exists before building. Code the council commissions SHOULD be published under an open licence unless a documented security or commercial reason prevents it.

**Rationale**:
The Local Digital Declaration and the Technology Code of Practice commit councils to common components, open standards and working in the open. Housing Benefit is administered by more than three hundred UK councils under identical regulations. Duplicated builds waste public money and diverge from the shared understanding of the rules.

**Implications**:

- Discovery includes a reuse search across council estate, government common components (identity, notifications, payments, publishing) and other councils' published code
- Build decisions are recorded in an Architecture Decision Record with the alternatives considered
- Bespoke build is reserved for what is genuinely distinctive about the council's service
- Published code excludes secrets, configuration and any data, and carries a clear licence
- Bought products are evaluated against these principles, particularly interoperability and data portability, so that reuse today does not become lock-in tomorrow

**Validation Gates**:

- [ ] Reuse search documented with candidates assessed and reasons for rejection
- [ ] Build versus buy analysis includes whole-life cost over at least five years
- [ ] Architecture Decision Record exists for every build decision
- [ ] Open-source publication decision recorded, with justification for any closed component
- [ ] Contracts preserve the council's right to its data and configuration on exit

**Example Scenarios**:

- ✅ **Good**: The team adopts the national notification service for letters and texts, adopts a government identity service for citizen sign-in, and builds only the claim-evidence workflow that is specific to the council.
- ❌ **Bad**: The team writes its own SMS gateway, its own document store and its own identity service because "it is quicker than procurement".

**Common Violations**:

- Skipping the reuse search because a supplier has already demonstrated a product
- Publishing code without a licence, or with credentials in the history
- Buying a product whose data can only be exported through a paid professional-services engagement

---

### 3. Scalability and Elasticity

**Principle Statement**:
All services MUST scale horizontally to meet demand and MUST adjust capacity automatically, both up and down, without manual intervention or architectural change.

**Rationale**:
Housing Benefit demand is spiky and predictable in shape but not in size: the April uprating and annual review, year-end subsidy reconciliation, cost-of-living announcements and Universal Credit migration tranches all produce bursts. Between bursts the caseload is shrinking, so paying for peak capacity all year is waste.

**Implications**:

- Stateless request handling so that any instance can serve any request
- No fixed capacity assumptions in code, licences or contracts
- Batch and payment runs designed to be split and parallelised
- Scaling triggers defined on observed demand metrics
- Scale-down is as important as scale-up given the falling caseload

**Validation Gates**:

- [ ] Load test demonstrates linear capacity growth with added instances
- [ ] No single component limits scaling without a documented reason
- [ ] Scaling triggers and limits defined and tested in both directions
- [ ] Cost model reflects variable rather than fixed capacity
- [ ] Peak-period capacity plan exists for April uprating and year-end

**Example Scenarios**:

- ✅ **Good**: During the April uprating run the service adds capacity for the recalculation and the resulting notification burst, then returns to baseline by the following week.
- ❌ **Bad**: The service is licensed per named server, so the April run is scheduled overnight across three weekends and claimants receive late notifications.

**Common Violations**:

- Session state held in application memory, preventing instance replacement
- Per-server licensing that makes scaling a procurement event
- Sizing for peak all year "to be safe"

---

### 4. Resilience and Fault Tolerance

**Principle Statement**:
All services MUST degrade gracefully when a dependency fails and MUST recover without loss of submitted claims, evidence or payment instructions.

**Rationale**:
The service depends on external parties the council does not control, including DWP data-sharing services, identity providers, payment networks and document services. A claimant halfway through a claim, or a payment run halfway through a file, must not be lost because a third party is unavailable.

**Implications**:

- Timeouts, retries with back-off and circuit breakers on every external call
- Work that cannot complete is queued durably and resumed, not discarded
- Non-critical enrichment (for example a lookup of benefits data) fails soft and is retried later, with the case flagged for review
- Payment runs are idempotent and resumable, never duplicated
- Failure modes are designed and tested, not discovered in production
- Bulkhead isolation so that a failure in one integration does not exhaust shared resources

**Validation Gates**:

- [ ] Failure modes catalogued for each external dependency with the designed behaviour
- [ ] Fault-injection testing performed before go-live and after major change
- [ ] Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined and agreed with the service owner
- [ ] Payment-run interruption and resumption tested without duplicate payments
- [ ] Degraded-mode behaviour documented in the operational runbook

**Example Scenarios**:

- ✅ **Good**: The DWP data-sharing service is unavailable for an afternoon. Claims continue to be accepted, the verification step queues, and caseworkers see a clear "awaiting verification" status that clears automatically.
- ❌ **Bad**: An identity-provider outage returns a blank page and the claimant's forty minutes of form entry is lost.

**Common Violations**:

- Synchronous calls to external services with no timeout
- Batch jobs that must restart from the beginning after a failure
- Health checks that report healthy while a critical dependency is down

---

### 5. Interoperability and Open Standards

**Principle Statement**:
All services MUST expose and consume functionality through well-defined, versioned interfaces using open standards. Direct access to another system's data store across a system boundary is prohibited.

**Rationale**:
The Housing Benefits service exchanges data with DWP, HM Revenue and Customs, landlords, the council's revenues and housing systems, and the subsidy audit process. Open standards let the council change any one component, including a supplier, without renegotiating every integration.

**Implications**:

- Interfaces defined in published, machine-readable specifications
- Open data standards preferred for exchange formats, including those mandated by DWP for statutory returns and data feeds
- Every interface versioned with a backward-compatibility commitment and a deprecation notice period
- File-based exchanges that DWP or the payment network require are wrapped behind an internal interface so the rest of the service does not depend on the file format
- Authentication, authorisation and error semantics are part of the interface contract

**Validation Gates**:

- [ ] Interface specifications published for every integration point
- [ ] Versioning and deprecation policy defined and applied
- [ ] No cross-system database or file-share coupling
- [ ] Statutory exchange formats mapped to internal canonical models
- [ ] Contract tests exist between each consumer and provider

**Example Scenarios**:

- ✅ **Good**: The revenues system consumes a versioned "award changed" interface. When the benefits case system is replaced, the interface contract is preserved and the revenues team makes no change.
- ❌ **Bad**: A nightly script reads the benefits database directly to update council tax accounts, and breaks silently when a column is renamed.

**Common Violations**:

- Reporting tools pointed at the live transactional database of another system
- Proprietary exchange formats where an open standard exists
- Unversioned interfaces changed in place

---

### 6. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence in depth with zero-trust principles, aligned to the NCSC Cyber Assessment Framework, and MUST hold Cyber Essentials Plus or an equivalent independently assessed baseline. Security is a foundational requirement, not a feature added later.

**Rationale**:
The service holds identity, income, health, disability, immigration status and bank details for the most vulnerable residents. Local authorities are a persistent target for ransomware and fraud. A breach harms claimants directly, and a loss of availability stops rent being paid.

**Zero Trust Pillars**:

1. **Identity-based access**: every request from a person or a service is authenticated; no trust is granted by network location
2. **Least privilege**: the minimum permission for the shortest time, with privileged access time-boxed and recorded
3. **Encryption everywhere**: data encrypted in transit and at rest, with keys managed separately from the data
4. **Continuous verification**: all access is logged, monitored and analysed for anomalies

**Mandatory Controls**:

- [ ] Multi-factor authentication for all staff and supplier access
- [ ] Service-to-service authentication with short-lived, scoped credentials
- [ ] Secrets held in a managed secrets store, never in code, configuration or tickets
- [ ] Network segmentation with the smallest practical trust zones
- [ ] Encryption at rest for every data store, backup and export
- [ ] Encrypted transport for every network communication, internal and external
- [ ] Structured, tamper-evident logging of authentication, authorisation and administrative events
- [ ] Vulnerability scanning in the delivery pipeline and independent penetration testing before go-live and annually
- [ ] Fraud controls proportionate to the risk, including bank-account change verification and duplicate-claim detection
- [ ] Supplier access governed by contract, time-limited and auditable

**Compliance Frameworks**:

- NCSC Cyber Assessment Framework, Cyber Essentials Plus, ISO 27001 where a supplier provides the service
- UK GDPR and Data Protection Act 2018 security obligations
- DWP security conditions attached to benefits data-sharing agreements
- Payment-network security requirements for any card or bank-file handling

**Exceptions**:

- NONE. Security principles are non-negotiable.
- Specific control implementations may vary where compensating controls are documented and approved by the SIRO.

**Validation Gates**:

- [ ] Threat model completed and reviewed before design sign-off
- [ ] Security controls mapped to requirements and to the Cyber Assessment Framework outcomes
- [ ] Security testing plan defined and executed
- [ ] Incident response runbook created and exercised
- [ ] Data-sharing agreement security conditions evidenced

**Example Scenarios**:

- ✅ **Good**: A caseworker's account is compromised. Multi-factor authentication blocks the sign-in, the attempt is logged and alerted, and privileged operations would in any case have required a separate approval.
- ❌ **Bad**: A shared "benefits admin" account with a password in a team wiki is used by everyone, including a supplier engineer, so nobody can say who changed a bank account.

**Common Violations**:

- Trusting the corporate network as a security boundary
- Long-lived API keys shared between environments
- Backups unencrypted or stored where the same credentials that reach production also reach them

---

### 7. Observability and Operational Excellence

**Principle Statement**:
All services MUST emit structured logs, metrics and traces with correlation identifiers, enabling real-time monitoring, troubleshooting, capacity planning and evidence for audit.

**Rationale**:
The council cannot operate, secure or defend at appeal what it cannot see. Observability also supplies the operational evidence needed for the subsidy audit, for Service Standard assessment and for the statutory 14-day decision target in ARC-001-REQ BR-002.

**Telemetry Requirements**:

- **Logging**: structured, correlated, personal data minimised or pseudonymised
- **Metrics**: request volume, latency percentiles (p50, p95, p99), error rates, queue depths, business measures such as claims received, decisions issued and days to decision
- **Tracing**: request flows across service and integration boundaries
- **Alerting**: based on Service Level Objectives with actionable runbooks

**Required Instrumentation**:

- Technical health of every component and integration
- Business flow health: claims in each state, evidence outstanding, payment-run completion
- Security events: authentication failures, privilege use, unusual data access patterns
- Cost signals so that spend is visible alongside load

**Log Retention**:

- **Security and audit logs**: minimum 12 months online, longer where the audit or records policy requires
- **Application logs**: 30 to 90 days, sufficient for troubleshooting
- **Metrics**: at least two years at reduced resolution for capacity and trend analysis

**Validation Gates**:

- [ ] Logs, metrics and traces instrumented across all components
- [ ] Dashboards and alerts configured for technical and business measures
- [ ] Service Level Objectives and Indicators defined and published
- [ ] Runbooks exist for known failure scenarios
- [ ] Personal data in telemetry reviewed and minimised

**Example Scenarios**:

- ✅ **Good**: A rise in "evidence requested" cases is visible on the service dashboard the same day, and the team traces it to a change in the upload component before claimants complain.
- ❌ **Bad**: The only sign of a broken DWP feed is a caseworker noticing three weeks later that no income changes have arrived.

**Common Violations**:

- Logging full claimant records "for debugging"
- Alerts on every error rather than on objectives, causing alert fatigue
- Business metrics available only through a monthly manual report

---

### 8. Cloud First, Commodity Where Possible

**Principle Statement**:
New services MUST be delivered on commodity cloud services hosted in the United Kingdom unless a documented assessment shows another model offers better value or is required by law. Teams SHOULD consume managed services in preference to operating infrastructure themselves.

**Rationale**:
The Technology Code of Practice and government Cloud First policy expect public bodies to use commodity services. A district council cannot economically run resilient, patched, monitored infrastructure for a shrinking service; consuming it lets scarce engineering effort go to the parts of the service that are genuinely the council's.

**Implications**:

- Hosting decisions favour services that scale, patch and back up as a matter of course
- UK data residency is a hard requirement (see Principle 10)
- Portability is preserved through open interfaces and infrastructure as code, so that a hosting choice is a decision, not a marriage
- Exit and data-return terms are agreed before any commitment
- Operating cost is monitored continuously, not discovered at invoice

**Validation Gates**:

- [ ] Cloud-first assessment recorded in an Architecture Decision Record
- [ ] Hosting region and residency confirmed for every data store and backup
- [ ] Exit plan documented, including data export format and timescale
- [ ] Shared-responsibility boundaries for security and operations written down
- [ ] Cost forecast and monitoring in place before go-live

**Example Scenarios**:

- ✅ **Good**: The service uses managed database, queue and object-storage services in a UK region, defined as code, with a documented path to re-create the environment elsewhere.
- ❌ **Bad**: A physical server in the council basement hosts the evidence store because "it is already paid for", and it is patched when someone remembers.

**Common Violations**:

- Lifting an existing virtual machine into the cloud unchanged and calling it cloud first
- Adopting a proprietary managed service with no export route for the data it holds
- Choosing a region outside the UK because it is marginally cheaper

---

## II. Data Principles

### 9. Privacy by Design (NON-NEGOTIABLE)

**Principle Statement**:
All processing of personal data MUST be designed to satisfy UK GDPR and the Data Protection Act 2018 from the outset, with data minimisation, purpose limitation, a documented lawful basis, and a Data Protection Impact Assessment completed before design sign-off. Decisions that produce legal effects for a claimant MUST include meaningful human involvement.

**Rationale**:
Housing Benefit processing involves special-category data (health, disability), financial data, immigration status and data about children. It is high-risk processing under UK GDPR Article 35. A benefits entitlement decision has legal effect; wholly automated decisions of that kind are constrained by Article 22 and are appealable to a tribunal.

**Implications**:

- Collect only what the regulations require to decide the claim, and only when it is needed
- Record the lawful basis and, where relied on, the specific public-task or statutory condition for each processing purpose
- Special-category data is segregated, access-controlled and logged separately
- Automated calculation is permitted; automated refusal or reduction without human review is not
- Data subject rights (access, rectification, erasure where applicable, objection) are supported by design, not by manual trawling
- Privacy notices are written for claimants and reflect actual processing, including data sharing with DWP and landlords
- Pseudonymisation or synthetic data for testing, analytics and training

**Validation Gates**:

- [ ] Data Protection Impact Assessment completed, DPO consulted and actions tracked
- [ ] Record of processing activity updated for every purpose and data flow
- [ ] Data minimisation review evidences each field against a regulatory need
- [ ] Human-review step designed into any adverse decision path
- [ ] Subject-access response can be produced within the statutory period without manual database queries
- [ ] Test and analytics environments contain no live personal data

**Example Scenarios**:

- ✅ **Good**: The claim asks for a disability-benefit reference only when the household composition makes it relevant, stores it in a segregated store, and the automated calculation flags an apparent overpayment for a caseworker to confirm before any letter is sent.
- ❌ **Bad**: The form collects National Insurance numbers for every household member up front "in case", and an automated rule closes claims and issues recovery letters with no human check.

**Common Violations**:

- Copying production data to a test environment to "get realistic cases"
- Treating a Data Protection Impact Assessment as a form to complete after build
- Sharing evidence documents with landlords beyond what the claimant consented to

---

### 10. Data Sovereignty, Residency and Retention

**Principle Statement**:
Data classification, residency, retention and access controls MUST comply with UK law, the council's records-retention schedule and the conditions of DWP data-sharing agreements. Personal data MUST be stored and processed in the United Kingdom, and retention MUST be enforced automatically.

**Data Classification Tiers**:

1. **Public**: no restrictions (published guidance, open data)
2. **Internal**: council staff only (procedures, non-personal operational data)
3. **Confidential**: need-to-know (claimant personal data, income, bank details, case notes)
4. **Restricted**: highest controls (special-category data, safeguarding markers, fraud investigation material, DWP-sourced data under sharing conditions)

**Data Residency**:

- All personal data, backups, logs containing personal data and disaster-recovery copies reside in the United Kingdom
- Support access from outside the UK is a transfer and requires a documented legal mechanism and approval
- DWP-sourced data is held only where the sharing agreement permits

**Data Retention**:

- Claim records and evidence retained for six years after the claim closes, consistent with ARC-001-REQ DR-002 and the subsidy audit cycle, then deleted automatically
- Legal hold suspends deletion for litigation, tribunal or investigation, and is itself recorded
- Backup retention aligned with recovery needs, not used as an informal archive
- Deletion covers derived copies, exports and search indexes, not only the system of record

**Validation Gates**:

- [ ] Every data store classified, with the tier recorded in the design
- [ ] Residency confirmed for primary, replica, backup and log storage
- [ ] Retention rules configured and automated deletion tested
- [ ] Legal-hold process defined and tested
- [ ] Access controls enforce need-to-know by role and case

**Example Scenarios**:

- ✅ **Good**: Six years after a claim closes, the record, its evidence documents, the search index entry and the archived correspondence are all deleted in the same automated run, and the deletion is logged.
- ❌ **Bad**: Evidence documents are "deleted" from the case system but remain in an object store, a reporting extract and a supplier's support ticket attachment indefinitely.

**Common Violations**:

- Disaster-recovery region outside the UK chosen by default
- Retention applied to the database but not to document storage or exports
- Reporting extracts on shared drives with no owner and no retention

---

### 11. Single Source of Truth

**Principle Statement**:
Every data domain MUST have one authoritative system of record. Derived copies MUST be read-only, labelled as derived, and synchronised on a defined schedule from the authoritative source.

**Rationale**:
A claimant's address, household, income and award appear in the benefits, council tax, housing, and customer-contact systems. When two systems disagree, the claimant is asked the same question twice, the wrong rent is paid, or the subsidy claim fails audit.

**Implications**:

- The system of record is identified for each entity: claimant identity, household, property, income evidence, award, payment, correspondence
- DWP is authoritative for the data it supplies (for example state-pension and Universal Credit status); the council is authoritative for the Housing Benefit and Council Tax Reduction award
- Other systems consume the authoritative record through interfaces and do not re-key it
- No bidirectional synchronisation without an explicit conflict-resolution rule
- Reference data (benefit rates, non-dependant deductions, applicable amounts) is versioned by effective date and held once

**Validation Gates**:

- [ ] System of record identified for every entity in the data model
- [ ] Derived copies documented with source, sync frequency and staleness tolerance
- [ ] No bidirectional sync without a documented conflict strategy
- [ ] Reference data managed centrally with effective-dated versions
- [ ] Re-keying of authoritative data eliminated or justified

**Example Scenarios**:

- ✅ **Good**: A change of address recorded once in the customer record propagates to benefits, council tax and housing through published interfaces, and each downstream copy shows the source and timestamp.
- ❌ **Bad**: The benefits team, the council tax team and the housing team each hold their own address for the same resident, and rent is paid to the old landlord.

**Common Violations**:

- Spreadsheets used as the working record for a caseload
- Uprating rates typed into three systems independently each April
- "Temporary" copies that become the version everyone uses

---

### 12. Data Quality and Lineage

**Principle Statement**:
Data pipelines and case processing MUST enforce defined quality rules at the point of capture and MUST provide end-to-end lineage from evidence to award, sufficient for the subsidy audit and for any appeal.

**Quality Standards**:

- **Completeness**: required fields present before a claim is treated as complete, because the 14-day decision clock starts at completeness
- **Consistency**: reconciliation across benefits, council tax and payment systems, and against DWP-supplied data
- **Accuracy**: validation rules and reference-data constraints applied at source, with clear error messages for claimants and caseworkers
- **Timeliness**: freshness targets for external feeds, monitored and alerted

**Lineage Requirements**:

- Every award traceable to the evidence, the regulation version and the rates in force on the effective date
- Transformation and calculation logic version-controlled and reviewable
- Data-quality measures reported per feed and per process step
- Impact analysis possible before a schema or rule change

**Validation Gates**:

- [ ] Quality rules defined, automated and reported
- [ ] Lineage captured and queryable from award back to evidence
- [ ] Data contracts agreed between producers and consumers
- [ ] Schema and rule evolution strategy documented
- [ ] Subsidy audit sample can be reconstructed from lineage without manual investigation

**Example Scenarios**:

- ✅ **Good**: The external auditor selects a case; the team produces the evidence, the calculation inputs, the rate table version and the caseworker decisions in one query.
- ❌ **Bad**: Reconstructing an award requires reading scanned letters, a spreadsheet of historical rates and a caseworker's memory.

**Common Violations**:

- Free-text fields where structured data is needed for calculation
- Calculation logic embedded in reports rather than in the versioned rules
- Feeds accepted without checking record counts or freshness

---

### 13. Auditability and Decision Explainability

**Principle Statement**:
Every decision that affects a claimant's entitlement or payment MUST be reconstructable: who or what made it, when, on what evidence, under which rules, and with what result. Automated calculations MUST be explainable in plain English to the claimant and to a tribunal.

**Rationale**:
Housing Benefit decisions carry a statutory right to reconsideration and appeal to the First-tier Tribunal. The council must defend decisions years later. The subsidy claim is audited annually and unexplained awards are disallowed at the council's cost. Public trust in algorithmic decision-making depends on transparency.

**Implications**:

- Immutable, tamper-evident audit trail of case events, decisions and administrative actions
- Effective-dated rules so that a historic decision is re-run under the rules that applied at the time
- Decision notices generated from the same calculation that produced the award, with the reasons expressed for the claimant
- Any use of automated risk-scoring or prioritisation is documented, bias-tested, published under the Algorithmic Transparency Recording Standard, and never the sole basis for an adverse outcome
- Administrative overrides require a reason and are reviewable

**Validation Gates**:

- [ ] Audit trail design reviewed and immutability demonstrated
- [ ] Historic recalculation under prior rules tested
- [ ] Decision notice content traceable to calculation outputs
- [ ] Algorithmic tools recorded and impact-assessed before use
- [ ] Override and correction paths logged with reasons

**Example Scenarios**:

- ✅ **Good**: A tribunal asks why an award was reduced in 2024. The team produces the evidence received, the regulation version, the calculation steps and the letter, all consistent.
- ❌ **Bad**: The rules engine was upgraded and the old logic discarded, so nobody can say how the 2024 figure was reached.

**Common Violations**:

- Overwriting case data in place with no history
- Decision letters written from a template that does not reflect the actual calculation
- Prioritisation models introduced as "just triage" without assessment or transparency

---

## III. Integration Principles

### 14. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, with independent data stores and independent deployment. Shared databases, shared file systems and tight runtime dependencies between systems are prohibited.

**Rationale**:
The council will replace components over the life of the service, including the case-management product, the payment channel and the identity provider. Loose coupling makes each replacement a bounded piece of work rather than a big-bang migration.

**Implications**:

- Communication through interfaces or events, never through another system's storage
- Each system owns its data lifecycle
- Shared libraries kept minimal; duplication is preferable to coupling
- No distributed transactions across system boundaries; use compensating actions
- Deployment of one system never requires simultaneous deployment of another

**Validation Gates**:

- [ ] Systems communicate through interfaces or events only
- [ ] No shared mutable state between systems
- [ ] Independent data store per system
- [ ] Independent deployment demonstrated
- [ ] Interface changes versioned with backward compatibility

**Example Scenarios**:

- ✅ **Good**: The evidence-upload component is replaced with a different product. Only the interface adapter changes; the claim service and caseworker tools are untouched.
- ❌ **Bad**: The case system, the correspondence system and the reporting warehouse share one database schema, so any change requires a coordinated release of all three.

**Common Violations**:

- Integration through database views granted to other teams
- Shared file drop with agreed column positions and no contract
- Cross-system transactions that leave partial state on failure

---

### 15. Asynchronous Communication

**Principle Statement**:
Systems SHOULD use asynchronous, event-driven communication for interactions that do not need an immediate response, with durable messaging and defined delivery guarantees. Synchronous calls MAY be used where the user needs an immediate answer or where consistency demands it.

**Rationale**:
Most benefits processing is not real-time: verification with DWP, evidence requests, notifications, payment runs and subsidy reporting all tolerate delay but not loss. Asynchronous patterns absorb the demand spikes of Principle 3 and the dependency failures of Principle 4.

**When to Use Async**:

- Change-of-circumstance notifications from DWP and other sources
- Notification and correspondence generation
- Payment file preparation and reconciliation
- Downstream updates to council tax, housing and reporting
- Any interaction with a slow or unreliable external party

**When Synchronous is Acceptable**:

- Interactive validation while a claimant completes a form
- Read-only queries for a caseworker screen
- Identity assertion at sign-in
- Operations that must be consistent before the user proceeds

**Validation Gates**:

- [ ] Asynchronous patterns used for non-real-time flows
- [ ] Message durability and delivery guarantees (at-least-once with idempotent consumers, or equivalent) defined
- [ ] Event schemas versioned and published
- [ ] Dead-letter handling and replay procedures defined and tested
- [ ] Ordering and duplicate-handling behaviour documented

**Example Scenarios**:

- ✅ **Good**: A change-of-circumstance event from DWP is queued, applied, and triggers a recalculation event and a notification event, each processed independently and retried on failure.
- ❌ **Bad**: The claim submission page waits for a synchronous call to DWP that times out after two minutes, and the claimant refreshes and submits twice.

**Common Violations**:

- Consumers that are not idempotent, causing duplicate letters or payments
- Dead-letter queues nobody monitors
- Synchronous chains of four services to render one page

---

### 16. Identity, Access and Delegated Consent

**Principle Statement**:
Citizen identity MUST be established to a documented level of assurance proportionate to the transaction, using recognised identity-assurance standards. Staff and supplier access MUST use the council's central identity service with role-based, least-privilege authorisation. Claimants MUST be able to delegate access to a representative without sharing credentials, and that delegation MUST be recorded and revocable.

**Rationale**:
Benefit fraud and identity theft are material risks, but excessive identity friction excludes the very claimants the service exists for. Many claimants rely on family members, advocates, support workers or appointees. Delegation by password-sharing destroys the audit trail and the claimant's control.

**Implications**:

- Level of identity assurance chosen per transaction: saving a draft needs less than changing bank details
- Government identity-assurance guidance (Good Practice Guide 44 and 45 or successors) used to define levels
- Reuse of a cross-government identity service preferred over a council-specific one
- Staff authorisation by role and, where appropriate, by case, with segregation of duties for payment approval
- Representative access modelled explicitly, with scope, expiry and an audit record
- Session and credential lifetimes proportionate to risk

**Validation Gates**:

- [ ] Assurance level documented for each transaction type
- [ ] Single sign-on with multi-factor authentication for all staff and suppliers
- [ ] Role model defined with segregation of duties for financial actions
- [ ] Delegated access designed, tested and auditable
- [ ] Account recovery route tested for claimants without smartphones or email

**Example Scenarios**:

- ✅ **Good**: A support worker at a homelessness charity is granted time-limited access to help a claimant complete and track a claim, with every action recorded against the support worker's own identity.
- ❌ **Bad**: The claimant gives their password to a neighbour, who later changes the bank details.

**Common Violations**:

- Demanding photo-ID identity verification just to start a claim
- Generic caseworker role that includes payment approval
- No delegation model, so staff informally "act as" claimants using their credentials

---

## IV. Quality Attributes

### 17. Performance and Efficiency

**Principle Statement**:
All services MUST meet defined, measured performance targets under expected and peak load, with efficient use of computational resources.

**Performance Targets** (to be defined per service and recorded in requirements):

- **Response time**: p50, p95 and p99 targets for interactive pages and interface calls
- **Throughput**: claims, recalculations and notifications per hour at April peak
- **Batch windows**: payment and uprating runs complete within their agreed windows with headroom
- **Resource efficiency**: utilisation targets that avoid both waste and saturation

**Implications**:

- Performance requirements agreed before implementation and expressed as measurable numbers
- Load tests at expected and peak volumes before go-live and after material change
- Continuous performance monitoring in production, not point-in-time tests
- Caching for expensive, stable lookups such as reference data
- Front-end performance on low-specification devices and slow connections is a target, not an afterthought

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets
- [ ] Load and soak tests performed at expected and peak capacity
- [ ] Production performance metrics monitored against targets
- [ ] Capacity planning model maintained
- [ ] Front-end performance budget defined and tested

**Example Scenarios**:

- ✅ **Good**: The April uprating recalculates the full caseload well inside its window and the notification burst completes the same day.
- ❌ **Bad**: Caseworker screens take twelve seconds to load because each renders by querying five downstream systems synchronously.

**Common Violations**:

- Performance tests run only on a small dataset
- No target, so any result is "acceptable"
- Page weight that makes the service unusable on a pay-as-you-go mobile connection

---

### 18. Availability and Reliability

**Principle Statement**:
All services MUST meet defined availability targets with automated recovery and minimal data loss. Payment runs are the critical path and MUST have the highest availability and recovery priority.

**Availability Targets** (to be defined per service and recorded in requirements):

- **Citizen-facing claim service**: target at least 99.9% monthly availability during service hours, with planned maintenance outside them
- **Payment processing**: no missed statutory payment run; RTO measured in hours, RPO measured in minutes
- **Caseworker tools**: availability aligned with service hours and the 14-day decision commitment

**High Availability Patterns**:

- Redundancy across independent failure domains within the UK
- Automated health checks and failover
- Regular disaster-recovery rehearsal, including restore from backup and full environment re-creation from code
- Backups tested by restoring them, not by confirming they exist

**Validation Gates**:

- [ ] Availability targets defined and agreed with the service owner
- [ ] RTO and RPO documented per component and tested
- [ ] Redundancy implemented across failure domains
- [ ] Failover and restore rehearsed at least annually
- [ ] Payment-run continuity plan exists for total platform loss

**Example Scenarios**:

- ✅ **Good**: A failure domain is lost on payment day. Traffic fails over automatically, the payment run resumes from its last checkpoint, and rent is paid on time.
- ❌ **Bad**: Backups have been taken nightly for two years and the first restore attempt, during a ransomware incident, fails.

**Common Violations**:

- Availability measured only by whether the home page responds
- Single instance of a "minor" component that all payment processing depends on
- Disaster-recovery plan that has never been executed

---

### 19. Maintainability and Evolvability

**Principle Statement**:
All services MUST be designed for change, with modular structure, clear separation of concerns, rules and rates held as versioned configuration rather than code, and current documentation including Architecture Decision Records.

**Rationale**:
Housing Benefit rules change every April, and often in-year. The working-age caseload is migrating away, so the service must shrink gracefully and eventually be decommissioned in part without disrupting what remains. Software spends most of its life being changed; design for that.

**Implications**:

- Benefit rates, applicable amounts, deductions and thresholds are effective-dated configuration, changeable without a code release
- Calculation logic is isolated, testable in its own right and versioned
- Modules have defined responsibilities and boundaries
- Architecture Decision Records for every significant choice, including the reasons for rejecting alternatives
- Automated tests give confidence to refactor
- Decommissioning is designed in: data export, archive and shutdown paths for a component or a whole caseload segment

**Validation Gates**:

- [ ] Architecture documentation current and reviewed at each gate
- [ ] Module boundaries and responsibilities defined
- [ ] Rates and rules changeable by configuration with an audit trail
- [ ] Architecture Decision Records exist for significant decisions
- [ ] Decommissioning and data-export path designed and tested

**Example Scenarios**:

- ✅ **Good**: The April uprating is applied by loading a new effective-dated rate set, verified by the automated regression pack, and released with no code change.
- ❌ **Bad**: Rates are hard-coded, the annual change takes six weeks of development and testing, and last year's logic is overwritten.

**Common Violations**:

- Business rules scattered across user interface, database triggers and reports
- No record of why a design choice was made, so it is relitigated every year
- No plan for turning part of the service off

---

### 20. Value for Money and Sustainability

**Principle Statement**:
All technology decisions MUST be justified on whole-life cost and public value, with continuous cost visibility in operation. Services SHOULD minimise their environmental impact in line with the Greening Government ICT commitments.

**Rationale**:
Councils operate under severe financial constraint and are accountable to residents and to external audit for value for money. Cloud consumption makes cost a daily engineering concern rather than an annual procurement one. Sustainability is a stated government commitment and increasingly a procurement criterion.

**Implications**:

- Whole-life cost over at least five years, including exit, in every build-or-buy decision
- Cost allocated to services and visible to the teams that incur it
- Capacity scaled down as the caseload falls (see Principle 3)
- Environment hygiene: non-production environments switched off when idle, data lifecycles enforced
- Supplier commercial terms avoid lock-in that would inflate future cost
- Energy efficiency and hardware lifecycle considered in hosting and device choices

**Validation Gates**:

- [ ] Whole-life cost model exists and is refreshed at each gate
- [ ] Cost monitoring and alerting in place before go-live
- [ ] Idle-resource and right-sizing reviews scheduled
- [ ] Exit cost included in supplier evaluation
- [ ] Environmental impact considered and recorded in hosting decisions

**Example Scenarios**:

- ✅ **Good**: Monthly cost per active claim is on the service dashboard, falls as the caseload migrates, and a spike is traced to a misconfigured environment within a day.
- ❌ **Bad**: The first sign of a cost problem is an invoice three times the budget because test environments ran at production scale for a quarter.

**Common Violations**:

- Comparing only licence cost when evaluating options
- No owner for cloud spend
- Buying capacity for a caseload the council no longer has

---

## V. Development Practices

### 21. Infrastructure as Code

**Principle Statement**:
All infrastructure and environment configuration MUST be defined as code, version-controlled, peer-reviewed and deployed through automated pipelines. Manual change to production infrastructure is prohibited outside a documented emergency procedure.

**Rationale**:
Manual change creates drift, undocumented state and unrepeatable environments. Infrastructure as code gives auditability, disaster recovery by re-creation, consistent security baselines and the portability that Principle 8 depends on.

**Implications**:

- Every environment reproducible from the repository
- Infrastructure changes reviewed like application changes
- Security baselines and policies expressed as code and enforced in the pipeline
- Emergency manual changes are time-limited and reconciled back into code
- Secrets injected at deployment from a managed store, never committed

**Validation Gates**:

- [ ] All infrastructure defined declaratively as code
- [ ] Infrastructure code version-controlled with peer review
- [ ] Automated pipeline deploys infrastructure changes
- [ ] Drift detection in place and manual change alerts
- [ ] Environment re-creation from code rehearsed

**Example Scenarios**:

- ✅ **Good**: A full production environment is re-created in a new region from code during a disaster-recovery rehearsal, with data restored from tested backups.
- ❌ **Bad**: A firewall rule added by hand during an incident two years ago is the only thing keeping an integration working, and nobody knows it exists.

**Common Violations**:

- Console changes "just this once"
- Configuration that lives in a supplier's head
- Environments that differ from each other in undocumented ways

---

### 22. Automated Testing

**Principle Statement**:
All changes MUST be validated by automated tests before deployment to production, including a regression pack for benefit calculations and automated accessibility checks.

**Test Pyramid**:

- **Unit tests**: fast, isolated, high coverage of calculation and business logic
- **Integration tests**: component and interface interactions, including contract tests with DWP-format exchanges
- **End-to-end tests**: critical user journeys, including the assisted-digital route

**Required Test Types**:

- Functional tests for claim, decision, payment and correspondence flows
- Calculation regression pack covering the published regulations and worked examples, re-run for every rate change
- Accessibility tests in the pipeline, supplemented by manual assistive-technology testing
- Performance tests at peak volumes
- Security tests: dependency scanning, static analysis, and dynamic testing before release
- Resilience tests: failure injection for external dependencies

**Validation Gates**:

- [ ] Automated tests pass before merge and before deployment
- [ ] Coverage thresholds defined and met for calculation logic
- [ ] Critical journeys have end-to-end tests
- [ ] Calculation regression pack maintained with effective-dated cases
- [ ] Accessibility and security tests run automatically in the pipeline

**Example Scenarios**:

- ✅ **Good**: A change to the non-dependant deduction logic fails a regression case from a prior year, is corrected, and ships the same day.
- ❌ **Bad**: A rate change is tested by a caseworker trying "a few claims" on a Friday afternoon.

**Common Violations**:

- Tests that use live personal data
- A regression pack that is never updated when regulations change
- Skipping tests to hit the April deadline

---

### 23. Continuous Integration and Delivery

**Principle Statement**:
All changes MUST flow through an automated build, test, security-scan and deployment pipeline with quality gates at each stage, and MUST be releasable in small increments with a tested rollback.

**Pipeline Stages**:

1. **Source control**: every change committed with review
2. **Build**: automated, reproducible artefacts
3. **Test**: the automated suites in Principle 22
4. **Security scan**: dependency, static and container or package vulnerability scanning
5. **Deployment**: automated promotion through environments to production

**Quality Gates**:

- All tests pass
- No unresolved critical or high vulnerabilities
- Peer review approved
- Production release checklist satisfied, including operational readiness and change record

**Validation Gates**:

- [ ] Automated pipeline exists from commit to production
- [ ] Security scanning integrated with blocking thresholds
- [ ] Deployment automated, repeatable and logged
- [ ] Rollback tested and time-bounded
- [ ] Release frequency and lead time measured

**Example Scenarios**:

- ✅ **Good**: A content fix to a decision letter is reviewed, tested, scanned and live within the hour, with the release recorded automatically.
- ❌ **Bad**: Releases happen quarterly, take a weekend, and are rolled back by restoring a database backup.

**Common Violations**:

- Manual deployment steps documented in a wiki
- Vulnerability scan results nobody triages
- Big-bang releases bundled to avoid the change process

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Ashcombe Digital Design Authority.

**Valid Exception Reasons**:

- Technical constraint that prevents compliance, evidenced rather than asserted
- Statutory or DWP-mandated requirement that conflicts with a principle
- Transitional state during migration, including Universal Credit migration and legacy decommissioning
- Time-boxed pilot or proof of concept with a defined end date and no live personal data

**Exception Request Requirements**:

- [ ] Justification with business and technical rationale
- [ ] Alternative approach and compensating controls
- [ ] Risk assessment and mitigation plan, recorded in the project risk register
- [ ] Expiry date; exceptions are time-bound and default to twelve months
- [ ] Remediation plan to achieve compliance

**Approval Process**:

1. Submit the exception request to the Digital Design Authority with an Architecture Decision Record
2. Review by the Digital Design Authority at its next session
3. Head of Digital approval for all exceptions; SIRO approval additionally for Principles 6 and 10; DPO approval additionally for Principles 9 and 13
4. Record the exception in the project's architecture documentation and the council exception register
5. Review all open exceptions quarterly; expired exceptions are escalated, not silently renewed

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture review at the following milestones, aligned to the Government Service Standard phases:

**Discovery and Alpha**:

- [ ] Architecture principles understood by the team
- [ ] Reuse search completed (Principle 2)
- [ ] High-level approach aligns with principles
- [ ] Data Protection Impact Assessment screening started
- [ ] No obvious principle violations

**Beta and Design**:

- [ ] Detailed architecture documented with Architecture Decision Records
- [ ] Compliance with each principle validated against its gates
- [ ] Exceptions requested and approved
- [ ] Security threat model and Data Protection Impact Assessment completed
- [ ] Accessibility audit scheduled

**Pre-Production**:

- [ ] Implementation matches the approved architecture
- [ ] All validation gates passed or exceptions in place
- [ ] Penetration test completed and findings remediated or accepted
- [ ] Operational readiness verified, including runbooks and disaster-recovery rehearsal
- [ ] Accessibility statement published

**Live**:

- [ ] Annual principles compliance review
- [ ] Exceptions reviewed quarterly
- [ ] Post-incident reviews assessed against principles

### Enforcement

- Architecture reviews are **mandatory** for all projects and for supplier-delivered services
- Principle violations must be remediated before production deployment
- Approved exceptions are time-bound and reviewed quarterly
- Retrospective reviews of live systems are conducted annually and after any significant incident
- Compliance scorecards are produced using `/arckit:principles-compliance` and reported to the Digital Design Authority

---

## VIII. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Validation |
|---|-----------|----------|-------------|------------|
| 1 | User Needs First and Accessible by Default | Strategic | CRITICAL | Accessibility audit, user research, assisted-digital test |
| 2 | Reuse Before Buy Before Build, Open by Default | Strategic | HIGH | Reuse search, ADR, licence decision |
| 3 | Scalability and Elasticity | Strategic | HIGH | Load testing, scaling triggers |
| 4 | Resilience and Fault Tolerance | Strategic | CRITICAL | Fault injection, RTO/RPO, payment-run resumption |
| 5 | Interoperability and Open Standards | Strategic | HIGH | Interface specs, versioning, contract tests |
| 6 | Security by Design | Strategic | CRITICAL | Threat model, penetration test, CAF mapping |
| 7 | Observability and Operational Excellence | Strategic | HIGH | Telemetry, SLOs, runbooks |
| 8 | Cloud First, Commodity Where Possible | Strategic | HIGH | ADR, residency, exit plan |
| 9 | Privacy by Design | Data | CRITICAL | DPIA, minimisation review, human review path |
| 10 | Data Sovereignty, Residency and Retention | Data | CRITICAL | Classification, residency, automated deletion |
| 11 | Single Source of Truth | Data | HIGH | System-of-record register, sync documentation |
| 12 | Data Quality and Lineage | Data | HIGH | Quality rules, lineage query, audit reconstruction |
| 13 | Auditability and Decision Explainability | Data | CRITICAL | Immutable audit trail, historic recalculation |
| 14 | Loose Coupling | Integration | HIGH | Deployment independence, no shared state |
| 15 | Asynchronous Communication | Integration | MEDIUM | Durable messaging, idempotency, dead-letter handling |
| 16 | Identity, Access and Delegated Consent | Integration | CRITICAL | Assurance levels, MFA, delegation audit |
| 17 | Performance and Efficiency | Quality | HIGH | Load testing, performance budget |
| 18 | Availability and Reliability | Quality | CRITICAL | Failover and restore rehearsal |
| 19 | Maintainability and Evolvability | Quality | HIGH | Configurable rules, ADRs, decommissioning path |
| 20 | Value for Money and Sustainability | Quality | HIGH | Whole-life cost, cost monitoring |
| 21 | Infrastructure as Code | DevOps | HIGH | Code coverage of infrastructure, drift detection |
| 22 | Automated Testing | DevOps | HIGH | Regression pack, accessibility and security tests |
| 23 | Continuous Integration and Delivery | DevOps | HIGH | Pipeline gates, rollback test |

### Consistency Notes

- Principle 8 (cloud first) and Principle 10 (UK residency) are reconciled by requiring UK-hosted commodity services; a cloud-first choice never overrides residency.
- Principle 15 (asynchronous) and Principle 17 (performance) are reconciled by the explicit list of where synchronous calls are acceptable.
- Principle 2 (reuse) never overrides Principles 6, 9 and 10; a reused or bought component must pass the same security and data gates as a built one.
- Principle 16 (identity) and Principle 1 (accessibility) are reconciled by proportionate assurance levels and a tested recovery route for claimants without smartphones or email.

### Related Council Artefacts

- ARC-001-REQ-v1.0 Housing Benefits Portal requirements: BR-002 informs the observability measures in Principle 7; DR-002 informs the retention period in Principle 10; DR-001 names an existing platform service and should be recorded as a constraint in an Architecture Decision Record under Principles 2 and 8.

---

**Document Version History**

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-09-03 | ArcKit AI | Initial draft for Digital Design Authority review |

## External References

> This section provides traceability from generated content back to source documents.
> Follow citation instructions in the project's citation reference guide.

### Document Register

| Doc ID | Filename | Type | Source Location | Description |
|--------|----------|------|-----------------|-------------|
| *None consulted* | — | — | — | — |

No external governance documents, policies or standards files were found in `projects/000-global/policies/`. The regulatory and framework references above are drawn from general knowledge of UK public-sector obligations and should be confirmed against the council's own policy set. To ground a future revision in the council's documents, place them in `projects/000-global/policies/` and re-run `/arckit:principles`.

---

**Generated by**: ArcKit `/arckit:principles` command
**Generated on**: 2026-09-03
**ArcKit Version**: 6.13.0
**Project**: Ashcombe District Council Digital Services (Project 000)
**AI Model**: Claude Fable 5.1 (claude-fable-5-1)

<!-- arckit-provenance:start -->

## Build Provenance

*Stamped automatically by the ArcKit plugin's `provenance-stamp.mjs` PostToolUse hook. Complements (does not replace) the human-authored footer above. Carries only fields the model can't authoritatively self-report: build context from `.arckit/state.json` and effort levels derived from command frontmatter + the silent-downgrade matrix.*

| Field | Value |
|-------|-------|
| Requested Effort | `high` |
| Effective Effort | _unknown — model not parsed from existing footer_ |
| Stamped at | 2026-09-03T08:07:05.209Z |

<!-- arckit-provenance:end -->
