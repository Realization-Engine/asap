---
title: "Citations for *The Architect and the Agent*"
subtitle: "Supporting citations for the whitepaper, updated alongside its versions."
author: "Dennis A. Landi"
version: "0.01"
date: "2026-04-22"
category: "Citations"
folio: "№ IV · a"
project: "ASAP"
source: "https://github.com/Realization-Engine/asap"
---

## Editorial Note

This citations document supports *The Architect and the Agent* (folio Nº IV, three parts). It is organized to surface the primary sources the paper's accuracy depends on, rather than to survey adjacent literature exhaustively.

The three categories that carry most of the paper's weight:

1. **The Realization Engine series**, the parent framework (M&M, folio Nº II) and the first companion memorandum (Enquiry, folio Nº III). A&A depends on both; every equation cited in the paper is cited by its M&M number.
2. **The IASA Business Technology Architecture Body of Knowledge (BTABoK) primary sources**, including the Manifesto and the specific engagement-model, competency-model, and career-path pages A&A instantiates the framework against. The paper's accuracy audit in development traced each architectural claim to a specific file path in the BTABoK repository; those file paths are listed here.
3. **The engineering artifacts that operationalize the paper's derivation**: the ASAP platform design document, SpecChat (as upstream dependency), and the Global Corp exemplar (as bench and substance-preserved corpus).

The remaining categories (formal methods, mentoring and apprenticeship transmission, automation and deskilling, commons governance) provide targeted support for specific claims in the paper's argument. Many of the adjacent literature threads the parent framework draws on (Cobb-Douglas production, labor-market polarization, Matthew effect, stochastic-parrots / mirror, jagged-frontier studies) are inherited through M&M and are catalogued in the M&M citations companion. They are not repeated here unless A&A makes a specific load-bearing use of them distinct from M&M's use.

---

## 1. The Realization Engine series

**[1.1]** Landi, D. A. *The Multiplier, Mirror and The Tipping Point.* Folio Nº II. F-Star project, 2026. `https://github.com/Realization-Engine/fstar`.
**Digest:** The parent framework. Establishes the general model of human capability under LLM amplification: output as multiplier times composite FORCE, the Mirror as a structured object with substance and presentation channels, the layered structure of FORCE, the atrophy equation, the tipping point and its hysteresis, the cohort discontinuity, the F→M transfer, the coupled phase portrait, the seven-loop cascade, the decision bottleneck, the erosion of competitive moats, the sovereignty question, the four futures. A&A cites M&M equations by number throughout; every equation reference (Eq. 1, 2, 3, 4, 4a, 6, 7, 7a, 9, 10, 11, 11a-c, 12, 12a, 12b, 13, 14, 14a, 15a/b, 16, 16a, 17, 18, 19, 20, 21, 22, 23, 24, 24a, 25, 26, 26a, 27, 28, 29, 30, 31, 32, 34, 36) is sourced from this document.

**[1.2]** Landi, D. A. *Enquiry Into Specification as Meaningful Struggle.* Folio Nº III. Spec Chat project, 2026. `https://github.com/Realization-Engine/spec-chat`.
**Digest:** The first companion memorandum. Narrows inside the Engagement Model of the body of knowledge to the specification medium, names SpecChat as the authored-commitment artifact the medium requires, identifies the developmental, medium, and practice questions, warns against cosmetic relocation, and introduces the practice-architecture boundary A&A zooms out from. A&A takes Enquiry's "realization engine" framing as given and extends the reach of the framework to Value, People, and Competency work.

**[1.3]** Landi, D. A. *The Multiplier and the Mirror, Citations.* Folio Nº II · a. F-Star project, 2026.
**Digest:** The adjacent-literature catalogue for the parent framework. A&A inherits these citations for the framework-general claims (Cobb-Douglas production, labor-market polarization, Matthew effect, stochastic-parrots / mirror, jagged-frontier studies, tacit-knowledge research, Ostrom commons). They are not duplicated here.

