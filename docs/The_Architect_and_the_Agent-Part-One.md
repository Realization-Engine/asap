---
title: "The Architect and the Agent, Part One: The Architect Under Amplification"
subtitle: "A companion whitepaper to The Multiplier and the Mirror, on the architect's practice under LLM amplification and the amplification architecture the Multiplier-Mirror framework requires."
author: "Dennis A. Landi"
version: "0.01"
date: "2026-04-21"
category: "Whitepaper"
folio: "Nº IV, Part One of Three"
project: "ASAP"
source: "https://github.com/Realization-Engine/asap"
prev-url: "The_Architect_and_the_Agent.html"
prev-title: "Introduction"
next-url: "The_Architect_and_the_Agent-Part-Two.html"
next-title: "Part Two, Ramifications in Architecture Practice"
---

# Part One - The Architect Under Amplification

## Where this fits

*Mirror* (Folio Nº I) names the Mirror as a cognitive feedback loop and stands upstream of the formal apparatus the rest of the program develops. *The Multiplier and the Mirror* (Folio Nº II) formalizes the Mirror as a structured object and establishes the **Multiplier-Mirror framework**, the general theory of human capability under large-language-model amplification. Output is written as $O = M \times F$, where $M$ is the Multiplier the model applies and $F$ is the practitioner's composite capability, called FORCE throughout. The paper's worked example is software engineering. Its scope note is explicit: any profession in which apprenticeship passes tacit knowledge through shared execution can be substituted for the engineer.

The Enquiry Into Specification as Meaningful Struggle is the framework's first substitution. It asks, for the software engineer specifically, whether specification work can carry the $\alpha \cdot S$ term (productive struggle) that implementation work historically carried, now that the Multiplier has absorbed most of implementation. It answers within one profession, at one load-bearing medium, and names SpecChat as the specification artifact through which the substitution becomes operable.

The enterprise architect is a second substitution, and a more demanding one, because the architect's work is not a single medium but a working surface. The architect authors decisions, runs stakeholder engagements, prepares governance packets, drafts business cases, maintains principles, reviews transition architectures, coaches extended-team practitioners, tracks technical debt, and demonstrates competency for certification. Each activity is a separable instance of the atrophy equation's $\alpha \cdot S$ term, operating at its own cadence, through its own artifacts, governed by its own institutional review channels. A defense that preserves FORCE at one medium but leaves the others exposed is a defense against one of the atrophy dynamics the framework identifies, not against the whole.

A further observation deserves naming at the outset. *The Multiplier and the Mirror* and the Enquiry both stayed inside the Engagement Model of BTABoK by construction. The parent paper's worked example, software engineering, treats implementation and specification as the practitioner's primary output; both are Engagement-Model artifact classes. Enquiry narrows further inside the Engagement Model to the specification medium and names SpecChat as the authored-commitment artifact the medium requires. Both papers are inside-view treatments of one working model, with the framework's general consequences examined against a single instantiation.

This paper is the first zoom-out. Now that one worked example exists at Engagement-Model scale, Global Corp, a BTABoK-aligned enterprise specification running under the SpecChat BTABOK profile, the framework's reach can be tested across the rest of architectural practice. Value, where investment prioritization and benefits realization live. People, where mentoring pipelines and community health live. Competency, where the developmental trajectory lives. These are not artifact-production domains in the Engagement-Model sense. They are sites where the practicing architect does work against a cadence with FORCE at stake, and where no formal medium underlies the work the way SpecChat underlies the Engagement Model.

The zoom-out is the paper's method. What the zoom-out tests is whether the framework scales. The parent paper writes its equations in general form but supports them with one Engagement-flavored instantiation. Enquiry narrows further inside that instantiation. This paper is the first in the series in which the framework's equations face qualitatively distinct work types: artifact production, strategic reasoning, relational work, developmental work. If Eq. 11 (atrophy), Eq. 12b (shared-work decline), Eq. 14 (tipping point), Eq. 18 (legibility crisis), and the rest apply without structural modification across those four working models, with only their coefficients changing per FORCE-form, the framework has passed a scaling test it had not yet faced. The scaling claim is what the zoom-out demonstrates. It is what makes the framework general rather than theme-specific. And it is what this paper's amplification architecture, through its coverage, its asymmetry, and its audit trail, is arranged to expose to empirical examination.

This paper is the framework's instantiation for enterprise architecture practice, and the derivation of the amplification architecture that instantiation requires. The software that implements it is ASAP Studio, and the paper introduces it the way the Enquiry introduces SpecChat: as the engineering artifact through which the derivation becomes operable.

---

## Architecture as a calendrical practice

A common description of the practicing architect is a day-in-the-life sketch: a morning of stakeholder conversations, an afternoon drawing diagrams, an evening reviewing decisions. The sketch is not wrong, but it locates the work in the wrong temporal unit. The practicing architect's work is not organized by the day. It is organized by the calendar.

Consider the cadences BTABoK specifies directly. Rapid Value Management organizes three indicator tiers by time horizon: early validation indicators register impact within the first ninety days of an initiative, ideally within thirty; leading indicators register within ninety-one days to one year; lagging indicators measure end-success. The Value Map that holds those indicators is updated at a minimum every two weeks, and every investment is validated against its indicators at least once a month. Architecturally significant decisions arrive on their own schedule and are recorded on arrival; the governance bodies that review them convene on cadences each practice sets. Mentoring engagement cycles run three-to-six-month assignments for Foundation and Associate architects within longer two-to-three-year trajectories, and one-to-three-year relationships (or longer) for Professional and Distinguished. Principles are maintained as a small set, eight to twelve memorable statements, with an update process the practice defines. The Technical Debt Ratio formalizes technical-debt measurement as (Remediation + Maintenance) over Development, times one hundred, with portfolios assessed on a periodic basis rather than on a prescribed calendar.

An amplification architecture layers additional operational cadences on top of these primary ones: weekly or biweekly scorecard refreshes against declared metrics, quarterly portfolio sweeps, annual cycles tied to funding allocation and certification maintenance, freshness sweeps against artifact service-level commitments, review-body convocations at per-practice intervals. These operational cadences are not BTABoK's own claims. They are ASAP Studio's operationalizations of the cadences BTABoK names, chosen to match the work's calendrical shape at each horizon. Part Three derives the specific ASAP Studio schedules and names their primary-source grounding where one exists.

The architect does not sit down each morning and choose from these. They arrive, each at its own interval, from its own triggering condition. A practicing architect's week is better described as the set of cadences intersecting it than as a sequence of tasks selected from a list.

This matters for the framework's gaze. The atrophy equation contests four pressures on FORCE: struggle-based growth, deliberate-engagement growth, passive-reliance decay, and organizational de-investment. In architecture practice, each cadence is a separable encounter with the tool, and each has its own balance of those four pressures. An architect whose business-case drafting becomes LLM-mediated experiences the passive-reliance decay term in the strategic-FORCE dimension. An architect whose mentoring rhythm becomes LLM-mediated experiences the tacit-knowledge transmission collapse the framework's Eq. 12b formalizes. An architect whose review-body packet preparation becomes LLM-mediated may experience the reverse: mechanical packet assembly shifts to the tool, freeing the architect to hold substance the tool cannot produce. The calendar is the surface on which the tipping-point dynamic plays out. Not the day.

