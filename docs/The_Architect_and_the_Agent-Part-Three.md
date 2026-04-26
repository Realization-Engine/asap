---
title: "The Architect and the Agent, Part Three: The Amplification Architecture"
subtitle: "A companion whitepaper to The Multiplier and the Mirror, on the architect's practice under LLM amplification and the amplification architecture the Multiplier-Mirror framework requires."
author: "Dennis A. Landi"
version: "0.01"
date: "2026-04-21"
category: "Whitepaper"
folio: "Nº IV, Part Three of Three"
project: "ASAP"
source: "https://github.com/Realization-Engine/asap"
prev-url: "The_Architect_and_the_Agent-Part-Two.html"
prev-title: "Part Two, Ramifications in Architecture Practice"
next-url: "The_Architect_and_the_Agent_Citations.html"
next-title: "Citations"
---

# Part Three - The Amplification Architecture

*Mirror* (Folio Nº I) names the cognitive feedback loop the program presupposes. Parts One and Two set up the question. Part Three answers it by deriving the amplification architecture the **Multiplier-Mirror framework** (Folio Nº II) requires for the enterprise architect, feature by feature, from the equations. The software that implements it is ASAP Studio. What follows is not a description of ASAP Studio's feature list; the feature list is in the platform design document that sits alongside this paper. What follows is the derivation: which equation licenses which feature, which stop-line follows from which loop, which delivery ordering follows from which constraint. A reader who finishes Part Three should be able to reconstruct most of the platform design from first principles.

The derivation is organized in eight sections. The authority gradient derives from the Variable Multiplier. The AI-suitability bands and safeguard patterns derive from the atrophy equation read across FORCE-forms. The asymmetric coverage across the four working models derives from the Variable Multiplier's shape across working surfaces. The ten primitives derive from the practitioner's calendrical working surface. The stop-lines derive from the tacit-knowledge, hysteresis, legibility, and meaning loops operating jointly. The six-wave delivery and the SpecChat dependency derive from the zoom-out this paper has been building throughout. Global Corp operates as bench, test, and substance-preserved corpus. The four futures for the architecture profession close the arc, and the research agenda states what ASAP Studio makes empirically testable.

---

## The authority gradient

ASAP Studio tiers authority into four levels: **Enforce** (the machine refuses an action that violates a deterministic rule; no override), **Gate** (machine-checked, human-authorized before the action proceeds), **Advise** (machine-proposed, human-decided), **Inform** (machine-executed within authored scope, human-informed afterward).

The four tiers are not an editorial choice. They derive from the framework's Variable Multiplier (Eq. 2 and Eq. 3), which says the substance multiplier is not a single number; it varies across domains and task types, reliably high where the work is formalizable, mechanical, and well-trained, unreliably low or negative where the work is novel, judgment-laden, and relational. A platform that applies uniform authority across this distribution is structurally mismatched. The right authority for a given point of machine contact is determined by where in the Variable Multiplier's distribution that contact sits.

*Enforce* is appropriate only where the substance multiplier is reliably high and the rule being enforced is a deterministic property of the formal medium. The cost of a false negative (a correct human action being refused) exceeds the cost of a false positive (an incorrect human action being permitted) only when the rule is mechanical and the Multiplier is high. Spec-medium validators that reject a commit violating topology rules or a missing required field meet this condition. The framework's Eq. 9 adds the negative-FORCE damage-limiter justification: a practitioner with a wrong mental model produces damage that scales with M times the magnitude of wrongness times the time before detection. Enforcement at the spec layer catches certain classes of architectural error at the keyboard rather than weeks later at a review board.

*Gate* is appropriate where the substance multiplier is moderate but the consequence of an incorrect action is irreversible or expensive to undo. The human signal is the safeguard. Gate-tier features require explicit acknowledgment before the action proceeds. Examples: waiver chain expansion before commit, governance-packet finalization before review-board distribution, decision-record close-out before archive.

*Advise* is appropriate where the substance multiplier is variable but composable; the work admits a plausible candidate but the judgment is the practitioner's. Advisory features produce candidates, recommendations, and critiques that the human may accept, modify, or reject. Examples: governance reviewer subagent on an architect-authored decision, benefits-realization modeler proposing dependency-network drafts, value-stream mapper offering stream representations.

*Inform* is appropriate where the substance multiplier is structurally low or negative (novel judgment, integration across unconnected concerns, relational work) and ASAP Studio should not propose. Inform features present facts without recommendation. Examples: canvas rendering, freshness-sweep reporting, scorecard projection.