**[1.4]** Landi, D. A. *Notes for The Architect and the Agent.* Preparatory notes, 2026. `https://github.com/Realization-Engine/asap/blob/main/docs/notes/Notes-for-The-Architect-and-the-Agent.md`.
**Digest:** The analytical groundwork for this paper. Organizes the architecture-practice corollaries of the framework section by section, derives the theoretical foundation for ASAP's design, and traces every load-bearing M&M concept into its operational form for enterprise architecture under LLM amplification. Superseded as the primary argumentative artifact by this paper; retained as preparatory reference.

---

## 2. IASA BTABoK primary sources

The body of knowledge A&A instantiates the framework against. Citations give the repository file path where the paper's primary-source claims can be verified.

**[2.1]** IASA Global. *Business Technology Architecture Body of Knowledge (BTABoK).* `https://iasa-global.github.io/btabok/`.
**Digest:** The authoritative source for all BTABoK claims in the paper. Repository mirror referenced during development: `E:/Archive/GitHub/dlandi/btabok`.

**[2.2]** IASA Global. *BTABoK Manifesto.* `pages/manifesto/manifesto.md`.
**Digest:** Names the five competency pillars every architect shares (Business Technology Strategy, Human Dynamics, Design, Quality Attributes, IT Environment) and the five specializations BIISS (Business, Information, Infrastructure, Software, Solution) layered atop them. A&A cites the Manifesto as the primary authority on the pillar/specialization distinction.

**[2.3]** IASA Global. *Get Started with the BTABoK.* `pages/top_menu/get_started_m.md`. By Paul Preiss.
**Digest:** Enumerates the BTABoK's working models: Outcome, Operating, Value, People, Engagement, Competency, Maturity, surrounded by the Architecture Practice article, the Structured Canvas Approach, and the Topic Areas. A&A cites this page as the primary source for the reach-note that the platform's four-working-model coverage is a selection from a larger set.

**[2.4]** IASA Global. *Architecture Practice.* `pages/engagement_model/architecture_practice.md`.
**Digest:** Establishes the practice model for BT architecture, grounded in professional-body framing parallel to medicine, law, and accounting. Primary source for the practice-architecture concept the paper builds on.

**[2.5]** IASA Global. *Architecture Lifecycle.* `pages/engagement_model/architecture_lifecycle.md`.
**Digest:** Primary source for the Architecture Development Life Cycle (ADLC) and its six stages: Innovation Cycle, Strategy, Planning, Transformation, Utilize and Measure, Decommissioning. A&A uses the primary-source stage names throughout.

**[2.6]** IASA Global. *Governance (Engagement Model).* `pages/engagement_model/governance_em.md`.
**Digest:** Primary source for the governance-spectrum framing, the directive that architects should be governed rather than do the governing, and the "avoid the police state" caution. Load-bearing for the authority-gradient derivation.

**[2.7]** IASA Global. *Decisions.* `pages/engagement_model/decisions.md`.
**Digest:** Primary source for the architecturally significant decision (ASD) concept, framed as "the stuff that matters" per Martin Fowler. Supports the Decision Bottleneck argument and the decision scribe subagent derivation.

**[2.8]** IASA Global. *Principles.* `pages/engagement_model/principles.md`.
**Digest:** Primary source for the eight-to-twelve memorable-principle rule and the properties of good principles (constructive, compelling, memorable, testable, decisive, useful).

**[2.9]** IASA Global. *Benefits Realization.* `pages/engagement_model/benefits_realization.md`.
**Digest:** Primary source for Rapid Value Management (RVM) and its three indicator tiers: early validation indicators (within the first 90 days, ideally 30), leading indicators (91 days to one year), lagging indicators (end-success). Also the biweekly Value Map update minimum and the monthly investment validation minimum. Load-bearing for the cadence section of Part One and for the RVM subagent derivation.

**[2.10]** IASA Global. *Investment Planning.* `pages/engagement_model/investment_planning.md`.
**Digest:** Primary source for the NABC (Needs, Approach, Benefits, Considerations) business case format and for the "attack the PMO" demand-shaping framing.

