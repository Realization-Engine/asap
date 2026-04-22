# Architect Support Agentic Platform

## Tracking

| Field | Value |
|---|---|
| Document ID | AGP-001 |
| itemType | PlatformDesign |
| slug | architect-support-agentic-platform |
| Version | 0.5.0 |
| Created | 2026-04-18 |
| Last Reviewed | 2026-04-18 |
| State | Draft |
| retentionPolicy | indefinite |
| Freshness SLA | 180 days |
| Owner | PER-01 Lena Brandt, Chief Architect |
| Approver | PER-11 Anja Petersen, Chair EARB |
| Dependencies | SpecLang-Design.md, Spec-Type-System.md, SpecChat-BTABOK-Implementation-Plan.md, MCP-Server-Integration-Design.md, BTABOK-Out-of-Scope-Models.md, SpecChat-Design-Decisions-Record.md |
| New repo | `E:\Archive\GitHub\dlandi\asap` (established 2026-04-18). This document is the founding design |
| Working product name | Architect Support Agentic Platform (ASAP) |
| SpecChat relationship | Dependency, not host. SpecChat is a consumed service |

## 0. Origin and Scope Decision

This document began as a SpecChat design artifact and grew into the design for a distinct application platform. The scope divergence (practitioner and practice as unit of concern; deployed service with stores, webhooks, and schedulers; audience beyond spec authors; data governance and privacy gates) exceeded what SpecChat-the-spec-language should carry.

Decision (2026-04-18): this design becomes the basis for a new repository with its own application architecture. Working name: **Architect Support Agentic Platform (ASAP)**. SpecChat is a dependency, not a host. ASAP consumes SpecChat's profile, validator, and canvas-rendering services through the MCP server; SpecChat is unaware of ASAP.

The fork point for shippable deliverables is at the end of Wave 4. Waves 1 through 4 remain SpecChat proper (profile, enforcement, governance mechanics, rendering). Waves 5 and 6 are ASAP deliverables. This boundary is marked in Section 9.

Subsequent revisions of this document will update cross-references, move ASAP-specific open questions to a separate section, and harden the SpecChat dependency contract.

## 1. Purpose

This document defines a complete agentic support platform for an architecture practitioner working within the BTABoK.

The platform serves the practitioner across **four of the BTABoK's working models**: Engagement, Value, People, and Competency. These four are selected from the larger set the body of knowledge names (Outcome, Operating, Value, People, Engagement, Competency, Maturity, per `get_started_m.md`) because they are the working models where the practicing architect does cadence work with FORCE at stake under LLM amplification. Engagement Model support is backed by SpecChat's in-scope BTABOK profile and its validators. Value, People, and Competency Model support is delivered agentically through the advisory, knowledge, and automation layers of ASAP, without extending the SpecLang profile boundary. The remaining BTABoK models (Outcome, Operating, Maturity) are either macro framings the Engagement Model instantiates, or measurement frames that run across the others, and are out of scope for direct platform features.

The scope discipline of [BTABOK-Out-of-Scope-Models.md](../../spec-chat/WIP/BTABOK-Out-of-Scope-Models.md) is preserved. The three out-of-profile models are out of scope for the **SpecLang profile**. They are **in scope for ASAP**. The distinction is load-bearing. Profile extension adds validators, concept types, and schema enforcement to a spec collection. Platform support adds agentic guidance, retrieval, orchestration, and automation around a practitioner's work without modifying the spec language.

This v0.5 revision is grounded in a direct read of the IASA BTABoK corpus and formalizes the separation from SpecChat. BTABoK's own framing shapes the content of Sections 3, 7, and 8.

## 2. Framing: Three Axes

A complete agentic platform is best understood as a cube across three axes.

**Axis A. The practitioner lifecycle.** Eight stages:

1. Discovery (interviews, concern mining, domain scan, Jobs-to-be-Done, empathy mapping)
2. Authoring (concept-by-concept spec creation)
3. Governance (decisions, waivers, review bodies)
4. Validation (profile validators, severity policy, migration)
5. Rendering (canvases, diagrams, stakeholder views)
6. Operation (runtime drift, scorecard refresh, metric reconciliation, Rapid Value Management)
7. Audit (retention, trail reconstruction, evidence packets)
8. Learning (onboarding, terminology, career progression, mentoring)

**Axis B. The agentic primitive menu.** Ten primitives:

1. MCP tools (deterministic computation)
2. Hooks (harness-enforced behaviors)
3. Scheduled tasks (cron, interval, calendar)
4. Remote triggers (PR, webhook, CI)
5. Subagents (specialized, context-isolated workers)
6. Slash commands (human entry points)
7. Skills (advisory authoring aids)
8. Preview and rendering (visual output)
9. Knowledge retrieval (RAG over BTABoK and adjacent corpora)
10. Worktrees (isolated sandboxes)

**Axis C. BTABoK model coverage.** Four models, each with a distinct agentic signature:

1. **Engagement Model.** Spec-authoring heavy. Profile-backed. Enforcement available. Organizes the six-stage Architecture Development Life Cycle (ADLC).
2. **Value Model.** Planning, portfolio, and outcome heavy. Interwoven with Engagement in BTABoK's own treatment, with Engagement carrying the execution side and Value carrying the outcome and measurement side. Advisory only.
3. **People Model.** Team, role, community, and managed-career-path heavy. Integration-heavy (directory, HR). Privacy-bounded. Advisory only.
4. **Competency Model.** Taxonomy of five pillars, five BIISS specializations, and five proficiency levels. Knowledge-retrieval heavy. Advisory only.

Every platform feature sits in a cell of this cube. Section 6 lays out the lifecycle-by-primitive matrix. Section 7 walks through each model's agentic surface using BTABoK's own vocabulary.

## 3. Authority Gradient

Agentic features vary in the force they apply to a practitioner. The platform makes the gradient legible.

| Tier | Force | Primitives | Example |
|---|---|---|---|
| Enforce | Blocks the action | Hooks, MCP validators in strict mode | Commit refused on Error severity diagnostic |
| Gate | Requires acknowledgment | Slash commands, PR status checks | Reviewer must approve the waiver chain before merge |
| Advise | Offers and argues | Skills, subagents | Value Model skill proposes benefits-realization fields |
| Inform | Provides facts | MCP tools, RAG retrieval, preview | Canvas renderer returns the projected view |

A feature should choose its tier deliberately. Enforcement earns trust when it is narrow and correct. Advice retains the practitioner's agency.

BTABoK itself is explicit about governance as a spectrum rather than a uniform enforcement layer: "Architects should be governed, not doing the governing" and "governance should enable agility, not become a police state." The platform's enforcement tier must honor this. Strict validation is appropriate for the spec language and the BTABoK profile rules that a collection has opted into. It is not appropriate as a general posture for BTABoK practice guidance.

Model coverage interacts with the gradient. Enforce-tier features are available only for the Engagement Model because only the Engagement Model has a backing profile with validators. Value, People, and Competency features operate at the Advise and Inform tiers only. This is deliberate and permanent. A platform that enforces Value Model judgment on a collection has quietly become a Value Model profile, which v0.1 scope discipline forbids.

