# ASAP Acronym and Term Glossary

## Tracking

| Field | Value |
|---|---|
| Document ID | AGP-GLOSSARY-001 |
| itemType | GlossaryDocument |
| slug | asap-acronym-and-term-glossary |
| Version | 0.1.0 |
| Created | 2026-04-18 |
| Last Reviewed | 2026-04-18 |
| State | Draft |
| retentionPolicy | indefinite |
| Freshness SLA | 90 days |
| Owner | PER-01 Lena Brandt, Chief Architect |
| Approver | PER-11 Anja Petersen, Chair EARB |
| Dependencies | Architect-Support-Agentic-Platform.md |
| Sibling glossary | `../../spec-chat/WIP/SpecChat-BTABOK-Acronym-and-Term-Glossary.md` (canonical for SpecChat, CoDL, CaDL, BTABoK profile terminology) |

## 1. Purpose

This document is the single reference for acronyms, abbreviations, and terminology used across the ASAP design corpus, starting with [Architect-Support-Agentic-Platform.md](Architect-Support-Agentic-Platform.md). Entries are organized by category. Every entry lists the expansion and a one-sentence definition. Terms that originate in the SpecChat corpus (CoDL, CaDL, SpecItem, BTABoKItem, profile mechanics) are summarized here with a pointer to the SpecChat glossary for the canonical definition.

## 2. How to Use This Glossary

Entries are grouped by concern: ASAP internals, agentic platform primitives, BTABoK core, Engagement Model practice, Value Model practice, People Model practice, Competency Model practice, topic areas, organizational and integration terms, and general technical. A flat alphabetical index follows in Section 12 for quick lookup.

## 3. ASAP Internals

**ASAP**: Architect Support Agentic Platform
The deployed service platform defined by this corpus. Wraps SpecChat with agentic primitives (skills, subagents, scheduled tasks, webhooks, preview, RAG) and adds four-band authority governance for BTABoK practice work across all four models. See Architect-Support-Agentic-Platform.md Section 0.

**HITL**: Human-in-the-Loop
The design principle that every AI-produced artifact or proposal requires a named human at the decision point. ASAP defines seven HITL patterns in Architect-Support-Agentic-Platform.md Section 8.2.

**ProfileContext**: (service name)
ASAP infrastructure service that reads a collection manifest and exposes the active SpecChat profile, profile version, and validator severity policy. See Section 4.10.

**ModelContext**: (service name)
ASAP infrastructure service that tracks which BTABoK model a given interaction is serving. Sibling to ProfileContext. See Section 4.10.

**CollectionIndex**: (service name)
ASAP infrastructure service providing an mtime-cached graph of concepts and refs in a spec collection. Originates in the SpecChat MCP server plan. See Section 4.10.

**CompetencyStore**: (service name)
Practitioner-scoped store for competency self-assessment and certification data. Strictly practitioner-owned. Never written to spec collections. See Section 4.10.

**PrivacyGate**: (service name)
ASAP authorization layer mediating access to People and Competency data. Default is aggregated views; named-individual views require explicit authorization. See Section 5.6.

**RetentionSink**: (service name)
Single audit-trail destination honoring the SpecItem retentionPolicy field. Extends BTABoK retention to the agentic trail. See Section 4.10.

**DiagnosticsBus**: (service name)
Publishes SpecChat validator output to hooks, PR comments, and session UI within ASAP. See Section 4.10.

**IdentityResolver**: (service name)
Resolves SpecChat `PersonRef` to directory entries, including BIISS specialization where known. See Section 4.10.

## 4. Agentic Platform Primitives

**MCP**: Model Context Protocol
The protocol by which ASAP consumes SpecChat's deterministic tools (`validate_collection`, `project_canvas`, etc.). Also the protocol by which ASAP exposes its own tools to the harness.

**RAG**: Retrieval-Augmented Generation
Pattern whereby ASAP skills and subagents retrieve grounding material from indexed BTABoK corpora (Engagement, Value, People, Competency, Canvas, Topics, Prior-art, Incident) before responding. See Section 4.9.

**Subagent**: (term)
A specialized worker with its own system prompt and context. ASAP defines subagents per BTABoK model in Section 4.5.

**Skill**: (term)
An advisory authoring aid. Skills advise; they do not enforce. See Section 4.7.

**Hook**: (term)
A harness-enforced behavior that runs outside the model. ASAP uses hooks for enforcement-tier features (Engagement Model only). See Section 4.2.