**[2.11]** IASA Global. *Technical Debt.* `pages/engagement_model/technical_debt.md`.
**Digest:** Primary source for the Technical Debt Ratio formula (Remediation plus Maintenance over Development, times 100) and for the typology of technical debt (code, structural, QA, value, legacy, organization). Note: tagged `operating_model` rather than `value_model` in the primary source; ASAP's operational placement of tech-debt under Value is a practice-architecture choice documented in Part Three.

**[2.12]** IASA Global. *Community.* `pages/engagement_model/community.md`.
**Digest:** Primary source for the "Community Eats Framework for Lunch" tenet and the "Specialization-Based Conflict Destroys Practices" warning. Tagged `people_model`.

**[2.13]** IASA Global. *Competency.* `pages/engagement_model/competency.md`.
**Digest:** Primary source for the five proficiency levels (Awareness, Basic, Delivery, Experienced, Shaping), the Bloom-hierarchy basis, the five pillars as the shared competency core, the BIISS specializations as lateral depth, and the 42 total competency count across pillars. A&A cites the level-label table (lines 46-52) as authoritative for proficiency-level labels.

**[2.14]** IASA Global. *Career.* `pages/engagement_model/career.md`.
**Digest:** Primary source for the six-level managed career path: Aspiring (Unmeasured), Foundational, Associate/Advanced, Professional, Distinguished, Chief. Establishes that the career path is distinct from the four-tier CITA certification ladder and that Aspiring is pre-certification while Chief is post-Distinguished, recognized through demonstrated practice. Load-bearing for the Part One §5 treatment of multi-form FORCE and the CITA-ladder asymmetry.

**[2.15]** IASA Global. *Organization.* `pages/engagement_model/organization.md`.
**Digest:** Primary source for the claim that rotation is "a critical component of architecture skill acquisition and shared value delivery" (line 186). Supports the Loop-3 and Loop-7 treatments of architect rotation.

**[2.16]** IASA Global. *Mentoring (BTABoK Overview).* `pages/btabok_overview/mentoring.md`.
**Digest:** Primary source for the three mentoring stages and their durations: Early Stage mentoring for Foundation and Associate architects at three-to-six-month engagements within two-to-three-year trajectories; Professional Mentoring for Professional and Distinguished at one-to-three-year relationships (or longer); Topic Area mentoring at one-to-three-month individual engagements. A&A cites the primary-source durations in Part One §2 and §6 and in Part Two Loop 3.

**[2.17]** IASA Global. *Adopting the Competency Model.* `pages/btabok_overview/adopting_the_competency_model.md`. By Paul Preiss.
**Digest:** Primary source for the five-levels-from-Bloom derivation, the four CITA certifications (Foundation, Associate, Professional, Distinguished), the four-method 360-degree measurement (self, peer, mentor, certification, per line 139), and the five operative rules of the IASA Mentoring Method (lines 155-166), most load-bearing of which is that architects cannot progress beyond critical milestones without reviewed outputs from one or more qualified mentors.

**[2.18]** IASA Global. *Culture.* `pages/engagement_model/culture.md`.
**Digest:** Primary source for the Westrum Culture Diagnostic and the Culture Map as canvases used in architecture practice. Supports the culture-diagnostic-runner subagent.

**[2.19]** IASA Global. *Engagement.* `pages/engagement_model/engagement.md`.
**Digest:** Primary source for two principles A&A cites: "the outcome of the work is more important than the method of achieving that outcome" (line 54) and "Stop Doing Architecture, Start Digitally Enhancing Your Customer" (principle heading, line 52).

**[2.20]** IASA Global. *Structured Canvases.* `pages/structured_canvases/structured_canvases_m.md`.
**Digest:** Primary source for the over-75 canvas count and the Structured Canvas Approach. Supports the canvas-library skill and the renderer in Preview/Rendering.

**[2.21]** IASA Global. *Topic Areas.* `pages/topics/`, including `cloud.md`, `ai_ml.md`, `security.md`, `integration.md`, `dev_ops.md`, `systems.md`, `agile.md`, `sustainability/`.
**Digest:** Primary source for the topic-areas-as-awareness-level framing: "starting points where topic areas provide context for IT architects to be aware of" (e.g., `topics/cloud.md` line 14). Supports the topic-area skills and the discipline that keeps them brief.