Two consequences follow. The first is that any platform supporting the architect under amplification must operate against the calendar, because the work does. Per-interaction tooling addresses the interaction but misses the cadence in which the atrophy happens. The second is that the calendar is also the discipline's natural measurement surface. An architect's trajectory toward or away from the tipping point is visible not in any single artifact but in the pattern of cadence work across months and quarters. The audit-trail proposition that appears in Part Three follows from this structural fact.

---

## The Collapse of Execution in architecture

The Enquiry names what happens when the language model absorbs the mechanical work that historically carried the software engineer's $\alpha \cdot S$ term. Implementation effort was the governor. Typing code took time. The time was thinking time. The synapse-encoding happened there. When the governor is removed, output rises while FORCE atrophies unless a different source of productive struggle is found.

The dynamic generalizes. In architecture practice the governor was not typing code; it was typing prose and drawing diagrams. Drafting an architecturally significant decision forced the architect to walk the cognitive path the decision described: the options considered, the trade-offs surfaced, the consequences named, the reversibility examined. Producing a one-page business case forced the architect through the Needs, Approach, Benefits, and Considerations sequence the body of knowledge calls NABC, each field a separate act of articulation. A viewpoint catalog forced the architect to name which stakeholder concerns the architecture addressed and which it deferred. A transition architecture forced the architect to reason about what had to hold across an intermediate state. The typing-as-governor mechanism operated in architecture with the same force it operated in software, and for the same reason: the artifacts were built through the walking.

The LLM has absorbed that. An architect with the tool can produce in minutes what took hours: a well-structured decision record, a clean business case, a coherent viewpoint, a transition architecture with named baseline, target, and intermediates. The artifacts look correct. They often are correct, for well-structured problems in well-trained domains. The typing-relief is real.

What the typing-relief does not guarantee is that the cognitive walk the typing used to compel still happens. The walk may happen. The walk may not happen. The artifact cannot distinguish. Institutional review channels that consume architectural artifacts, the Enterprise Architecture Review Board, senior-architect sign-off, governance body packets, consume the artifact, not the walk.

A counter-argument is worth sitting with. Field studies of LLM-augmented knowledge workers on well-covered tasks consistently show compression of the performance distribution: the lowest performers improve the most, the spread narrows, the field looks like it is leveling. The framework treats this finding directly. The compression is correct at introduction, on tasks dense in the training distribution. The framework's prediction is different: on tasks at or beyond the model's capability frontier, and over time horizons long enough for FORCE to develop or atrophy, the distribution stretches rather than compresses. Both observations are correct. They measure different things, at different horizons, on different regions of the task frontier.

For architecture practice the split maps cleanly. Canvas drafting, framework recall, standard viewpoint structures, boilerplate business-case sections, and the mechanical components of governance packet assembly are dense in training data and benefit from the compression effect. Novel architectural judgment under ambiguity, integration across previously unconnected concerns, cross-sector transition architectures, and the deep-layer FORCE that distinguishes a senior architect from a polished one are the trajectory regime. The counter-argument captures what is true at introduction. The framework captures what is true over career horizons.

Two structural properties make architecture practice exceptionally exposed. The first is that almost every architectural deliverable is a textual or visual presentation form whose surface fluency the presentation channel produces excellently. The second is that stakeholder consumption is presentation-mediated. Architects are evaluated by how their artifacts read to executive sponsors, governance bodies, and review boards. The institutions that grant authority and funding consume artifacts, not the walks behind them. The presentation channel translates directly into perceived competence, which translates into authority, which translates into career progression. A profession whose authority flows through presentation-shaped artifacts is exposed to the presentation channel's decoupling from substance to an unusual degree.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 400" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="ce-t ce-d">
  <title id="ce-t">The collapse of execution across the ADLC</title>
  <desc id="ce-d">A six by three grid. Columns are the six ADLC stages (Innovation Cycle, Strategy, Planning, Transformation, Utilize and Measure, Decommissioning). Rows are the three FORCE layers: Surface at the top, Middle in the middle, Deep at the bottom. Each cell names the characteristic architectural work at that stage and layer. The Surface row is shaded red to indicate near-full LLM substitution. The Middle row is shaded amber to indicate partial substitution. The Deep row is shaded blue to indicate that the LLM cannot substitute. A footer states that the LLM absorbs the top row fully, the middle row partially, the bottom row barely; the artifact is produced, but the walk the typing used to force may or may not still happen.</desc>
  <text x="192" y="65" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Innovation</text>
  <text x="192" y="78" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Cycle</text>
  <text x="317" y="65" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Strategy</text>
  <text x="442" y="65" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Planning</text>
  <text x="567" y="65" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Transformation</text>
  <text x="692" y="65" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Utilize and</text>
  <text x="692" y="78" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Measure</text>
  <text x="817" y="65" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Decommis-</text>
  <text x="817" y="78" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">sioning</text>
  <rect x="130" y="85" width="750" height="80" fill="#d62828" fill-opacity="0.08" stroke="#d62828" stroke-width="1.2"/>
  <text x="75" y="125" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828" text-anchor="middle">Surface</text>
  <text x="75" y="140" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">LLM sub</text>
  <text x="75" y="152" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">near full</text>
  <line x1="255" y1="85" x2="255" y2="165" stroke="#fff" stroke-width="1"/>
  <line x1="380" y1="85" x2="380" y2="165" stroke="#fff" stroke-width="1"/>
  <line x1="505" y1="85" x2="505" y2="165" stroke="#fff" stroke-width="1"/>
  <line x1="630" y1="85" x2="630" y2="165" stroke="#fff" stroke-width="1"/>
  <line x1="755" y1="85" x2="755" y2="165" stroke="#fff" stroke-width="1"/>
  <text x="192" y="117" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">trend scans,</text>
  <text x="192" y="130" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">corpus retrieval</text>
  <text x="317" y="117" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">framework recall,</text>
  <text x="317" y="130" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">template drafts</text>
  <text x="442" y="117" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">RACI tables,</text>
  <text x="442" y="130" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">standard viewpoints</text>
  <text x="567" y="117" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">migration scripts,</text>
  <text x="567" y="130" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">rollout checklists</text>
  <text x="692" y="117" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">scorecard projection,</text>
  <text x="692" y="130" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">metric pulls</text>
  <text x="817" y="117" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">dependency scans,</text>
  <text x="817" y="130" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">shutdown checklists</text>
  <rect x="130" y="165" width="750" height="80" fill="#d4a017" fill-opacity="0.10" stroke="#d4a017" stroke-width="1.2"/>
  <text x="75" y="205" font-family="sans-serif" font-size="11" font-weight="700" fill="#d4a017" text-anchor="middle">Middle</text>
  <text x="75" y="220" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">LLM sub</text>
  <text x="75" y="232" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">partial</text>
  <line x1="255" y1="165" x2="255" y2="245" stroke="#fff" stroke-width="1"/>
  <line x1="380" y1="165" x2="380" y2="245" stroke="#fff" stroke-width="1"/>
  <line x1="505" y1="165" x2="505" y2="245" stroke="#fff" stroke-width="1"/>
  <line x1="630" y1="165" x2="630" y2="245" stroke="#fff" stroke-width="1"/>
  <line x1="755" y1="165" x2="755" y2="245" stroke="#fff" stroke-width="1"/>
  <text x="192" y="197" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">JTBD articulation,</text>
  <text x="192" y="210" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">opportunity framing</text>
  <text x="317" y="197" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">NABC business case,</text>
  <text x="317" y="210" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">strategic thesis</text>
  <text x="442" y="197" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">ADR drafting,</text>
  <text x="442" y="210" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">transition architecture</text>
  <text x="567" y="197" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">stakeholder coaching,</text>
  <text x="567" y="210" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">exception handling</text>
  <text x="692" y="197" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">benefits realization,</text>
  <text x="692" y="210" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">KPI interpretation</text>
  <text x="817" y="197" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">risk assessment,</text>
  <text x="817" y="210" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">contract unwinding</text>
  <rect x="130" y="245" width="750" height="80" fill="#3a86ff" fill-opacity="0.08" stroke="#3a86ff" stroke-width="1.2"/>
  <text x="75" y="285" font-family="sans-serif" font-size="11" font-weight="700" fill="#3a86ff" text-anchor="middle">Deep</text>
  <text x="75" y="300" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">LLM sub</text>
  <text x="75" y="312" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">near none</text>
  <line x1="255" y1="245" x2="255" y2="325" stroke="#fff" stroke-width="1"/>
  <line x1="380" y1="245" x2="380" y2="325" stroke="#fff" stroke-width="1"/>
  <line x1="505" y1="245" x2="505" y2="325" stroke="#fff" stroke-width="1"/>
  <line x1="630" y1="245" x2="630" y2="325" stroke="#fff" stroke-width="1"/>
  <line x1="755" y1="245" x2="755" y2="325" stroke="#fff" stroke-width="1"/>
  <text x="192" y="277" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">novel architectural</text>
  <text x="192" y="290" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">intuition</text>
  <text x="317" y="277" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">cross-concern</text>
  <text x="317" y="290" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">integration judgment</text>
  <text x="442" y="277" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">architectural-</text>
  <text x="442" y="290" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">significance adjudication</text>
  <text x="567" y="277" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">judgment under</text>
  <text x="567" y="290" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">real-world conflict</text>
  <text x="692" y="277" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">felt sense of</text>
  <text x="692" y="290" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">structural trouble</text>
  <text x="817" y="277" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">legacy reasoning</text>
  <text x="817" y="290" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">from experience</text>
  <line x1="40" y1="355" x2="880" y2="355" stroke="#999" stroke-width="1"/>
  <text x="450" y="375" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">The LLM absorbs the top row fully, the middle row partially, the bottom row barely.</text>
  <text x="450" y="390" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">The artifact is produced. The walk the typing used to force may or may not still happen.</text>
