---
title: "The Architect and the Agent, Part Two: Ramifications in Architecture Practice"
subtitle: "A companion whitepaper to The Multiplier and the Mirror, on the enterprise architect's practice under LLM amplification and the amplification architecture the Multiplier-Mirror framework requires."
author: "Dennis A. Landi"
version: "0.01"
date: "2026-04-21"
category: "Whitepaper"
folio: "Nº IV, Part Two of Three"
project: "ASAP"
source: "https://github.com/Realization-Engine/asap"
prev-url: "The_Architect_and_the_Agent-Part-One.html"
prev-title: "Part One, The Architect Under Amplification"
next-url: "The_Architect_and_the_Agent-Part-Three.html"
next-title: "Part Three, The Amplification Architecture"
---

# Part Two - Ramifications in Architecture Practice

Part One instantiated the **Multiplier-Mirror framework** (Folio Nº II) for architecture practice and named three commitments the amplification architecture must honor. Part Two works out the framework's ramifications in the architectural domain, using the seven-loop cascade as the structuring device, and shows how each loop produces a specific operational pressure on the profession. A note on the treatment throughout: each loop operates in all four working models ASAP Studio covers (Engagement, Value, People, Competency), but not identically. Inside the Engagement Model, where a formal specification medium (SpecChat) exists and where artifacts are validated by machine, the loop manifests through artifact-level dynamics that leave a trail, and brakes there can be formal. Inside Value, People, and Competency, where no formal medium underlies the work, the loop manifests through cadence-level dynamics that are visible only in aggregate pattern, and brakes there can only be agentic and advisory. The difference does not weaken the scaling claim. It confirms it: same mechanism, different surface, different brake. Each loop below is presented in both surfaces, so the scaling is legible at the loop level.

---

## The cascade

The Multiplier and the Mirror describes seven reinforcing feedback loops in the coupled human-LLM system, each amplifying the atrophy dynamic, few with natural brakes, operating together as a cascade that pulls trajectories below the tipping point faster than any single loop in isolation. The cascade is not a speculative construct. Each loop is derived from equations in the main-line framework and formalized for the software engineer in the parent paper's Part Two. The question this paper now asks is whether the cascade operates in architecture practice the way the framework predicts it should, with only parameters changing per FORCE-form. That is the scaling claim stated precisely. The seven loops below work the claim one loop at a time.

### Loop 1. Atrophy, epistemic corruption, undetected architectural failures

The framework's Eq. 11 contests four pressures on FORCE: struggle-based growth, deliberate-engagement growth, passive-reliance decay, and organizational de-investment. When middle-layer FORCE decays under the passive-reliance term, self-assessment erodes first, because self-assessment is itself a middle-layer capability. The practitioner feels more confident in work that is quietly getting worse, which delays correction. The framework names this the epistemic gap (Eq. 10): the distance between apparent and warranted competence.

In architecture practice the loop operates through artifact production and decision quality. An architect whose architecturally-significant-decision drafting becomes LLM-mediated produces fluent decision records whose options-and-consequences sections look rigorous. The mentor review that would previously have detected weak reasoning now reviews LLM-rendered reasoning; the mentor must work harder to distinguish fluent presentation from substantive thought. Over a quarter the atrophy is invisible. Over a year the architect's unassisted decision quality measurably declines, while her assisted decision quality holds or even rises. Three years in, the architect cannot reliably make a novel architectural decision without the tool, but her track record of logged decisions shows no decline. The epistemic gap has opened under a steady output curve.

Inside the Engagement Model the brake exists. Substance-channel discipline in the specification medium (validators, traceability requirements, mandatory rationale fields, decision provenance) preserves the assessment signal at the artifact layer. A disciplined spec medium forces the architect through the cognitive walk her decision record purports to represent. ASAP Studio's structural refusal to widen SpecChat's formal scope is precisely the refusal to extend this brake to domains the medium cannot formalize. In Value, People, and Competency, no formal medium exists to hold substance discipline the same way. The brake there is agentic: the governance reviewer subagent critiques against the principles the practice has declared; the ADLC stage coach prompts the walk the artifact requires; the competency-coverage features surface the atrophy pattern before it becomes visible in output. These brakes detect; they do not prevent.

### Loop 2. Epistemic corruption, review bottleneck, governance overload

The framework's Eq. 7 establishes that as creation cost approaches zero while evaluation cost holds or rises, throughput becomes bounded by evaluation capacity. Eq. 18 further shows that evaluation capacity is itself reduced when the presentation channel collapses the signal-to-noise ratio on substantive difference: the same reviewer now spends more time on each artifact to separate polished hollowness from genuine thought. Eq. 7a, the organizational paradox, follows. The highest-FORCE practitioners must be sent to review rather than creation, precisely because the presentation channel has made creation democratic while evaluation has become harder. The optimal allocation sends scarce evaluation capacity to the bottleneck; the bottleneck grows faster than the capacity.

In architecture practice the governance bodies that consume the artifact stream, the senior-architect sign-off chain, the decision approval committees, the review boards where they exist, feel this directly. As LLM-mediated artifacts proliferate, review cycle time extends. Tier-one architectural decisions that previously fit a weekly or biweekly review cadence now queue. The chair's preparation time compounds because the packet is larger and the work of distinguishing substantive from hollow items is heavier. Senior architects, already the scarce resource, spend more time reviewing others' work and less time creating their own. The creation-to-evaluation ratio shifts unfavorably, and the bottleneck tightens.

Inside the Engagement Model, mechanical governance preparation is a strong case for automation. ASAP Studio's review-packet assembly automation, freshness sweeps, and waiver-chain expansion reduce the mechanical overhead of running governance, reserving human attention for the substance that requires it. The decision scribe drafts records; the architect signs. The governance reviewer subagent assembles risk summaries; the chair decides. The authority gradient permits this because the mechanical work has a reliably high substance multiplier. Outside the Engagement Model, where governance is relational rather than procedural, the brake is weaker. The culture diagnostic runner, the community health observer, the team capability-gap analyzer each surface signals; only humans can interpret and act on them. Eq. 7a holds in both surfaces; the operational response differs.

### Loop 3. Organizational efficiency, tacit knowledge decay, team FORCE collapse

The framework's Eqs. 12 and 12b model the tacit-knowledge pipeline. Transmission requires shared work; shared work declines exponentially as the multiplier absorbs delegable tasks; at some threshold the pipeline enters irreversible decline because more knowledge leaves (through retirement, attrition, memory fade) than arrives (through senior-to-junior transmission).

The architectural form is sharp. The shared work that carried architectural tacit knowledge was the work of drafting decision records, assembling review packets, canvassing stakeholders, running waiver chains, populating viewpoint catalogs. The junior worked beside the senior on this work, and the senior's handling of edge cases, the moments of hesitation, the choice of which consideration to foreground, were the transmission. Under LLM mediation the senior's artifact looks the same but the work is different: she reviewed rather than produced; mentor-in-the-work has become mentor-in-the-review. The junior sees less, and the junior's own artifact-drafting work is itself LLM-mediated, which means the junior is learning to prompt rather than to reason. The three-to-six-month mentoring engagement the IASA Mentoring Method prescribes for Foundation and Associate architects was calibrated against a volume of shared work that is shrinking.

The brake exists unevenly across the four working models. Inside Engagement, the audit trail can surface where senior-junior shared work is actually happening (versus being asserted) and where it has collapsed. Outside Engagement, the mentor-as-AI-backstage band, the deliberate surfacing of shared-work opportunities, and the AI-excluded category around mentor judgment are ASAP Studio's structural responses to this loop specifically. The People Model is where this loop lives most visibly; ASAP Studio's heaviest non-Engagement investment is here, because the framework's Eq. 12b has its sharpest operational form in architecture's developmental pipeline.

### Loop 4. FORCE decay, motivation decay, further FORCE decay

The framework's Eq. 23 and Eq. 1 together produce the Meaning Problem: motivation enters the FORCE product multiplicatively, which means its decay drags the entire product down, which means FORCE itself decays faster, which means motivation decays faster. This is a fully internal loop that operates without external input. It requires only that the practitioner lose autonomy, competence, or relatedness, the three psychological needs the framework names as motivation's substrate.

In architecture practice, autonomy loss looks like this: the architect who used to decide which principle to foreground in a decision now reviews the LLM's draft, which has already foregrounded one. Competence displacement looks like this: the work that used to require hours of the architect's most practiced craft is produced in seconds by a tool the client, the manager, and the junior can all invoke. Relatedness weakens as shared work declines (Loop 3) and as the architect spends more time in review rooms and less time at whiteboards. The Distinguished architect who built her career on the satisfaction of seeing a clean transition architecture emerge from a messy problem now watches the transition architecture emerge from the tool; her role is to catch what the tool missed. The role's meaning has shifted without anyone announcing the shift.

The brake is what the framework calls the studio-mirror function. Above F*, with the architect substantively engaged, the LLM is a feedback instrument that compounds the architect's capability and her sense of agency. ASAP Studio's commitment to human-in-the-loop discipline, to the AI-strong-with-human-signature pattern, to categorical exclusions on judgment work, is partially a defense of motivation. A platform that absorbed the substantive work would, by the framework's own coupling, accelerate the collapse it exists to prevent.

### Loop 5. Variance amplification, barbell, talent concentration, evaluation bottleneck

The framework's Eq. 4 says output variance scales as M squared. Eq. 4a strengthens this because high-FORCE practitioners extract a higher effective multiplier from the same tool; the effective multiplier is itself positively correlated with FORCE, so the variance grows faster than the simple squared-M prediction. The barbell effect of Eq. 6 is the distributional consequence: the middle hollows, the high end compounds, a new low-FORCE orchestration tier emerges. Talent concentration follows: high-FORCE practitioners migrate toward firms that can use and reward them; low-FORCE firms lose evaluation capacity and become less attractive to high-FORCE talent.