**[2.22]** IASA Global. *Competency Model Index.* `pages/competency_model/competency_model_m.html`.
**Digest:** The index page that navigates the 42 competencies across the five pillars plus the additional competencies per BIISS specialization. Note: the page's navigational grouping (listing pillar headers and specialization headers together in a flat list) is a common source of confusion between pillars and specializations; the Manifesto (`[2.2]`) is the authoritative taxonomy.

**[2.23]** IASA Global. *Design Decisions (Overview).* `pages/btabok_overview/design_decisions_3.md`.
**Digest:** Primary source for the Decision Bias Calibrator concept ("The BTABoK includes a set of decision bias calibrators to help unearth biases found", line 138). Supports the decision-scribe subagent's invocation of the calibrator.

---

## 3. The engineering artifacts

**[3.1]** Landi, D. A. *Architect Support Agentic Platform (ASAP) Design Document.* `https://github.com/Realization-Engine/asap/blob/main/WIP/Architect-Support-Agentic-Platform.md`.
**Digest:** The practice architecture A&A derives. Enumerates the ten primitives, the authority gradient, the AI-suitability bands and seven safeguard patterns, the asymmetric coverage across the four working models the platform covers, the ten platform components, the six-wave delivery plan with the product fork at end of Wave 4, the stop-lines, and the evaluation criteria. Where A&A states "the platform does X," the specific mechanism is described in this document.

**[3.2]** Landi, D. A. *SpecChat and SpecLang.* `https://github.com/Realization-Engine/spec-chat`.
**Digest:** The specification medium ASAP consumes as an upstream dependency. SpecLang is the specification language; SpecChat is the implementation including parser, validator, MCP server, canvas rendering, and the BTABOK profile. A&A refers to SpecChat throughout as the Engagement-Model inside view, and to ASAP as the zoomed-out view that surrounds it.

**[3.3]** Landi, D. A. *Global Corp. Enterprise Architecture Exemplar (narrative).* `https://github.com/Realization-Engine/asap/blob/main/docs/examples/global-corp/Global-Corp-Exemplar.md`.
**Digest:** The worked enterprise against which ASAP components are designed and tested, maintained as a long-form narrative document in the ASAP repository. A fictional global supply-chain company specified completely in BTABoK terms: strategic thesis, portfolio of capabilities and value streams, decision register, waiver process, view gallery, personas, ASRs, and governance bodies. Functions in A&A as fixed-point bench, substance-channel test bench, and, over the long arc, as part of the substance-preserved corpus.

**[3.3a]** Global Corp. SpecChat spec collection. `https://github.com/Realization-Engine/spec-chat/tree/main/docs/examples/global-corp/`.
**Digest:** The machine-processable companion to [3.3]. A full BTABOK-profile spec collection (architecture spec, application specs, gate specs, manifest) that SpecChat validators exercise end-to-end. The narrative at [3.3] is authoritative for prose; the spec files are authoritative for cross-references, counts, and IDs.

**[3.4]** Landi, D. A. *ASAP Acronym and Term Glossary.* `https://github.com/Realization-Engine/asap/blob/main/WIP/ASAP-Acronym-and-Term-Glossary.md`.
**Digest:** Working glossary for ASAP-internal terms, BTABoK-practice terms used in ASAP, and the agentic-platform primitive vocabulary. The glossary is a working reference; the Manifesto (`[2.2]`) and `competency.md` (`[2.13]`) remain authoritative for BTABoK taxonomy claims.

---

## 4. Formal specification and specification-driven realization

Supporting Future 4 (the return to specification) as the architectural form of the framework's fourth future. The Enquiry catalogues this tradition more fully; here only the sources A&A cites directly are listed.

**[4.1]** Hoare, C. A. R. "An Axiomatic Basis for Computer Programming." *Communications of the ACM*, 12(10), 1969, pp. 576-580, 583. DOI: 10.1145/363235.363259.
**Digest:** Foundational statement that programming is precise reasoning about behavior, not merely manual construction. Supports A&A's Future 4 framing of architect-as-author-of-commitments.