The authority gradient also operates as a **legibility-restoration apparatus**. The framework's Eq. 18 says the institution loses the ability to distinguish substantive from polished-hollow output because the presentation channel renders both at comparable fluency. Per-feature authority-tier labeling restores the signal at the feature level. A practitioner's work carries a tier label; the institution can read which features were Enforce (the machine's), which were Gate (human-authorized), which were Advise (human-decided with AI input), which were Inform (human-acted on AI facts). The gradient denies the institution the option of consuming an artifact and inferring competence behind it.

Model coverage interacts with the gradient structurally. Enforce-tier features are available only for the Engagement Model because only the Engagement Model has a formal specification medium (SpecChat) with validators. Value, People, and Competency features operate at the Advise and Inform tiers only. This is not a current limitation awaiting future extension. It is a permanent consequence of the Variable Multiplier's shape, derived in the asymmetric-coverage section below.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 380" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="ag-t ag-d">
  <title id="ag-t">The authority gradient</title>
  <desc id="ag-d">Four horizontal stripes stacked vertically. Enforce at top, then Gate, Advise, Inform at bottom. Each stripe names the tier, describes the machine-human split, gives example features, and states where the tier applies. Enforce and Gate apply inside the Engagement Model only. Advise and Inform apply across all four working models. A left-side arrow marks press intensity from hard at top to soft at bottom. A footer states that the gradient is derived from the Variable Multiplier, not selected for editorial balance.</desc>
  <defs>
    <marker id="ag-arr-down" viewBox="0 0 10 10" refX="5" refY="9" markerWidth="7" markerHeight="7" orient="auto"><path d="M0,0 L5,10 L10,0 z" fill="#1a1a2e"/></marker>
  </defs>
  <line x1="40" y1="60" x2="40" y2="310" stroke="#1a1a2e" stroke-width="1" marker-end="url(#ag-arr-down)"/>
  <text x="30" y="55" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">hard</text>
  <text x="30" y="320" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">soft</text>
  <text x="20" y="185" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle" transform="rotate(-90 20 185)">press intensity</text>
  <rect x="60" y="60" width="820" height="55" fill="#d62828" fill-opacity="0.12" stroke="#d62828" stroke-width="1.5" rx="4"/>
  <text x="140" y="85" font-family="sans-serif" font-size="14" font-weight="700" fill="#d62828" text-anchor="middle">Enforce</text>
  <text x="140" y="102" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">Eq. 9</text>
  <text x="225" y="80" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="start">Machine refuses; no override.</text>
  <text x="225" y="96" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="start">SpecChat topology violation blocked at commit; missing required field rejected.</text>
  <text x="870" y="80" font-family="sans-serif" font-size="10" font-weight="700" fill="#d62828" text-anchor="end">Engagement Model only</text>
  <text x="870" y="96" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="end">formal medium with validators</text>
  <rect x="60" y="125" width="820" height="55" fill="#e67e22" fill-opacity="0.12" stroke="#e67e22" stroke-width="1.5" rx="4"/>
  <text x="140" y="150" font-family="sans-serif" font-size="14" font-weight="700" fill="#e67e22" text-anchor="middle">Gate</text>
  <text x="140" y="167" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">Eq. 7</text>
  <text x="225" y="145" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="start">Machine-checked; human-authorized before the action proceeds.</text>
  <text x="225" y="161" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="start">Waiver-chain expansion; governance-packet finalization; ADR close-out.</text>
  <text x="870" y="145" font-family="sans-serif" font-size="10" font-weight="700" fill="#e67e22" text-anchor="end">Engagement Model</text>
  <text x="870" y="161" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="end">irreversible or expensive to undo</text>
  <rect x="60" y="190" width="820" height="55" fill="#3a86ff" fill-opacity="0.12" stroke="#3a86ff" stroke-width="1.5" rx="4"/>
  <text x="140" y="215" font-family="sans-serif" font-size="14" font-weight="700" fill="#3a86ff" text-anchor="middle">Advise</text>
  <text x="140" y="232" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">Eq. 2, 3</text>
  <text x="225" y="210" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="start">Machine-proposed; human-decided.</text>
  <text x="225" y="226" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="start">Governance-reviewer subagent; benefits-realization modeler; value-stream mapper.</text>
  <text x="870" y="210" font-family="sans-serif" font-size="10" font-weight="700" fill="#3a86ff" text-anchor="end">All four working models</text>
  <text x="870" y="226" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="end">substance multiplier is variable</text>
  <rect x="60" y="255" width="820" height="55" fill="#27ae60" fill-opacity="0.12" stroke="#27ae60" stroke-width="1.5" rx="4"/>
  <text x="140" y="280" font-family="sans-serif" font-size="14" font-weight="700" fill="#27ae60" text-anchor="middle">Inform</text>
  <text x="140" y="297" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">Eq. 18</text>
  <text x="225" y="275" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="start">Machine-executed within scope; human-informed afterward.</text>
  <text x="225" y="291" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="start">Canvas rendering; freshness-sweep reporting; scorecard projection.</text>
  <text x="870" y="275" font-family="sans-serif" font-size="10" font-weight="700" fill="#27ae60" text-anchor="end">All four working models</text>
  <text x="870" y="291" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="end">facts without recommendation</text>
  <line x1="40" y1="335" x2="880" y2="335" stroke="#999" stroke-width="1"/>
  <text x="450" y="355" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">The gradient is derived from the Variable Multiplier (Eq. 2, Eq. 3), not selected for editorial balance.</text>
  <text x="450" y="370" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Per-feature tier labeling also restores signal at the feature level (Eq. 18).</text>
</svg>

---

## The AI-suitability bands and the seven safeguard patterns

The authority gradient classifies *how hard* the machine presses on a decision. A second dimension classifies *whether the machine is a suitable proposer at all*, independent of how hard it would press. The platform names four bands on this second dimension: **AI-strong** (machine drafts the bulk of the work, named human confirms), **AI-backstage** (machine prepares material for a human role without surfacing in the primary relationship), **AI-proposer** (machine generates candidates, human adjudicates each), **AI-excluded** (categorical refusal regardless of capability).

The bands derive from the atrophy equation (Eq. 11) read across FORCE-forms. The equation's passive-reliance term (βR) operates with different strengths depending on the FORCE-form the work touches. Some work has low atrophy risk because the FORCE it would atrophy is surface-layer and near-fully substitutable by the tool (mechanical cadence, retrieval over structured corpora, assembly of well-defined artifacts from typed inputs). Some work has maximum atrophy risk because it is precisely the work whose FORCE is middle-layer, judgment-laden, or relational, the layers where the LLM cannot produce substance and where the passive-reliance term is strongest (mentor judgment, performance rating, certification award, compensation-setting, hiring, firing, funding allocation). Each form of architectural work must be classified by the atrophy risk the LLM imposes on the FORCE-form it touches, and the band must be calibrated accordingly.

*AI-strong* features have the lowest atrophy risk. The AI carries most of the labor on work whose substance the tool can produce; a named human confirms the result. The decision scribe drafts a record; the architect signs. Draft-and-review is the characteristic pattern.

*AI-backstage* features preserve a load-bearing human relationship. The machine prepares material for a human role without surfacing in the primary relationship. The mentor packet is assembled offstage; the mentor enters the mentoring session with the packet in hand; the mentee sees the mentor, not the machine. Hiring-interview preparation follows the same pattern: the manager receives a candidate summary; the candidate faces the manager, not a scoring model. The framework's Loop 3 (tacit-knowledge transmission collapse) is the structural reason for this band: mentoring is the transmission channel, and the transmission cannot survive the machine in the room.

*AI-proposer* features generate candidates for a decision the human makes individually. The rotation coordinator proposes pairings; the manager approves each. The mentoring matchmaker proposes mentor-mentee pairs; mentor and mentee confirm. The feature produces candidates, not verdicts.

*AI-excluded* features are off-limits regardless of capability. Performance rating, mentor judgment on work products, certification grant, compensation allocation, hiring decisions, firing decisions, funding allocation. These are decisions the profession's own framing treats as constitutive of its discipline; they are also decisions where the atrophy risk per Eq. 11 is at its maximum. The platform produces no output that reads as a recommendation in any of these categories. The exclusion is encoded as a structural property of feature design, not as a runtime rule that could be overridden.

The seven safeguard patterns describe how AI and the practitioner share each piece of work once the band is fixed. *Draft-and-review*: AI drafts, named human owns the artifact. *Assemble-and-present*: AI gathers inputs, human interprets and acts. *Propose-and-confirm*: AI suggests an action, human confirms each one. *Monitor-and-alert*: AI watches signals, human decides response. *Coach-and-capture*: AI guides a practitioner-owned process, data stays with the practitioner. *Shadow-and-record*: AI observes, human acts, AI builds the audit trail. *Gate-and-block*: AI cannot proceed past a checkpoint without an explicit human signal.

Every feature ASAP Studio ships is classified by exactly one band and at least one pattern. The classification is a property of the feature's design. The bands calibrate atrophy defenses per FORCE-form; the patterns calibrate the interaction choreography; the authority gradient calibrates how hard the machine presses. These three classifications are orthogonal, and ASAP Studio's systemic property is that each feature declares all three.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 460" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="oc-t oc-d">
  <title id="oc-t">The three orthogonal classifications</title>
  <desc id="oc-d">Three parallel vertical axes. Authority Tier on the left with four positions (Enforce, Gate, Advise, Inform). AI-suitability Band in the middle with four positions (AI-strong, AI-backstage, AI-proposer, AI-excluded). Safeguard Pattern on the right with seven positions (Draft-and-review, Assemble-and-present, Propose-and-confirm, Monitor-and-alert, Coach-and-capture, Shadow-and-record, Gate-and-block). Six example ASAP Studio features are drawn as polylines that connect their position on each of the three axes. A note near the AI-excluded band records that ASAP Studio ships no feature at that band. A legend below identifies each polyline. A footer states that every feature declares all three classifications.</desc>
  <text x="180" y="32" font-family="sans-serif" font-size="13" font-weight="700" fill="#1a1a2e" text-anchor="middle">Authority Tier</text>
  <text x="450" y="32" font-family="sans-serif" font-size="13" font-weight="700" fill="#1a1a2e" text-anchor="middle">AI-suitability Band</text>
  <text x="720" y="32" font-family="sans-serif" font-size="13" font-weight="700" fill="#1a1a2e" text-anchor="middle">Safeguard Pattern</text>
  <line x1="180" y1="50" x2="180" y2="330" stroke="#1a1a2e" stroke-width="1.5"/>
  <circle cx="180" cy="80" r="3" fill="#1a1a2e"/>
  <text x="165" y="83" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">Enforce</text>
  <circle cx="180" cy="150" r="3" fill="#1a1a2e"/>
  <text x="165" y="153" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">Gate</text>
  <circle cx="180" cy="220" r="3" fill="#1a1a2e"/>
  <text x="165" y="223" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">Advise</text>
  <circle cx="180" cy="290" r="3" fill="#1a1a2e"/>
  <text x="165" y="293" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">Inform</text>
  <line x1="450" y1="50" x2="450" y2="330" stroke="#1a1a2e" stroke-width="1.5"/>
  <circle cx="450" cy="80" r="3" fill="#1a1a2e"/>
  <text x="455" y="83" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">AI-strong</text>
  <circle cx="450" cy="160" r="3" fill="#1a1a2e"/>
  <text x="455" y="163" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">AI-backstage</text>
  <circle cx="450" cy="230" r="3" fill="#1a1a2e"/>
  <text x="455" y="233" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">AI-proposer</text>
  <circle cx="450" cy="310" r="3" fill="#1a1a2e"/>
  <text x="455" y="313" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">AI-excluded</text>
  <line x1="720" y1="50" x2="720" y2="330" stroke="#1a1a2e" stroke-width="1.5"/>
  <circle cx="720" cy="65" r="3" fill="#1a1a2e"/>
  <text x="725" y="68" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">Draft-and-review</text>
  <circle cx="720" cy="105" r="3" fill="#1a1a2e"/>
  <text x="725" y="108" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">Assemble-and-present</text>
  <circle cx="720" cy="145" r="3" fill="#1a1a2e"/>
  <text x="725" y="148" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">Propose-and-confirm</text>
  <circle cx="720" cy="185" r="3" fill="#1a1a2e"/>
  <text x="725" y="188" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">Monitor-and-alert</text>
  <circle cx="720" cy="225" r="3" fill="#1a1a2e"/>
  <text x="725" y="228" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">Coach-and-capture</text>
  <circle cx="720" cy="265" r="3" fill="#1a1a2e"/>
  <text x="725" y="268" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">Shadow-and-record</text>
  <circle cx="720" cy="305" r="3" fill="#1a1a2e"/>
  <text x="725" y="308" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="start">Gate-and-block</text>
  <polyline points="180,220 450,80 720,65" fill="none" stroke="#3a86ff" stroke-width="1.6" opacity="0.85"/>
  <polyline points="180,220 450,230 720,65" fill="none" stroke="#27ae60" stroke-width="1.6" opacity="0.85" stroke-dasharray="5 2"/>
  <polyline points="180,220 450,160 720,105" fill="none" stroke="#8e44ad" stroke-width="1.6" opacity="0.85"/>
  <polyline points="180,220 450,230 720,145" fill="none" stroke="#e67e22" stroke-width="1.6" opacity="0.85" stroke-dasharray="2 2"/>
  <polyline points="180,80 450,80 720,305" fill="none" stroke="#d62828" stroke-width="1.6" opacity="0.85"/>
  <polyline points="180,290 450,80 720,185" fill="none" stroke="#d4a017" stroke-width="1.6" opacity="0.85"/>
  <line x1="450" y1="310" x2="720" y2="310" stroke="#555" stroke-width="1.2" stroke-dasharray="3 3" opacity="0.5"/>
  <text x="600" y="326" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">(no feature ships at the AI-excluded band)</text>
  <g transform="translate(60, 355)">
    <text x="0" y="0" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e">Examples:</text>
    <line x1="80" y1="-3" x2="110" y2="-3" stroke="#3a86ff" stroke-width="1.6"/>
    <text x="115" y="0" font-family="sans-serif" font-size="10" fill="#1a1a2e">Decision scribe</text>
    <line x1="220" y1="-3" x2="250" y2="-3" stroke="#27ae60" stroke-width="1.6" stroke-dasharray="5 2"/>
    <text x="255" y="0" font-family="sans-serif" font-size="10" fill="#1a1a2e">Governance-reviewer subagent</text>
    <line x1="460" y1="-3" x2="490" y2="-3" stroke="#8e44ad" stroke-width="1.6"/>
    <text x="495" y="0" font-family="sans-serif" font-size="10" fill="#1a1a2e">Mentor-packet assembler</text>
    <line x1="660" y1="-3" x2="690" y2="-3" stroke="#e67e22" stroke-width="1.6" stroke-dasharray="2 2"/>
    <text x="695" y="0" font-family="sans-serif" font-size="10" fill="#1a1a2e">Rotation coordinator</text>
  </g>
  <g transform="translate(60, 380)">
    <line x1="80" y1="-3" x2="110" y2="-3" stroke="#d62828" stroke-width="1.6"/>
    <text x="115" y="0" font-family="sans-serif" font-size="10" fill="#1a1a2e">SpecChat topology validator (hook)</text>
    <line x1="340" y1="-3" x2="370" y2="-3" stroke="#d4a017" stroke-width="1.6"/>
    <text x="375" y="0" font-family="sans-serif" font-size="10" fill="#1a1a2e">Freshness-sweep scheduled task</text>
  </g>
  <line x1="40" y1="405" x2="880" y2="405" stroke="#999" stroke-width="1"/>
  <text x="450" y="425" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">Three orthogonal classifications. Every ASAP Studio feature declares all three.</text>
  <text x="450" y="443" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">The classification is a property of the feature's design, not a runtime rule.</text>
</svg>

---

## Asymmetric coverage across the four working models

The four working models ASAP Studio covers (Engagement, Value, People, Competency, selected from BTABoK's larger set for the reasons Part One named) are not equally enforce-eligible. The asymmetry is not editorial. It is derived from the Variable Multiplier's shape across working surfaces.

**Engagement Model** has a formal specification medium (SpecChat) and validators. Errors are computable: a topology rule is violated or it is not, a freshness SLA has lapsed or it has not, a waiver chain is complete or it is broken. The substance multiplier on these mechanical checks is reliably high. Enforcement is available across the whole Engagement surface, and ASAP Studio takes it. The full authority gradient applies: Enforce, Gate, Advise, and Inform features are all legitimate.

**Value Model** asks whether benefits proposed in a business case are being realized, whether a strategic investment is returning value, whether a portfolio's technical-debt ratio is healthy. The answer is judgment under uncertainty, not computation. The substance multiplier is variable and domain-sensitive. Enforcement is structurally mismatched. Advise and Inform tiers are the strongest appropriate postures.

**People Model** concerns relationships, mentoring, community health, reporting structures, role coverage, team topology. These are sites of human judgment the machine cannot mechanize without misshaping. The substance multiplier on the substantive work (mentor judgment, community-conflict resolution, role-design under organizational pressure) is low. Advise and Inform tiers only; several key work types fall under the AI-excluded band regardless of tier.

**Competency Model** tracks practitioner development across pillars, specializations, and proficiency levels, with self, peer, mentor, and certification distributing the judgment across four parties by design (per `adopting_the_competency_model.md`). AI authority over any of these would compress what is meant to be distributed. Advise and Inform tiers only; certification grant and mentor judgment on work products fall under AI-excluded.

The decision to permit enforcement only inside the Engagement Model is permanent. Widening enforcement into Value, People, or Competency would be a category error: the substance multiplier there is not reliably high, and enforcement would lock in mistakes at the rate the Multiplier is wrong. The asymmetry is the derivation. No product-convenience pressure, no customer request, no future model capability can change it without changing the underlying equation, which does not change because models improve.

Two corollaries complete the section. First, **the Creation/Evaluation inversion** is the structural reason the Engagement Model receives ASAP Studio's heaviest investment. Architecture's bottleneck has shifted from artifact authorship to governance; ASAP Studio's Engagement-Model features (decision scribe, governance reviewer, review-packet assembly, Decision Bias Calibrator, PR-flow integration, ADLC stage coach) are ASAP Studio organizing around the new bottleneck. Second, **the F→M transfer dynamic** shapes the Knowledge Layer (the RAG component). The framework's Eq. 26 says human expertise flows into models through training, RLHF, and evaluation data, with transfer efficiency decreasing as the FORCE-layer deepens. The Knowledge Layer is ASAP Studio's only deliberate, controlled, citable F→M transfer; every retrieval is attributed, every claim is traceable. ASAP Studio makes its own use of F→M transfer explicit, distinct from the tacit absorption happening by default elsewhere.

The four-model selection is also the minimum coverage the SMB-practice architect requires (Part Two, "The SMB-architect"). An enterprise-embedded architect inherits much of the People-Model and Competency-Model work passively through adjacent functions; a small architecture firm or solo contract architect must carry the full four-model surface personally. The selection widens under enterprise deployment; it does not narrow under SMB deployment.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 360" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="ac-t ac-d">
  <title id="ac-t">Asymmetric coverage across the four working models</title>
  <desc id="ac-d">A four by four grid. Rows are the four working models (Engagement, Value, People, Competency); columns are the four authority tiers (Enforce, Gate, Advise, Inform). Cells are colored to show which tier-model combination is available. Engagement Model is available at all four tiers. Value, People, and Competency are available only at Advise and Inform; Enforce and Gate cells in those rows are grayed as structurally mismatched. People and Competency carry an AI-excluded overlay on their Advise cell to show that specific work types are categorically refused. A footer states the asymmetry is permanent.</desc>
  <text x="220" y="55" font-family="sans-serif" font-size="12" font-weight="700" fill="#d62828" text-anchor="middle">Enforce</text>
  <text x="400" y="55" font-family="sans-serif" font-size="12" font-weight="700" fill="#e67e22" text-anchor="middle">Gate</text>
  <text x="580" y="55" font-family="sans-serif" font-size="12" font-weight="700" fill="#3a86ff" text-anchor="middle">Advise</text>
  <text x="760" y="55" font-family="sans-serif" font-size="12" font-weight="700" fill="#27ae60" text-anchor="middle">Inform</text>
  <text x="110" y="118" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="end">Engagement</text>
  <text x="110" y="178" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="end">Value</text>
  <text x="110" y="238" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="end">People</text>
  <text x="110" y="298" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="end">Competency</text>
  <rect x="130" y="80" width="180" height="60" fill="#d62828" fill-opacity="0.15" stroke="#d62828" stroke-width="1.2"/>
  <text x="220" y="114" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">hooks, validators,</text>
  <text x="220" y="127" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">topology rules</text>
  <rect x="310" y="80" width="180" height="60" fill="#e67e22" fill-opacity="0.15" stroke="#e67e22" stroke-width="1.2"/>
  <text x="400" y="114" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">waivers, packets,</text>
  <text x="400" y="127" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">ADR close-out</text>
  <rect x="490" y="80" width="180" height="60" fill="#3a86ff" fill-opacity="0.15" stroke="#3a86ff" stroke-width="1.2"/>
  <text x="580" y="114" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">decision scribe,</text>
  <text x="580" y="127" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">governance reviewer</text>
  <rect x="670" y="80" width="180" height="60" fill="#27ae60" fill-opacity="0.15" stroke="#27ae60" stroke-width="1.2"/>
  <text x="760" y="114" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">canvas rendering,</text>
  <text x="760" y="127" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">freshness reports</text>
  <rect x="130" y="140" width="180" height="60" fill="#f5f5f5" stroke="#ccc" stroke-width="1" stroke-dasharray="3 3"/>
  <text x="220" y="170" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">structurally</text>
  <text x="220" y="183" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">mismatched</text>
  <rect x="310" y="140" width="180" height="60" fill="#f5f5f5" stroke="#ccc" stroke-width="1" stroke-dasharray="3 3"/>
  <text x="400" y="170" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">structurally</text>
  <text x="400" y="183" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">mismatched</text>
  <rect x="490" y="140" width="180" height="60" fill="#3a86ff" fill-opacity="0.15" stroke="#3a86ff" stroke-width="1.2"/>
  <text x="580" y="170" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">RVM coach,</text>
  <text x="580" y="184" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">benefits-realization modeler</text>
  <rect x="670" y="140" width="180" height="60" fill="#27ae60" fill-opacity="0.15" stroke="#27ae60" stroke-width="1.2"/>
  <text x="760" y="170" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">scorecard projection,</text>
  <text x="760" y="184" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">tech-debt reports</text>
  <rect x="130" y="200" width="180" height="60" fill="#f5f5f5" stroke="#ccc" stroke-width="1" stroke-dasharray="3 3"/>
  <text x="220" y="230" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">structurally</text>
  <text x="220" y="243" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">mismatched</text>
  <rect x="310" y="200" width="180" height="60" fill="#f5f5f5" stroke="#ccc" stroke-width="1" stroke-dasharray="3 3"/>
  <text x="400" y="230" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">structurally</text>
  <text x="400" y="243" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">mismatched</text>
  <rect x="490" y="200" width="180" height="60" fill="#3a86ff" fill-opacity="0.15" stroke="#3a86ff" stroke-width="1.2"/>
  <text x="580" y="222" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">mentoring matchmaker,</text>
  <text x="580" y="236" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">team topology analyst</text>
  <text x="580" y="252" font-family="sans-serif" font-size="9" font-style="italic" fill="#d62828" text-anchor="middle">AI-excluded on mentor judgment</text>
  <rect x="670" y="200" width="180" height="60" fill="#27ae60" fill-opacity="0.15" stroke="#27ae60" stroke-width="1.2"/>
  <text x="760" y="222" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">role-coverage scans,</text>
  <text x="760" y="236" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">community-health observer</text>
  <rect x="130" y="260" width="180" height="60" fill="#f5f5f5" stroke="#ccc" stroke-width="1" stroke-dasharray="3 3"/>
  <text x="220" y="290" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">structurally</text>
  <text x="220" y="303" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">mismatched</text>
  <rect x="310" y="260" width="180" height="60" fill="#f5f5f5" stroke="#ccc" stroke-width="1" stroke-dasharray="3 3"/>
  <text x="400" y="290" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">structurally</text>
  <text x="400" y="303" font-family="sans-serif" font-size="10" font-style="italic" fill="#999" text-anchor="middle">mismatched</text>
  <rect x="490" y="260" width="180" height="60" fill="#3a86ff" fill-opacity="0.15" stroke="#3a86ff" stroke-width="1.2"/>
  <text x="580" y="282" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">self-assessment coach,</text>
  <text x="580" y="296" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">CITA path planner</text>
  <text x="580" y="312" font-family="sans-serif" font-size="9" font-style="italic" fill="#d62828" text-anchor="middle">AI-excluded on certification grant</text>
  <rect x="670" y="260" width="180" height="60" fill="#27ae60" fill-opacity="0.15" stroke="#27ae60" stroke-width="1.2"/>
  <text x="760" y="282" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">capability-gap scans,</text>
  <text x="760" y="296" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">certification-expiry alerts</text>
  <line x1="40" y1="335" x2="880" y2="335" stroke="#999" stroke-width="1"/>
  <text x="450" y="352" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">The asymmetry is permanent. Widening Enforce or Gate into Value, People, or Competency is a category error.</text>
</svg>

---

## The ten primitives

ASAP Studio names ten agentic primitives. They are not a feature menu. They are the minimum agentic vocabulary required to cover the cadence-shaped working surface Part One derived. Each primitive corresponds to a distinct type of work the working surface requires and is matched to one or more authority tiers, bands, and patterns.

**MCP tools (deterministic computation).** The factual backbone. Never summarized by a model. Each MCP tool is a computable function with a defined input and output. The authority tier is Inform when the tool returns a fact, Enforce when the tool is wired through a hook. Examples: collection validation, canvas projection, migration tooling, freshness-SLA check, waiver-chain expansion, Technical Debt Ratio scoring, role-coverage computation, competency-gap computation.

**Hooks (harness-enforced behaviors).** The only Enforce-tier primitive. Engagement Model only, because only Engagement has validators whose cost of false negatives beats the cost of false positives. Hooks run outside the model and cannot be argued with. Session start, prompt submit on a collection root, post-edit on `specs/**`, pre-compact, stop.

**Scheduled tasks.** The cadence backbone Part One named. Architecture is calendrical; scheduled tasks own the calendar across the four working models ASAP Studio covers. Engagement cadences (freshness sweeps, waiver-expiry scans, review-body agenda assembly, archived-spec rot checks, ADLC stage checkpoints). Value cadences (Rapid Value Management early checks monthly, leading-indicator reviews quarterly, lagging-indicator reviews annually, scorecard refreshes against declared metrics, tech-debt portfolio reviews, investment-prioritization prompts). People cadences (team topology reviews, succession and coverage scans, governance-body rotation alerts, architect-rotation tracking). Competency cadences (capability-coverage scans, CITA maintenance prompts, certification-expiry alerts, mentoring engagement checkpoints, learning-plan refreshes). These cadences are ASAP Studio's operational layer over the cadences BTABoK names directly; the primary-source RVM indicator horizons (30-90 days, 91 days to 1 year, end-state) and the IASA Mentoring Method's engagement durations (three-to-six-month for Foundation and Associate, one-to-three-year for Professional and Distinguished) set the time constants.

**Remote triggers and CI integration.** Spec change rarely happens in isolation. PR triggers on `specs/**` run the review subagent. Webhooks on incident creation associate with affected specs via the concept graph. Tag-on-release publishes the canvas bundle and audit trail export. Directory, HRIS, and PMO webhooks refresh the identity, competency, and initiative stores within their privacy constraints.

**Subagents.** The right primitive for multi-step work that benefits from its own system prompt and context. Engagement subagents (governance reviewer with mentor tone, decision scribe invoking the Decision Bias Calibrator, stakeholder concern miner using Jobs-to-be-Done and empathy-map structures, migration pilot, roadmap planner, ADLC stage coach). Value subagents (benefits-realization modeler, value-stream mapper, tech-debt portfolio analyst, investment prioritizer, business case drafter producing NABC format per `investment_planning.md`, RVM coach). People subagents (team topology analyst, role coverage mapper using BIISS specializations, community health observer, mentoring matchmaker, culture diagnostic runner using the Westrum Culture Diagnostic and Culture Map). Competency subagents (competency self-assessment coach, certification path planner, team capability-gap analyzer, Architect Skills Gap Analysis runner, peer-assessment orchestrator). Every subagent operates at the Advise tier; none has commit or merge authority on governance artifacts.

**Slash commands.** Human entry points. Every slash command is Gate-tier: the practitioner's invocation is the explicit authorization.

**Skills.** Advisory authoring aids. Advise tier only. The skills layer holds the BTABoK guidance per working model and topic area, surfaced at authoring time rather than carried as specification.

**Preview and rendering.** Visual output. Inform tier. The rendering layer projects the specification model into canvases, diagrams, roadmaps, dashboards, progress views, and traceability matrices. These are views over the specification; nothing the preview layer shows is stored separately.

**Knowledge retrieval (RAG).** The deliberate F→M transfer ASAP Studio endorses. Separate indexes per working model, all queryable from skills, subagents, and slash commands. Every retrieval is attributed. Every claim is traceable to its source. The RAG layer is ASAP Studio's only deliberate F→M transfer; every other transfer is the tacit absorption happening by default.

**Worktrees.** Isolated sandboxes for migration pilots and bulk refactor work. Scoped to the Validation stage of the practitioner lifecycle.

The ten primitives are minimal in the sense that removing any one leaves a class of work in the practitioner's calendrical surface unsupported. They are also complete in the sense that no additional primitive the practitioner's calendar requires has been identified through BTABoK's larger set or ASAP Studio's worked example. If future work finds such a gap, the primitive menu extends; if the gap is eliminated by a composition of existing primitives, the menu does not.

---

## Stop-lines

The stop-lines are the work ASAP Studio categorically refuses to touch, regardless of tier, band, or pattern. They are the operational form of the AI-excluded band, and they are load-bearing. Each stop-line is derived from the cascade loops Part Two worked out, operating jointly rather than singly.

**Performance rating.** Rating a named practitioner's performance is the institution's primary signal on whether the three-way resource competition (Eq. 28) is producing FORCE growth or FORCE displacement. If AI produces an output that reads as a rating, the institution substitutes presentation fluency for substance signal, and Eq. 18's legibility crisis closes over the only counter-signal the institution has.

**Mentor judgment on work products.** The IASA Mentoring Method requires reviewed outputs from qualified mentors for career-path progression (`adopting_the_competency_model.md`). The mentor's signature is the transmission signal between tacit and explicit (Loop 3). If AI produces mentor-style judgments, the transmission channel narrows even while appearing to widen, per the bus-factor illusion (Eq. 29).

**Certification grant.** CITA certification is recognition by a board of the practitioner's demonstrated competence. The board's judgment is itself middle-to-deep-layer FORCE. Eq. 27's ceiling on F→M transfer says the model cannot absorb the tacit judgment the board applies; Eq. 32 says the board itself degrades if its members lose access to the work-type the board is judging. AI authorship of certification grant collapses both.

**Compensation, hiring, firing.** These are role-constitutive decisions the practice's own framing treats as human-owned. They are also decisions where a wrong mental model produces damage that scales with M times wrongness times time (Eq. 9). Enforcement at these boundaries is not about capability; it is about keeping the damage-limiter coefficient human.

**Funding allocation.** Investment decisions shape the three-way resource competition itself. An AI-produced funding recommendation, even labeled advisory, shifts decision anchoring toward the recommendation, and the recommendation's provenance becomes opaque to the committee consuming it.

**Principle authorship without human ownership.** Principles are the practice's eight-to-twelve memorable guardrails (per `principles.md`). They are the institutional expression of the architect's judgment. An AI-authored principle carries no practitioner FORCE; a principle without FORCE does not guardrail.

**Waiver approval without human authorization; decision close-out without documented reasoning.** These are Gate-tier in the authority gradient; the stop-line repeats the Gate requirement at ASAP Studio's refusal boundary. A waiver auto-approved by AI is not a waiver, and a decision closed without reasoning is not a decision.

The stop-lines are structural properties of feature design, not runtime rules. An organization that wishes to bypass them would have to change ASAP Studio, not configure it. That difficulty is intentional. The framework's Eq. 14a says tipping-point descent is faster than recovery; a feature that could be toggled across a stop-line would be toggled under pressure, and the resulting descent would be asymmetric to undo.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 520" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="sl-t sl-d">
  <title id="sl-t">Stop-lines as structural perimeter</title>
  <desc id="sl-d">A two-column layout. The left column is ASAP Studio's scope: the authority tiers the platform permits, the four working models it covers, and the per-feature tier-band-pattern declaration. A dashed vertical refusal boundary separates scope from the right column, which lists seven stop-lines as red-bordered boxes: performance rating, mentor judgment on work products, certification grant, compensation and hiring and firing, funding allocation, principle authorship without human ownership, and waiver approval or decision close-out without authorization. Each stop-line carries the loop or equation reference from which its refusal is derived. A footer states that the stop-lines are structural, not configurable.</desc>
  <text x="225" y="35" font-family="sans-serif" font-size="14" font-weight="700" fill="#1a1a2e" text-anchor="middle">ASAP Studio's scope</text>
  <text x="665" y="35" font-family="sans-serif" font-size="14" font-weight="700" fill="#d62828" text-anchor="middle">Stop-lines (structural refusal)</text>
  <line x1="430" y1="50" x2="430" y2="460" stroke="#d62828" stroke-width="1.5" stroke-dasharray="6 4"/>
  <text x="430" y="475" font-family="sans-serif" font-size="10" font-style="italic" fill="#d62828" text-anchor="middle">structural refusal boundary</text>
  <rect x="40" y="55" width="370" height="400" fill="#3a86ff" fill-opacity="0.04" stroke="#3a86ff" stroke-width="1.2" rx="6"/>
  <text x="225" y="80" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e" text-anchor="middle">Authority &#215; Band &#215; Pattern design space</text>
  <line x1="70" y1="95" x2="380" y2="95" stroke="#ccc" stroke-width="1"/>
  <text x="60" y="120" font-family="sans-serif" font-size="11" font-weight="600" fill="#d62828">Enforce</text>
  <text x="150" y="120" font-family="sans-serif" font-size="10" fill="#1a1a2e">hooks, validators (Engagement)</text>
  <text x="60" y="155" font-family="sans-serif" font-size="11" font-weight="600" fill="#e67e22">Gate</text>
  <text x="150" y="155" font-family="sans-serif" font-size="10" fill="#1a1a2e">waivers, packets, close-out</text>
  <text x="60" y="190" font-family="sans-serif" font-size="11" font-weight="600" fill="#3a86ff">Advise</text>
  <text x="150" y="190" font-family="sans-serif" font-size="10" fill="#1a1a2e">subagents across all four models</text>
  <text x="60" y="225" font-family="sans-serif" font-size="11" font-weight="600" fill="#27ae60">Inform</text>
  <text x="150" y="225" font-family="sans-serif" font-size="10" fill="#1a1a2e">rendering, scans, reports</text>
  <line x1="70" y1="250" x2="380" y2="250" stroke="#ccc" stroke-width="1"/>
  <text x="225" y="275" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e" text-anchor="middle">Four working models covered</text>
  <text x="225" y="300" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">Engagement &#8226; Value &#8226; People &#8226; Competency</text>
  <line x1="70" y1="320" x2="380" y2="320" stroke="#ccc" stroke-width="1"/>
  <text x="225" y="345" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e" text-anchor="middle">Every feature declares</text>
  <text x="225" y="362" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">tier, band, and pattern</text>
  <text x="225" y="400" font-family="sans-serif" font-size="10" font-style="italic" fill="#3a86ff" text-anchor="middle">Substance-channel audit trail</text>
  <text x="225" y="415" font-family="sans-serif" font-size="10" font-style="italic" fill="#3a86ff" text-anchor="middle">across every point of use</text>
  <rect x="460" y="55" width="410" height="50" fill="#d62828" fill-opacity="0.08" stroke="#d62828" stroke-width="1.2" rx="4"/>
  <text x="475" y="78" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828">Performance rating</text>
  <text x="475" y="94" font-family="sans-serif" font-size="9" font-style="italic" fill="#555">Eq. 18: collapses the last counter-signal the institution has</text>
  <rect x="460" y="110" width="410" height="50" fill="#d62828" fill-opacity="0.08" stroke="#d62828" stroke-width="1.2" rx="4"/>
  <text x="475" y="133" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828">Mentor judgment on work products</text>
  <text x="475" y="149" font-family="sans-serif" font-size="9" font-style="italic" fill="#555">Loop 3, Eq. 29: mentor signature is the tacit transmission channel</text>
  <rect x="460" y="165" width="410" height="50" fill="#d62828" fill-opacity="0.08" stroke="#d62828" stroke-width="1.2" rx="4"/>
  <text x="475" y="188" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828">Certification grant</text>
  <text x="475" y="204" font-family="sans-serif" font-size="9" font-style="italic" fill="#555">Eqs. 27, 32: board's judgment is tacit; absorption collapses the ceiling</text>
  <rect x="460" y="220" width="410" height="50" fill="#d62828" fill-opacity="0.08" stroke="#d62828" stroke-width="1.2" rx="4"/>
  <text x="475" y="243" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828">Compensation, hiring, firing</text>
  <text x="475" y="259" font-family="sans-serif" font-size="9" font-style="italic" fill="#555">Eq. 9: damage-limiter coefficient must remain human</text>
  <rect x="460" y="275" width="410" height="50" fill="#d62828" fill-opacity="0.08" stroke="#d62828" stroke-width="1.2" rx="4"/>
  <text x="475" y="298" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828">Funding allocation</text>
  <text x="475" y="314" font-family="sans-serif" font-size="9" font-style="italic" fill="#555">Eq. 28: investment shapes the three-way resource competition itself</text>
  <rect x="460" y="330" width="410" height="50" fill="#d62828" fill-opacity="0.08" stroke="#d62828" stroke-width="1.2" rx="4"/>
  <text x="475" y="353" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828">Principle authorship without human ownership</text>
  <text x="475" y="369" font-family="sans-serif" font-size="9" font-style="italic" fill="#555">A principle without FORCE does not guardrail</text>
  <rect x="460" y="385" width="410" height="50" fill="#d62828" fill-opacity="0.08" stroke="#d62828" stroke-width="1.2" rx="4"/>
  <text x="475" y="408" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828">Waiver approval / decision close-out without authorization</text>
  <text x="475" y="424" font-family="sans-serif" font-size="9" font-style="italic" fill="#555">Gate-tier requirement repeated at the refusal boundary</text>
  <line x1="40" y1="490" x2="880" y2="490" stroke="#999" stroke-width="1"/>
  <text x="450" y="510" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">Structural, not configurable. An organization that wishes to bypass would have to change ASAP Studio, not configure it.</text>
</svg>

---

## The six-wave delivery and the SpecChat dependency

The delivery plan has six waves. Each is a coherent increment that could stand on its own, and the sequencing is itself a derivation from the framework.

**Wave 1. Enforce and Inform (Engagement).** The profile context, model context, collection index, diagnostics bus, and retention sink are the infrastructure the rest of ASAP Studio depends on. Engagement hooks (session start, prompt submit, post-edit on specs, stop) run at this wave because only Engagement has the validators that justify Enforce. MCP tools for weak-reference resolution, freshness-SLA check, and severity-policy simulation make the Engagement substrate queryable. Exit criterion: a spec change that violates profile rules is blocked locally and an audit record exists.

**Wave 2. PR flow and governance mechanics (Engagement).** Remote trigger on `specs/**` PRs, the governance reviewer subagent with mentor tone, the decision scribe with Decision Bias Calibrator invocation, the slash commands for review, waiver, and review-board preparation. MCP tools for review-packet assembly and waiver-chain expansion. Exit criterion: a spec-touching PR produces a review digest; the review-body chair retrieves the week's packet; the bias calibrator is invoked on every logged decision.

**Wave 3. Calendar and operation (Engagement, begin Value).** Engagement scheduled tasks (freshness sweep, waiver expiry, review-body agenda, archived-spec rot, ADLC stage checkpoints). The drift detector and ADLC stage coach. The first Value cadence enters here: the monthly RVM early-indicator check, along with scorecard refresh against the existing `MetricDefinition` and `ScorecardDefinition` metadata. Exit criterion: scheduled freshness, waiver, scorecard, and RVM early-indicator tasks run without human invocation; ADLC stage guidance available on demand.

**Wave 4. Rendering and communication (Engagement). SpecChat GA exit.** The canvas renderer across the in-profile canvases, the C4 diagram generator, the roadmap visualizer, the ADLC progress view, the dependency graph. Slash commands for canvas, new-spec, and ADLC. The preview integration. Exit criterion: a stakeholder who cannot read the spec language itself reads the rendered view and obtains the same information.

**Waves 1 through 4 are SpecChat deliverables.** They complete the Engagement-Model inside view. SpecChat ships GA at the end of Wave 4, at its own cadence, without depending on ASAP.

**Wave 5. Knowledge and Value Model. ASAP Wave 1.** This is the zoom-out. RAG indexes for Engagement, Value, Canvas (with competency cross-references), Topics, and Prior-art. The skills layer for `spec-btabok`, `spec-canvas-library`, `spec-onboarding`, `spec-adlc`, `spec-jtbd`, and the Value-aligned skills. Value subagents (stakeholder concern miner, migration pilot, roadmap planner, benefits-realization modeler, value-stream mapper, tech-debt portfolio analyst, investment prioritizer, business case drafter, RVM coach). Value scheduled tasks for quarterly leading indicators, annual lagging indicators, quarterly tech-debt, annual investment, annual OKR, annual principles review. Value MCP tools and preview views. The sibling-folder convention (`value-model/`) and weak-reference pattern that keeps Value artifacts out of the specification model. Topic-area skills. Exit criterion: an architect can invoke Value Model guidance, receive BTABoK-grounded advice, produce sidecar artifacts, and track RVM indicators on monthly, quarterly, and annual cadence.

**Wave 6. People and Competency Models. ASAP Wave 2.** The identity resolver, privacy gate, and competency store. RAG indexes for People and Competency. Skills, subagents, scheduled tasks, preview views, and MCP tools for each. HRIS integration webhook. All privacy gates active. No People or Competency data leaks into spec collections. Exit criterion: a practitioner can self-assess competency, plan a CITA path, run Architect Skills Gap Analysis, analyze team topology, and track role coverage across the BIISS specializations, with the audit trail intact across all four working models.

**Waves 5 and 6 are ASAP Studio deliverables.** They complete the zoom-out from Engagement to all four working models ASAP Studio covers.

The product fork at the end of Wave 4 is the structural reflection of the paper's zoom-out argument. SpecChat is the artifact of the Engagement-Model inside view. ASAP Studio is the artifact of the zoomed-out view. The dependency points one way: ASAP Studio consumes SpecChat through the MCP server surface; SpecChat does not depend on ASAP Studio. A team can adopt SpecChat for specification work without adopting ASAP Studio. A team adopting ASAP Studio finds SpecChat doing the load-bearing work in the spec layer underneath.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 440" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="wd-t wd-d">
  <title id="wd-t">The six-wave delivery and the SpecChat dependency</title>
  <desc id="wd-d">Six sequential wave boxes along a horizontal lane. Waves one through four belong to SpecChat and are color-coded blue; waves five and six belong to ASAP Studio and are color-coded purple. A SpecChat GA marker sits at wave four. Above the waves, two headers span the respective scopes. Below the waves, a dependency arrow curves from ASAP Studio back to SpecChat, labeled as a one-way dependency. A footer states that the product fork is the structural reflection of the paper's zoom-out.</desc>
  <defs>
    <marker id="wd-arr" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#1a1a2e"/></marker>
    <marker id="wd-arr-p" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#8e44ad"/></marker>
  </defs>
  <rect x="50" y="50" width="530" height="32" fill="#3a86ff" fill-opacity="0.15" stroke="#3a86ff" stroke-width="1.2" rx="4"/>
  <text x="315" y="72" font-family="sans-serif" font-size="13" font-weight="700" fill="#1a1a2e" text-anchor="middle">SpecChat scope (Waves 1 to 4)</text>
  <rect x="590" y="50" width="260" height="32" fill="#8e44ad" fill-opacity="0.15" stroke="#8e44ad" stroke-width="1.2" rx="4"/>
  <text x="720" y="72" font-family="sans-serif" font-size="13" font-weight="700" fill="#1a1a2e" text-anchor="middle">ASAP Studio scope (Waves 5 to 6)</text>
  <rect x="50" y="115" width="125" height="170" fill="#3a86ff" fill-opacity="0.08" stroke="#3a86ff" stroke-width="1.3" rx="5"/>
  <text x="112" y="137" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="middle">Wave 1</text>
  <line x1="60" y1="145" x2="165" y2="145" stroke="#ccc" stroke-width="1"/>
  <text x="112" y="162" font-family="sans-serif" font-size="10" font-weight="600" fill="#1a1a2e" text-anchor="middle">Enforce + Inform</text>
  <text x="112" y="175" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">(Engagement)</text>
  <text x="112" y="200" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">hooks, diagnostics,</text>
  <text x="112" y="212" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">retention sink,</text>
  <text x="112" y="224" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">profile context</text>
  <text x="112" y="255" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">exit: violation</text>
  <text x="112" y="267" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">blocked locally</text>
  <rect x="185" y="115" width="125" height="170" fill="#3a86ff" fill-opacity="0.08" stroke="#3a86ff" stroke-width="1.3" rx="5"/>
  <text x="247" y="137" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="middle">Wave 2</text>
  <line x1="195" y1="145" x2="300" y2="145" stroke="#ccc" stroke-width="1"/>
  <text x="247" y="162" font-family="sans-serif" font-size="10" font-weight="600" fill="#1a1a2e" text-anchor="middle">PR flow +</text>
  <text x="247" y="175" font-family="sans-serif" font-size="10" font-weight="600" fill="#1a1a2e" text-anchor="middle">governance mechanics</text>
  <text x="247" y="200" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">governance reviewer,</text>
  <text x="247" y="212" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">decision scribe,</text>
  <text x="247" y="224" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">Decision Bias Calibrator</text>
  <text x="247" y="255" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">exit: PR digest,</text>
  <text x="247" y="267" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">weekly packet</text>
  <rect x="320" y="115" width="125" height="170" fill="#3a86ff" fill-opacity="0.08" stroke="#3a86ff" stroke-width="1.3" rx="5"/>
  <text x="382" y="137" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="middle">Wave 3</text>
  <line x1="330" y1="145" x2="435" y2="145" stroke="#ccc" stroke-width="1"/>
  <text x="382" y="162" font-family="sans-serif" font-size="10" font-weight="600" fill="#1a1a2e" text-anchor="middle">Calendar + operation</text>
  <text x="382" y="175" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">(Eng, begin Value)</text>
  <text x="382" y="200" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">freshness sweep,</text>
  <text x="382" y="212" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">waiver expiry,</text>
  <text x="382" y="224" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">RVM monthly check</text>
  <text x="382" y="255" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">exit: scheduled tasks</text>
  <text x="382" y="267" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">run without invocation</text>
  <rect x="455" y="115" width="125" height="170" fill="#3a86ff" fill-opacity="0.12" stroke="#3a86ff" stroke-width="1.5" rx="5"/>
  <text x="517" y="137" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="middle">Wave 4</text>
  <line x1="465" y1="145" x2="570" y2="145" stroke="#ccc" stroke-width="1"/>
  <text x="517" y="162" font-family="sans-serif" font-size="10" font-weight="600" fill="#1a1a2e" text-anchor="middle">Rendering +</text>
  <text x="517" y="175" font-family="sans-serif" font-size="10" font-weight="600" fill="#1a1a2e" text-anchor="middle">communication</text>
  <text x="517" y="200" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">canvas renderer,</text>
  <text x="517" y="212" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">C4 generator,</text>
  <text x="517" y="224" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">roadmap, ADLC view</text>
  <text x="517" y="255" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">exit: rendered view</text>
  <text x="517" y="272" font-family="sans-serif" font-size="10" font-weight="700" fill="#d4a017" text-anchor="middle">&#9733; SpecChat GA</text>
  <rect x="590" y="115" width="125" height="170" fill="#8e44ad" fill-opacity="0.08" stroke="#8e44ad" stroke-width="1.3" rx="5"/>
  <text x="652" y="137" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="middle">Wave 5</text>
  <line x1="600" y1="145" x2="705" y2="145" stroke="#ccc" stroke-width="1"/>
  <text x="652" y="162" font-family="sans-serif" font-size="10" font-weight="600" fill="#1a1a2e" text-anchor="middle">Knowledge +</text>
  <text x="652" y="175" font-family="sans-serif" font-size="10" font-weight="600" fill="#1a1a2e" text-anchor="middle">Value Model</text>
  <text x="652" y="188" font-family="sans-serif" font-size="9" font-style="italic" fill="#8e44ad" text-anchor="middle">ASAP Wave 1</text>
  <text x="652" y="210" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">RAG indexes,</text>
  <text x="652" y="222" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">Value subagents,</text>
  <text x="652" y="234" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">RVM coach</text>
  <text x="652" y="258" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">exit: Value Model</text>
  <text x="652" y="270" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">guidance live</text>
  <rect x="725" y="115" width="125" height="170" fill="#8e44ad" fill-opacity="0.08" stroke="#8e44ad" stroke-width="1.3" rx="5"/>
  <text x="787" y="137" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="middle">Wave 6</text>
  <line x1="735" y1="145" x2="840" y2="145" stroke="#ccc" stroke-width="1"/>
  <text x="787" y="162" font-family="sans-serif" font-size="10" font-weight="600" fill="#1a1a2e" text-anchor="middle">People +</text>
  <text x="787" y="175" font-family="sans-serif" font-size="10" font-weight="600" fill="#1a1a2e" text-anchor="middle">Competency</text>
  <text x="787" y="188" font-family="sans-serif" font-size="9" font-style="italic" fill="#8e44ad" text-anchor="middle">ASAP Wave 2</text>
  <text x="787" y="210" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">identity resolver,</text>
  <text x="787" y="222" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">privacy gate,</text>
  <text x="787" y="234" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">CITA path planner</text>
  <text x="787" y="258" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">exit: all four models</text>
  <text x="787" y="270" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">audit-trailed</text>
  <line x1="175" y1="200" x2="185" y2="200" stroke="#1a1a2e" stroke-width="1" marker-end="url(#wd-arr)"/>
  <line x1="310" y1="200" x2="320" y2="200" stroke="#1a1a2e" stroke-width="1" marker-end="url(#wd-arr)"/>
  <line x1="445" y1="200" x2="455" y2="200" stroke="#1a1a2e" stroke-width="1" marker-end="url(#wd-arr)"/>
  <line x1="580" y1="200" x2="590" y2="200" stroke="#1a1a2e" stroke-width="1" marker-end="url(#wd-arr)"/>
  <line x1="715" y1="200" x2="725" y2="200" stroke="#1a1a2e" stroke-width="1" marker-end="url(#wd-arr)"/>
  <path d="M 652 300 Q 652 345 400 345 Q 250 345 250 300" fill="none" stroke="#8e44ad" stroke-width="1.4" marker-end="url(#wd-arr-p)"/>
  <text x="450" y="360" font-family="sans-serif" font-size="10" font-style="italic" fill="#8e44ad" text-anchor="middle">ASAP Studio consumes SpecChat (one-way dependency)</text>
  <line x1="40" y1="395" x2="880" y2="395" stroke="#999" stroke-width="1"/>
  <text x="450" y="415" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">The product fork at Wave 4 is the structural reflection of the paper's zoom-out argument.</text>
  <text x="450" y="430" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">SpecChat ships independently; ASAP Studio consumes SpecChat through the MCP server surface.</text>
</svg>

---

## Global Corp

ASAP Studio's design becomes concrete against a worked enterprise. [Global Corp](examples/global-corp/Global-Corp-Exemplar.html) is a fictional global supply-chain company specified completely in BTABoK terms: a strategic thesis with named objectives, a portfolio of capabilities and value streams, a multi-application architecture spec collection, a decision register, a waiver process, a view gallery, and the personas, architecturally significant requirements, and governance bodies that organize them. The narrative document lives in this repository alongside the paper; the formal spec collection lives in the sibling [spec-chat repository](https://github.com/Realization-Engine/spec-chat/tree/main/docs/examples/global-corp/) where SpecChat validators exercise it end-to-end.

Global Corp serves three roles in the derivation.

First, it is the **fixed point against which ASAP Studio components are designed**. Each subagent, scheduled task, skill, and primitive is shaped by what it would actually do for the architect responsible for Global Corp's evolution. The governance reviewer subagent is calibrated against Global Corp's review-body packets. The RVM coach is calibrated against Global Corp's initiatives at the three indicator horizons. The mentoring matchmaker is calibrated against Global Corp's distributed architect team across six regional hubs. Without this fixed point, ASAP Studio's features would be hypothetical; with it, each feature is dimensioned against concrete practitioner work.

Second, Global Corp is the **substance-channel test bench**. Every ASAP Studio feature must produce, against Global Corp, output whose substance is genuinely traceable to the architect's input. Not output whose presentation looks impressive against an unfalsifiable enterprise, but output whose substance withstands the inspection that an architect responsible for a real enterprise would apply. The framework's Eq. 10 (the epistemic gap) is most dangerous when the problem is under-specified; Global Corp is specified enough that the gap is visible in any feature's output that produces presentation without substance. This is the fixture against which ASAP Studio's features are structurally falsifiable, even in advance of production deployment.

Third, and over the long arc, Global Corp is part of the **substance-preserved corpus** Part Two named. As the general architectural corpus degrades under the data-quality spiral (Eq. 31), deliberately maintained exemplars where the substance channel was disciplined become reference material for the practice and, in the demand-side commons intervention ASAP Studio endorses, for future training data. The substance-preserved corpus is also the F→M transfer ASAP Studio endorses: not the tacit absorption that happens by default, but the deliberate contribution of substance-disciplined work back into the training signal. ASAP Studio's audit trail makes this contribution legible: the corpus is not just architecturally good work; it is work whose substantive provenance is traceable.

Global Corp is not illustrative. It is the bench, the test, and the counter-example, all at once.

---

## Four futures for the architecture profession

The framework's terminal-dynamics analysis distinguishes three regimes the coupled (F, M) system can settle into: virtuous (FORCE maintained, training signal high, both grow together), managed decline (FORCE atrophies moderately, signal degrades slowly, a lower equilibrium holds), collapse spiral (FORCE atrophies severely, signal degrades enough to stall or reverse M, both reinforce each other downward). The framework's Part Three names four specific futures the software profession may inhabit, governed by whether a substitute source of productive struggle can be found or created as the Multiplier absorbs the activities that historically provided it. The four futures translate to architecture practice without modification.

**Future 1. The pilot model.** Aviation maintains pilot FORCE through deliberate manual-flight training, even though autopilot handles routine operations. Applied to architecture: organizations and certification bodies (IASA, the CITA structure) deliberately preserve unassisted architectural practice as a developmental requirement. The architect-in-training does the work without the LLM as a condition of advancement. Senior architects accept short-term productivity loss for long-term FORCE maintenance. This is expensive and requires institutional discipline. The framework predicts it works because the atrophy equation does not care why struggle is present; it just needs struggle to be nonzero.

**Future 2. Permanent bifurcation.** The profession splits irreversibly. A shrinking class of pre-LLM-trained architects, the deep-FORCE holders, sits above F* and compounds. Below them, a larger class of LLM-mediated practitioners produces architectural artifacts that look correct, populate the registers, and pass governance review on the strength of the presentation channel. They lack the FORCE to handle novel problems, sector-specific concerns, or the integration work that requires deep judgment. The workforce runs on borrowed time: the time of the pre-LLM cohort that is aging out. The framework's Eq. 13 gives the timeline: when tacit-knowledge transmission falls below decay, the knowledge stock enters irreversible decline, and the clock is the retirement curve.

**Future 3. The role dissolves.** Enterprise architect as a distinct profession ceases to exist, absorbed into adjacent disciplines. Domain specialists (the medical, financial, logistics, regulatory experts) specify what their systems should do from deep domain knowledge; the LLM mediates the architectural artifacts; a small cadre of deep-FORCE systems thinkers handles the failure modes and the integrations the LLM cannot reach. The middle of the architecture profession is absorbed entirely.

**Future 4. The return to specification.** The profession's craft moves upward into a formal specification layer: the architect specifies what must hold across the system's behavior, the LLM realizes within the specification, the architect's substance work is the precision of the specification rather than the manual production of artifacts. The framework is cautiously optimistic about whether specification-derived FORCE can substitute for implementation-derived FORCE; it identifies the transition as the danger zone. Current senior architects developed FORCE through implementation and artifact work; Future 4's architects would need to develop FORCE through specification work. Whether this is possible without an implementation or artifact-production foundation is empirically untested, and Eq. 14a (hysteresis) warns that if the transition is botched, recovery is harder than the initial descent.

ASAP Studio's design is an **explicit bet on Future 1 plus Future 4**. Future 1 is the rationale for the apprenticeship-preservation mechanisms: the mentor-as-AI-backstage band, the AI-excluded categories around mentor judgment and certification, the deliberate surfacing of shared-work opportunities, the audit-trail support for unassisted-work demonstration. Future 4 is the rationale for the SpecChat dependency: ASAP Studio is built on top of a formal specification language because its bet is that architectural commitment lives in specification, not in artifact production, and that specification struggle can carry what implementation and artifact-production struggle used to carry. ASAP Studio refuses Futures 2 and 3 as outcomes by design. It cannot prevent them. It can only structure the conditions under which Future 1 and Future 4 remain reachable.

At SMB scale (Part Two, "The SMB-architect"), Futures 1 and 4 depend even more heavily on the practitioner's personal adoption of the amplification architecture's disciplines, because the institutional scaffolding that partially defends those futures at enterprise scale is absent. ASAP Studio as a personal calendrical instrument, deployed by a solo contract architect or a small architecture firm without an enterprise governance wrapper, is a first-class case of the amplification architecture rather than a scaled-down special case.

The window for choosing is finite. The framework gives the clock explicitly: the retirement curve of the pre-LLM cohort, who carry the deep layer the next cohort can still receive from if the channels are preserved. ASAP Studio exists to preserve those channels while the cohort is still available to use them.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 510" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="ff-t ff-d">
  <title id="ff-t">Four futures for the architecture profession</title>
  <desc id="ff-d">Four horizontal trajectory lanes showing FORCE dynamics over time for each future the framework predicts. Future 1, the pilot model: FORCE is deliberately preserved, trajectory stays high. Future 2, permanent bifurcation: a pre-LLM cohort trajectory stays high while a post-LLM cohort trajectory declines; the pre-LLM cohort ages out. Future 3, the role dissolves: middle-layer practitioners are absorbed; trajectory declines toward zero. Future 4, the return to specification: struggle relocates to the specification layer; trajectory dips through a transition danger zone, then rebuilds on a specification-derived foundation. Futures 1 and 4 are marked as ASAP Studio's bet. Futures 2 and 3 are marked as refused by design. A footer states that the clock is the pre-LLM cohort's retirement curve.</desc>
  <text x="130" y="35" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="middle">Future</text>
  <text x="460" y="35" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="middle">FORCE trajectory over time</text>
  <text x="800" y="35" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="middle">Terminal state</text>
  <rect x="20" y="55" width="860" height="90" fill="#3a86ff" fill-opacity="0.05" stroke="#3a86ff" stroke-width="1.3" rx="4"/>
  <text x="130" y="80" font-family="sans-serif" font-size="11" font-weight="700" fill="#3a86ff" text-anchor="middle">1. Pilot model</text>
  <text x="130" y="98" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">deliberate preservation of</text>
  <text x="130" y="110" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">unassisted practice</text>
  <text x="130" y="130" font-family="sans-serif" font-size="9" font-style="italic" fill="#3a86ff" text-anchor="middle">ASAP Studio's bet</text>
  <line x1="280" y1="135" x2="680" y2="135" stroke="#ddd" stroke-width="0.6" stroke-dasharray="2 2"/>
  <line x1="280" y1="60" x2="680" y2="60" stroke="#ddd" stroke-width="0.6" stroke-dasharray="2 2"/>
  <path d="M 280 85 Q 480 80 680 85" fill="none" stroke="#3a86ff" stroke-width="2"/>
  <text x="480" y="125" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">FORCE maintained via struggle-preservation requirement</text>
  <text x="795" y="90" font-family="sans-serif" font-size="10" font-weight="700" fill="#3a86ff" text-anchor="middle">Virtuous</text>
  <text x="795" y="108" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">FORCE and M</text>
  <text x="795" y="120" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">grow together</text>
  <rect x="20" y="155" width="860" height="90" fill="#d62828" fill-opacity="0.04" stroke="#d62828" stroke-width="1.2" rx="4"/>
  <text x="130" y="180" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828" text-anchor="middle">2. Permanent bifurcation</text>
  <text x="130" y="198" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">two cohorts diverge;</text>
  <text x="130" y="210" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">pre-LLM ages out</text>
  <text x="130" y="230" font-family="sans-serif" font-size="9" font-style="italic" fill="#d62828" text-anchor="middle">refused by design</text>
  <line x1="280" y1="235" x2="680" y2="235" stroke="#ddd" stroke-width="0.6" stroke-dasharray="2 2"/>
  <line x1="280" y1="160" x2="680" y2="160" stroke="#ddd" stroke-width="0.6" stroke-dasharray="2 2"/>
  <path d="M 280 180 L 500 183 L 600 205 L 680 230" fill="none" stroke="#3a86ff" stroke-width="1.5" stroke-dasharray="5 2"/>
  <text x="300" y="175" font-family="sans-serif" font-size="8" font-style="italic" fill="#3a86ff" text-anchor="start">pre-LLM cohort</text>
  <path d="M 280 210 Q 480 218 680 225" fill="none" stroke="#d62828" stroke-width="1.5"/>
  <text x="300" y="222" font-family="sans-serif" font-size="8" font-style="italic" fill="#d62828" text-anchor="start">post-LLM cohort</text>
  <text x="795" y="190" font-family="sans-serif" font-size="10" font-weight="700" fill="#d62828" text-anchor="middle">Managed decline</text>
  <text x="795" y="208" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">Eq. 13: clock is</text>
  <text x="795" y="220" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">retirement curve</text>
  <rect x="20" y="255" width="860" height="90" fill="#d62828" fill-opacity="0.04" stroke="#d62828" stroke-width="1.2" rx="4"/>
  <text x="130" y="280" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828" text-anchor="middle">3. Role dissolves</text>
  <text x="130" y="298" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">middle absorbed into</text>
  <text x="130" y="310" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">adjacent disciplines</text>
  <text x="130" y="330" font-family="sans-serif" font-size="9" font-style="italic" fill="#d62828" text-anchor="middle">refused by design</text>
  <line x1="280" y1="335" x2="680" y2="335" stroke="#ddd" stroke-width="0.6" stroke-dasharray="2 2"/>
  <line x1="280" y1="260" x2="680" y2="260" stroke="#ddd" stroke-width="0.6" stroke-dasharray="2 2"/>
  <path d="M 280 280 Q 400 295 500 320 Q 600 335 680 335" fill="none" stroke="#d62828" stroke-width="2"/>
  <text x="480" y="325" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">architect as distinct profession fades</text>
  <text x="795" y="290" font-family="sans-serif" font-size="10" font-weight="700" fill="#d62828" text-anchor="middle">Absorbed</text>
  <text x="795" y="308" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">domain specialists</text>
  <text x="795" y="320" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">plus thin senior cadre</text>
  <rect x="20" y="355" width="860" height="95" fill="#3a86ff" fill-opacity="0.05" stroke="#3a86ff" stroke-width="1.3" rx="4"/>
  <text x="130" y="380" font-family="sans-serif" font-size="11" font-weight="700" fill="#3a86ff" text-anchor="middle">4. Return to specification</text>
  <text x="130" y="398" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">struggle relocates</text>
  <text x="130" y="410" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">to the specification layer</text>
  <text x="130" y="430" font-family="sans-serif" font-size="9" font-style="italic" fill="#3a86ff" text-anchor="middle">ASAP Studio's bet</text>
  <line x1="280" y1="440" x2="680" y2="440" stroke="#ddd" stroke-width="0.6" stroke-dasharray="2 2"/>
  <line x1="280" y1="365" x2="680" y2="365" stroke="#ddd" stroke-width="0.6" stroke-dasharray="2 2"/>
  <path d="M 280 385 Q 360 420 440 420 Q 520 420 580 400 Q 640 380 680 370" fill="none" stroke="#3a86ff" stroke-width="2"/>
  <text x="370" y="440" font-family="sans-serif" font-size="8" font-style="italic" fill="#d62828" text-anchor="middle">transition danger zone (Eq. 14a)</text>
  <text x="620" y="393" font-family="sans-serif" font-size="8" font-style="italic" fill="#3a86ff" text-anchor="middle">spec-derived FORCE rebuilds</text>
  <text x="795" y="390" font-family="sans-serif" font-size="10" font-weight="700" fill="#3a86ff" text-anchor="middle">Virtuous (new)</text>
  <text x="795" y="408" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">specification-as-craft</text>
  <text x="795" y="420" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle">(empirically untested)</text>
  <line x1="40" y1="475" x2="880" y2="475" stroke="#999" stroke-width="1"/>
  <text x="450" y="495" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">ASAP Studio bets on Futures 1 and 4; it refuses to produce Futures 2 and 3. The clock is the pre-LLM cohort's retirement curve.</text>
</svg>

---

## Research agenda

ASAP Studio's existence creates an opportunity to empirically constrain the framework's scaling claim in the architecture-practice domain. The audit trail is the data infrastructure; the four-working-model coverage provides the FORCE-form decomposition; the CITA certification ladder and the six-level managed career path provide the cohort stratification; the zoom-out that distinguishes this paper from its predecessors provides the breadth the scaling test requires. The framework's predictions, stated at the general level in *The Multiplier and the Mirror* and worked for architecture practice in Parts One and Two, become measurable at the ASAP Studio operation layer.

Seven predictions, each framed as a falsifiable claim and each measurable through ASAP Studio's audit trail over cohort-scale time.

**1. Output variance increases post-platform adoption.** Eq. 4 predicts variance scales as M-squared. In architecture teams with platform access, the within-team variance of decision-record quality, business-case substance, viewpoint catalog coherence, and transition-architecture precision should grow faster than the between-team variance across platform-using and non-using practices. Measurable through audit-trailed quality metrics on artifacts produced with and without AI-strong patterns, stratified by CITA level.

**2. Judgment-heavy Engagement work commands rising within-firm value relative to execution-heavy work.** Eq. 22 predicts judgment moats amplify and execution moats collapse. In firms with platform adoption, compensation and promotion signals should shift toward architects whose substantive contribution is decision adjudication, principle authorship, and integration-under-ambiguity rather than toward architects whose contribution is artifact production. Measurable through compensation data by work-type over time.

**3. Post-LLM architect cohorts show lower unassisted performance at equivalent CITA stage than pre-LLM cohorts.** Eq. 32 predicts cohort-ceiling descent. Board examinations or live-challenge components administered without platform access should reveal widening unassisted-performance gaps between pre-LLM and post-LLM cohorts at equivalent certification stage. Measurable through CITA board protocols.

**4. Organizations with higher LLM adoption show declining performance on novel architectural challenges.** Eqs. 14a (hysteresis) and 26-27 (F→M transfer ceiling) jointly predict this. Firms whose architects have high platform adoption should show measurably worse performance on cross-sector integration, novel regulatory-regime adaptation, post-merger architectural reconciliation, and incident response under novel failure modes. Measurable through case-study protocols and post-incident review data.

**5. High-FORCE architects extract measurably higher effective M from the same platform features.** Eq. 4a predicts this. Given identical platform access, Distinguished architects should produce higher-quality outputs per unit platform engagement than Associate architects, by margins larger than the FORCE differential alone would predict. Measurable through audit-trailed output-quality metrics stratified by CITA level.

**6. Evaluation bottlenecks (review-body cycle time, decision approval lead time) increase post-platform deployment.** Eq. 7 predicts this. Firms with platform adoption should show longer review-body cycle times and longer decision approval lead times as the artifact stream grows and the substance-distinguishability problem compounds. Measurable through governance process instrumentation.

**7. The separatrix F*(M) for the architecture profession becomes measurable through cohort-level competency tracking against observed multiplier growth.** The phase-portrait geometry of Eqs. 34 (separatrix) and 36 (irreversibility frontier) is, in principle, empirically characterizable. Different monotone regimes of signal-quality dependence predict distinct separatrix curvatures and distinct irreversibility-frontier locations. Cross-cohort measurement of workforce capability against observed multiplier growth, controlling for policy and environmental differences, can in principle discriminate among the regimes the framework's phase portrait distinguishes. ASAP Studio makes this data collectible at architecture-practice scale.

Each prediction is stated with enough precision to be tested. The framework is strong enough to make these specific, non-obvious claims; ASAP Studio is the instrument through which the profession can hold itself accountable to them. If the predictions hold across the four working models ASAP Studio covers, the scaling claim this paper has been building is empirically confirmed in the architecture-practice domain. If they fail in one working model but hold in others, the failure itself is informative about which parameter is not portable and where the scaling claim breaks.

---

## Closing

The Multiplier exists. The Mirror operates at two scales. The atrophy equation applies to architecture practice with only parameter change per FORCE-form. The cascade operates, the decision bottleneck binds, the legibility crisis collapses the institution's assessment signal, the sovereignty question fires at two scales. The framework's scope note, which invites any profession where apprenticeship passes tacit knowledge through shared execution to substitute for the engineer, holds for architecture practice. The scaling claim the zoom-out tests passes, across the four working models ASAP Studio covers, in the specific ways Parts Two and Three have worked through.

The amplification architecture the framework requires has been derived. Its authority is tiered to the Variable Multiplier's shape. Its AI-suitability bands and safeguard patterns are calibrated to atrophy risk per FORCE-form. Its coverage across Engagement, Value, People, and Competency is the minimum the zoom-out requires. Its ten primitives are the minimum agentic vocabulary the practitioner's calendrical surface demands. Its stop-lines are structural, not configurable. Its six-wave delivery and the SpecChat dependency are the engineered form of the paper's zoom-out. Global Corp is the bench. The four futures are the regimes. The seven predictions are what ASAP Studio commits to making empirically constrainable.

ASAP Studio is the implementation of the amplification architecture this paper derives. It is one response to the framework. It is not the only possible response. It is the response this paper derives and the worked instantiation the series now names.

Build the FORCE. Preserve the channels through which the next cohort can receive what the current cohort still carries. The multiplication, and the scaling, take care of themselves. What in the architect's craft is worth carrying, the Mirror lets us see.