Inside an architecture team the dynamics are acute. The Distinguished architect and the Associate both have platform access, the same models, the same retrievals. The Distinguished's effective multiplier is higher because her prompts carry substance the Associate's do not. Her throughput on decision records, viewpoints, transition architectures, business cases, and stakeholder engagement artifacts grows faster. At the team level, her output displaces the Associate's in contests for review bandwidth, approval cycles, and stakeholder attention, because her artifacts clear the bar faster and with fewer revisions. The within-team gap widens without anyone doing anything wrong.

The ROI paradox of Eq. 17 operates next. The Distinguished's marginal return on platform usage is higher than the Associate's, so rational allocation concentrates platform time on the Distinguished. The Distinguished's evaluation return is also highest, because she can distinguish substance from presentation faster than any Associate. The three-way resource competition of Eq. 28 becomes operational: building, reviewing, teaching the model. Her scarcity was already acute pre-LLM; the multiplier makes her an order of magnitude more valuable for each of the three activities, and an order of magnitude more constrained in her ability to do all three.

ASAP Studio's partial brake is the AI-suitability band structure Part Three derives in detail. AI-strong patterns let the Associate contribute through draft-and-review and assemble-and-present, with the Distinguished in final-signature position, preserving the Associate's role as author-with-assistance rather than operator-of-tool. AI-backstage patterns let the Distinguished's review burden decrease without the Associate inferring that the review was agentic; the mentor relationship stays human-to-human. Gate-and-block patterns prevent work that was formerly the Distinguished's sole responsibility (architectural-significance adjudication, for instance) from drifting into AI-produced output that reads as if she signed it. None of this eliminates the variance amplification. It slows it, and it prevents the institution from being misled about who did the work.

### Loop 6. F→M transfer, organizational de-investment, training signal degradation, multiplier stagnation

The framework's Eqs. 26 through 31 formalize the F→M transfer: senior practitioner output flows into the model through fine-tuning, RLHF, evaluation data, and retrieval systems, with transfer efficiency decreasing as the FORCE-layer deepens. The ceiling (Eq. 27) converges to the explicit portion of what the experts know, weighted by layer transfer efficiency. The tacit residual remains with the human. The bus-factor illusion (Eq. 29) is the organizational confusion between what transferred and what the expert actually knew. The data-quality spiral (Eq. 31) closes the loop: if average workforce FORCE declines under the atrophy dynamics this paper has been working through, the human signal feeding next-generation training degrades, which degrades future model quality, which degrades the conditions under which future practitioners develop FORCE.

The architectural form has its own specificity. The IASA BTABoK corpus is being absorbed into LLM training right now: surface-layer material (framework names, canvas structures, definitional content) near-completely; middle-layer material (judgment patterns in context) partially; deep-layer material (architectural intuition built through decades of consequences) barely. The ceiling Eq. 27 names is therefore a ceiling on how well the mirror can reflect architecture practice specifically: high on standard framework material, partial on context-sensitive judgment, low on the structural intuition that distinguishes a senior architect. The bus-factor illusion has an architectural form at the enterprise scale: organizations that have used LLM-assisted documentation to capture their senior architects' knowledge believe they have reduced their key-person risk; they have captured the articulable surface while the tacit residual has remained with the practitioner or has already retired.

ASAP Studio's response to this loop is to make its own F→M transfer deliberate rather than inadvertent. The Knowledge Layer is the only deliberate, controlled, attribution-preserving F→M transfer ASAP Studio performs; every retrieval is attributed, every claim is traceable to its source. Global Corp, treated in Part Three, functions in part as a substance-preserved corpus: deliberately maintained architectural exemplars where the substance channel was disciplined, citable as counter-evidence to the generally degrading corpus, contributable to the demand-side of the training-signal commons without the tacit absorption that happens by default.

### Loop 7. Cohort discontinuity, reduced absorption, accelerated pipeline collapse

The framework's Eq. 32 establishes that each successive cohort entering the profession under the multiplier faces a lower FORCE ceiling, not through individual deficiency but through structural reduction in the conditions under which FORCE forms. This is the cohort discontinuity. It compounds Loop 3: post-LLM cohorts both have less shared work to be the receiver in, and are less capable of absorbing when they are present for it, because the struggle history that would prepare them for the absorption is itself absent.

Part One worked out the architectural form in detail under the CITA certification ladder (Foundation, Associate, Professional, Distinguished) and the six-level managed career path (Aspiring, Foundational, Associate, Professional, Distinguished, Chief). Here Part Two adds the prediction. If the profession does not act to preserve the conditions under which Foundational and Associate architects develop middle-layer FORCE, the profession will, within a generation, produce architects whose CITA certifications match their predecessors' but whose Shaping-layer competency does not. Certification will remain; deep FORCE will attenuate; the bus-factor illusion at the profession scale will grow until the pre-LLM cohort that carries the deep layer ages out. The framework gives the timeline through Eq. 13: when tacit-knowledge transmission falls below decay, the pipeline is broken, and the clock is the retirement curve of the cohort that carries the tacit stock.

ASAP Studio brakes this loop through deliberate apprenticeship-preservation mechanisms Part Three derives in detail. The brakes cannot recreate the conditions that produced senior practitioners. They can only protect the channels that still exist. This is the framework's most uncomfortable architectural prediction, and it is the one ASAP Studio's existence is calibrated most directly against.

### The cascade as a system