**[4.2]** Lamport, L. *Specifying Systems: The TLA+ Language and Tools for Hardware and Software Engineers.* Addison-Wesley, 2002.
**Digest:** Treating specification as the primary engineering artifact; tying high-level intent to machine-checkable behavior. The architectural analog is the authored-commitment boundary A&A preserves at the spec layer and surrounds with agentic practice.

**[4.3]** Dijkstra, E. W. *A Discipline of Programming.* Prentice-Hall, 1976.
**Digest:** Specification and reasoning as the discipline's substance. Cited as precedent for the transition A&A describes from implementation-derived FORCE to specification-derived FORCE, with the warning that Dijkstra's generation built specification FORCE on top of implementation FORCE, a sequencing whose post-LLM substitute is untested.

**[4.4]** Abrial, J.-R. *Modeling in Event-B: System and Software Engineering.* Cambridge University Press, 2010.
**Digest:** Refinement as an explicit relation with proof obligations. Supports A&A's treatment of ADLC stage transitions as refinement events with proof-of-progression obligations.

---

## 5. Architecture practice, mentoring, and apprenticeship transmission

Supporting Loop 3 (tacit-knowledge transmission collapse) and Loop 7 (cohort discontinuity) as architecture-specific dynamics, and the six-level career path as the profession's developmental trajectory.

**[5.1]** American Institute of Architects (AIA). *Making Mentoring Work.* 2019. Via Catalyst.org.
**Digest:** Cited by the IASA Mentoring Method (`[2.17]`) as the structural precedent for separating managers from mentors. Supports A&A's analysis of the mentoring channel as the profession's primary transmission mechanism for tacit FORCE.

**[5.2]** Preiss, P. *BTABoK Career Path and Managed Profession Framing.* In `[2.14]`.
**Digest:** The managed career path as the profession's alternative to role-based employment, grounded in research from Iasa's focus groups, 2000-plus surveys, 1000-plus interviews, 200-plus corporate assessments, and 4500-plus individual competency assessments. Load-bearing for A&A's claim that the CITA ladder's calibration depends on a development trajectory the LLM is absorbing.

---

## 6. Automation, deskilling, and out-of-the-loop fragility

Supporting the atrophy equation's architectural form and the platform's categorical exclusions on developmental work.

**[6.1]** Bainbridge, L. "Ironies of Automation." *Automatica*, 19(6), 1983, pp. 775-779.
**Digest:** The foundational statement that automation can create new vulnerabilities by removing the conditions under which operator skill forms. Direct theoretical support for the atrophy dynamic M&M formalizes in Eq. 11 and A&A instantiates for architecture.

**[6.2]** Endsley, M. R. "From Here to Autonomy: Lessons Learned from Human-Automation Research." *Human Factors*, 59(1), 2017, pp. 5-27.
**Digest:** Synthesizes decades of automation research on out-of-the-loop performance problems, loss of situation awareness, and the specific conditions under which automation degrades operator capability. Supports the audit-trail proposition as a structural response to out-of-the-loop fragility in architecture practice.

**[6.3]** Skitka, L. J., Mosier, K. L., & Burdick, M. "Does Automation Bias Decision-Making?" *International Journal of Human-Computer Studies*, 51(5), 1999, pp. 991-1006.
**Digest:** Classical evidence for automation bias: users accept incorrect automated recommendations even when contrary information is available. Supports the Mirror's failure dimensions (automation-bias risk specifically) as a structural property the AI-suitability bands must calibrate against.

---

## 7. Commons governance and the substance-preserved corpus

Supporting Part Two's sovereignty section and Part Three's Global Corp framing as demand-side commons intervention.

**[7.1]** Ostrom, E. *Governing the Commons: The Evolution of Institutions for Collective Action.* Cambridge University Press, 1990.
**Digest:** The canonical framework for institutional design around common-pool resources. A&A's demand-side FORCE-commons argument is an application of Ostrom's analysis to the architecture profession's training-signal substrate. The institutional-design question A&A leaves open ("what monitoring, norm, and incentive structures could preserve the architecture-practice FORCE commons across firms that compete on the surface but share the underlying training-signal substrate?") is in Ostrom's terms.