**Slash command**: (term)
A human entry point to agentic features. ASAP slash commands are Gate-tier (require acknowledgment). See Section 4.6.

**Worktree**: (term)
An isolated sandbox for spec refactor or profile migration work. Used by the Migration Pilot subagent. See Section 4.5.

**Authority gradient**: (term)
The four-tier classification (Enforce, Gate, Advise, Inform) that every ASAP feature declares. See Section 3.

**AI-suitability band**: (term)
The four-band classification (AI-strong, AI-backstage, AI-proposer, AI-excluded) assigned to every human role covered by ASAP. See Section 8.1.

## 5. BTABoK Core

Canonical BTABoK definitions live in the SpecChat glossary at `../../spec-chat/WIP/SpecChat-BTABOK-Acronym-and-Term-Glossary.md`. Entries below are short working definitions.

**BTABoK** (also **BTABOK**): Business Technology Architecture Body of Knowledge
The IASA-published body of knowledge comprising four models (Engagement, Value, People, Competency), 75-plus structured canvases, and topic areas. Source of truth for all ASAP BTABoK-aligned features.

**IASA**: International Association of Software Architects (IASA Global)
The professional body publishing the BTABoK, CoDL, CaDL, and CITA certifications. Authoritative source for all BTABoK content ASAP retrieves.

**SpecChat**: (product name)
The upstream dependency. Owns SpecLang, the BTABOK profile, validators, and canvas rendering. Consumed by ASAP through the MCP server surface. See `../../spec-chat/WIP/SpecLang-Design.md`.

**SpecLang**: (language name)
The spec language SpecChat implements. ASAP does not modify SpecLang.

**CoDL**: Concept Definition Language
Published by IASA. The storage schema for BTABoK concepts. Canonical definition in the SpecChat glossary.

**CaDL**: Canvas Definition Language
Published by IASA. The rendering language for canvases as views over CoDL concepts.

**Profile**: (SpecChat term)
A named bundle of additions on top of Core SpecLang. SpecChat ships three: `Core`, `TheStandard`, `BTABOK`. A collection declares exactly one active profile.

**SD-ONEPROF**: Settled Decision, one profile per collection
The SpecChat v0.1 decision that a collection declares exactly one active profile. Cross-profile collections deferred to v0.2-plus. See `../../spec-chat/WIP/SpecLang-Design.md` Section 3.

**Collection**: (SpecChat term)
The container for a set of spec items under a single active profile. The unit of SpecChat delivery. ASAP reads but does not modify collections.

**SpecItem**: (SpecChat term)
The core metadata record carried by every spec item regardless of profile. ASAP's weakRef references into collections resolve at this level.

**BTABoKItem**: (SpecChat term)
The CoDL metadata record for a BTABoK concept instance under the BTABOK profile.

**weakRef**: (SpecChat term)
A cross-collection reference. ASAP sidecar artifacts in `value-model/` and `people-model/` folders reference spec collections through weakRef.

## 6. Engagement Model Practice

**ADLC**: Architecture Development Life Cycle
The six-stage BTABoK lifecycle: Innovate, Strategy, Plan, Transform, Utilize and Measure, Decommission. ASAP provides per-stage checkpoints and an ADLC stage coach subagent. See Section 7.1.

**ADR**: Architecture Decision Record
A structured record of an architectural decision with context, options, tradeoffs, rationale, and outcome. Produced by the decision scribe subagent.

**ASD**: Architecturally Significant Decision
A decision BTABoK classifies as requiring formal record. Every ASD produces an ADR or DecisionRecord.

**ASR**: Architecturally Significant Requirement
A requirement that shapes architecture. Captured in an ASRCard under the BTABOK profile.

**EARB**: Enterprise Architecture Review Board
A governance body reviewing Tier 1 architecture decisions. ASAP's governance reviewer subagent assembles EARB packets; the board decides.

**Decision Bias Calibrator**: (BTABoK canvas)
A structured check run before finalizing a decision to surface cognitive biases. Invoked by the decision scribe in Wave 2.

**Governance spectrum**: (BTABoK principle)
The BTABoK position that governance ranges from lightweight mentoring (most work) to rigorous formal review (Tier 1 only). ASAP's governance reviewer defaults to mentor tone.

**Viewpoint**: (BTABoK concept)
A stakeholder-specific lens on an architecture. Represented as a ViewpointCard.