The seven loops are not independent. They interact, and several pairs mutually reinforce. Loop 1's atrophy fuels Loop 2's signal collapse, which accelerates Loop 5's talent concentration by overloading evaluation, which accelerates Loop 4's motivation decay in the overloaded seniors, which accelerates Loop 3's tacit collapse as those seniors disengage from mentoring, which accelerates Loop 7's cohort discontinuity, which closes back into Loop 6's training-signal degradation and through it to Loop 1 at the next generation. The framework is explicit that few natural brakes exist on these interactions; ASAP Studio's value as a *system*, distinct from its value as a feature set, is in introducing deliberate brakes at multiple loop intersections, slowing the cascade enough that institutional and practitioner choices remain meaningful. Part Three derives each brake feature by feature.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 720" width="100%" style="max-width:1000px;display:block;margin:1.5em auto;" role="img" aria-labelledby="ca-t ca-d">
  <title id="ca-t">The cascade for architecture practice</title>
  <desc id="ca-d">A central node labeled F-arch represents the architect's composite FORCE. Eleven surrounding nodes are connected via seven colored feedback loops, each rendering the framework's cascade in architecture-specific vocabulary. Loop 1 (red): F-arch exchanges with an epistemic gap on ADR and decision quality. Loop 2 (orange): the epistemic gap feeds into an EARB and sign-off queue extension. Loop 3 (green): the EARB queue feeds into shared packet and drafting work decline, which feeds into tacit architectural knowledge decay, which returns to F-arch. Loop 4 (purple): F-arch exchanges with craft-work motivation decay. Loop 5 (yellow): the variance amplifier in the team feeds into the Distinguished saturating review bandwidth, which feeds into the EARB queue. Loop 6 (blue): F-arch feeds the F-to-M transfer of BTABoK material into the training corpus, which drives both firm de-investment in architect FORCE and model degradation on BTABoK-niche work, both returning to F-arch. Loop 7 (brown): cohort discontinuity at CITA stages feeds into tacit knowledge decay and into F-arch. A legend at the bottom names all seven loops.</desc>
  <defs>
    <marker id="ca-a1" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#e74c3c"/></marker>
    <marker id="ca-a2" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#e67e22"/></marker>
    <marker id="ca-a3" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#27ae60"/></marker>
    <marker id="ca-a4" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#8e44ad"/></marker>
    <marker id="ca-a5" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#d4a017"/></marker>
    <marker id="ca-a6" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#2980b9"/></marker>
    <marker id="ca-a7" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#8b4513"/></marker>
  </defs>
  <circle cx="500" cy="360" r="48" fill="#1a1a2e" stroke="none"/>
  <text x="500" y="355" font-family="serif" font-size="20" font-style="italic" font-weight="700" fill="white" text-anchor="middle">F</text>
  <text x="514" y="362" font-family="serif" font-size="11" font-style="italic" fill="white" text-anchor="start">arch</text>
  <text x="500" y="383" font-family="sans-serif" font-size="9" fill="white" text-anchor="middle">Eq. 1, 11</text>
  <text x="500" y="395" font-family="sans-serif" font-size="8" fill="white" text-anchor="middle">per FORCE-form</text>
  <rect x="420" y="105" width="160" height="50" fill="none" stroke="#8e44ad" stroke-width="1.5" rx="6"/>
  <text x="500" y="127" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">Craft-work</text>
  <text x="500" y="143" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">motivation decays</text>
  <rect x="670" y="115" width="180" height="50" fill="none" stroke="#d4a017" stroke-width="1.5" rx="6"/>
  <text x="760" y="137" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">Variance amplifier</text>
  <text x="760" y="153" font-family="sans-serif" font-size="11" fill="#555" text-anchor="middle">within the team (Eq. 4)</text>
  <rect x="740" y="245" width="180" height="50" fill="none" stroke="#d4a017" stroke-width="1.5" rx="6"/>
  <text x="830" y="267" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">Distinguished</text>
  <text x="830" y="283" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">saturates review</text>
  <rect x="630" y="335" width="180" height="50" fill="none" stroke="#e74c3c" stroke-width="1.5" rx="6"/>
  <text x="720" y="357" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">Epistemic gap on</text>
  <text x="720" y="373" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">ADR / decision quality</text>
  <rect x="630" y="475" width="180" height="50" fill="none" stroke="#e67e22" stroke-width="1.5" rx="6"/>
  <text x="720" y="497" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">EARB / sign-off</text>
  <text x="720" y="513" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">queue extends</text>
  <rect x="535" y="595" width="180" height="50" fill="none" stroke="#27ae60" stroke-width="1.5" rx="6"/>
  <text x="625" y="617" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">Shared packet /</text>
  <text x="625" y="633" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">drafting work declines</text>
  <rect x="295" y="595" width="200" height="50" fill="none" stroke="#27ae60" stroke-width="1.5" rx="6"/>
  <text x="395" y="617" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">Tacit architectural</text>
  <text x="395" y="633" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">knowledge decays</text>
  <rect x="60" y="595" width="180" height="50" fill="none" stroke="#8b4513" stroke-width="1.5" rx="6"/>
  <text x="150" y="617" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">Cohort discontinuity</text>
  <text x="150" y="633" font-family="sans-serif" font-size="11" fill="#555" text-anchor="middle">at CITA stages (Eq. 32)</text>
  <rect x="190" y="335" width="180" height="50" fill="none" stroke="#2980b9" stroke-width="1.5" rx="6"/>
  <text x="280" y="357" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">F&#8594;M: BTABoK</text>
  <text x="280" y="373" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">into training corpus</text>
  <rect x="20" y="175" width="180" height="50" fill="none" stroke="#2980b9" stroke-width="1.5" rx="6"/>
  <text x="110" y="197" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">Firm de-invests in</text>
  <text x="110" y="213" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">architect FORCE</text>
  <rect x="20" y="485" width="180" height="50" fill="none" stroke="#2980b9" stroke-width="1.5" rx="6"/>
  <text x="110" y="507" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">Model degrades on</text>
  <text x="110" y="523" font-family="sans-serif" font-size="12" font-weight="600" fill="#1a1a2e" text-anchor="middle">BTABoK-niche work</text>
  <path d="M 548 348 Q 585 320 630 348" fill="none" stroke="#e74c3c" stroke-width="1.6" marker-end="url(#ca-a1)"/>
  <path d="M 630 372 Q 585 400 548 372" fill="none" stroke="#e74c3c" stroke-width="1.6" marker-end="url(#ca-a1)"/>
  <text x="585" y="315" font-family="sans-serif" font-size="11" fill="#e74c3c" font-weight="700">L1</text>
  <path d="M 720 385 Q 745 430 720 475" fill="none" stroke="#e67e22" stroke-width="1.6" marker-end="url(#ca-a2)"/>
  <text x="752" y="435" font-family="sans-serif" font-size="11" fill="#e67e22" font-weight="700">L2</text>
  <path d="M 680 525 Q 650 570 625 595" fill="none" stroke="#27ae60" stroke-width="1.6" marker-end="url(#ca-a3)"/>
  <path d="M 535 620 Q 515 628 495 620" fill="none" stroke="#27ae60" stroke-width="1.6" marker-end="url(#ca-a3)"/>
  <path d="M 400 595 Q 430 490 482 401" fill="none" stroke="#27ae60" stroke-width="1.6" marker-end="url(#ca-a3)"/>
  <text x="655" y="578" font-family="sans-serif" font-size="11" fill="#27ae60" font-weight="700">L3</text>
  <path d="M 488 316 Q 450 225 488 158" fill="none" stroke="#8e44ad" stroke-width="1.6" marker-end="url(#ca-a4)"/>
  <path d="M 512 158 Q 550 225 512 316" fill="none" stroke="#8e44ad" stroke-width="1.6" marker-end="url(#ca-a4)"/>
  <text x="440" y="245" font-family="sans-serif" font-size="11" fill="#8e44ad" font-weight="700">L4</text>
  <path d="M 760 165 Q 810 205 820 245" fill="none" stroke="#d4a017" stroke-width="1.6" marker-end="url(#ca-a5)"/>
  <path d="M 830 295 Q 855 390 775 475" fill="none" stroke="#d4a017" stroke-width="1.6" marker-end="url(#ca-a5)"/>
  <text x="822" y="210" font-family="sans-serif" font-size="11" fill="#d4a017" font-weight="700">L5</text>
  <path d="M 455 370 Q 395 395 370 370" fill="none" stroke="#2980b9" stroke-width="1.6" marker-end="url(#ca-a6)"/>
  <path d="M 240 340 Q 185 295 165 228" fill="none" stroke="#2980b9" stroke-width="1.6" marker-end="url(#ca-a6)"/>
  <path d="M 240 380 Q 185 425 165 482" fill="none" stroke="#2980b9" stroke-width="1.6" marker-end="url(#ca-a6)"/>
  <path d="M 190 210 Q 320 250 460 346" fill="none" stroke="#2980b9" stroke-width="1.6" marker-end="url(#ca-a6)"/>
  <path d="M 190 500 Q 320 475 460 373" fill="none" stroke="#2980b9" stroke-width="1.6" marker-end="url(#ca-a6)"/>
  <text x="390" y="352" font-family="sans-serif" font-size="11" fill="#2980b9" font-weight="700">L6</text>
  <path d="M 240 620 Q 270 628 295 620" fill="none" stroke="#8b4513" stroke-width="1.6" marker-end="url(#ca-a7)"/>
  <path d="M 170 595 Q 290 480 468 395" fill="none" stroke="#8b4513" stroke-width="1.6" marker-end="url(#ca-a7)"/>
  <text x="268" y="600" font-family="sans-serif" font-size="11" fill="#8b4513" font-weight="700">L7</text>
  <g transform="translate(40, 685)">
    <text x="0" y="0" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e">Loops:</text>
    <rect x="55" y="-10" width="12" height="12" fill="#e74c3c"/><text x="71" y="0" font-family="sans-serif" font-size="11" fill="#1a1a2e">L1 atrophy</text>
    <rect x="170" y="-10" width="12" height="12" fill="#e67e22"/><text x="186" y="0" font-family="sans-serif" font-size="11" fill="#1a1a2e">L2 review bottleneck</text>
    <rect x="325" y="-10" width="12" height="12" fill="#27ae60"/><text x="341" y="0" font-family="sans-serif" font-size="11" fill="#1a1a2e">L3 tacit decay</text>
    <rect x="450" y="-10" width="12" height="12" fill="#8e44ad"/><text x="466" y="0" font-family="sans-serif" font-size="11" fill="#1a1a2e">L4 motivation</text>
    <rect x="570" y="-10" width="12" height="12" fill="#d4a017"/><text x="586" y="0" font-family="sans-serif" font-size="11" fill="#1a1a2e">L5 variance</text>
    <rect x="670" y="-10" width="12" height="12" fill="#2980b9"/><text x="686" y="0" font-family="sans-serif" font-size="11" fill="#1a1a2e">L6 F&#8594;M transfer</text>
    <rect x="800" y="-10" width="12" height="12" fill="#8b4513"/><text x="816" y="0" font-family="sans-serif" font-size="11" fill="#1a1a2e">L7 cohort</text>
  </g>