</svg>

---

## The Mirror at two scales

The Mirror in the framework is a cognitive feedback loop between a single user and a single LLM. The substance channel scales with the user's FORCE, projected through a domain-specific amplification. The presentation channel runs broadly high, independent of substance. The epistemic gap between the two channels is the source of the atrophy dynamic's most dangerous failure mode.

Architecture practice exhibits the Mirror at a second scale that the framework has not treated. The architect does not only use the LLM as a reflective surface; the architect is themselves a reflective surface for the enterprise. The architect's core work is to hold a mirror to the organization: to articulate what the enterprise is, what it commits to, which stakeholder concerns it serves, which principles it upholds, which decisions it has made, which architectural bets are in flight. The central artifacts of architecture practice (architecturally significant requirements, decision records, principles, viewpoints, transition architectures, scorecards) are the surface on which the enterprise sees itself.

Under LLM amplification the architect now holds a reflective surface that is itself a reflective surface. The enterprise is reflected to itself through a Mirror whose substance channel may or may not be doing its work, and whose presentation channel runs high in either case. This is the Mirror at two scales.

The two scales couple.

At the individual scale, the dynamics are those the framework formalized. Above the tipping point, the LLM is a studio mirror: a feedback instrument the architect uses to detect discrepancies in her own thinking, calibrate uncertainty, and update control. Below the tipping point, the LLM is Narcissus's pool: a flattering surface whose presentation rendering persuades the architect that she has substance she lacks. This is the Mirror at the individual scale, operating as the framework predicts.

At the enterprise scale, the individual substance discipline propagates outward. When the architect's substance channel is working, the artifacts she produces reflect the enterprise faithfully: a portfolio strategy whose benefits-dependency network actually traces enablers to outcomes, principles that actually encode trade-offs the enterprise has adjudicated, decision records whose options-and-consequences analysis is genuine, viewpoints that name the stakeholder concerns they claim to serve. When the architect's substance channel is attenuated, the artifacts still look correct, because the presentation channel renders them with the same fluency. A vague portfolio strategy reflects back as a polished strategic narrative. A thin governance practice reflects back as a comprehensive register. Underdeveloped principles reflect back as eight memorable rules in confident prose. The enterprise then consumes the reflection and makes decisions on the strength of it.

The coupling is vicious. Institutional reward flows through the presentation channel, because the presentation channel is what institutions can see. Presentation selects for architects whose individual substance discipline is weakest, the ones for whom presentation is most of what they have, because substance is what they never built. Those architects, promoted, run the enterprise Mirror with even less substance discipline than the practitioners they replaced. The enterprise sees itself flattered more completely each cycle. Over time, the decisions the enterprise makes are grounded less in an architecture that was actually thought through and more in an architecture that was rendered fluently.