**Transition Architecture**: (BTABoK concept)
An intermediate state between a baseline and target architecture. Modeled in roadmaps.

## 7. Value Model Practice

**NABC**: Needs, Approach, Benefits, Considerations
One-page business case format BTABoK prescribes for PMO cycles. Produced by the business case drafter subagent.

**OKR**: Objectives and Key Results
Goal-setting framework used for strategic, supporting, and practice-level objectives.

**KR**: Key Result
A measurable component of an OKR.

**SMART**: Specific, Measurable, Achievable, Relevant, Time-bound
Criteria for writing a KR.

**RVM**: Rapid Value Management
The BTABoK value-tracking discipline using three tiered indicators: early validation (30-90 days), leading (91 days to one year), lagging (end-state). ASAP implements a monthly RVM early check, quarterly leading review, annual lagging review.

**TDR**: Technical Debt Ratio
BTABoK's technical debt metric: (Remediation plus Maintenance) divided by Development, times 100. Tracked by the tech-debt portfolio analyst.

**PMO**: Project Management Office
The organizational body that allocates funding to initiatives. BTABoK frames architects as "attacking the PMO" with business cases to shape demand.

**JTBD**: Jobs-to-be-Done
BTABoK customer-understanding framework. Used by the stakeholder concern miner subagent during Discovery.

**PESTLE**: Political, Economic, Social, Technological, Legal, Environmental
Strategic scan framework. Referenced in BTABoK canvas library.

**NPS**: Net Promoter Score
Customer-satisfaction metric, used as an example KR in BTABoK objectives guidance.

**Benefits Dependency Network**: (BTABoK canvas)
Traces digital enablers to business outcomes through enabling changes and business changes. Produced by the benefits-realization modeler subagent.

**Value stream**: (BTABoK concept)
The end-to-end flow by which an organization delivers value to a stakeholder. Mapped by the value-stream mapper subagent.

**Scorecard**: (BTABoK concept)
A collection of metric definitions and targets. SpecChat already defines `ScorecardDefinition` and `MetricDefinition`; ASAP reads these for refresh.

**Principle**: (BTABoK concept)
One of 8-12 memorable guardrails guiding architectural decisions. BTABoK insists principles remain guidance, not enforced rules.

## 8. People Model Practice

**BIISS**: Business, Information, Infrastructure, Software, Solution
The five architecture specializations in BTABoK. Business, Information, Infrastructure, and Software are the four primary specializations. Solution is the generalist.

**CoP**: Community of Practice
The professional community binding a practice together. BTABoK treats the CoP as load-bearing tissue ("Community Eats Framework for Lunch").

**CoE**: Center of Excellence
An organizational unit hosting and stewarding a practice. BTABoK distinguishes federated, centralized, and value-stream CoE models.

**Managed career path**: (BTABoK concept)
Six-level progression: Aspiring, Foundation, Associate, Professional, Distinguished, Chief. Distinct from internal HR role levels.

**Extended Team**: (BTABoK concept)
Non-titled practitioners (developers, operations, business analysts, PMs) contributing architecture work within an architecture community.

**Engagement Model Steering Committee**: (BTABoK body)
Body of all architect levels that defines the practice's engagement model, success metrics, and value delivery.

**Westrum Culture Diagnostic**: (external instrument)
Culture assessment tool BTABoK references. Applied by the culture diagnostic runner subagent.

**Culture Map**: (BTABoK canvas)
A canvas-based culture assessment.

**Rotation**: (BTABoK practice)
Movement of architects through diverse experience contexts. BTABoK treats rotation as critical for skill acquisition and avoiding early specialization.

**Mentoring engagement cycle**: (BTABoK practice)
Structured 3-6 month assignments for Foundation and Associate architects, 1-3 year relationships for Professional and above. Required for Professional-plus career progression.

**HR**: Human Resources
The organizational function owning hiring, compensation, and performance. Strict AI-excluded surface for most ASAP features.

**HRIS**: Human Resources Information System
The system of record for employment data. ASAP integrates via webhook for refreshing certification and proficiency data, within PrivacyGate constraints.

**L&D**: Learning and Development
The organizational function designing learning programs. ASAP's team capability-gap analyzer produces aggregated inputs for L&D.

**SI**: Systems Integrator
External consulting organization providing contracted architects. BTABoK expects SI architects to participate in the community with equivalent competency.