</svg>

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 540" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="br-t br-d">
  <title id="br-t">The seven loops and the two brake regimes</title>
  <desc id="br-d">Seven horizontal rows, one per loop in the cascade. Each row has three cells: the loop identity on the left, the formal brake available inside the Engagement Model in the middle, and the agentic brake available across the Value, People, and Competency surfaces on the right. Row colors match the cascade loops L1 through L7. A footer note states that the scaling claim is visible in the asymmetry: same mechanism, different surface, different brake.</desc>
  <text x="90" y="30" font-family="sans-serif" font-size="13" font-weight="700" fill="#1a1a2e" text-anchor="middle">Loop</text>
  <text x="345" y="30" font-family="sans-serif" font-size="13" font-weight="700" fill="#1a1a2e" text-anchor="middle">Engagement Model: formal brake</text>
  <text x="705" y="30" font-family="sans-serif" font-size="13" font-weight="700" fill="#1a1a2e" text-anchor="middle">V / P / C surfaces: agentic brake</text>
  <line x1="20" y1="42" x2="880" y2="42" stroke="#999" stroke-width="1"/>
  <rect x="20" y="55" width="140" height="55" fill="#e74c3c" fill-opacity="0.08" stroke="#e74c3c" stroke-width="1.2" rx="4"/>
  <text x="90" y="77" font-family="sans-serif" font-size="11" font-weight="700" fill="#e74c3c" text-anchor="middle">L1</text>
  <text x="90" y="93" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Atrophy,</text>
  <text x="90" y="106" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">epistemic corruption</text>
  <rect x="170" y="55" width="350" height="55" fill="none" stroke="#3a86ff" stroke-width="1" rx="4"/>
  <text x="345" y="78" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Validators, traceability, rationale fields on ADRs</text>
  <text x="345" y="96" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">preserves the cognitive walk at the artifact layer</text>
  <rect x="530" y="55" width="350" height="55" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-dasharray="4 3" rx="4"/>
  <text x="705" y="78" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Governance-reviewer subagent; ADLC stage coach</text>
  <text x="705" y="96" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">detects; does not prevent</text>
  <rect x="20" y="120" width="140" height="55" fill="#e67e22" fill-opacity="0.08" stroke="#e67e22" stroke-width="1.2" rx="4"/>
  <text x="90" y="142" font-family="sans-serif" font-size="11" font-weight="700" fill="#e67e22" text-anchor="middle">L2</text>
  <text x="90" y="158" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Review bottleneck,</text>
  <text x="90" y="171" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">governance overload</text>
  <rect x="170" y="120" width="350" height="55" fill="none" stroke="#3a86ff" stroke-width="1" rx="4"/>
  <text x="345" y="143" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Packet assembly, freshness sweeps, waiver expansion</text>
  <text x="345" y="161" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">reserves human attention for substance that requires it</text>
  <rect x="530" y="120" width="350" height="55" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-dasharray="4 3" rx="4"/>
  <text x="705" y="143" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Culture diagnostic; community-health observer</text>
  <text x="705" y="161" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">surfaces signals only humans can interpret</text>
  <rect x="20" y="185" width="140" height="55" fill="#27ae60" fill-opacity="0.08" stroke="#27ae60" stroke-width="1.2" rx="4"/>
  <text x="90" y="207" font-family="sans-serif" font-size="11" font-weight="700" fill="#27ae60" text-anchor="middle">L3</text>
  <text x="90" y="223" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Shared work declines,</text>
  <text x="90" y="236" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">tacit knowledge decays</text>
  <rect x="170" y="185" width="350" height="55" fill="none" stroke="#3a86ff" stroke-width="1" rx="4"/>
  <text x="345" y="208" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Audit trail on senior-junior shared work</text>
  <text x="345" y="226" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">distinguishes work actually shared from work asserted</text>
  <rect x="530" y="185" width="350" height="55" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-dasharray="4 3" rx="4"/>
  <text x="705" y="208" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Mentor-as-AI-backstage; shared-work surfacing</text>
  <text x="705" y="226" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">AI-excluded category on mentor judgment</text>
  <rect x="20" y="250" width="140" height="55" fill="#8e44ad" fill-opacity="0.08" stroke="#8e44ad" stroke-width="1.2" rx="4"/>
  <text x="90" y="272" font-family="sans-serif" font-size="11" font-weight="700" fill="#8e44ad" text-anchor="middle">L4</text>
  <text x="90" y="288" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Motivation decays,</text>
  <text x="90" y="301" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">FORCE drags down</text>
  <rect x="170" y="250" width="350" height="55" fill="none" stroke="#3a86ff" stroke-width="1" rx="4"/>
  <text x="345" y="273" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">AI-strong-with-human-signature pattern</text>
  <text x="345" y="291" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">authorship remains the architect's work</text>
  <rect x="530" y="250" width="350" height="55" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-dasharray="4 3" rx="4"/>
  <text x="705" y="273" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Studio-mirror role discipline</text>
  <text x="705" y="291" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">categorical exclusions on judgment work</text>
  <rect x="20" y="315" width="140" height="55" fill="#d4a017" fill-opacity="0.08" stroke="#d4a017" stroke-width="1.2" rx="4"/>
  <text x="90" y="337" font-family="sans-serif" font-size="11" font-weight="700" fill="#d4a017" text-anchor="middle">L5</text>
  <text x="90" y="353" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Variance amplifier,</text>
  <text x="90" y="366" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">talent concentration</text>
  <rect x="170" y="315" width="350" height="55" fill="none" stroke="#3a86ff" stroke-width="1" rx="4"/>
  <text x="345" y="338" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">AI-strong draft-and-review; assemble-and-present</text>
  <text x="345" y="356" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Associates author with assistance, not operate a tool</text>
  <rect x="530" y="315" width="350" height="55" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-dasharray="4 3" rx="4"/>
  <text x="705" y="338" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Competency-coverage features; band on-ramps</text>
  <text x="705" y="356" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">surface single-points-of-failure before they fire</text>
  <rect x="20" y="380" width="140" height="55" fill="#2980b9" fill-opacity="0.08" stroke="#2980b9" stroke-width="1.2" rx="4"/>
  <text x="90" y="402" font-family="sans-serif" font-size="11" font-weight="700" fill="#2980b9" text-anchor="middle">L6</text>
  <text x="90" y="418" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">F&#8594;M transfer,</text>
  <text x="90" y="431" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">signal degradation</text>
  <rect x="170" y="380" width="350" height="55" fill="none" stroke="#3a86ff" stroke-width="1" rx="4"/>
  <text x="345" y="403" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Knowledge Layer with attributed retrieval</text>
  <text x="345" y="421" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">every claim is traceable to its source</text>
  <rect x="530" y="380" width="350" height="55" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-dasharray="4 3" rx="4"/>
  <text x="705" y="403" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Substance-preserved corpus (Global Corp)</text>
  <text x="705" y="421" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">deliberate, attributed, controlled F&#8594;M transfer</text>
  <rect x="20" y="445" width="140" height="55" fill="#8b4513" fill-opacity="0.08" stroke="#8b4513" stroke-width="1.2" rx="4"/>
  <text x="90" y="467" font-family="sans-serif" font-size="11" font-weight="700" fill="#8b4513" text-anchor="middle">L7</text>
  <text x="90" y="483" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Cohort discontinuity,</text>
  <text x="90" y="496" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">reduced absorption</text>
  <rect x="170" y="445" width="350" height="55" fill="none" stroke="#3a86ff" stroke-width="1" rx="4"/>
  <text x="345" y="468" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Audit trail on CITA progression signals</text>
  <text x="345" y="486" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">mentor signature attests to FORCE, not to artifact</text>
  <rect x="530" y="445" width="350" height="55" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-dasharray="4 3" rx="4"/>
  <text x="705" y="468" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Apprenticeship-preservation mechanisms</text>
  <text x="705" y="486" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">protect the channels that still exist</text>
  <line x1="20" y1="515" x2="880" y2="515" stroke="#999" stroke-width="1"/>
  <text x="450" y="532" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">Same mechanism, different surface, different brake. The scaling claim is visible in the asymmetry.</text>
</svg>

---

## The decision bottleneck and the architectural moats

### The Creation/Evaluation inversion, architecturally specific

The framework's Eq. 7 makes a structural point about throughput after the multiplier: creation collapses, evaluation holds or rises, the bottleneck flips. Eq. 20 generalizes it one level further: with amplified execution, decision speed becomes the binding constraint on total output. The opportunity cost of indecision (Eq. 21) scales with the multiplier itself; every hour spent deliberating about what to build wastes M times more potential output than it did before.

Architecture practice sits precisely at the binding constraint. Architecture is, in the primary-source framing the BTABoK Manifesto and the Engagement Model material supply, the discipline that produces strategic decisions about systems: what to build, what to retire, what to integrate, what to govern, what to permit, what to constrain. The Architecture Development Life Cycle is in its structure a decision-sequencing process across six stages (Innovation Cycle, Strategy, Planning, Transformation, Utilize and Measure, Decommissioning, per `architecture_lifecycle.md`). The architecturally significant decision is the named artifact BTABoK calls "the stuff that matters" (`decisions.md`). Architecture's institutional review bodies are the forums for adjudicating those decisions.

What the framework predicts for the profession is therefore load-bearing for the firm. As execution capacity expands under the multiplier, the firm's throughput is bounded by its decision rate, and the decision rate is in substantial part the architecture practice's output. The architecture practice that was a cost center supporting engineering becomes the practice that determines whether the firm has competitive throughput at all.

### The three moats under the multiplier

The framework's Eq. 22 decomposes competitive advantage into three types under LLM amplification, each responding differently to the multiplier.

*Execution moats* (speed, volume, feature density) depend on surface-layer FORCE. Surface-layer FORCE is where the effective multiplier is near-total (Eq. 1a). Execution moats therefore commoditize. Firms that built their advantage on "we ship faster" or "we have more engineers" watch that advantage evaporate as the multiplier gives their competitors the same shipping speed. The execution moat is a surface-layer moat, and the surface is what the tool absorbs first.

*Judgment moats* (architectural taste, system-design judgment, evaluation capability, integration foresight) depend on middle and deep FORCE. These are the layers where the multiplier's effective substitution rate is partial to near-zero. Judgment moats therefore survive. More than survive: they are amplified. Eq. 22 says advantage scales with the FORCE differential times M, so a judgment gap that was worth x pre-LLM is worth M · x post-LLM. The firm with architectural judgment-density advantage compounds it faster than the firm without.

*Decision-speed moats* (how quickly and accurately the firm decides what to build) were rarely the binding constraint pre-LLM because execution was slow enough to absorb indecision. Post-LLM, every hour of indecision wastes M-amplified execution capacity. The firm that decides in a day what its competitor debates for a week captures a week's worth of multiplied execution; the gap compounds with each decision cycle.