The equations that govern this are not new. The framework's Eq. 18 (legibility crisis, signal-to-noise collapse driven by $M_p$) and Eq. 19 (Goodhart's trap on any measure the presentation channel can reach) operate at both scales. The individual-scale consequence is misassessment of architects. The enterprise-scale consequence is misassessment of enterprise architectures. The same mechanism; a different object on the receiving end.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 340" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="ma-t ma-d">
  <title id="ma-t">The Mirror at two coupled scales</title>
  <desc id="ma-d">Two coupled reflective loops side by side. The left loop, the individual Mirror, shows the architect and the LLM exchanging substance and presentation signals. The right loop, the enterprise Mirror, shows the architect and the enterprise exchanging the same two channels through architectural artifacts. An arrow across the middle shows that the architect's individual substance discipline propagates into the enterprise loop's substance fidelity. A red dashed arrow below each scale shows the atrophy risk: below the tipping point, the individual Mirror flatters and the enterprise Mirror attenuates.</desc>
  <defs>
    <marker id="ma-arr" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="8" markerHeight="8" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#1a1a2e"/></marker>
    <marker id="ma-arr-b" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="8" markerHeight="8" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#3a86ff"/></marker>
    <marker id="ma-arr-r" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="8" markerHeight="8" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#d62828"/></marker>
  </defs>
  <text x="200" y="24" font-family="sans-serif" font-size="13" font-weight="700" fill="#1a1a2e" text-anchor="middle">Individual Mirror</text>
  <rect x="60" y="60" width="130" height="60" fill="none" stroke="#1a1a2e" stroke-width="1.5" rx="6"/>
  <text x="125" y="85" font-family="sans-serif" font-size="12" fill="#1a1a2e" text-anchor="middle">Architect</text>
  <text x="125" y="105" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">F_arch</text>
  <rect x="250" y="60" width="130" height="60" fill="none" stroke="#1a1a2e" stroke-width="1.5" rx="6"/>
  <text x="315" y="85" font-family="sans-serif" font-size="12" fill="#1a1a2e" text-anchor="middle">LLM</text>
  <text x="315" y="105" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">Mirror object</text>
  <line x1="190" y1="80" x2="250" y2="80" stroke="#3a86ff" stroke-width="1.6" marker-end="url(#ma-arr-b)"/>
  <text x="220" y="72" font-family="sans-serif" font-size="10" fill="#3a86ff" text-anchor="middle">prompt</text>
  <line x1="250" y1="100" x2="190" y2="100" stroke="#1a1a2e" stroke-width="1.6" marker-end="url(#ma-arr)"/>
  <text x="220" y="115" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">M_s + M_p</text>
  <text x="200" y="158" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Substance scales with F_arch</text>
  <text x="200" y="173" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Presentation runs broadly high</text>
  <path d="M 440 80 Q 470 80 500 80" fill="none" stroke="#d62828" stroke-width="2" marker-end="url(#ma-arr-r)"/>
  <text x="470" y="65" font-family="sans-serif" font-size="10" font-style="italic" fill="#d62828" text-anchor="middle">couples</text>
  <text x="470" y="95" font-family="sans-serif" font-size="10" font-style="italic" fill="#d62828" text-anchor="middle">individual &#8594; enterprise</text>
  <text x="700" y="24" font-family="sans-serif" font-size="13" font-weight="700" fill="#1a1a2e" text-anchor="middle">Enterprise Mirror</text>
  <rect x="520" y="60" width="130" height="60" fill="none" stroke="#1a1a2e" stroke-width="1.5" rx="6"/>
  <text x="585" y="85" font-family="sans-serif" font-size="12" fill="#1a1a2e" text-anchor="middle">Architect</text>
  <text x="585" y="105" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">same practitioner</text>
  <rect x="710" y="60" width="130" height="60" fill="none" stroke="#1a1a2e" stroke-width="1.5" rx="6"/>
  <text x="775" y="85" font-family="sans-serif" font-size="12" fill="#1a1a2e" text-anchor="middle">Enterprise</text>
  <text x="775" y="105" font-family="sans-serif" font-size="10" fill="#555" text-anchor="middle">via ASRs, ADRs, views</text>
  <line x1="650" y1="80" x2="710" y2="80" stroke="#3a86ff" stroke-width="1.6" marker-end="url(#ma-arr-b)"/>
  <text x="680" y="72" font-family="sans-serif" font-size="10" fill="#3a86ff" text-anchor="middle">artifacts</text>
  <line x1="710" y1="100" x2="650" y2="100" stroke="#1a1a2e" stroke-width="1.6" marker-end="url(#ma-arr)"/>
  <text x="680" y="115" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">decisions, funding</text>
  <text x="700" y="158" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Substance fidelity inherits F_arch</text>
  <text x="700" y="173" font-family="sans-serif" font-size="10" font-style="italic" fill="#555" text-anchor="middle">Presentation fluency runs high</text>
  <line x1="125" y1="120" x2="125" y2="225" stroke="#d62828" stroke-width="1.3" stroke-dasharray="4 3" marker-end="url(#ma-arr-r)"/>
  <line x1="585" y1="120" x2="585" y2="225" stroke="#d62828" stroke-width="1.3" stroke-dasharray="4 3" marker-end="url(#ma-arr-r)"/>
  <rect x="60" y="230" width="270" height="70" fill="none" stroke="#d62828" stroke-width="1.2" rx="6"/>
  <text x="195" y="252" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828" text-anchor="middle">F_arch below F&#42;</text>
  <text x="195" y="270" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Mirror flatters the architect</text>
  <text x="195" y="286" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Eq. 11 atrophy term dominates</text>
  <rect x="520" y="230" width="270" height="70" fill="none" stroke="#d62828" stroke-width="1.2" rx="6"/>
  <text x="655" y="252" font-family="sans-serif" font-size="11" font-weight="700" fill="#d62828" text-anchor="middle">Enterprise Mirror attenuates</text>
  <text x="655" y="270" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Fluent artifacts, thin substance</text>
  <text x="655" y="286" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="middle">Decisions on flattering reflection</text>
  <text x="450" y="325" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">Individual substance discipline determines enterprise substance fidelity. The two scales couple.</text>
</svg>

One consequence of the two-scale formulation is directional. A defense that improves the architect's individual substance discipline, through feedback, review, mentor oversight, rigorous authoring, improves the enterprise Mirror's fidelity, by the same mechanism. A defense that does not touch individual substance but only polishes the artifact layer worsens the enterprise Mirror's fidelity, by making the presentation-substance decoupling harder to detect. The amplification architecture this paper derives operates at the individual scale, because that is where the enterprise scale is produced.

The two-scale formulation is itself a scaling claim about the Mirror object. The substance/presentation decomposition, and the reflective, presentation, and failure dimensions the framework catalogs, were defined at the individual scale, practitioner engaging the tool. They reappear at the enterprise scale, practitioner engaging the organization through artifacts the tool helped produce, with the same internal structure and only different parameters governing the strength of each channel. If the Mirror dynamics carry across this qualitative discontinuity, tool-mediated reflection to institutionally-mediated reflection, with the equations intact, the Mirror is not an artifact of the tool-user interaction. It is a structural property of reflective systems under LLM amplification. The amplification architecture in Part Three takes this as given, and Part Three's audit trail is the instrument that exposes the enterprise-scale dynamics to observation.

---

## Multi-form FORCE

The framework defines FORCE as a Cobb-Douglas composite of capability components. Any critical component approaching zero collapses the product toward zero. The multiplicative form is a structural claim about capability, not an incidental modeling choice.

The enterprise architect's FORCE admits the same structure, with a specific instantiation drawn from BTABoK.

BTABoK names **five competency pillars** that every architect shares: Business Technology Strategy, Human Dynamics, Design, Quality Attributes, and IT Environment. An architect missing any of these does not have diminished competence; they do not function. An architect without Human Dynamics cannot hold a stakeholder conversation under real conflict, which means no architecturally significant requirement she elicits is grounded in actual concern. An architect without Design cannot articulate views, viewpoints, or trade-offs, which means every decision she logs is a record in form only. An architect without Quality Attributes cannot reason about the systemic properties that make an architecture fit for purpose, which means she cannot adjudicate architectural significance when it arrives. The pillars are mutually necessary. The multiplicative form applies directly.