## 4. Platform Components

The platform is ten layered components. Each has a bounded responsibility and a defined interface.

### 4.1 Deterministic core (MCP tools)

The factual backbone. Never summarized by a model.

Existing: `validate_collection`, `project_canvas`, `migrate_to_btabok`, `get_supported_versions`, `get_deprecation_schedule`.

Proposed, Engagement-aligned: `resolve_weakref`, `check_freshness_sla`, `expand_waiver_chain`, `diff_transition_architecture`, `simulate_severity_policy`, `assemble_earb_packet`, `render_roadmap`, `detect_drift`, `export_audit_trail`.

Proposed, Value-aligned: `compute_benefits_dependency`, `score_tech_debt_portfolio` (using BTABoK's Technical Debt Ratio: Remediation plus Maintenance over Development times 100), `evaluate_investment_tradeoff`, `refresh_scorecard`, `run_rvm_check` (Rapid Value Management early or leading indicator check).

Proposed, People-aligned: `compute_role_coverage`, `list_governance_body_members`, `summarize_team_topology`, `check_mentoring_coverage`, `compute_rotation_status`.

Proposed, Competency-aligned: `list_competency_areas` (across the 5 pillars, 5 BIISS specializations, and 80-plus areas), `assess_team_coverage`, `map_cita_path` (across the 4 certifications Foundation, Associate, Professional, Distinguished), `compute_proficiency_gap` (against the 5 proficiency levels).

Authority tier: Inform as queries, Enforce when wired through hooks.

### 4.2 Enforcement layer (hooks)

Hooks run outside the model and cannot be argued with. **Engagement Model only**, because only Engagement has validators.

Candidates:
- `SessionStart` loads the manifest, surfaces the active profile, lists stale specs.
- `UserPromptSubmit` on a collection root injects profile context.
- `PostToolUse` on Edit to `specs/**` runs the profile validator subset and blocks commit on Error severity.
- `PreCompact` persists unresolved diagnostics into a workspace note.
- `Stop` emits an audit record capturing tools run, specs touched, diagnostics raised.

Authority tier: Enforce.

### 4.3 Automation layer (scheduled tasks)

BTABoK is calendrical. Scheduled tasks own the calendar across the four working models the platform covers.

Engagement-aligned:
- Nightly freshness SLA sweep.
- Daily waiver expiry scan with N-day lookahead.
- EARB morning agenda assembly.
- Per-stage ADLC checkpoints: did each stage have sufficient stakeholder buy-in, resources, and success criteria to advance?
- Monthly archived-spec rot check.

Value-aligned (the Rapid Value Management cadence is explicit in BTABoK):
- Monthly RVM early validation check (30-90 days since initiative start).
- Quarterly leading indicator review (91 days to one year).
- Annual lagging indicator and end-state benefits review.
- Weekly scorecard refresh against `MetricDefinition` and `ScorecardDefinition` targets.
- Quarterly tech-debt portfolio refresh (Technical Debt Ratio tracking).
- Annual investment prioritization prompt before the funding cycle ("attack the PMO" support).
- Annual OKR and objectives review.
- Annual principles review (keep to the 8-12 memorable rule).

People-aligned:
- Quarterly team topology review prompt.
- Annual succession and coverage scan.
- Governance-body membership rotation alerts.
- Architect rotation cadence tracking (BTABoK treats rotation as critical for skill acquisition).
- Engagement Model Steering Committee prompts.

Competency-aligned:
- Quarterly team capability-coverage scan against role requirements and specialization.
- CITA maintenance prompts (annual hours for contribution, learning, delivery focus; required for Professional and above).
- Certification expiry alerts (CITA, SFIA plus, TOGAF).
- Mentoring engagement cycle checkpoints (3-6 months for Foundation and Associate, 1-3 years for Professional).
- Annual learning-plan refresh.

Authority tier: Inform, with Gate escalation for notifications that require acknowledgment.

### 4.4 Integration layer (remote triggers and CI)

Spec change rarely happens in isolation.

Candidates:
- PR trigger on `specs/**`: runs the review subagent, posts a digest, applies a status check.
- Webhook on incident created: associates with affected specs via the concept graph.
- Tag on release: publishes the canvas bundle and audit trail export.
- Webhook on IASA BTABoK version change: flags profile freshness and knowledge-base freshness for review.
- Directory sync webhook (People Model): refreshes the IdentityResolver on org changes.
- HRIS or learning-system webhook (Competency Model): refreshes certification and proficiency data.
- PMO or portfolio-system webhook (Value Model): refreshes initiative status for demand shaping.

Authority tier: Gate for the PR status check, Inform for the others.

### 4.5 Specialist workers (subagents)

Subagents carry their own system prompt and context. They are the right home for multi-step work.

Engagement-aligned:
- **Governance reviewer** ingests a proposed DecisionRecord, affected ASRs, active waivers. Produces an EARB readiness packet. Tone: mentor, not police.
- **Stakeholder concern miner** reads meeting transcripts or interview notes. Drafts StakeholderCard, ASRCard candidates. Uses BTABoK's Jobs-to-be-Done and empathy-map structures.
- **Migration pilot** runs a Core to BTABOK migration in a worktree, returns the diff and a risk summary.
- **Drift detector** compares spec assertions against runtime telemetry and code.
- **Decision scribe** turns a meeting transcript into a DecisionRecord draft with explicit options, consequences, reversibility. Invokes the Decision Bias Calibrator step before finalizing.
- **Roadmap planner** proposes TransitionArchitecture steps between a baseline and a target.
- **ADLC stage coach** helps a practitioner enter or exit any of the six ADLC stages (Innovation Cycle, Strategy, Planning, Transformation, Utilize and Measure, Decommissioning, per `architecture_lifecycle.md`) using the matching BTABoK canvases.

Value-aligned:
- **Benefits-realization modeler** drafts a benefits-dependency network from a strategic goal.
- **Value-stream mapper** produces a value-stream representation from capabilities and interactions.
- **Tech-debt portfolio analyst** organizes debt items with Technical Debt Ratio scoring.
- **Investment prioritizer** ranks candidate initiatives against active principles and the scorecard.
- **Business case drafter** produces NABC-format (Needs, Approach, Benefits, Considerations) briefs for the PMO.
- **RVM coach** walks a practitioner through early validation, leading, and lagging indicator definition for a new initiative.

People-aligned:
- **Team topology analyst** describes current team boundaries, dependencies, cognitive-load hot spots.
- **Role coverage mapper** identifies role gaps against delivery and governance needs, using the BIISS specialization taxonomy (Business, Information, Infrastructure, Software, plus Solution).
- **Community health observer** summarizes community-of-practice signals (fragmentation, isolation, mentoring coverage).
- **Mentoring matchmaker** proposes mentor-mentee pairings based on pillar-level strengths and gaps.
- **Culture diagnostic runner** applies the Westrum Culture Diagnostic and Culture Map to a team.

Competency-aligned:
- **Competency self-assessment coach** walks a practitioner through self-rating across the five pillars and their chosen BIISS specialization.
- **Certification path planner** maps a practitioner's current level to a CITA progression plan (Foundation, Associate, Professional, Distinguished).
- **Team capability-gap analyzer** aggregates individual competency data into team gap analysis, with privacy controls.
- **Architect Skills Gap Analysis runner** uses the BTABoK canvas of the same name.
- **Peer-assessment orchestrator** manages 360-degree assessment cycles (self, peer, mentor, certification).

Authority tier: Advise. None of these has commit or merge authority on governance artifacts.

### 4.6 Human entry points (slash commands)

Existing: `/spec-btabok`.

Engagement-aligned: `/spec-new <type>`, `/spec-review`, `/spec-waiver`, `/spec-canvas <name>`, `/spec-freshness`, `/spec-earb-prep`, `/spec-migrate`, `/spec-adlc <stage>`.

Value-aligned: `/spec-value-draft`, `/spec-scorecard`, `/spec-techdebt`, `/spec-nabc` (business case drafter), `/spec-rvm` (Rapid Value Management setup).

People-aligned: `/spec-team-topology`, `/spec-role-coverage`, `/spec-mentor-match`, `/spec-culture-diagnostic`.

Competency-aligned: `/spec-competency-assess`, `/spec-cita-plan`, `/spec-team-capability`, `/spec-skills-gap` (Architect Skills Gap Analysis).

Authority tier: Gate.

### 4.7 Advisory layer (skills)

Engagement-aligned:
- `spec-btabok` core BTABoK authoring guide.
- `spec-adlc` six-stage lifecycle navigator.
- `spec-canvas-library` picker and renderer across the 75-plus BTABoK canvases.
- `spec-jtbd` Jobs-to-be-Done and empathy-mapping guide.
- `spec-onboarding` new-practitioner walkthrough.

Value-aligned:
- `spec-value` Value Model authoring aid.
- `spec-benefits-realization` benefits-dependency modeling guide.
- `spec-value-stream` value-stream mapping guide.
- `spec-investment` investment prioritization and tech-debt portfolio guide.
- `spec-rvm` Rapid Value Management guide with the three indicator tiers.
- `spec-principles` guide to the 8-12 memorable-principle rule.

People-aligned:
- `spec-people` People Model aid.
- `spec-team-topologies` team-boundary and cognitive-load guide.
- `spec-role-definition` role and BIISS specialization authoring guide.
- `spec-career-path` managed-career-path navigator across the six levels (Aspiring, Foundation, Associate, Professional, Distinguished, Chief).
- `spec-mentoring` mentoring-relationship guide.
- `spec-extended-team` guide for non-titled practitioners doing architecture work.

Competency-aligned:
- `spec-competency` competency-model navigator across the five pillars and BIISS specializations.
- `spec-cita-prep` CITA certification preparation guide for each of the four levels.
- `spec-learning-plan` personal learning plan guide.

Topic-area lenses (cross-cutting, brief per BTABoK's own treatment): `spec-topic-ai`, `spec-topic-cloud`, `spec-topic-security`, `spec-topic-sustainability`, `spec-topic-devops`, `spec-topic-integration`, `spec-topic-agile`. These are context-aware lenses, not full frameworks. The skill wording must match BTABoK's own positioning ("starting points for awareness").

Authority tier: Advise.

### 4.8 Rendering and communication (preview)

Engagement-aligned:
- CaDL canvas renderer for all 20 in-profile canvases.
- C4 diagram generator from the systems register.
- Roadmap visualizer for baseline, transition, target.
- ADLC progress view across the six stages.
- Dependency graph of concepts and refs.

Value-aligned:
- Benefits dependency network diagram.
- Value-stream map.
- Scorecard dashboard view.
- Tech-debt quadrant with Technical Debt Ratio.
- RVM indicator timeline across early, leading, lagging tiers.

People-aligned:
- Team topology map.
- Role coverage heatmap across the BIISS specializations.
- Governance-body composition diagram.
- Career progression ladder across the six levels.
- Mentoring network graph.

Competency-aligned:
- Competency radar across the five pillars and BIISS specializations.
- Team capability heatmap against role requirements.
- CITA progression timeline.
- Proficiency matrix at the five levels.

Authority tier: Inform.

### 4.9 Knowledge layer (RAG)

The highest-leverage investment for out-of-profile model support. Separate indexes per domain, all queryable from skills, subagents, and slash commands.

- **Engagement index.** IASA Engagement Model pages, SpecChat design docs, glossary, decisions record, ADLC material.
- **Value index.** IASA Value Model pages, benefits-dependency and value-stream literature, Technical Debt Ratio references, RVM material.
- **People index.** IASA People Model pages, team topologies literature, community-of-practice literature, Westrum and culture diagnostic material.
- **Competency index.** IASA Competency Model pages (five pillars, five BIISS specializations, 80-plus areas across both), SFIA plus, TOGAF Skills Framework, European e-CF, CITA levels.
- **Canvas index.** IASA structured canvas catalog covering all 75-plus canvases. Cross-references every canvas to its competency pillar links (BTABoK canvases explicitly map back to competencies).
- **Topics index.** IASA topic-area pages. Shallow by BTABoK's own design, used for awareness rather than deep guidance.
- **Prior-art index.** Cross-collection DecisionRecord repository.
- **Incident index.** Postmortems and incident reports where referenced.

Retrieval replaces "encode into the profile" with "retrieve at authoring time" for any content that does not belong in the spec language.

Authority tier: Inform.

### 4.10 Shared infrastructure

- `ProfileContext`: reads the manifest, exposes active profile, profile version, severity policy.
- `ModelContext`: tracks which BTABoK model a given interaction is serving. Used by skills and subagents. Defaults to Engagement in a BTABOK-profiled collection.
- `CollectionIndex`: mtime-cached graph of concepts and refs.
- `IdentityResolver`: resolves PersonRef to directory entries. Carries BIISS specialization where known.
- `CompetencyStore`: practitioner-scoped store for competency self-assessment and certification data. Strictly practitioner-owned.
- `RetentionSink`: single audit-trail destination honoring the retentionPolicy field.
- `DiagnosticsBus`: publishes validator output to hooks, PR comments, and the session UI.
- `PrivacyGate`: enforces People and Competency data access controls. Aggregated views default; named-individual views require explicit authorization.

Authority tier: Infrastructure, no direct user contact.

## 5. Cross-Cutting Architecture Concerns

### 5.1 Profile awareness

Every layer reads the active profile from `ProfileContext` at invocation time. Enforcement is Engagement Model only. Advisory features read `ModelContext` to tailor guidance to the model the practitioner is currently engaged with.

### 5.2 Scope boundary preservation

The platform does not widen the SpecLang profile boundary. Value, People, and Competency support is delivered through RAG, advisory skills, subagents, and scheduled tasks. No validator, concept type, or schema rule for these models enters a collection's active profile.

When an out-of-profile interaction produces an artifact the practitioner wants to keep, the platform writes it to a sibling folder (`value-model/`, `people-model/`) and references it with `weakRef` from the spec collection. Competency data is a deliberate exception: it lives in the practitioner-scoped `CompetencyStore`, never in a collection.

### 5.3 Authority legibility

The practitioner must always be able to tell which tier a feature is operating in. Model coverage is also visible: a Value Model skill identifies itself as Value Model and as advisory.

### 5.4 Retention and audit trail

The agentic trail extends BTABoK retention policy. The RetentionSink is the single destination. Trails for People and Competency features pass through the PrivacyGate.

### 5.5 Governance judgment boundary

Mechanics can be automated. Judgment cannot. The platform assembles review packets, surfaces risks, drafts candidate entries. It does not approve waivers, close decisions, sign off on ASRs, award certifications, or adjust compensation bands.

BTABoK is especially clear on this at the Engagement and People boundaries. The governance reviewer subagent is a mentor, not a police officer. The mentoring matchmaker proposes pairings; it does not assign them. The team capability-gap analyzer produces aggregate views; it does not recommend HR actions. These constraints are not optional.

### 5.6 Privacy boundary

People and Competency data is sensitive. The PrivacyGate mediates access. Defaults:
- Aggregated and anonymized views are open to any practitioner in the same collection.
- Named-individual views require explicit authorization from the data subject or an authorized approver.
- Competency self-assessment data is practitioner-owned and not retained without consent.
- Team capability views aggregate individual data but suppress identifying detail below a small-team threshold.
- Culture diagnostic results are team-scoped and aggregated.

### 5.7 Grounding and source authority

Content that contradicts IASA BTABoK authoritative material is a defect. Skills and subagents that cite practice guidance must ground in the RAG index and cite source. Each model index carries a freshness SLA of 180 days.

The canvas index is a special case: BTABoK canvases explicitly cross-reference competencies. The RAG layer preserves those cross-references so a canvas query can surface the relevant pillars, and a competency query can surface the canvases that exercise it.

### 5.8 Failure modes and guardrails

- Hooks that block must be narrow.
- Scheduled tasks must be idempotent and observable.
- Subagents fail closed. On error they return an advisory note, never a decision.
- RAG attributes every retrieved snippet. Ungrounded claims are errors.
- Privacy-gated features fail closed. Absence of authorization denies access.

## 6. The Lifecycle-by-Primitive Matrix

A marked cell is a strong fit. Unmarked is not a prohibition.

| Stage / Primitive | MCP | Hook | Sched | Remote | Subagent | Slash | Skill | Preview | RAG | Worktree |
|---|---|---|---|---|---|---|---|---|---|---|
| Discovery |  |  |  |  | X | X | X |  | X |  |
| Authoring | X | X |  |  | X | X | X | X | X |  |
| Governance | X | X | X | X | X | X |  |  | X |  |
| Validation | X | X | X | X |  | X |  |  |  | X |
| Rendering | X |  |  |  |  | X |  | X |  |  |
| Operation | X |  | X | X | X |  |  | X |  |  |
| Audit | X | X | X |  |  | X |  |  |  |  |
| Learning |  |  |  |  |  | X | X |  | X |  |

Worktrees are reserved for Migration Pilot and bulk refactor work in the Validation stage.

## 7. Agentic Support by BTABoK Model

Each model is served by a distinct mix of the ten primitives. This section uses BTABoK's own vocabulary wherever possible.

### 7.1 Engagement Model

Status: in scope for the BTABoK profile. Fully supported across all four authority tiers.

BTABoK framing. The Engagement Model is the operating framework that describes how architecture practices execute work across the full lifecycle. Its core workflow is the **Architecture Development Life Cycle (ADLC)** with six iterative stages per `architecture_lifecycle.md`: **Innovation Cycle, Strategy, Planning, Transformation, Utilize and Measure, Decommissioning**. The practice of architecture in BTABoK's own words is outcomes-focused ("the outcome of the work is more important than the method of achieving that outcome", from `engagement.md`) and customer-obsessed ("Stop Doing Architecture, Start Digitally Enhancing Your Customer", the principle heading in `engagement.md`).

Characteristic work. ADLC stage entry and exit; architecturally significant decisions (ASDs) with traceability; ASR cards; waiver chains; governance bodies operating as a spectrum from lightweight mentoring to rigorous Tier 1 review; principles as 8-12 memorable guardrails; viewpoint cards; transition architectures; roadmaps.

Primary primitives. MCP tools, hooks, subagents (governance reviewer, migration pilot, decision scribe with Decision Bias Calibrator, ADLC stage coach), slash commands, preview (canvases, C4, roadmap, ADLC view), skills (`spec-btabok`, `spec-adlc`, `spec-jtbd`).

Enforcement available. Yes. The BTABoK profile's 13 validators and the core 10 validators run through hooks.

Named BTABoK workflows the platform automates:
- **Demand shaping** ("attack the PMO"). Architects create business cases (NABC) before the PMO prioritization cycle. Platform support: `/spec-nabc`, business case drafter subagent, annual scheduled prompt.
- **ASD capture**. Every architecturally significant decision logged with explicit options, consequences, reversibility. Platform support: decision scribe, Decision Bias Calibrator invocation, governance reviewer for EARB-tier decisions.
- **Governance inspection**. Bottom-up mentoring for most work; formal review for Tier 1. Platform support: governance reviewer subagent with tone set to mentor; EARB packet assembly only for Tier 1 decisions.
- **Principle development and review**. Annual workshop to maintain the 8-12 memorable principles. Platform support: annual scheduled prompt, `spec-principles` skill.
- **Roadmap update**. Quarterly realignment with business context. Platform support: roadmap planner subagent, roadmap visualizer, quarterly scheduled prompt.

Delivery dependency. [SpecChat-BTABOK-Implementation-Plan.md](../../spec-chat/WIP/SpecChat-BTABOK-Implementation-Plan.md) Phases 1 through 4 underwrite the profile the enforcement layer depends on.

### 7.2 Value Model

Status: out of profile, in platform. Advisory and Inform tiers only.

BTABoK framing. Value Model is interwoven with Engagement. The platform reflects this: Value features often run adjacent to Engagement features rather than in separate sessions. A useful characterization of the split: Engagement carries how the architect executes work across the lifecycle; Value carries why the work was undertaken and whether benefits are realized. The characterization is ours, not a direct BTABoK quotation; the underlying interweaving is BTABoK's own.

Characteristic work. Objectives as SMART key results; investment planning with demand shaping; tech-debt portfolios measured by **Technical Debt Ratio** (Remediation plus Maintenance over Development times 100, managed as a healthy payback schedule); value streams; **Rapid Value Management** with three tiered indicators (early validation 30-90 days, leading 91 days to one year, lagging at end-state); principles as value-driven guardrails; risk methods; structural complexity analysis.

Primary primitives. Skills (`spec-value`, `spec-benefits-realization`, `spec-value-stream`, `spec-investment`, `spec-rvm`, `spec-principles`), subagents (benefits-realization modeler, value-stream mapper, tech-debt portfolio analyst, investment prioritizer, business case drafter, RVM coach), scheduled tasks (monthly RVM early check, quarterly leading review, annual lagging review, weekly scorecard, quarterly tech-debt portfolio, annual investment and OKR prompt, annual principles review), preview (benefits dependency network, value-stream map, scorecard dashboard, tech-debt quadrant, RVM timeline), RAG Value index, MCP tools (`compute_benefits_dependency`, `score_tech_debt_portfolio`, `evaluate_investment_tradeoff`, `refresh_scorecard`, `run_rvm_check`).

Named BTABoK workflows the platform automates:
- **NABC business case drafting**. Needs, Approach, Benefits, Considerations on one page for the PMO cycle.
- **Benefits dependency network construction**. Digital enablers traced to business outcomes.
- **Rapid Value Management**. Initiative-level tracking across the three indicator tiers with distinct cadences. This is the core operational Value workflow.
- **Technical debt portfolio management**. Debt organized as healthy payback, not moral failure. Tracked via Technical Debt Ratio.
- **Investment prioritization**. Candidate initiatives ranked against active principles and the scorecard.

Partial overlap with the profile. `MetricDefinition` and `ScorecardDefinition` exist in the Engagement profile. Value Model scheduled tasks read these to drive scorecard refresh without profile change. This is the cleanest pattern for platform-profile collaboration.

Output placement. Sibling `value-model/` folder, referenced by `weakRef` from the spec collection.

### 7.3 People Model

Status: out of profile, in platform. Advisory and Inform tiers only. Privacy-bounded.

BTABoK framing. The People Model defines the structure, reporting, and administration of the group of internal architects, extended team members, and external influences shaping an architecture practice. It treats architecture as a profession requiring external competency validation, not merely employer-defined roles.

Characteristic work. Organization (federated, centralized, value-stream); **BIISS specializations** (Business, Information, Infrastructure, Software, Solution, with the last as generalist); **managed career path** across six levels (Aspiring, Foundational, Associate, Professional, Distinguished, Chief) per `career.md`; extended team (non-titled practitioners doing architecture work); mentoring required at every critical career-path transition per the IASA Mentoring Method (`adopting_the_competency_model.md` line 155-156), with progressively deeper relationships at Professional and Distinguished; community of practice; culture (Westrum Culture Diagnostic, Culture Map); role definitions; mindset.

Primary primitives. Skills (`spec-people`, `spec-team-topologies`, `spec-role-definition`, `spec-career-path`, `spec-mentoring`, `spec-extended-team`), subagents (team topology analyst, role coverage mapper, community health observer, mentoring matchmaker, culture diagnostic runner), directory and HR webhooks, scheduled tasks (team topology review, succession scan, governance rotation, architect rotation tracking, Engagement Model Steering Committee prompts), preview (team topology map, role coverage heatmap, governance composition, career progression ladder, mentoring network), RAG People index, MCP tools (`compute_role_coverage`, `list_governance_body_members`, `summarize_team_topology`, `check_mentoring_coverage`, `compute_rotation_status`).

Named BTABoK workflows the platform automates:
- **Architect rotation**. BTABoK treats rotation as critical for skill acquisition. Scheduled tracking of time-in-role and cross-domain exposure.
- **Mentoring engagement cycles**. 3-6 month assignments for Foundation and Associate, 1-3 year or longer for Professional. The mentoring matchmaker proposes; humans confirm.
- **Architect Skills Gap Analysis**. Direct BTABoK canvas, rendered and tracked over time.
- **Community health monitoring**. Fragmentation between specializations is a named BTABoK risk ("Specialization-Based Conflict Destroys Practices"). The community health observer watches for signals.

Partial overlap with the profile. Core SpecItem metadata uses `PersonRef` for `authors`, `reviewers`, `committer`. The People Model platform layer resolves these into organizational context (team, BIISS specialization, career level, reporting chain) without embedding that context in the spec.

Privacy. Primary concern throughout. PrivacyGate mediates every feature. BTABoK itself signals relational sensitivity: reporting structure changes, mentoring relationships, community conflict, and extended-team credibility are all flagged as requiring human judgment before acting. The platform respects this.

Output placement. Sibling `people-model/` folder, referenced by `weakRef` where useful.

### 7.4 Competency Model

Status: out of profile, in platform. Advisory and Inform tiers only. Strongly privacy-bounded.

BTABoK framing. The Competency Model is the professional development substrate. Platform support for this model is **practitioner development**, not spec authoring. The separation is intentional and permanent.

Structure (from the BTABoK Manifesto and `competency.md`):
- **5 pillars**: Business Technology Strategy, Human Dynamics, Design, Quality Attributes, IT Environment. Every architect shares these.
- **5 BIISS specializations**: Business, Information, Infrastructure, Software, Solution (the last as a generalist), layered laterally on top of the five pillars.
- **80-plus competency areas** distributed across the five pillars (42 core per `competency.md`) and the specialization tracks (additional areas per specialization).
- **5 proficiency levels** (Awareness, Basic, Delivery, Experienced, Shaping), Bloom-aligned, per `competency.md` line 46-52.
- **4 CITA certification levels** (Foundation, Associate, Professional, Distinguished). Note the asymmetry: proficiency levels count five, certifications count four. The platform preserves both.
- **6-level managed career path** (Aspiring, Foundational, Associate, Professional, Distinguished, Chief) per `career.md`, distinct from the CITA certification ladder. Aspiring is pre-certification; Chief is post-Distinguished and recognized through demonstrated practice.
- **360-degree assessment** via self, peer, mentor, and certification (per `adopting_the_competency_model.md` line 139). All four methods are first-class.

Primary primitives. Skills (`spec-competency`, `spec-cita-prep`, `spec-learning-plan`), subagents (competency self-assessment coach, certification path planner, team capability-gap analyzer, Architect Skills Gap Analysis runner, peer-assessment orchestrator), RAG Competency index, scheduled tasks (quarterly capability scan, CITA maintenance prompts, certification expiry, mentoring checkpoints, annual learning-plan refresh), preview (competency radar across the five pillars and BIISS specializations, team capability heatmap, CITA timeline, proficiency matrix), MCP tools (`list_competency_areas`, `assess_team_coverage`, `map_cita_path`, `compute_proficiency_gap`), HRIS integration webhook.

Named BTABoK workflows the platform automates:
- **Self-assessment cycle**. Individual practitioner rates against the five pillars and their chosen BIISS specialization.
- **Peer assessment cycle**. Peer scores the same areas, scoped by team trust.
- **Mentor review cycle**. Mentor reviews demonstrated work products. Per `adopting_the_competency_model.md`, reviewed mentor outputs are required at every critical career-path transition; Professional and Distinguished levels require the deepest mentoring relationships (one-to-three years or longer, per `mentoring.md`).
- **CITA path mapping**. Current level to target progression plan with maintenance hour tracking.
- **Team capability-gap analysis**. Aggregated view suppressing identifying detail below the small-team threshold.

No overlap with the profile. By design. The platform layer never puts competency data into a spec.

Privacy. Maximum. Self-assessment data is practitioner-owned and stored in `CompetencyStore`, not in collections. Team aggregations enforce the small-team threshold. Certification data may be surfaced with authorization. No subagent recommends HR actions (compensation, promotion, termination, hiring). The platform supports preparation and path planning; it does not grant certifications.

Output placement. Practitioner-scoped `CompetencyStore`, distinct from collections.

### 7.5 Cross-Model Topic Areas

BTABoK topic areas (AI, Cloud, Security, Integration, DevOps, Sustainability, Systems, Agile) are **awareness-level contextual guides**, not full frameworks. BTABoK itself describes them as "starting points where topic areas provide context for IT architects to be aware of." The platform honors this framing.

Implementation: topic-area skills (`spec-topic-<area>`) invocable in any model context. Each reads `ModelContext` and tailors guidance to the model currently engaged. The skills are brief. They surface relevant canvases and competencies and point to deeper IASA references. They do not pretend to be authoritative on cloud, security, or AI.

## 8. Human-in-the-Loop Role Architecture

Sections 4 and 7 specify what each platform component does. This section specifies what each component is not allowed to do, keyed to the human roles BTABoK names in the three out-of-profile models. It makes the authority gradient of Section 3 concrete at the role level rather than the feature level.

### 8.1 The AI-Suitability Gradient

Roles across the Value, People, and Competency models sort into four bands:

1. **AI-strong.** Drafting artifacts, running cadences, aggregating data, coaching walkthroughs, surfacing evidence. AI carries most of the work. A named human confirms.
2. **AI-backstage.** Preparing material for a human role (mentor packets, manager calibration aids, hiring interview scorecards). AI never surfaces in the primary relationship. It prepares the human.
3. **AI-proposer.** Matchmaking, rotation, ranking against rubrics. AI produces proposals. Humans accept, modify, or reject each one.
4. **AI-excluded.** Performance rating, mentor judgment, certification, compensation, hiring, firing, funding allocation. AI has no authority here and must not produce output that reads as a recommendation.

Every subagent, MCP tool, scheduled task, and skill is assigned to exactly one band. The assignment is a property of the feature's design, not a runtime decision.

### 8.2 The HITL Pattern Language

Seven safeguard patterns recur across role-level analysis. The delivery plan references these by name.

| Pattern | Description | Example |
|---|---|---|
| Draft-and-review | AI drafts; named human owns the artifact | Decision scribe produces a DecisionRecord; architect signs |
| Assemble-and-present | AI gathers inputs; human interprets and acts | Governance reviewer assembles the EARB packet; chair decides |
| Propose-and-confirm | AI suggests an action; human confirms each one | Mentoring matchmaker proposes pairings; mentor and mentee confirm |
| Monitor-and-alert | AI watches signals; human decides response | RVM coach flags deviation; benefit owner decides continue, restructure, or decommit |
| Coach-and-capture | AI guides a practitioner-owned process; data stays with the practitioner | Self-assessment coach walks the pillars; `CompetencyStore` owned by the practitioner |
| Shadow-and-record | AI observes; human acts; AI builds the audit trail | Culture diagnostic facilitator runs the exercise; AI aggregates and records outcomes |
| Gate-and-block | AI cannot proceed past a checkpoint without an explicit human signal | Hiring scorecard prep cannot export candidate rankings; manager must author the decision |

### 8.3 Value Model Roles

| Role | Band | Primary pattern | HITL safeguard |
|---|---|---|---|
| Executive sponsor | AI-strong | Draft-and-review | Sponsor owns OKR wording; quarterly review required |
| Strategic planner | AI-strong | Draft-and-review | Planner selects; no option auto-adopted |
| Investment prioritizer (portfolio committee) | AI-proposer | Propose-and-confirm | Committee decides; AI ranking is input, not verdict |
| Business case author (architect) | AI-strong | Draft-and-review | Architect signs; sponsor countersigns |
| PMO analyst | AI-strong | Assemble-and-present | PMO runs the cycle; AI output is agenda material |
| Benefit owner | AI-strong | Monitor-and-alert | Owner decides continue, restructure, or decommit |
| Value stream owner | AI-strong | Monitor-and-alert | Owner decides interventions |
| Capability owner | AI-strong | Draft-and-review | Owner funds and sequences |
| Tech-debt steward | AI-strong | Assemble-and-present | Steward approves; portfolio committee funds |
| RVM monitor | AI-strong | Monitor-and-alert | Monitor and benefit owner decide the response |
| Principle author (practice) | AI-strong | Draft-and-review | Workshop group adopts |
| Risk owner | AI-strong | Draft-and-review | Owner decides accept, transfer, or mitigate |
| Scorecard owner | AI-strong | Draft-and-review | Owner signs off on scorecard revisions |
| Objectives cascader | AI-strong | Draft-and-review | Team leads commit |

Stop-line. AI never allocates funding, approves a business case, or signs OKRs on behalf of a human.

### 8.4 People Model Roles

| Role | Band | Primary pattern | HITL safeguard |
|---|---|---|---|
| Chief Architect | AI-strong | Draft-and-review | Communications reviewed before sending |
| Distinguished Architect | AI-strong | Draft-and-review | Architect owns every output |
| Professional Architect | AI-strong | Draft-and-review | Architect retains decision rights |
| Associate Architect | AI-strong | Coach-and-capture | Mentor approves progression |
| Foundation Architect | AI-strong | Coach-and-capture | Mentor oversees progression |
| Aspiring Architect | AI-strong | Coach-and-capture | Individual-led; no organizational decisions |
| BIISS specialist (any of five) | AI-strong | Draft-and-review | Practitioner owns outputs |
| Mentor | AI-backstage | Assemble-and-present | Mentor fully owns evaluation; AI never judges work products |
| Mentee | AI-strong | Coach-and-capture | Relationship with mentor remains primary |
| Community of Practice lead | AI-strong | Draft-and-review | Lead decides direction and cadence |
| Engagement Model Steering Committee member | AI-proposer | Assemble-and-present | Committee decides |
| Line manager | AI-backstage | Assemble-and-present | Manager owns every people decision |
| Extended Team member | AI-strong | Coach-and-capture | Individual chooses engagement |
| External architect (vendor or SI) | AI-strong | Draft-and-review | Engagement manager owns the relationship |
| HR representative | AI-backstage | Assemble-and-present | HR owns every decision |
| Hiring manager | AI-backstage | Gate-and-block | Manager decides; AI never ranks candidates |
| Culture assessment facilitator | AI-strong | Shadow-and-record | Facilitator interprets; team leaders act |
| Rotation coordinator | AI-proposer | Propose-and-confirm | Coordinator proposes; manager approves |
| Mentoring matchmaker (practice) | AI-proposer | Propose-and-confirm | Humans confirm every pairing |

Stop-lines. AI never rates performance, judges mentor work products, ranks hiring candidates, or recommends compensation actions.

### 8.5 Competency Model Roles

| Role | Band | Primary pattern | HITL safeguard |
|---|---|---|---|
| Self-assessor (the practitioner) | AI-strong | Coach-and-capture | Practitioner sets every rating; data in `CompetencyStore` |
| Peer assessor | AI-strong | Coach-and-capture | Peer sets ratings; results not auto-shared |
| Mentor-assessor | AI-backstage | Assemble-and-present | Mentor performs the assessment; AI surfaces evidence |
| Certification authority (CITA board) | AI-excluded | — | Out of platform scope |
| Certification path planner (self) | AI-strong | Draft-and-review | Practitioner adopts the plan |
| Hiring manager (using competency data) | AI-backstage | Gate-and-block | Manager decides; PrivacyGate authorizes reads |
| HR representative | AI-backstage | Assemble-and-present | HR systems own decisions |
| Learning and Development manager | AI-strong | Assemble-and-present | L&D designs and delivers |
| Team capability reviewer | AI-strong | Assemble-and-present | Small-team suppression; no identifying detail leaks |
| 360-degree assessment orchestrator | AI-proposer | Assemble-and-present | Practitioner owns participation; mentor owns evaluation |
| Competency Model Steering Committee member | AI-proposer | Assemble-and-present | Committee decides |
| CITA maintenance tracker | AI-strong | Shadow-and-record | Practitioner verifies logged hours |

Stop-lines. AI never rates work products, links competency data to compensation, or grants certifications.

### 8.6 Platform-Wide Constraints

Three BTABoK principles constrain AI authority more strictly than technical capability would:

- "Architects should be governed, not doing the governing." Any AI feature that looks like governance enforcement from the architect's perspective is misaligned, even when technically feasible.
- "Community eats framework for lunch." Mentoring and community relationships are the practice's load-bearing tissue. Patterns that substitute for these erode the practice over time.
- The 360-degree assessment distributes judgment across self, peer, mentor, and certification. AI collapsing any of these into automation violates the model's own safeguard.

Conversely, BTABoK invites AI hardest in three areas:
- Mechanical cadence work (RVM checks, rotation tracking, freshness sweeps, maintenance-hour logging).
- Artifact drafting (NABC business cases, ADRs, canvases, role specifications).
- Cross-reference retrieval across the BTABoK corpus (canvas to competency to pillar to specialization).

### 8.7 Mapping to Delivery Waves

Each subagent in the delivery plan carries its band and primary pattern. Waves 5 and 6 reference this section for every shipped subagent. New subagents added in future waves inherit the classification discipline established here.

## 9. Delivery Plan

Six waves. Each is a coherent increment that could stand on its own.

**Product fork.** Waves 1 through 4 are **SpecChat** deliverables (profile, enforcement, governance mechanics, rendering). Waves 5 and 6 are **ASAP** deliverables and ship from the new repository. The dependency arrow points from ASAP to SpecChat: ASAP consumes SpecChat through the MCP server surface. SpecChat ships independently on its own cadence without waiting for ASAP.

### 9.1 Wave 1. Enforce and Inform (Engagement)

Prerequisites: [MCP-Server-Integration-Design.md](../../spec-chat/WIP/MCP-Server-Integration-Design.md) Phases 1 through 4 complete.

Deliverables:
- `ProfileContext`, `ModelContext`, `CollectionIndex`, `DiagnosticsBus`, `RetentionSink`.
- Engagement hooks: `SessionStart`, `UserPromptSubmit`, `PostToolUse` on `specs/**`, `Stop`.
- MCP tools: `resolve_weakref`, `check_freshness_sla`, `simulate_severity_policy`.

Exit criterion: a spec change that violates profile rules is blocked locally and an audit record exists.

### 9.2 Wave 2. PR flow and governance mechanics (Engagement)

Deliverables:
- Remote trigger on `specs/**` PRs.
- Governance reviewer subagent (mentor tone).
- Decision scribe subagent with Decision Bias Calibrator step.
- Slash commands: `/spec-review`, `/spec-waiver`, `/spec-earb-prep`.
- MCP tools: `assemble_earb_packet`, `expand_waiver_chain`.

Exit criterion: a PR touching specs produces a review digest; the EARB chair can retrieve the week's packet; the bias calibrator is invoked on every decision.

### 9.3 Wave 3. Calendar and operation (Engagement, begin Value)

Deliverables:
- Engagement scheduled tasks: freshness sweep, waiver expiry, EARB agenda, archived-spec rot, ADLC stage checkpoints.
- Drift detector subagent.
- ADLC stage coach subagent.
- MCP tools: `detect_drift`, `export_audit_trail`.
- Value-aligned scorecard refresh against existing `MetricDefinition` and `ScorecardDefinition`.
- MCP tools: `refresh_scorecard`, `run_rvm_check`.
- Monthly RVM early validation scheduled task (this is the first operational Value cadence).

Exit criterion: scheduled freshness, waiver, scorecard, and RVM early-indicator tasks run without human invocation; ADLC stage guidance available on demand.

### 9.4 Wave 4. Rendering and communication (Engagement). **SpecChat GA exit.**

Deliverables:
- CaDL canvas renderer for all 20 in-profile canvases ([MCP-Server-Integration-Design.md](../../spec-chat/WIP/MCP-Server-Integration-Design.md) Phase 5).
- C4 diagram generator, roadmap visualizer, ADLC progress view, dependency graph.
- Slash commands: `/spec-canvas`, `/spec-new`, `/spec-adlc`.
- Preview integration.

Exit criterion: a stakeholder who cannot read CoDL reads the rendered view and obtains the same information.

### 9.5 Wave 5. Knowledge and Value Model. **ASAP Wave 1.**

Deliverables:
- RAG indexes: Engagement, Value, Canvas (with competency cross-references), Topics, Prior-art.
- Skills: `spec-btabok`, `spec-canvas-library`, `spec-onboarding`, `spec-adlc`, `spec-jtbd`, `spec-value`, `spec-benefits-realization`, `spec-value-stream`, `spec-investment`, `spec-rvm`, `spec-principles`.
- Subagents: stakeholder concern miner (with JTBD and empathy structures), migration pilot, roadmap planner, benefits-realization modeler, value-stream mapper, tech-debt portfolio analyst, investment prioritizer, business case drafter, RVM coach.
- Value scheduled tasks: quarterly leading indicators, annual lagging indicators, quarterly tech-debt, annual investment, annual OKR, annual principles review.
- Value MCP tools: `compute_benefits_dependency`, `score_tech_debt_portfolio`, `evaluate_investment_tradeoff`.
- Value preview: benefits dependency network, value-stream map, scorecard dashboard, tech-debt quadrant, RVM timeline.
- Slash commands: `/spec-migrate`, `/spec-value-draft`, `/spec-scorecard`, `/spec-techdebt`, `/spec-nabc`, `/spec-rvm`.
- Sibling-folder convention (`value-model/`) and `weakRef` pattern.
- Topic-area skills: `spec-topic-ai`, `spec-topic-cloud`, `spec-topic-security`, `spec-topic-sustainability`, `spec-topic-devops`, `spec-topic-integration`, `spec-topic-agile`.

Exit criterion: an architect can invoke Value Model guidance, receive IASA-grounded advice, produce sidecar artifacts, and track RVM indicators on a monthly, quarterly, and annual cadence.

### 9.6 Wave 6. People and Competency Models. **ASAP Wave 2.**

Deliverables:
- `IdentityResolver`, `PrivacyGate`, `CompetencyStore`.
- RAG indexes: People, Competency.
- People skills: `spec-people`, `spec-team-topologies`, `spec-role-definition`, `spec-career-path`, `spec-mentoring`, `spec-extended-team`.
- Competency skills: `spec-competency`, `spec-cita-prep`, `spec-learning-plan`.
- People subagents: team topology analyst, role coverage mapper, community health observer, mentoring matchmaker, culture diagnostic runner.
- Competency subagents: competency self-assessment coach, certification path planner, team capability-gap analyzer, Architect Skills Gap Analysis runner, peer-assessment orchestrator.
- Directory and HRIS integration webhooks.
- People and Competency scheduled tasks.
- People and Competency preview views.
- People and Competency MCP tools.
- Slash commands: `/spec-team-topology`, `/spec-role-coverage`, `/spec-mentor-match`, `/spec-culture-diagnostic`, `/spec-competency-assess`, `/spec-cita-plan`, `/spec-team-capability`, `/spec-skills-gap`.

Exit criterion: a practitioner can self-assess competency, plan a CITA path, run Architect Skills Gap Analysis, analyze team topology, and track role coverage across the BIISS specializations. All privacy gates active. No People or Competency data leaks into spec collections.

## 10. Out of Platform Scope

Explicitly not delivered:
- Automated governance decisions (waiver approval, decision closure, ASR sign-off, certification award).
- Profile extension to Value, People, or Competency models in SpecLang.
- Cross-profile collections (deferred to v0.2 plus).
- Spec language changes.
- Runtime code generation or direct system modification.
- HR decisions (compensation, promotion, performance rating, hiring, firing).
- Certification granting. The platform supports preparation and path planning only.
- Mentor assignment. The matchmaker proposes; humans assign.
- Principle enforcement as hard rules. Principles remain guidance.

## 11. Evaluation

Engagement:
1. EARB packet preparation moves from hours to minutes.
2. Freshness SLA compliance rises above 90 percent without human reminders.
3. Waiver expiries are never missed.
4. PR review latency on spec PRs drops.
5. Decision Bias Calibrator invocation rate approaches 100 percent on logged decisions.
6. Time from first stakeholder interview to reviewable StakeholderCard plus candidate ASRs drops by a measurable multiple.

Value:
7. NABC business cases for PMO cycles are drafted faster with platform support.
8. RVM early validation indicators exist for a majority of active initiatives.
9. Technical Debt Ratio is tracked continuously rather than on ad-hoc review.
10. Scorecard misses are surfaced proactively against `MetricDefinition` targets.

People:
11. Role coverage gaps for a new collection are identified before kickoff.
12. Architect rotation status is visible and prompts action on over-tenure.
13. Governance-body rotations happen without manual tracking.
14. Mentoring coverage is visible per practitioner, and gaps are surfaced.

Competency:
15. Practitioners complete self-assessments more frequently than under manual processes.
16. CITA progression is tracked per practitioner with planning output.
17. Team capability data is never leaked in identifying form.
18. Peer and mentor assessment cycles are orchestrated without losing artifacts.

Each criterion has an owning metric and a baseline established in Wave 1.

## 12. Open Questions

- Agent trail retention format. A dedicated schema, or reuse of the existing SpecItem retention model?
- `ModelContext` storage. Session-scoped, workspace-scoped, or derived from slash command invocation?
- Subagent approval boundary. Which advisory output can be accepted with a single reviewer, and which requires governance-body review?
- RAG source freshness. What is the right re-index interval per model index?
- PrivacyGate implementation. What authorization mechanism, and what audit surface?
- `CompetencyStore` location. Practitioner-local, platform-hosted, or external HRIS?
- People and Competency data retention defaults.
- Hook scope negotiation. User, workspace, plugin level?
- Slash command discoverability across a growing list.
- Topic-area skill interaction with model skills. Layered or exclusive?
- Decision Bias Calibrator implementation. A checklist subagent, or an MCP tool, or a hook?
- CITA proficiency-level asymmetry (5 proficiency levels, 4 CITA certifications). How does the UI express this cleanly?

## 13. Source References

**[R1]** SpecLang Design. [SpecLang-Design.md](../../spec-chat/WIP/SpecLang-Design.md). Profile architecture and the one-profile-at-a-time decision.

**[R2]** Spec Type System. [Spec-Type-System.md](../../spec-chat/WIP/Spec-Type-System.md). Three-layer stratification.

**[R3]** SpecChat BTABOK Implementation Plan. [SpecChat-BTABOK-Implementation-Plan.md](../../spec-chat/WIP/SpecChat-BTABOK-Implementation-Plan.md). Phases and deliverables for the profile itself.

**[R4]** MCP Server Integration Design. [MCP-Server-Integration-Design.md](../../spec-chat/WIP/MCP-Server-Integration-Design.md). Existing MCP tools and planned additions.

**[R5]** BTABOK Out of Scope Models. [BTABOK-Out-of-Scope-Models.md](../../spec-chat/WIP/BTABOK-Out-of-Scope-Models.md). The profile boundary this platform must respect while delivering platform-layer support for the four working models the platform covers.

**[R6]** SpecChat Design Decisions Record. [SpecChat-Design-Decisions-Record.md](../../spec-chat/WIP/SpecChat-Design-Decisions-Record.md). Settled decisions including SD-ONEPROF.

**[R7]** SpecChat BTABOK Acronym and Term Glossary. [SpecChat-BTABOK-Acronym-and-Term-Glossary.md](../../spec-chat/WIP/SpecChat-BTABOK-Acronym-and-Term-Glossary.md). Canonical for SpecChat terminology.

**[R7a]** ASAP Acronym and Term Glossary. [ASAP-Acronym-and-Term-Glossary.md](ASAP-Acronym-and-Term-Glossary.md). Canonical for ASAP terminology.

**[R8]** IASA Global. Business Technology Architecture Body of Knowledge (BTABoK). `https://iasa-global.github.io/btabok/`. Authoritative source for all BTABoK working models. The platform covers Engagement, Value, People, and Competency; the remaining working models (Outcome, Operating, Maturity) are out of platform scope.

**[R9]** IASA Global. Engagement Model. Pages including `engagement.md`, `architecture_practice.md`, `architecture_lifecycle.md`, `decisions.md`, `governance_em.md`, `principles.md`, `stakeholders.md`, `roadmap.md`.

**[R10]** IASA Global. Value Model content. Pages including `objectives.md`, `investment_planning.md`, `technical_debt.md`, `benefits_realization.md`, `value_streams.md`, `value_methods.md`, `risk_methods.md`.

**[R11]** IASA Global. People Model content. Pages including `organization.md`, `roles.md`, `career.md`, `extended_team.md`, `community.md`, `competency.md`, `culture.md`, `mentoring.md`.

**[R12]** IASA Global. Competency Model. `https://iasa-global.github.io/btabok/competency_model_m.html`. Five pillars and five BIISS specializations (per Manifesto and `competency.md`), 80-plus areas across both, five proficiency levels, four CITA certifications, six-level managed career path (Aspiring through Chief).

**[R13]** IASA Global. Structured Canvases. `https://iasa-global.github.io/btabok/structured_canvases_m.html`. The 75-plus canvas library with competency cross-references.

**[R14]** IASA Global. Topic Areas. Pages in `topics/` including `agile.md`, `ai_ml.md`, `cloud.md`, `dev_ops.md`, `integration.md`, `security.md`, `systems.md`, plus `sustainability/`. Brief contextual guides by BTABoK's own framing.