Enterprise architecture sits at the intersection of the second and third moats. It is the discipline through which the firm builds judgment moat (architectural taste, system-design judgment, integration foresight, accumulated over a managed career path) and through which the firm operationalizes decision-speed moat (faster, better-grounded architectural decisions, supported by the Engagement Model's decision structure). For an enterprise navigating the LLM-amplified competitive environment, architecture practice is no longer cost-center overhead. It is the practice that determines whether the firm has any durable moat at all.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 380" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="mt-t mt-d">
  <title id="mt-t">The three moats under the multiplier</title>
  <desc id="mt-d">Two side-by-side panels. Left panel, pre-LLM: three bars of roughly equal height represent the three moats: execution, judgment, and decision-speed. Right panel, post-LLM: execution has collapsed to near zero and is labeled commoditized; judgment has expanded by factor M; decision-speed is shown as a rising staircase of successive decision cycles, each taller than the previous, annotated as compounding per cycle. A footer line states that enterprise architecture sits at the intersection of the second and third moats.</desc>
  <defs>
    <marker id="mt-arr" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#3a86ff"/></marker>
  </defs>
  <text x="220" y="30" font-family="sans-serif" font-size="14" font-weight="700" fill="#1a1a2e" text-anchor="middle">Pre-LLM</text>
  <text x="670" y="30" font-family="sans-serif" font-size="14" font-weight="700" fill="#1a1a2e" text-anchor="middle">Post-LLM</text>
  <line x1="420" y1="50" x2="420" y2="320" stroke="#ccc" stroke-width="1"/>
  <text x="220" y="105" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Three moats of comparable depth.</text>
  <text x="220" y="120" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Execution dominated as a source of advantage.</text>
  <line x1="50" y1="290" x2="400" y2="290" stroke="#1a1a2e" stroke-width="1.2"/>
  <rect x="80" y="140" width="70" height="150" fill="#3a86ff" fill-opacity="0.25" stroke="#3a86ff" stroke-width="1.2"/>
  <text x="115" y="310" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Execution</text>
  <rect x="185" y="135" width="70" height="155" fill="#3a86ff" fill-opacity="0.25" stroke="#3a86ff" stroke-width="1.2"/>
  <text x="220" y="310" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Judgment</text>
  <rect x="290" y="145" width="70" height="145" fill="#3a86ff" fill-opacity="0.25" stroke="#3a86ff" stroke-width="1.2"/>
  <text x="325" y="310" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Decision-speed</text>
  <line x1="440" y1="290" x2="880" y2="290" stroke="#1a1a2e" stroke-width="1.2"/>
  <rect x="460" y="270" width="70" height="20" fill="#d62828" fill-opacity="0.25" stroke="#d62828" stroke-width="1.2"/>
  <text x="495" y="310" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Execution</text>
  <text x="495" y="325" font-family="sans-serif" font-size="9" font-style="italic" fill="#d62828" text-anchor="middle">commoditized</text>
  <text x="495" y="255" font-family="sans-serif" font-size="10" font-style="italic" fill="#d62828" text-anchor="middle">Eq. 1a: surface layer</text>
  <text x="495" y="243" font-family="sans-serif" font-size="10" font-style="italic" fill="#d62828" text-anchor="middle">substituted</text>
  <rect x="565" y="75" width="70" height="215" fill="#3a86ff" fill-opacity="0.35" stroke="#3a86ff" stroke-width="1.5"/>
  <text x="600" y="310" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Judgment</text>
  <text x="600" y="325" font-family="sans-serif" font-size="9" font-style="italic" fill="#3a86ff" text-anchor="middle">&#215; M (Eq. 22)</text>
  <line x1="600" y1="140" x2="600" y2="85" stroke="#3a86ff" stroke-width="1.4" marker-end="url(#mt-arr)"/>
  <text x="600" y="60" font-family="sans-serif" font-size="10" font-style="italic" fill="#3a86ff" text-anchor="middle">FORCE differential &#215; M</text>
  <rect x="670" y="260" width="32" height="30" fill="#3a86ff" fill-opacity="0.2" stroke="#3a86ff" stroke-width="1"/>
  <text x="686" y="278" font-family="sans-serif" font-size="8" fill="#1a1a2e" text-anchor="middle">c1</text>
  <rect x="708" y="235" width="32" height="55" fill="#3a86ff" fill-opacity="0.3" stroke="#3a86ff" stroke-width="1"/>
  <text x="724" y="265" font-family="sans-serif" font-size="8" fill="#1a1a2e" text-anchor="middle">c2</text>
  <rect x="746" y="200" width="32" height="90" fill="#3a86ff" fill-opacity="0.4" stroke="#3a86ff" stroke-width="1"/>
  <text x="762" y="250" font-family="sans-serif" font-size="8" fill="#1a1a2e" text-anchor="middle">c3</text>
  <rect x="784" y="150" width="32" height="140" fill="#3a86ff" fill-opacity="0.5" stroke="#3a86ff" stroke-width="1"/>
  <text x="800" y="225" font-family="sans-serif" font-size="8" fill="#1a1a2e" text-anchor="middle">c4</text>
  <rect x="822" y="90" width="32" height="200" fill="#3a86ff" fill-opacity="0.6" stroke="#3a86ff" stroke-width="1"/>
  <text x="838" y="195" font-family="sans-serif" font-size="8" fill="#1a1a2e" text-anchor="middle">c5</text>
  <text x="762" y="310" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Decision-speed</text>
  <text x="762" y="325" font-family="sans-serif" font-size="9" font-style="italic" fill="#3a86ff" text-anchor="middle">compounds per decision cycle</text>
  <text x="762" y="70" font-family="sans-serif" font-size="10" font-style="italic" fill="#3a86ff" text-anchor="middle">Eq. 20, 21</text>
  <line x1="20" y1="345" x2="880" y2="345" stroke="#999" stroke-width="1"/>
  <text x="450" y="365" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">Enterprise architecture sits at the intersection of the judgment and decision-speed moats.</text>
</svg>

### ASAP Studio's investment follows the constraint

ASAP Studio's heaviest Engagement-Model investment (decision scribe, governance reviewer subagent, review-packet assembly, Decision Bias Calibrator invocation, PR-flow integration, ADLC stage coach) is ASAP Studio organizing around the firm's new binding constraint. The investment is not arbitrary feature density. It is architecture-specifically what the Creation/Evaluation inversion and the decision bottleneck jointly require. Governance mechanics (packet assembly, freshness sweeps, waiver-chain expansion, agenda preparation) are delegable because their substance multiplier is reliably high. Decision-making itself is not delegable, and ASAP Studio refuses to delegate it, for reasons Eqs. 14 and 22 jointly make load-bearing: automating the decision would accelerate the atrophy dynamic exactly where the firm can least afford it, and would erode the judgment moat the firm's competitive position depends on.

---

## The variance amplifier inside an architecture team

Loop 5 named the variance-amplification dynamic at the general level. This section treats it inside a single architecture practice, because the operational consequences are distinct from the market-level consequences Loop 5 covered.

A team composed of one Distinguished, two Professionals, three Associates, and four Foundationals, a shape not uncommon in enterprise architecture practices, distributes FORCE log-normally across a ten-practitioner team. Pre-LLM, the output distribution roughly mirrored the FORCE distribution; the Distinguished produced the highest-value artifacts, the Foundationals produced the lowest, and the middle filled the middle. Platform deployment under uniform licensing (the default procurement posture) amplifies the variance as the framework predicts, with a specifically within-team consequence: the Distinguished's output grows faster than the Foundational's on absolute terms, but the Foundational's output also grows (per the floor-raising finding the framework's Eq. 15a handles at introduction), which masks the widening gap during the first quarter or two.

By the second year, the gap is visible in three specific ways. First, the review queue skews: the Distinguished's artifacts clear faster because her substance-dense prompts produce substance-dense artifacts that pass governance with fewer revisions. Second, the stakeholder allocation skews: business sponsors learn which architect produces the fastest high-quality output and route their requests accordingly. Third, the CITA progression skews: mentor sign-off requires demonstrated substantive contribution, and the demonstrable Foundational contributions are fewer because the Distinguished's platform-amplified output is absorbing the shared-work vehicle that would have produced them. The within-team gap widens not because the Foundationals are failing but because the variance amplifier has restructured the throughput of the team in ways the career-path trajectory cannot absorb.

The three-way resource competition the framework's Eq. 28 formalizes falls hardest on the Distinguished. She is needed for building (where the multiplier's return on her FORCE is highest), for reviewing (where she is the only practitioner who can reliably separate substance from presentation at speed), and for teaching the model (whether deliberately through retrieval curation and fine-tuning or inadvertently through every interaction). Each hour she spends on one is an hour not spent on the others. The ROI paradox of Eq. 17 says rational allocation concentrates ASAP Studio on her; the evaluation-bottleneck paradox of Eq. 7a says the same allocation needs her in review; the F→M transfer of Eq. 28 says she is also the training-data source of highest quality. Organizations cannot have all three simultaneously, and the framework makes no pretense that ASAP Studio can either.