## 9. Competency Model Practice

**CITA**: Certified IT Architect
IASA's certification ladder with four levels: Foundation, Associate, Professional, Distinguished. ASAP supports preparation and path planning; never grants certifications.

**Pillars (9)**: (BTABoK taxonomy)
Business Technology Strategy, Human Dynamics, Design, IT Environment, Quality Attributes, Business Architecture, Information Architecture, Infrastructure Architecture, Software Architecture. The top-level structure of the Competency Model.

**Proficiency levels (5)**: (BTABoK taxonomy)
Awareness, Basic, Delivery, Experienced, Shaping. Bloom-aligned. The five proficiency levels map unevenly to the four CITA certifications; ASAP preserves both.

**360-degree assessment**: (BTABoK practice)
Four-method assessment: self, peer, mentor, and certification. BTABoK deliberately distributes judgment. ASAP never collapses any of the four into automation.

**SFIA**: Skills Framework for the Information Age
External competency framework. Referenced in the Competency Model for cross-mapping.

**SFIA+**: Extended SFIA
SFIA plus additional architecture-specific competencies.

**TOGAF**: The Open Group Architecture Framework
External architecture framework. Its Skills Framework cross-maps to BTABoK pillars.

**e-CF**: European e-Competence Framework
European competency framework for ICT professionals. Cross-references BTABoK.

**Architect Skills Gap Analysis**: (BTABoK canvas)
Structured competency gap analysis across the pillars. Run by the Architect Skills Gap Analysis runner subagent.

## 10. Topic Areas

BTABoK treats topic areas as awareness-level contextual guides, not full frameworks. ASAP topic-area skills match this positioning.

**AI**: Artificial Intelligence
BTABoK topic area. Spans machine learning, generative AI, agentic AI, and enterprise adoption patterns.

**ML**: Machine Learning
Subset of AI. Appears in the `ai_ml.md` BTABoK topic page.

**DevOps**: Development Operations
BTABoK topic area covering the integration of development and operations practices.

**Cloud**: (topic area)
BTABoK coverage of IaaS, PaaS, SaaS, and cloud-architecture considerations.

**Security**: (topic area)
BTABoK topic area aligned with the NIST Cybersecurity Framework (Identify, Detect, Protect, Respond, Recover).

**Sustainability**: (topic area)
BTABoK topic area covering environmental, economic, and social sustainability in architecture. Aligns with ESG and the UN SDGs.

**ESG**: Environmental, Social, Governance
Sustainability framing BTABoK references in its sustainability topic area.

**UN SDG**: United Nations Sustainable Development Goals
Global goal framework BTABoK's sustainability topic area aligns to.

**Agile**: (topic area, not an acronym)
BTABoK topic area covering agile practices as they affect architecture.

**Integration**: (topic area)
BTABoK topic area on integration architecture.

**Systems**: (topic area)
BTABoK topic area on systems architecture.

## 11. Organizational, Integration, and General Technical

**GA**: General Availability
Product-lifecycle status indicating readiness for general use. SpecChat Wave 4 is the GA exit for the SpecChat product; ASAP ships its first GA after its own Wave 2.

**PR**: Pull Request
A code-review mechanism. ASAP uses PR triggers on `specs/**` to run the review subagent.

**CI**: Continuous Integration
The automated build and test pipeline. ASAP integrates via remote triggers.

**SLA**: Service Level Agreement
A commitment on behavior. ASAP uses Freshness SLA fields on spec metadata and RAG indexes (180 days for BTABoK material, 90 days for this glossary).

**UI**: User Interface
The practitioner-facing surface. ASAP UI conventions distinguish authority tiers (Enforce, Gate, Advise, Inform) and model coverage.

**CLI**: Command Line Interface
SpecChat's primary delivery shape. ASAP extends beyond the CLI into a deployed service.

**API**: Application Programming Interface
The MCP surface ASAP consumes from SpecChat is an API.

**C4**: C4 model (Context, Container, Component, Code)
Simon Brown's architecture diagramming method. ASAP includes a C4 diagram generator in Wave 4.

**OTel**: OpenTelemetry
Observability framework. Referenced as a possible source for drift detection (spec vs. runtime).

**PII**: Personally Identifiable Information
Category of data triggering PrivacyGate controls.

**DPP**: Digital Product Passport
Regulatory data concept referenced in BTABoK sustainability material. Not currently an ASAP feature.