The pillars are not the whole of architectural FORCE. They are a shared core. **Five lateral specializations** are layered on top, one per deep track: Business, Information, Infrastructure, Software, and Solution. An architect holds the five pillars and a specialization, not the pillars alone. The specializations are additive across architects (a team covers what no individual covers) and multiplicative within any one architect (a Business Architect without the Business specialization's deep competencies is not a Business Architect). The framework's Eq. 2 generalization from single-multiplier to domain-dependent substance amplification maps directly: the specializations are the domains.

FORCE also has temporal structure. The framework distinguishes a surface layer (half-life of months, nearly full LLM substitution), a middle layer (half-life of years, partial substitution, silent decay), and a deep layer (half-life of decades, barely any substitution). The architect's competency progression, the **five proficiency levels** BTABoK takes from Bloom's Taxonomy and maps to Iasa certifications, overlays this temporal structure cleanly. Awareness and Basic correspond to the surface layer: recall of canvas names, framework structure, definitional content, the things the LLM recalls flawlessly. Delivery and Experienced correspond to the middle layer: judgment in context, applying canvases to messy engagements, the things the LLM cannot produce substance for but produces presentation for. Shaping corresponds to the deep layer: structural architectural intuition, the sense of system behavior under novel pressure, the ability to operate in genuine ambiguity. The LLM does not teach this. Direct experience does.

This mapping has a specific consequence for the atrophy equation. The framework's Eq. 11c shows the deep layer's dynamics: growth from struggle, decay from passive reliance, no LLM-assisted compounding term. An architect whose middle-layer work is LLM-mediated can still produce Delivery-and-Experienced-level artifacts indefinitely. An architect whose work is entirely LLM-mediated never reaches Shaping, because the conditions under which Shaping forms are the conditions the LLM smooths away. The cohort discontinuity the framework formalizes in Eq. 32 is not an abstract risk; it is a prediction about which proficiency levels post-LLM cohorts can reach under current institutional design.

BTABoK's certification structure makes the framework's trajectory geometry visible. **Four CITA certifications**, Foundation, Associate, Professional, and Distinguished, recognize attained competence across a practitioner's career. The proficiency-level-to-certification mapping carries an asymmetry: five levels, four certifications. The deepest level, Shaping, is defined in the primary source as "significant industry level competency" recognized through "papers, research and leadership," which positions it as the end of a long career arc rather than a target for point-in-time examination. This certification ladder is the mechanism through which the profession has historically verified its own FORCE. Under the framework's gaze, it is also what the atrophy equation most threatens, because the mechanism by which a Foundation architect becomes an Associate becomes a Professional is precisely the shared senior-junior work the framework's Eq. 12b says the LLM absorbs exponentially in the Multiplier.

One more property of FORCE matters for the architect, and it does not come from the framework directly. An architect's FORCE is simultaneously individual and collective. Team composition, role coverage, community health, mentor availability, extended-team engagement, and governance-body membership are all inputs to what any one architect can actually do. The People Model material in BTABoK is the site where this collective dimension lives. For the concept paper the consequence is that the atrophy dynamic cannot be diagnosed at the individual level alone. A Distinguished Architect whose team has lost its Foundation-to-Associate mentoring pipeline operates above her tipping point individually while the practice around her slides below it collectively, and the collective slide eventually pulls her down through the three-way resource competition the framework's Eq. 28 formalizes: building, reviewing others' LLM-augmented work, and teaching the model.

This is why the amplification architecture derived in Part Three commits to coverage across four working models this paper selects from BTABoK's larger set, the four where cadence work with FORCE at stake happens under LLM amplification: Engagement, where artifact production lives; Value, where the strategic-FORCE cadences live; People, where the collective dimension lives; and Competency, where the developmental trajectory lives. The coverage is derived from the multiplicative structure of FORCE, not from editorial preference for breadth.

The coverage has a second derivation, parallel to the multiplicative one. The parent paper's worked example and Enquiry's companion memorandum both treat Engagement-Model work. Their productive-struggle terms concern implementation effort and specification struggle. Their atrophy pressures concern code quality and artifact precision. Their cohort predictions concern the engineer's developmental trajectory through artifact authoring. The framework's equations are written generally; both prior papers instantiate them inside one working model. This paper is the first zoom-out, and coverage across the four models is what the zoom-out requires to be informative. The framework's equations either apply to Value, People, and Competency work as they apply to Engagement, or they do not. A platform that covers only Engagement cannot answer the question.

A reach-note is warranted. BTABoK names more working models than four. The IASA Get Started overview lists Outcome, Operating, Value, People, Engagement, Competency, and Maturity, surrounded by the Architecture Practice article, the Structured Canvas Approach, and the Topic Areas. This paper does not claim coverage across all of these. Outcome and Operating are macro framings the Engagement Model instantiates; they are not sites where the practicing architect does cadence work with FORCE at stake in the ordinary sense. Maturity is a measurement frame that runs across the others. Topic Areas are explicitly shallow by BTABoK's own design. The four working models this paper covers are the ones where the architect does work against a cadence with FORCE at stake, which is the condition under which the framework's atrophy dynamics apply. The zoom-out is one-of-many to four-of-many, selected by where the framework's equations have operative consequences.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 480" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="cd-t cd-d">
  <title id="cd-t">Multi-form FORCE for the architect</title>
  <desc id="cd-d">A multiplicative composition diagram. At the top, the Cobb-Douglas formula states that the architect's FORCE is the product of five shared competency pillars and one specialization. Five pillar boxes span the upper row: Business Technology Strategy, Human Dynamics, Design, Quality Attributes, and IT Environment. A central composite node marked F-arch sits between the rows. Five lateral specialization boxes span the lower row in BIISS order: Business, Information, Infrastructure, Software, Solution. Each component carries a small LLM-substitution bar. Red indicates near-full substitution at the surface layer, amber indicates partial substitution at the middle layer, blue indicates near-zero substitution at the deep layer. Faint converging lines show all components feeding into the F-arch composite. A footer states that any component near zero collapses the product; specializations are additive across a team but multiplicative within any one architect.</desc>
  <rect x="40" y="30" width="820" height="45" fill="#1a1a2e" fill-opacity="0.05" stroke="#1a1a2e" stroke-width="1" rx="4"/>
  <text x="450" y="54" font-family="serif" font-size="14" font-style="italic" fill="#1a1a2e" text-anchor="middle">F_arch = (BTS &#183; HD &#183; Des &#183; QA &#183; ITE) &#215; Specialization_j</text>
  <text x="450" y="70" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">Cobb-Douglas: every component enters multiplicatively; any component near zero collapses the product</text>
  <text x="450" y="100" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e" text-anchor="middle">Five shared competency pillars (every architect holds all five)</text>
  <rect x="30" y="110" width="155" height="75" fill="#d4a017" fill-opacity="0.1" stroke="#d4a017" stroke-width="1.3" rx="4"/>
  <text x="107" y="130" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Business Technology</text>
  <text x="107" y="143" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Strategy</text>
  <text x="107" y="160" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">middle-to-deep</text>
  <rect x="45" y="170" width="124" height="6" fill="#d4a017" fill-opacity="0.5"/>
  <text x="107" y="182" font-family="sans-serif" font-size="8" fill="#d4a017" text-anchor="middle">partial substitution</text>
  <rect x="195" y="110" width="155" height="75" fill="#3a86ff" fill-opacity="0.1" stroke="#3a86ff" stroke-width="1.3" rx="4"/>
  <text x="272" y="130" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Human Dynamics</text>
  <text x="272" y="147" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">deep / relational</text>
  <text x="272" y="160" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">conflict-bearing</text>
  <rect x="210" y="170" width="31" height="6" fill="#3a86ff" fill-opacity="0.5"/>
  <text x="272" y="182" font-family="sans-serif" font-size="8" fill="#3a86ff" text-anchor="middle">near-zero substitution</text>
  <rect x="360" y="110" width="155" height="75" fill="#d4a017" fill-opacity="0.1" stroke="#d4a017" stroke-width="1.3" rx="4"/>
  <text x="437" y="130" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Design</text>
  <text x="437" y="147" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">views, viewpoints,</text>
  <text x="437" y="160" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">trade-off articulation</text>
  <rect x="375" y="170" width="124" height="6" fill="#d4a017" fill-opacity="0.5"/>
  <text x="437" y="182" font-family="sans-serif" font-size="8" fill="#d4a017" text-anchor="middle">partial substitution</text>
  <rect x="525" y="110" width="155" height="75" fill="#d4a017" fill-opacity="0.1" stroke="#d4a017" stroke-width="1.3" rx="4"/>
  <text x="602" y="130" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Quality Attributes</text>
  <text x="602" y="147" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">systemic properties,</text>
  <text x="602" y="160" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">fitness for purpose</text>
  <rect x="540" y="170" width="124" height="6" fill="#d4a017" fill-opacity="0.5"/>
  <text x="602" y="182" font-family="sans-serif" font-size="8" fill="#d4a017" text-anchor="middle">partial substitution</text>
  <rect x="690" y="110" width="155" height="75" fill="#d62828" fill-opacity="0.08" stroke="#d62828" stroke-width="1.3" rx="4"/>
  <text x="767" y="130" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">IT Environment</text>
  <text x="767" y="147" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">technical knowledge,</text>
  <text x="767" y="160" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">tooling fluency</text>
  <rect x="705" y="170" width="124" height="6" fill="#d62828" fill-opacity="0.5"/>
  <text x="767" y="182" font-family="sans-serif" font-size="8" fill="#d62828" text-anchor="middle">high substitution</text>
  <line x1="107" y1="185" x2="418" y2="248" stroke="#1a1a2e" stroke-width="0.6" opacity="0.4"/>
  <line x1="272" y1="185" x2="432" y2="230" stroke="#1a1a2e" stroke-width="0.6" opacity="0.4"/>
  <line x1="437" y1="185" x2="450" y2="223" stroke="#1a1a2e" stroke-width="0.6" opacity="0.4"/>
  <line x1="602" y1="185" x2="468" y2="230" stroke="#1a1a2e" stroke-width="0.6" opacity="0.4"/>
  <line x1="767" y1="185" x2="482" y2="248" stroke="#1a1a2e" stroke-width="0.6" opacity="0.4"/>
  <circle cx="450" cy="265" r="42" fill="#1a1a2e"/>
  <text x="450" y="262" font-family="serif" font-size="18" font-style="italic" font-weight="700" fill="white" text-anchor="middle">F</text>
  <text x="462" y="268" font-family="serif" font-size="10" font-style="italic" fill="white" text-anchor="start">arch</text>
  <text x="450" y="285" font-family="sans-serif" font-size="8" fill="white" text-anchor="middle">Cobb-Douglas</text>
  <text x="450" y="296" font-family="sans-serif" font-size="8" fill="white" text-anchor="middle">composite</text>
  <line x1="107" y1="350" x2="418" y2="282" stroke="#1a1a2e" stroke-width="0.6" opacity="0.4"/>
  <line x1="272" y1="350" x2="432" y2="300" stroke="#1a1a2e" stroke-width="0.6" opacity="0.4"/>
  <line x1="437" y1="350" x2="450" y2="307" stroke="#1a1a2e" stroke-width="0.6" opacity="0.4"/>
  <line x1="602" y1="350" x2="468" y2="300" stroke="#1a1a2e" stroke-width="0.6" opacity="0.4"/>
  <line x1="767" y1="350" x2="482" y2="282" stroke="#1a1a2e" stroke-width="0.6" opacity="0.4"/>
  <text x="450" y="345" font-family="sans-serif" font-size="11" font-weight="700" fill="#1a1a2e" text-anchor="middle">Five BIISS specializations (one per architect; the team covers all five)</text>
  <rect x="30" y="355" width="155" height="65" fill="#3a86ff" fill-opacity="0.1" stroke="#3a86ff" stroke-width="1.3" rx="4"/>
  <text x="107" y="375" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Business</text>
  <text x="107" y="392" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">domain-relational</text>
  <rect x="45" y="405" width="31" height="6" fill="#3a86ff" fill-opacity="0.5"/>
  <rect x="195" y="355" width="155" height="65" fill="#d4a017" fill-opacity="0.1" stroke="#d4a017" stroke-width="1.3" rx="4"/>
  <text x="272" y="375" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Information</text>
  <text x="272" y="392" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">data / schema</text>
  <rect x="210" y="405" width="124" height="6" fill="#d4a017" fill-opacity="0.5"/>
  <rect x="360" y="355" width="155" height="65" fill="#d4a017" fill-opacity="0.1" stroke="#d4a017" stroke-width="1.3" rx="4"/>
  <text x="437" y="375" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Infrastructure</text>
  <text x="437" y="392" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">platform / topology</text>
  <rect x="375" y="405" width="124" height="6" fill="#d4a017" fill-opacity="0.5"/>
  <rect x="525" y="355" width="155" height="65" fill="#d4a017" fill-opacity="0.1" stroke="#d4a017" stroke-width="1.3" rx="4"/>
  <text x="602" y="375" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Software</text>
  <text x="602" y="392" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">patterns / structure</text>
  <rect x="540" y="405" width="124" height="6" fill="#d4a017" fill-opacity="0.5"/>
  <rect x="690" y="355" width="155" height="65" fill="#d4a017" fill-opacity="0.1" stroke="#d4a017" stroke-width="1.3" rx="4"/>
  <text x="767" y="375" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">Solution</text>
  <text x="767" y="392" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">integration across</text>
  <rect x="705" y="405" width="124" height="6" fill="#d4a017" fill-opacity="0.5"/>
  <g transform="translate(30, 440)">
    <text x="0" y="0" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e">LLM substitution:</text>
    <rect x="110" y="-8" width="12" height="12" fill="#d62828" fill-opacity="0.5"/>
    <text x="126" y="0" font-family="sans-serif" font-size="10" fill="#1a1a2e">high (surface)</text>
    <rect x="225" y="-8" width="12" height="12" fill="#d4a017" fill-opacity="0.5"/>
    <text x="241" y="0" font-family="sans-serif" font-size="10" fill="#1a1a2e">partial (middle)</text>
    <rect x="345" y="-8" width="12" height="12" fill="#3a86ff" fill-opacity="0.5"/>
    <text x="361" y="0" font-family="sans-serif" font-size="10" fill="#1a1a2e">near-zero (deep)</text>
  </g>
  <line x1="40" y1="455" x2="860" y2="455" stroke="#999" stroke-width="1"/>
  <text x="450" y="472" font-family="sans-serif" font-size="10" font-style="italic" fill="#1a1a2e" text-anchor="middle">An architect without any one pillar does not function. Specializations are additive across a team; multiplicative within any one architect.</text>
</svg>

---

## The cohort discontinuity under the CITA ladder

The framework's Eq. 32 establishes that each successive cohort entering a profession under the Multiplier faces a lower FORCE ceiling, not through individual deficiency but through structural reduction of the conditions under which FORCE forms. The proof requires no assumption specific to software. Any profession whose developmental pipeline depends on shared work between seniors and juniors is subject to it.

The enterprise architect's developmental pipeline is such a pipeline. The IASA Mentoring Method, on which the CITA ladder depends, has five operative rules, summarized faithfully from the primary source. Architects cannot progress without reviewed outputs from one or more qualified mentors. Managers are responsible for day-to-day assignments but must ensure opportunity for broad skill development. Mentors and mentees meet regularly. Mentors support delivery of tasks that extend beyond the architect's current skill level, or mentees are given time to work on these tasks with a mentor. Promotion beyond critical milestones must include mentor support and must be documented by the mentor. The rules are structurally dependent on two conditions: shared work of enough substance that mentor review is meaningful, and mentees whose existing FORCE is enough to absorb what is reviewed.

Both conditions are under pressure under the framework.

The shared-work condition is the framework's Eq. 12b directly applied. The volume of work juniors and seniors do together declines exponentially with the Multiplier, because the most delegable work, the high-volume, well-specified, mechanically-executable work that was the traditional vehicle for mentoring through doing, is the work the LLM absorbs first. Mentoring sessions on decision-record drafting, business-case assembly, viewpoint authoring, and canvas population that used to produce reviewable artifacts at a steady cadence now produce either LLM-mediated artifacts, on which the mentor's review is partially a review of the mentee's prompt discipline rather than of their reasoning, or fewer artifacts altogether, because the cadence shifted. The three-to-six-month Foundation-to-Associate assignment was calibrated against a volume of delegable work that is shrinking.

The absorptive-capacity condition is the framework's Eq. 32 applied to the mentee. A mentee who never built implementation-layer FORCE, in the architect's case who never suffered through the pre-LLM act of typing a decision record that is actually hard to write because the thinking is hard, enters the mentoring relationship with less to absorb what the senior is transmitting. The architect mentor can demonstrate the quality of a decision; the architect mentee can watch. Whether the mentee actually encodes what they watched depends on the FORCE they already have. An LLM-prepared mentee is watching the demonstration through the equivalent of a video screen: they see, but the seeing does not do the work.

The break in the mentoring pipeline is therefore bidirectional. Seniors do not share the work they once shared; mentees are less capable of absorbing when they are shared with. The CITA progression timeline, three-to-six months, one-to-three years, multi-year Distinguished, is built into the calendar of the profession. If that calendar is no longer carrying FORCE transmission at the rate it was designed for, the profession produces, at a predictable rate, architects whose CITA status matches an earlier generation's while whose Shaping-layer FORCE does not.

A counter-argument deserves engagement. The LLM is not only an absorber of shared work; it could also serve as an amplifier of mentoring, producing more feedback at lower cost, enabling mentors to support more mentees, surfacing scenarios the mentor would not have surfaced alone. This argument is structurally true. It is the $\gamma \cdot E \cdot F$ term in the framework's Eq. 11 from the start: deliberate engagement compounds FORCE, multiplicatively with existing FORCE, above the tipping point. The counter-argument says the LLM can work this way in mentoring. It can. The framework's claim is that which mode dominates depends on the FORCE the mentee and mentor bring and on the specific discipline of the mentoring practice. Above the tipping point, with mentor and mentee both disciplined, the LLM is a mentoring multiplier. Below the tipping point, the LLM is a mentoring substitute, and the substitution produces artifacts-of-progress without progress.

The CITA ladder's defense against the substitution risk has always been the requirement of mentor-signed demonstrations. That defense was calibrated against a world in which mentees could not produce credible artifacts without the FORCE the ladder required. The defense is not calibrated against a world in which artifacts-without-FORCE are a click away. The ladder requires redesign. Part Three proposes the specific redesign the amplification architecture operationalizes, and states what ASAP Studio will not do because the profession itself must do it.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 440" width="100%" style="max-width:900px;display:block;margin:1.5em auto;" role="img" aria-labelledby="co-t co-d">
  <title id="co-t">Cohort discontinuity under the CITA ladder</title>
  <desc id="co-d">A trajectory chart showing four architect cohorts progressing across the six-level managed career path (Aspiring, Foundational, Associate, Professional, Distinguished, Chief) over four time points. Cohort A, pre-LLM, rises from Associate at time zero to Chief at time three, then retires. Cohort B, entering at time zero, plateaus at Professional. Cohort C, entering at time one, plateaus at Associate. Cohort D, entering at time two, stunts at Foundational. A dashed horizontal band near the top marks the Shaping-layer FORCE boundary that only the pre-LLM cohort attains. A footer states that Eq. 32 predicts each successive cohort's ceiling descends; the clock is Cohort A's retirement curve.</desc>
  <defs>
    <marker id="co-arr" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0,0 L10,5 L0,10 z" fill="#555"/></marker>
  </defs>
  <rect x="130" y="60" width="720" height="290" fill="none" stroke="#1a1a2e" stroke-width="1"/>
  <line x1="130" y1="80" x2="850" y2="80" stroke="#eee" stroke-width="0.8"/>
  <text x="120" y="83" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">Chief</text>
  <line x1="130" y1="130" x2="850" y2="130" stroke="#eee" stroke-width="0.8"/>
  <text x="120" y="133" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">Distinguished</text>
  <line x1="130" y1="180" x2="850" y2="180" stroke="#eee" stroke-width="0.8"/>
  <text x="120" y="183" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">Professional</text>
  <line x1="130" y1="230" x2="850" y2="230" stroke="#eee" stroke-width="0.8"/>
  <text x="120" y="233" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">Associate</text>
  <line x1="130" y1="280" x2="850" y2="280" stroke="#eee" stroke-width="0.8"/>
  <text x="120" y="283" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">Foundational</text>
  <line x1="130" y1="330" x2="850" y2="330" stroke="#eee" stroke-width="0.8"/>
  <text x="120" y="333" font-family="sans-serif" font-size="10" fill="#1a1a2e" text-anchor="end">Aspiring</text>
  <text x="60" y="210" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle" transform="rotate(-90 60 210)">Managed career path</text>
  <text x="200" y="370" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">t = 0</text>
  <text x="200" y="382" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">pre-LLM</text>
  <text x="370" y="370" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">t = 1</text>
  <text x="370" y="382" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">early LLM</text>
  <text x="540" y="370" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">t = 2</text>
  <text x="540" y="382" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">cohort boundary</text>
  <text x="710" y="370" font-family="sans-serif" font-size="10" font-weight="700" fill="#1a1a2e" text-anchor="middle">t = 3</text>
  <text x="710" y="382" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="middle">generational transition</text>
  <rect x="130" y="80" width="720" height="50" fill="#3a86ff" fill-opacity="0.05"/>
  <line x1="130" y1="80" x2="850" y2="80" stroke="#3a86ff" stroke-width="1.3" stroke-dasharray="6 3"/>
  <text x="840" y="100" font-family="sans-serif" font-size="9" font-style="italic" fill="#3a86ff" text-anchor="end">Shaping-layer FORCE boundary</text>
  <text x="840" y="112" font-family="sans-serif" font-size="9" font-style="italic" fill="#3a86ff" text-anchor="end">(deep layer, attained only pre-LLM)</text>
  <path d="M 200 230 L 370 180 L 540 130 L 710 80" fill="none" stroke="#3a86ff" stroke-width="2.5"/>
  <circle cx="200" cy="230" r="4" fill="#3a86ff"/>
  <circle cx="370" cy="180" r="4" fill="#3a86ff"/>
  <circle cx="540" cy="130" r="4" fill="#3a86ff"/>
  <circle cx="710" cy="80" r="4" fill="#3a86ff"/>
  <line x1="710" y1="80" x2="800" y2="80" stroke="#3a86ff" stroke-width="2" stroke-dasharray="4 2"/>
  <line x1="800" y1="80" x2="830" y2="55" stroke="#555" stroke-width="1.3" marker-end="url(#co-arr)"/>
  <text x="835" y="50" font-family="sans-serif" font-size="9" font-style="italic" fill="#555" text-anchor="start">retires</text>
  <text x="210" y="222" font-family="sans-serif" font-size="9" font-weight="700" fill="#3a86ff">A: pre-LLM</text>
  <path d="M 200 330 L 370 280 L 540 230 L 710 180" fill="none" stroke="#d4a017" stroke-width="2" stroke-dasharray="5 2"/>
  <circle cx="200" cy="330" r="3.5" fill="#d4a017"/>
  <circle cx="370" cy="280" r="3.5" fill="#d4a017"/>
  <circle cx="540" cy="230" r="3.5" fill="#d4a017"/>
  <circle cx="710" cy="180" r="3.5" fill="#d4a017"/>
  <text x="720" y="175" font-family="sans-serif" font-size="9" font-weight="700" fill="#d4a017">B: plateau</text>
  <path d="M 370 330 L 540 280 L 710 230" fill="none" stroke="#e67e22" stroke-width="2" stroke-dasharray="5 2"/>
  <circle cx="370" cy="330" r="3.5" fill="#e67e22"/>
  <circle cx="540" cy="280" r="3.5" fill="#e67e22"/>
  <circle cx="710" cy="230" r="3.5" fill="#e67e22"/>
  <text x="720" y="225" font-family="sans-serif" font-size="9" font-weight="700" fill="#e67e22">C: plateau</text>
  <path d="M 540 330 L 710 295" fill="none" stroke="#d62828" stroke-width="2" stroke-dasharray="5 2"/>
  <circle cx="540" cy="330" r="3.5" fill="#d62828"/>
  <circle cx="710" cy="295" r="3.5" fill="#d62828"/>
  <text x="720" y="295" font-family="sans-serif" font-size="9" font-weight="700" fill="#d62828">D: stunted</text>
  <line x1="40" y1="405" x2="860" y2="405" stroke="#999" stroke-width="1"/>
  <text x="450" y="423" font-family="sans-serif" font-size="11" font-style="italic" fill="#1a1a2e" text-anchor="middle">Eq. 32 predicts each successive cohort's FORCE ceiling descends. The clock is Cohort A's retirement curve.</text>
</svg>

The theoretical argument is supply-side, predicting a ceiling descent cohort by cohort. A demand-side observation from the profession's practice literature complements it: BTABoK's primary author (Preiss [5.3]) records that the growth segment of architectural demand sits in small and medium organizations that have not historically had access to architectural expertise and are now making consequential technology decisions without it. The cohort entering the profession under the Multiplier is likely to encounter the amplification architecture in the SMB practice structures Part Two treats under "The SMB-architect," not in Fortune 500 engagements. The CITA ladder's redesign, insofar as it reaches the incoming cohort, reaches them there.

---

## The three commitments

The preceding sections establish four claims about enterprise architecture under LLM amplification. Architecture is calendrical, so interventions must operate against the calendar, not the interaction. The profession is exceptionally exposed to the presentation-substance decoupling, so the defense must assess substance, not presentation. The Mirror operates at two coupled scales, so defenses at the individual scale carry through to the enterprise scale whether the defender intends it or not. FORCE in architecture is multi-form, layered, and simultaneously individual and collective, so any platform that addresses one form while leaving the others exposed induces atrophy in the uncovered forms.

Three commitments follow. They are the operative requirements the amplification architecture in Part Three instantiates. The commitments are derived from the framework; they are not selected for editorial balance, and they are not negotiable against product convenience.

**Commitment 1. Cover the four working models this paper selects from BTABoK's larger set, the four where cadence work with FORCE at stake happens under LLM amplification.** Engagement, where artifact production lives, is the obvious site and already has formal machinery. Value, where strategic-FORCE cadences live (investment prioritization, benefits realization, value-stream mapping, Rapid Value Management), is where the decision bottleneck has its sharpest operational form. People, where the collective dimension lives, is where the mentoring pipeline and community health determine whether the profession can maintain itself at all. Competency, where the developmental trajectory lives, is where the cohort discontinuity either operates or is countered. Some concerns BTABoK tags under its Operating-Model axis (technical-debt management, decision mechanics, lifecycle operations) surface their load-bearing cadences inside these four; ASAP Studio's operational grouping assigns each concern to the working-model surface where its cadence lives, which is an amplification-architecture choice, not a BTABoK categorization. Partial coverage is itself an atrophy pattern: an architect whose Engagement work is well-supported but whose Value, People, and Competency work is unsupported sees the uncovered forms atrophy under daily pressure. The coverage commitment is derived twice: from the multiplicative structure of FORCE, which collapses the product when a critical component approaches zero, and from the zoom-out that makes this paper structurally different from its predecessors. *The Multiplier and the Mirror* and the Enquiry stayed inside the Engagement Model. The test that distinguishes a general framework from a theme-specific one is whether the equations survive application across qualitatively distinct work types. Commitment 1 is therefore also the commitment that makes the scaling claim empirically tractable. A platform covering only the Engagement Model repeats the prior papers' scope; a platform covering all four models is the instrument through which the framework's scaling can be tested in architecture practice.

**Commitment 2. Authority asymmetric to formalizability.** The Variable Multiplier is not a single number. The substance amplification varies across domains and task types; it is reliably high where the work is formalizable, mechanical, and well-trained, and it is unreliably low or negative where the work is novel, judgment-laden, and relational. A platform that applies uniform authority across this distribution is structurally mismatched to the Variable Multiplier. Enforcement is appropriate only where the Multiplier is reliably high; advisory posture is the strongest appropriate posture where the Multiplier is variable or unreliable. In architecture practice the asymmetry maps cleanly to the distinction between the working models. Engagement Model work has a formal medium (SpecChat) with validators and rule-based enforcement. Value, People, and Competency work is tacit and judgment-bearing, with no formal medium underneath. ASAP Studio's authority tiering therefore tracks the framework's Variable Multiplier across architectural work types. The asymmetry is derived.

**Commitment 3. Human-in-the-loop discipline calibrated to atrophy risk per FORCE-form.** The atrophy dynamic operates on FORCE that is exercised, through the compounding term, and degrades what is not, through the passive-reliance term. Different forms of architectural FORCE have different sensitivities and different exposure profiles. Mentor judgment is an atrophy-maximum: the work that builds middle-layer FORCE the most is also the work that atrophies fastest if the LLM substitutes. Mechanical cadence (freshness sweeps, waiver expiry scans, rotation tracking) is atrophy-neutral: the machine can carry it without degrading any FORCE the profession cares to maintain. Decision-record drafting is atrophy-contested: the machine can draft, but the architect must author. Business-case drafting is the same. Each form of architectural work must be classified by the atrophy risk the LLM imposes on the FORCE-form it touches, and ASAP Studio's human-in-the-loop discipline around that work must be calibrated accordingly. Part Three names this with a four-band AI-suitability classification (AI-strong, AI-backstage, AI-proposer, AI-excluded) and seven interaction-pattern safeguards. Each ASAP Studio feature is classified by band and by pattern. Categorical exclusions are encoded as structural properties of feature design, not as runtime rules that could be overridden.

These three commitments are where the framework ends and the amplification architecture begins. They are also where the scaling claim is operationalized. A platform that covers the four working models, tiers authority asymmetrically to formalizability, and calibrates human-in-the-loop discipline per FORCE-form is, among other things, an instrument through which the framework's predictions can be measured in architecture practice. Part Two works out the ramifications of the framework in the architectural domain, using the seven-loop cascade as the structuring device, and shows how each loop produces a specific operational pressure on the profession, visible differently inside the Engagement Model, where it has formal machinery, than in Value, People, and Competency, where it operates agentically. Part Three derives ASAP Studio feature by feature from the commitments, tests the derivation against a worked enterprise, and names the four trajectories the architecture profession may inhabit as the Multiplier grows.