ASAP Studio softens but cannot eliminate the concentration. The competency-coverage features surface where the talent concentration is creating single-points-of-failure; the band structure provides differentiated on-ramps so that Associates can contribute meaningfully through AI-strong patterns without pretending to the Distinguished's judgment; the knowledge-layer captures what can be captured of the Distinguished's explicit reasoning without pretending to capture what cannot (Eq. 27's ceiling on F→M transfer). The brake is partial. The Distinguished remains the bottleneck; ASAP Studio makes her bottleneck-ness legible and reserves her for the work only she can do.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 470" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="tp-t tp-d">
  <title id="tp-t">The ten-practitioner architecture team under variance amplification</title>
  <desc id="tp-d">Two side-by-side panels showing an architecture team of one Distinguished, two Professionals, three Associates, and four Foundationals. Left panel, pre-LLM: the ten practitioners form a pyramid, each contributing proportionally to throughput, with mentoring arrows flowing down the tiers. Right panel, post-LLM year two and beyond: the Distinguished's effective multiplier expands with a visual halo; a review-queue box on the left of the panel feeds arrows pointing to the Distinguished; the Foundational tier's demonstrable-contribution channel is shaded as narrowed; mentoring arrows between tiers are thinner and dashed. Footer names Eq. 28's three-way resource competition landing on the Distinguished.</desc>
  <defs>
    <marker id="tp-arr-b" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#3a86ff"/></marker>
    <marker id="tp-arr-r" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#d62828"/></marker>
    <marker id="tp-arr" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#1a1a2e"/></marker>
  </defs>
  <text x="210" y="30" font-family="sans-serif" font-size="14" font-weight="700" fill="#1a1a2e" text-anchor="middle">Pre-LLM</text>
  <text x="680" y="30" font-family="sans-serif" font-size="14" font-weight="700" fill="#1a1a2e" text-anchor="middle">Post-LLM (year 2 and beyond)</text>
  <line x1="440" y1="50" x2="440" y2="355" stroke="#ccc" stroke-width="1"/>
  <rect x="180" y="60" width="90" height="36" fill="none" stroke="#1a1a2e" stroke-width="1.4" rx="4"/>
  <text x="225" y="82" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Distinguished</text>
  <rect x="130" y="110" width="84" height="34" fill="none" stroke="#1a1a2e" stroke-width="1.2" rx="4"/>
  <text x="172" y="131" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Professional</text>
  <rect x="230" y="110" width="84" height="34" fill="none" stroke="#1a1a2e" stroke-width="1.2" rx="4"/>
  <text x="272" y="131" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Professional</text>
  <rect x="80" y="158" width="80" height="32" fill="none" stroke="#1a1a2e" stroke-width="1.1" rx="4"/>
  <text x="120" y="178" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Associate</text>
  <rect x="180" y="158" width="80" height="32" fill="none" stroke="#1a1a2e" stroke-width="1.1" rx="4"/>
  <text x="220" y="178" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Associate</text>
  <rect x="280" y="158" width="80" height="32" fill="none" stroke="#1a1a2e" stroke-width="1.1" rx="4"/>
  <text x="320" y="178" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Associate</text>
  <rect x="40" y="205" width="80" height="30" fill="none" stroke="#1a1a2e" stroke-width="1" rx="4"/>
  <text x="80" y="224" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Foundational</text>
  <rect x="130" y="205" width="80" height="30" fill="none" stroke="#1a1a2e" stroke-width="1" rx="4"/>
  <text x="170" y="224" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Foundational</text>
  <rect x="220" y="205" width="80" height="30" fill="none" stroke="#1a1a2e" stroke-width="1" rx="4"/>
  <text x="260" y="224" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Foundational</text>
  <rect x="310" y="205" width="80" height="30" fill="none" stroke="#1a1a2e" stroke-width="1" rx="4"/>
  <text x="350" y="224" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Foundational</text>
  <line x1="225" y1="96" x2="200" y2="108" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <line x1="225" y1="96" x2="248" y2="108" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <line x1="172" y1="144" x2="140" y2="156" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <line x1="172" y1="144" x2="210" y2="156" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <line x1="272" y1="144" x2="240" y2="156" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <line x1="272" y1="144" x2="310" y2="156" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <line x1="120" y1="190" x2="90" y2="203" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <line x1="120" y1="190" x2="150" y2="203" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <line x1="220" y1="190" x2="200" y2="203" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <line x1="220" y1="190" x2="260" y2="203" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <line x1="320" y1="190" x2="330" y2="203" stroke="#3a86ff" stroke-width="1" marker-end="url(#tp-arr-b)"/>
  <rect x="395" y="70" width="28" height="165" fill="#3a86ff" fill-opacity="0.15" stroke="#3a86ff" stroke-width="1" rx="3"/>
  <text x="409" y="155" font-family="sans-serif" font-size="9" fill="#1a1a2e" text-anchor="middle" transform="rotate(-90 409 155)">Throughput</text>
  <text x="210" y="260" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Output distribution mirrors the FORCE distribution.</text>
  <text x="210" y="275" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">All ten contribute; mentoring flows down the tiers.</text>
  <circle cx="695" cy="80" r="38" fill="#d4a017" fill-opacity="0.15" stroke="#d4a017" stroke-width="1" stroke-dasharray="3 2"/>
  <rect x="650" y="60" width="90" height="36" fill="none" stroke="#1a1a2e" stroke-width="1.4" rx="4"/>
  <text x="695" y="82" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Distinguished</text>
  <text x="695" y="130" font-family="sans-serif" font-size="9" font-style="italic" fill="#d4a017" text-anchor="middle">effective multiplier compounds</text>
  <rect x="600" y="145" width="84" height="34" fill="none" stroke="#1a1a2e" stroke-width="1.2" rx="4"/>
  <text x="642" y="166" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Professional</text>
  <rect x="700" y="145" width="84" height="34" fill="none" stroke="#1a1a2e" stroke-width="1.2" rx="4"/>
  <text x="742" y="166" font-family="sans-serif" font-size="11" fill="#1a1a2e" text-anchor="middle">Professional</text>
  <rect x="550" y="190" width="80" height="32" fill="none" stroke="#1a1a2e" stroke-width="1" rx="4"/>
  <text x="590" y="210" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Associate</text>
  <rect x="650" y="190" width="80" height="32" fill="none" stroke="#1a1a2e" stroke-width="1" rx="4"/>
  <text x="690" y="210" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Associate</text>
  <rect x="750" y="190" width="80" height="32" fill="none" stroke="#1a1a2e" stroke-width="1" rx="4"/>
  <text x="790" y="210" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Associate</text>
  <rect x="500" y="233" width="370" height="35" fill="#d62828" fill-opacity="0.06" stroke="none"/>
  <rect x="510" y="237" width="80" height="28" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-opacity="0.4" rx="4"/>
  <text x="550" y="255" font-family="sans-serif" font-size="10" fill="#1a1a2e" fill-opacity="0.5" text-anchor="middle">Foundational</text>
  <rect x="600" y="237" width="80" height="28" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-opacity="0.4" rx="4"/>
  <text x="640" y="255" font-family="sans-serif" font-size="10" fill="#1a1a2e" fill-opacity="0.5" text-anchor="middle">Foundational</text>
  <rect x="690" y="237" width="80" height="28" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-opacity="0.4" rx="4"/>
  <text x="730" y="255" font-family="sans-serif" font-size="10" fill="#1a1a2e" fill-opacity="0.5" text-anchor="middle">Foundational</text>
  <rect x="780" y="237" width="80" height="28" fill="none" stroke="#1a1a2e" stroke-width="1" stroke-opacity="0.4" rx="4"/>
  <text x="820" y="255" font-family="sans-serif" font-size="10" fill="#1a1a2e" fill-opacity="0.5" text-anchor="middle">Foundational</text>
  <text x="680" y="283" font-family="sans-serif" font-size="9" font-style="italic" fill="#d62828" text-anchor="middle">demonstrable-contribution channel narrows</text>
  <line x1="695" y1="96" x2="670" y2="143" stroke="#3a86ff" stroke-width="0.8" stroke-dasharray="3 2" marker-end="url(#tp-arr-b)"/>
  <line x1="695" y1="96" x2="720" y2="143" stroke="#3a86ff" stroke-width="0.8" stroke-dasharray="3 2" marker-end="url(#tp-arr-b)"/>
  <line x1="642" y1="179" x2="610" y2="188" stroke="#3a86ff" stroke-width="0.8" stroke-dasharray="3 2" marker-end="url(#tp-arr-b)"/>
  <line x1="742" y1="179" x2="770" y2="188" stroke="#3a86ff" stroke-width="0.8" stroke-dasharray="3 2" marker-end="url(#tp-arr-b)"/>
  <line x1="590" y1="222" x2="565" y2="235" stroke="#3a86ff" stroke-width="0.6" stroke-dasharray="2 2" marker-end="url(#tp-arr-b)"/>
  <line x1="790" y1="222" x2="810" y2="235" stroke="#3a86ff" stroke-width="0.6" stroke-dasharray="2 2" marker-end="url(#tp-arr-b)"/>
  <rect x="460" y="60" width="70" height="40" fill="none" stroke="#d62828" stroke-width="1.2" rx="4"/>
  <text x="495" y="78" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Review</text>
  <text x="495" y="92" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">queue</text>
  <line x1="532" y1="80" x2="645" y2="80" stroke="#d62828" stroke-width="1.4" marker-end="url(#tp-arr-r)"/>
  <text x="588" y="72" font-family="sans-serif" font-size="9" font-style="italic" fill="#d62828" text-anchor="middle">scarce evaluation capacity</text>
  <text x="680" y="310" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Distinguished's effective multiplier grows faster;</text>
  <text x="680" y="325" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">review bandwidth concentrates on her;</text>
  <text x="680" y="340" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">mentor-through-shared-work channels thin.</text>
  <line x1="20" y1="380" x2="880" y2="380" stroke="#999" stroke-width="1"/>
  <text x="450" y="402" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">Eq. 28's three-way resource competition (building, reviewing, teaching the model) lands on the Distinguished.</text>
  <text x="450" y="419" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">ASAP Studio softens the concentration; it does not eliminate it.</text>
</svg>

---

## The legibility crisis and Goodhart's trap

### The signal collapse on architectural assessment

The framework's Eq. 18 establishes the legibility crisis: as the presentation projection grows, the signal-to-noise ratio on capability assessment collapses, because the presentation channel renders all output at comparable fluency regardless of substance. Output-observation ceases to discriminate. The framework's recommendation is to shift assessment from output inspection to process observation.

Architecture practice is exceptionally exposed. Architectural assessment has historically depended on output observation: the design document, the presentation, the decision record, the whiteboard session's diagram, the interview's architecture walk-through. These are the signals architectural institutions use to evaluate candidates, advance practitioners through CITA levels, select principals, assess extended-team members, and award certifications. Every one of these signals is presentation-shaped, which means every one of these signals is inflated by the presentation channel in roughly equal measure across candidates, across CITA stages, across sectors.

The institutional consequence is that the architectural community loses, progressively, the ability to distinguish the substantive Distinguished from the polished Associate with platform access. The CITA certification boards, the EARB chairs where such bodies exist, the hiring managers, and the extended-team reviewers all face the same problem: their assessment instruments were calibrated for a pre-LLM distribution of output fluency, and they are now calibrated against a world in which fluency is free. The mentor-signed-output requirement the IASA Mentoring Method imposes as a condition of career-path progression was the profession's structural defense against this dynamic. The mentor signature was calibrated against a world in which the mentee could not produce credible artifacts without the FORCE the sign-off was attesting to. In the new world, the mentee can produce the artifact; the mentor must attest to the FORCE, without the artifact being the evidence it used to be. The instrument has not failed; the calibration has.

### Goodhart's trap on the response

The framework's Eq. 19 anticipates the response. Once the institution recognizes the legibility crisis and reaches for a better measure (live whiteboard sessions, architectural interviews under time pressure, structured CITA board reviews), the same presentation channel becomes available to every candidate preparing for that measure. The measure becomes a target, and the target is gameable.

In architecture practice this will manifest specifically. Architects will use LLMs to prepare for CITA board interviews, to rehearse architectural walkthroughs, to polish decision-cascade presentations, to simulate architectural sophistication on demand. The LLM becomes simultaneously the thing that makes architectural FORCE economically decisive (per the decision bottleneck and moat arguments above), the thing that makes architectural FORCE hard to measure (via the legibility crisis), and the tool candidates use to game the measurement. Certification boards that add live-challenge components to their rubrics will find the boards' own preparation materials feeding back into LLM training corpora, which further feeds the gaming. There is no simple measurement fix. Eq. 19 says the gaming room scales with the presentation projection itself: the more capable the model becomes, the more measurement-space there is to inflate.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 460" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="as-t as-d">
  <title id="as-t">Architectural assessment signals under the legibility crisis</title>
  <desc id="as-d">A 2D plane with substance discrimination on the horizontal axis and presentation inflation on the vertical axis. The top-left quadrant, high presentation with low substance discrimination, is shaded as the gameable zone. The bottom-right quadrant, high substance discrimination with low presentation inflation, is marked as the genuine signal region. Five architectural assessment signals are plotted: design document, decision record, interview walk-through, whiteboard session, and mentor-signed output. Each signal has a pre-LLM position and a post-LLM position connected by an arrow showing the drift. The mentor-signed-output signal is highlighted as the only instrument that remains close to the genuine-signal corner after the drift, though its calibration is slipping. A footer notes that Goodhart's trap extends the drift as institutions calibrate against new measures.</desc>
  <defs>
    <marker id="as-arr" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#d62828"/></marker>
    <marker id="as-arr-b" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#3a86ff"/></marker>
  </defs>
  <rect x="120" y="60" width="620" height="300" fill="none" stroke="#1a1a2e" stroke-width="1.3"/>
  <rect x="120" y="60" width="310" height="150" fill="#d62828" fill-opacity="0.06" stroke="none"/>
  <text x="275" y="130" font-family="sans-serif" font-size="13" font-weight="700" fill="#d62828" fill-opacity="0.5" text-anchor="middle">GAMEABLE</text>
  <text x="275" y="150" font-family="sans-serif" font-size="11" fill="#d62828" fill-opacity="0.7" text-anchor="middle">high presentation,</text>
  <text x="275" y="164" font-family="sans-serif" font-size="11" fill="#d62828" fill-opacity="0.7" text-anchor="middle">low substance signal</text>
  <rect x="430" y="210" width="310" height="150" fill="#3a86ff" fill-opacity="0.06" stroke="none"/>
  <text x="585" y="295" font-family="sans-serif" font-size="13" font-weight="700" fill="#3a86ff" fill-opacity="0.5" text-anchor="middle">GENUINE</text>
  <text x="585" y="315" font-family="sans-serif" font-size="11" fill="#3a86ff" fill-opacity="0.7" text-anchor="middle">low presentation inflation,</text>
  <text x="585" y="329" font-family="sans-serif" font-size="11" fill="#3a86ff" fill-opacity="0.7" text-anchor="middle">high substance signal</text>
  <line x1="120" y1="210" x2="740" y2="210" stroke="#aaa" stroke-width="0.6" stroke-dasharray="2 3"/>
  <line x1="430" y1="60" x2="430" y2="360" stroke="#aaa" stroke-width="0.6" stroke-dasharray="2 3"/>
  <text x="430" y="385" font-family="sans-serif" font-size="12" fill="#1a1a2e" text-anchor="middle">Substance discrimination &#8594;</text>
  <text x="60" y="210" font-family="sans-serif" font-size="12" fill="#1a1a2e" text-anchor="middle" transform="rotate(-90 60 210)">Presentation inflation &#8594;</text>
  <circle cx="570" cy="190" r="5" fill="white" stroke="#1a1a2e" stroke-width="1.4"/>
  <text x="578" y="194" font-family="sans-serif" font-size="10" fill="#555" text-anchor="start">Design document</text>
  <path d="M 566 190 L 254 114" stroke="#d62828" stroke-width="1" stroke-dasharray="3 2" marker-end="url(#as-arr)"/>
  <circle cx="250" cy="110" r="5" fill="#d62828"/>
  <circle cx="595" cy="170" r="5" fill="white" stroke="#1a1a2e" stroke-width="1.4"/>
  <text x="603" y="173" font-family="sans-serif" font-size="10" fill="#555" text-anchor="start">Decision record (ADR)</text>
  <path d="M 591 170 L 279 104" stroke="#d62828" stroke-width="1" stroke-dasharray="3 2" marker-end="url(#as-arr)"/>
  <circle cx="275" cy="100" r="5" fill="#d62828"/>
  <circle cx="625" cy="220" r="5" fill="white" stroke="#1a1a2e" stroke-width="1.4"/>
  <text x="633" y="224" font-family="sans-serif" font-size="10" fill="#555" text-anchor="start">Interview walk-through</text>
  <path d="M 621 220 L 354 149" stroke="#d62828" stroke-width="1" stroke-dasharray="3 2" marker-end="url(#as-arr)"/>
  <circle cx="350" cy="145" r="5" fill="#d62828"/>
  <circle cx="640" cy="260" r="5" fill="white" stroke="#1a1a2e" stroke-width="1.4"/>
  <text x="648" y="263" font-family="sans-serif" font-size="10" fill="#555" text-anchor="start">Whiteboard session</text>
  <path d="M 636 260 L 384 174" stroke="#d62828" stroke-width="1" stroke-dasharray="3 2" marker-end="url(#as-arr)"/>
  <circle cx="380" cy="170" r="5" fill="#d62828"/>
  <circle cx="680" cy="300" r="5" fill="white" stroke="#3a86ff" stroke-width="1.8"/>
  <text x="688" y="303" font-family="sans-serif" font-size="10" font-weight="700" fill="#3a86ff" text-anchor="start">Mentor-signed output</text>
  <path d="M 676 300 L 604 262" stroke="#3a86ff" stroke-width="1.2" marker-end="url(#as-arr-b)"/>
  <circle cx="600" cy="260" r="5" fill="#3a86ff"/>
  <text x="595" y="250" font-family="sans-serif" font-size="9" font-style="italic" fill="#3a86ff" text-anchor="end">calibration slipping</text>
  <g transform="translate(120, 395)">
    <circle cx="0" cy="0" r="5" fill="white" stroke="#1a1a2e" stroke-width="1.4"/>
    <text x="10" y="3" font-family="sans-serif" font-size="10" fill="#1a1a2e">Pre-LLM position</text>
    <circle cx="140" cy="0" r="5" fill="#d62828"/>
    <text x="150" y="3" font-family="sans-serif" font-size="10" fill="#1a1a2e">Post-LLM position</text>
    <line x1="290" y1="0" x2="320" y2="0" stroke="#d62828" stroke-width="1" stroke-dasharray="3 2"/>
    <text x="325" y="3" font-family="sans-serif" font-size="10" fill="#1a1a2e">drift under the presentation channel</text>
  </g>
  <line x1="20" y1="422" x2="880" y2="422" stroke="#999" stroke-width="1"/>
  <text x="450" y="442" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">Goodhart's trap extends the drift as institutions calibrate against new measures; the mentor-signed-output instrument is the only one whose defense was structural, not metric-based.</text>
</svg>

### The audit trail as a structural response

ASAP Studio's response is structural rather than metric-based. Every AI-vs-human attribution at ASAP Studio's point of use is process observation captured at source. The audit trail records which work was the practitioner's, which was the tool's, and which was the tool's with practitioner signature. The institution can read this trail across time and detect the pattern: a practitioner whose audit trail shows consistent substantive contribution is credible; a practitioner whose audit trail shows assembly and signature without authorship is not. The audit trail does not measure FORCE directly. It makes the gameable presentation channel structurally separable from the FORCE the institution needs to assess.

This is how the scaling claim cashes out empirically. The audit trail covers all four working models ASAP Studio treats: Engagement-Model artifact production, Value-Model strategic work, People-Model mentoring and rotation, Competency-Model self-assessment and peer review. Across the four, the legibility crisis operates as the framework predicts, Goodhart's trap operates as the framework predicts, and ASAP Studio's process-observation response applies uniformly with only parameter change per FORCE-form. If the predictions hold across four qualitatively distinct domains of architectural work, the framework has passed a scaling test on this dimension. If they fail in one, we learn which parameter is not portable and where the scaling claim breaks.

---

## Sovereignty at two scales

### Enterprise-scale sovereignty

The framework's Eqs. 24 and 24a formalize the resilience test: a workforce's expected capability is FORCE times M discounted by the probability of access, and the resilience test is whether the workforce can function when M is unavailable. A workforce that has atrophied while relying on the multiplier fails the resilience test at exactly the moment it matters, when access is withdrawn or degrades.

The enterprise architectural form of this test has its own specificity. When an enterprise's architects have atrophied while relying on LLM-mediated artifact production, the resilience test fires on three distinct events: when the LLM service becomes unavailable, when the model's behavior changes materially between releases, and when the required domain coverage shifts outside the training distribution. In any of these events, the enterprise discovers whether its architectural capacity was owned or rented. Rented capacity cannot adjudicate architectural significance under novel conditions; it cannot produce decision records whose reasoning is substantive when the reasoning must extend beyond the training distribution; it cannot reconcile cross-sector integrations the model did not see. The enterprise whose architectural capacity was rented fails its own resilience test in ways that are hard to detect before they matter.

ASAP Studio's substance-channel discipline is, at the enterprise level, a sovereignty defense. The audit trail gives the enterprise an objective record of where its architectural FORCE actually lives, distinct from the artifacts the LLM produced. Competency-coverage features surface atrophy before it becomes structural. The human-in-the-loop bands preserve the work that builds deep FORCE (mentor judgment, novel decision adjudication, principle authorship under real conflict) as work the enterprise's architects actually do, not as work the tool does for them. None of this fully insures against service degradation or access change. It preserves the domestic capacity the enterprise will need if either event fires.

### Profession-scale sovereignty

At the profession level, the sovereignty problem has three distinct channels the framework names, each with an architecture-specific form.

*Access dependency*. Architecture practice today depends on LLM services provided by a small number of commercial entities subject to geopolitical, regulatory, and commercial pressures. Architectural-practice access to these services is not a given. A nation or sector that has outsourced its architectural throughput to foreign-provided models faces the same access risk the framework names generally, with the additional property that architectural capacity rebuilds on a mentoring-paced timescale (years at minimum, a career at the deep layer) rather than on a hiring timescale.

*Training-priority dependency*. Eq. 3 says that provider training investment determines which domains the multiplier reflects well. IASA BTABoK is not a top-priority training domain for any major commercial LLM provider; investment is concentrated in domains with broader commercial applications (general technical prose, standard software engineering, customer support, marketing content). The mirror reflects BTABoK-specific architectural concerns, sector-specific regulatory architectures, and niche integration patterns materially worse than it reflects general technical material. Architects who drift toward what the mirror reflects well drift away from the specialized depth their profession and their sectors require. This is the conformity pressure the framework names as a testable prediction, and it has an architecture-specific shape: pressure away from deep sector architecture and toward generic framework material.

*Talent-formation dependency*. Eq. 32 is the deepest of the three. A profession whose developmental conditions have been absorbed by the multiplier produces, cohort by cohort, practitioners whose ceiling is lower than their predecessors'. Rebuilding takes a generation at minimum; in professions where mentoring is the primary transmission channel (architecture alongside medicine, law, and accounting), rebuilding requires senior practitioners whose own FORCE has been preserved, which requires the three-way resource competition of Eq. 28 to be resolved in favor of mentor availability. This resolution is expensive for any single firm and has the commons structure the framework's FORCE-as-Commons analysis names.

### The substance-preserved corpus

The framework distinguishes supply-side and demand-side dynamics in the FORCE-as-Commons question. The supply side is competitive: LLM providers have strong incentive to maintain training signal quality because signal quality is a direct commercial differentiator. For architecture specifically, this supply-side pressure operates weakly, because architecture is not a top-priority training corpus, and because high-FORCE architects are a thin stratum the providers cannot easily acquire in quantity. The demand-side problem is acute: each firm that allows its architects to atrophy contributes marginally to a degradation no single firm bears. No single actor has sufficient incentive to maintain workforce FORCE for the sake of the commons.

The substance-preserved corpus is the architectural profession's demand-side intervention. Deliberately maintained architectural exemplars where the substance channel was disciplined, Global Corp is the paper's worked example, treated in Part Three, serve three functions. First, they give the profession citable counter-evidence to the generally degrading corpus. Second, they give the next generation of architects reference material whose quality has been preserved rather than absorbed. Third, they give enterprises a substrate against which their own audit-trailed work can be compared, surfacing where their practice has drifted from the discipline's preserved exemplars. ASAP Studio endorses this F→M transfer directly, because it is the only F→M transfer that is deliberate, attributed, and controlled. Every other transfer is the tacit absorption happening by default, which the framework's Eq. 31 says degrades the training signal over time.

This is the scope at which architecture practice's long-run trajectory is set. The three regimes the framework's terminal-dynamics analysis distinguishes (virtuous, managed decline, collapse spiral) apply to architecture with specific architectural forms Part Three will name. The window to act is finite. The clock is the retirement curve of the pre-LLM cohort that carries the deep layer, and it is already running.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 460" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="sv-t sv-d">
  <title id="sv-t">Sovereignty at two scales</title>
  <desc id="sv-d">Two side-by-side panels. Left panel, enterprise scale: an enterprise architectural-capacity box divided into an owned lobe and a rented lobe; three trigger arrows point at the box from above, labeled service unavailable, model behavior changes materially, and work shifts out-of-distribution; two outcomes below the box show owned capacity adjudicating under novel conditions and rented capacity failing detection before it matters. Right panel, profession scale: three vertical dependency columns (access, training-priority, talent-formation) with their recovery timescales (hiring-scale months, provider-negotiation years, career-scale a generation). A strip below the columns names the substance-preserved corpus exemplar, Global Corp, as the demand-side intervention. A footer line states that the enterprise fires on events while the profession rebuilds on a career.</desc>
  <defs>
    <marker id="sv-arr" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#3a86ff"/></marker>
    <marker id="sv-arr-r" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#d62828"/></marker>
  </defs>
  <text x="220" y="30" font-family="sans-serif" font-size="14" font-weight="700" fill="#1a1a2e" text-anchor="middle">Enterprise scale</text>
  <text x="680" y="30" font-family="sans-serif" font-size="14" font-weight="700" fill="#1a1a2e" text-anchor="middle">Profession scale</text>
  <line x1="440" y1="50" x2="440" y2="370" stroke="#ccc" stroke-width="1"/>
  <text x="100" y="68" font-family="sans-serif" font-size="10" fill="#d62828" text-anchor="middle">Service</text>
  <text x="100" y="80" font-family="sans-serif" font-size="10" fill="#d62828" text-anchor="middle">unavailable</text>
  <line x1="100" y1="90" x2="155" y2="150" stroke="#d62828" stroke-width="1.3" marker-end="url(#sv-arr-r)"/>
  <text x="215" y="68" font-family="sans-serif" font-size="10" fill="#d62828" text-anchor="middle">Model behavior</text>
  <text x="215" y="80" font-family="sans-serif" font-size="10" fill="#d62828" text-anchor="middle">changes materially</text>
  <line x1="215" y1="90" x2="215" y2="150" stroke="#d62828" stroke-width="1.3" marker-end="url(#sv-arr-r)"/>
  <text x="335" y="68" font-family="sans-serif" font-size="10" fill="#d62828" text-anchor="middle">Work shifts</text>
  <text x="335" y="80" font-family="sans-serif" font-size="10" fill="#d62828" text-anchor="middle">out-of-distribution</text>
  <line x1="335" y1="90" x2="275" y2="150" stroke="#d62828" stroke-width="1.3" marker-end="url(#sv-arr-r)"/>
  <rect x="80" y="155" width="280" height="80" fill="none" stroke="#1a1a2e" stroke-width="1.5" rx="6"/>
  <text x="220" y="176" font-family="sans-serif" font-size="12" font-weight="700" fill="#1a1a2e" text-anchor="middle">Enterprise architectural capacity</text>
  <line x1="220" y1="185" x2="220" y2="235" stroke="#1a1a2e" stroke-width="1" stroke-dasharray="3 2"/>
  <rect x="82" y="192" width="136" height="41" fill="#3a86ff" fill-opacity="0.1" stroke="none"/>
  <text x="150" y="210" font-family="sans-serif" font-size="11" font-weight="600" fill="#3a86ff" text-anchor="middle">Owned</text>
  <text x="150" y="225" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">(FORCE preserved)</text>
  <rect x="222" y="192" width="136" height="41" fill="#d62828" fill-opacity="0.1" stroke="none"/>
  <text x="290" y="210" font-family="sans-serif" font-size="11" font-weight="600" fill="#d62828" text-anchor="middle">Rented</text>
  <text x="290" y="225" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">(tool-mediated)</text>
  <line x1="150" y1="235" x2="150" y2="260" stroke="#3a86ff" stroke-width="1.4" marker-end="url(#sv-arr)"/>
  <rect x="60" y="262" width="180" height="50" fill="none" stroke="#3a86ff" stroke-width="1.3" rx="5"/>
  <text x="150" y="283" font-family="sans-serif" font-size="11" font-weight="600" fill="#1a1a2e" text-anchor="middle">Adjudicates</text>
  <text x="150" y="300" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">under novel conditions</text>
  <line x1="290" y1="235" x2="290" y2="260" stroke="#d62828" stroke-width="1.4" marker-end="url(#sv-arr-r)"/>
  <rect x="200" y="262" width="180" height="50" fill="none" stroke="#d62828" stroke-width="1.3" rx="5"/>
  <text x="290" y="283" font-family="sans-serif" font-size="11" font-weight="600" fill="#1a1a2e" text-anchor="middle">Fails detection</text>
  <text x="290" y="300" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">before it matters</text>
  <text x="220" y="335" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Eq. 24's resilience test fires event-by-event.</text>
  <text x="220" y="350" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">The audit trail records where the capacity actually lives.</text>
  <rect x="480" y="60" width="110" height="200" fill="none" stroke="#1a1a2e" stroke-width="1.2" rx="5"/>
  <text x="535" y="82" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e" text-anchor="middle">Access</text>
  <text x="535" y="97" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">dependency</text>
  <line x1="490" y1="108" x2="580" y2="108" stroke="#ccc" stroke-width="1"/>
  <text x="535" y="130" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Commercial</text>
  <text x="535" y="145" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">provider</text>
  <text x="535" y="160" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">concentration</text>
  <rect x="490" y="225" width="90" height="12" fill="#3a86ff" fill-opacity="0.3" stroke="#3a86ff" stroke-width="1"/>
  <text x="535" y="250" font-family="sans-serif" font-size="10" fill="#3a86ff" text-anchor="middle">Hiring-scale</text>
  <text x="535" y="263" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">(months)</text>
  <rect x="605" y="60" width="110" height="200" fill="none" stroke="#1a1a2e" stroke-width="1.2" rx="5"/>
  <text x="660" y="82" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e" text-anchor="middle">Training-priority</text>
  <text x="660" y="97" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">dependency</text>
  <line x1="615" y1="108" x2="705" y2="108" stroke="#ccc" stroke-width="1"/>
  <text x="660" y="130" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">BTABoK is not</text>
  <text x="660" y="145" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">a top-priority</text>
  <text x="660" y="160" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">training corpus</text>
  <rect x="615" y="215" width="90" height="22" fill="#d4a017" fill-opacity="0.3" stroke="#d4a017" stroke-width="1"/>
  <text x="660" y="250" font-family="sans-serif" font-size="10" fill="#d4a017" text-anchor="middle">Provider-negotiation</text>
  <text x="660" y="263" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">(years)</text>
  <rect x="730" y="60" width="130" height="200" fill="none" stroke="#1a1a2e" stroke-width="1.2" rx="5"/>
  <text x="795" y="82" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e" text-anchor="middle">Talent-formation</text>
  <text x="795" y="97" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">dependency</text>
  <line x1="740" y1="108" x2="850" y2="108" stroke="#ccc" stroke-width="1"/>
  <text x="795" y="130" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Mentoring pipeline,</text>
  <text x="795" y="145" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">cohort discontinuity,</text>
  <text x="795" y="160" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">deep-layer rebuild</text>
  <rect x="740" y="190" width="110" height="47" fill="#d62828" fill-opacity="0.3" stroke="#d62828" stroke-width="1"/>
  <text x="795" y="250" font-family="sans-serif" font-size="10" fill="#d62828" text-anchor="middle">Career-scale</text>
  <text x="795" y="263" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">(a generation)</text>
  <rect x="480" y="285" width="380" height="50" fill="#3a86ff" fill-opacity="0.08" stroke="#3a86ff" stroke-width="1.2" rx="5"/>
  <text x="670" y="305" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e" text-anchor="middle">Substance-preserved corpus: Global Corp exemplar</text>
  <text x="670" y="323" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">demand-side intervention: deliberate, attributed, controlled F&#8594;M transfer</text>
  <line x1="20" y1="395" x2="880" y2="395" stroke="#999" stroke-width="1"/>
  <text x="450" y="415" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">Different scales, different clocks. The enterprise fires on events; the profession rebuilds on a career.</text>
  <text x="450" y="432" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">The pre-LLM cohort's retirement curve is the timeline the profession is racing.</text>
</svg>

---

Part Three derives the amplification architecture from the commitments Part One named and the ramifications Part Two worked out: the authority gradient from the Variable Multiplier, the AI-suitability bands and safeguard patterns from the atrophy equation per FORCE-form, the asymmetric model coverage from the Variable Multiplier's shape across working surfaces, the ten primitives and six-wave delivery from the practitioner-lifecycle analysis, the stop-lines from the tacit-knowledge, hysteresis, legibility, and meaning loops operating jointly. Global Corp is the bench against which the derivation is tested. The four trajectories the architecture profession may inhabit close the paper.