**PER-NN**: Person reference prefix
Identifier format from the Global Corp exemplar (e.g., PER-01, PER-11). Used in tracking metadata to name owners and approvers.

**AGP-NNN**: ASAP document identifier prefix
ASAP's document ID namespace. AGP-001 is the founding platform design; AGP-GLOSSARY-001 is this glossary.

## 12. Alphabetical Index

| Acronym / Term | Section |
|---|---|
| 360-degree assessment | §9 |
| ADLC | §6 |
| ADR | §6 |
| Agile | §10 |
| AGP-NNN | §11 |
| AI | §10 |
| AI-suitability band | §4 |
| API | §11 |
| ASAP | §3 |
| ASD | §6 |
| ASR | §6 |
| Architect Skills Gap Analysis | §9 |
| Authority gradient | §4 |
| Benefits Dependency Network | §7 |
| BIISS | §8 |
| BTABoK / BTABOK | §5 |
| BTABoKItem | §5 |
| C4 | §11 |
| CaDL | §5 |
| CI | §11 |
| CITA | §9 |
| CLI | §11 |
| Cloud | §10 |
| CoDL | §5 |
| CoE | §8 |
| Collection | §5 |
| CollectionIndex | §3 |
| CompetencyStore | §3 |
| CoP | §8 |
| Culture Map | §8 |
| Decision Bias Calibrator | §6 |
| DevOps | §10 |
| DiagnosticsBus | §3 |
| DPP | §11 |
| EARB | §6 |
| e-CF | §9 |
| Engagement Model Steering Committee | §8 |
| ESG | §10 |
| Extended Team | §8 |
| GA | §11 |
| Governance spectrum | §6 |
| HITL | §3 |
| Hook | §4 |
| HR | §8 |
| HRIS | §8 |
| IASA | §5 |
| IdentityResolver | §3 |
| Integration | §10 |
| JTBD | §7 |
| KR | §7 |
| L&D | §8 |
| Managed career path | §8 |
| MCP | §4 |
| Mentoring engagement cycle | §8 |
| ML | §10 |
| ModelContext | §3 |
| NABC | §7 |
| NPS | §7 |
| OKR | §7 |
| OTel | §11 |
| PER-NN | §11 |
| PESTLE | §7 |
| PII | §11 |
| Pillars (9) | §9 |
| PMO | §7 |
| PR | §11 |
| Principle | §7 |
| PrivacyGate | §3 |
| Proficiency levels (5) | §9 |
| Profile | §5 |
| ProfileContext | §3 |
| RAG | §4 |
| RetentionSink | §3 |
| Rotation | §8 |
| RVM | §7 |
| Scorecard | §7 |
| SD-ONEPROF | §5 |
| Security | §10 |
| SFIA | §9 |
| SFIA+ | §9 |
| SI | §8 |
| Skill | §4 |
| Slash command | §4 |
| SLA | §11 |
| SMART | §7 |
| SpecChat | §5 |
| SpecItem | §5 |
| SpecLang | §5 |
| Subagent | §4 |
| Sustainability | §10 |
| Systems | §10 |
| TDR | §7 |
| TOGAF | §9 |
| Transition Architecture | §6 |
| UI | §11 |
| UN SDG | §10 |
| Value stream | §7 |
| Viewpoint | §6 |
| weakRef | §5 |
| Westrum Culture Diagnostic | §8 |
| Worktree | §4 |

## 13. Source References

**[R1]** Architect Support Agentic Platform. Workspace: [Architect-Support-Agentic-Platform.md](Architect-Support-Agentic-Platform.md). The platform design this glossary supports.

**[R2]** SpecChat and BTABOK Acronym and Term Glossary. Workspace: `../../spec-chat/WIP/SpecChat-BTABOK-Acronym-and-Term-Glossary.md`. Canonical definitions for SpecChat-originated terminology.

**[R3]** IASA Global. Business Technology Architecture Body of Knowledge. `https://iasa-global.github.io/btabok/`. Authoritative source for all BTABoK terminology.

**[R4]** IASA Global. Competency Model. `https://iasa-global.github.io/btabok/competency_model_m.html`. The nine pillars, five proficiency levels, four CITA certifications.

**[R5]** IASA Global. Structured Canvases. `https://iasa-global.github.io/btabok/structured_canvases_m.html`. The 75-plus canvas library.