**[7.2]** Ostrom, E., Gardner, R., & Walker, J. *Rules, Games, and Common-Pool Resources.* University of Michigan Press, 1994.
**Digest:** Extends [7.1] with formal game-theoretic analysis. Cited here because A&A's supply-side / demand-side distinction in the FORCE-as-commons analysis maps cleanly onto the rule-classes Ostrom, Gardner, and Walker identify.

---

## 8. Professional models and the managed profession

Supporting A&A's treatment of architecture as a profession with structural defenses that LLM amplification challenges.

**[8.1]** Abbott, A. *The System of Professions: An Essay on the Division of Expert Labor.* University of Chicago Press, 1988.
**Digest:** Foundational sociology-of-professions analysis. Cited here because A&A's claim that architecture's institutional review channels (CITA boards, EARBs, mentor sign-off) are the profession's structural defenses against the legibility crisis is an application of Abbott's framework to LLM amplification specifically.

**[8.2]** Larson, M. S. *The Rise of Professionalism: A Sociological Analysis.* University of California Press, 1977.
**Digest:** Foundational analysis of how professions establish jurisdictional authority. Supports A&A's reading of BTABoK's managed-career-path commitment as the architecture profession's jurisdictional project.

---

## 9. Empirical-research framing

Supporting the research agenda in Part Three §21. The jagged-frontier and variance-amplification empirical sources are inherited from the M&M citations ([1.3] above, §4 of the M&M companion) and are not duplicated here.

**[9.1]** Dell'Acqua, F., McFowland, E., Mollick, E., et al. "Navigating the Jagged Technological Frontier." *Harvard Business School Working Paper No. 24-013*, 2023.
**Digest:** The single most important empirical source for the variable-multiplier and variance-amplification dynamics the research agenda proposes to test in the architecture domain. The jagged-frontier finding translates cleanly to architecture practice through the paper's working-model decomposition.

**[9.2]** Peng, S., Kalliamvakou, E., Cihon, P., & Demirer, M. "The Impact of AI on Developer Productivity: Evidence from GitHub Copilot." arXiv:2302.06590, 2023.
**Digest:** The RCT methodology this paper uses (and which M&M cites) is the prototype for the architecture-practice studies the research agenda proposes. Extending it to architectural tasks (decision authoring, governance review, principle-set revision) is an open empirical project the platform makes tractable.

---

## 10. Ancillary and background

**[10.1]** Iasa Global. *CITA Certification Program Information.* `https://iasaglobal.org/certification/`.
**Digest:** The four CITA levels (Foundation, Associate, Professional, Distinguished) and the board-review process. A&A cites CITA as the profession's certification structure and names it as the empirical instrument through which cohort-level predictions become testable.

**[10.2]** IASA Global. *SpecChat-BTABOK Implementation Plan.* `https://github.com/Realization-Engine/spec-chat/blob/main/docs/design-notes/btabok/SpecChat-BTABOK-Implementation-Plan.md`.
**Digest:** The staged implementation plan for the BTABoK profile in SpecChat. Load-bearing for A&A's six-wave delivery plan, which places SpecChat Waves 1-4 before the ASAP Wave 5-6 zoom-out.

**[10.3]** IASA Global. *Concept Definition Language (CoDL) and Canvas Definition Language (CaDL).* BTABoK 3.2 education portal, April 2026.
**Digest:** The CoDL/CaDL publications referenced in the Global Corp Exemplar as the canonical vocabulary for BTABoK concept instances and canvas definitions. A&A treats CoDL/CaDL as the upstream vocabulary ASAP consumes through SpecChat without further modification.

---

## Verification note

All BTABoK primary-source citations (§2) were verified against the repository mirror at `E:/Archive/GitHub/dlandi/btabok` during the paper's accuracy pass. Each file-path reference above can be checked directly in the mirror or at the corresponding URL on `iasa-global.github.io/btabok`. The Manifesto (`[2.2]`) is authoritative where the navigational grouping on the Competency Model index (`[2.22]`) or on specialization-area pages might suggest a different count of pillars or specializations.
