# The Architect and the Agent

## 1. Where this fits

The Realization Engine investigates how human capability scales through collaborative systems, and how those systems, in turn, reshape the practitioners working inside them. *The Multiplier and the Mirror* set out the general argument. *Enquiry Into Specification as Meaningful Struggle* applied it to software, naming specification as the medium where the human's commitments now live and where AI's realization work must be contained. This document picks up there.

Specification, as the Enquiry argues, is one site of meaningful struggle. The architect's working life has many. Architecture as a profession is not principally the act of authoring a specification; it is the slow, distributed labor of keeping a practice alive across years and across teams. Specifications are one artifact of that labor. Decisions, governance, mentoring, portfolio judgment, scorecard refresh, stakeholder concern mining, and dozens of named cadences are others. Each has its own character, its own rhythm, and its own answer to the question of where AI belongs.

This is the proposition this document defends. The architect's full working surface is well-suited to agentic augmentation, if and only if the augmentation is built with a clear theory of where AI belongs and where it does not. The theory is the contribution. The platform is the instantiation.

The platform is called the Architect Support Agentic Platform, abbreviated ASAP. The full design lives in a separate working document. A worked example of the practitioner environment ASAP supports, a fictional BTABoK-complete enterprise called Global Corp, lives alongside the SpecChat documentation. This document introduces the concept and names its constraints. The rest follows.

## 2. The practitioner

A practising architect's day, viewed honestly, is not mostly drawing diagrams. It is surfacing stakeholder concerns the team has stopped hearing. Refreshing the scorecard before the quarterly review. Drafting the NABC business case the PMO will see in three weeks. Watching for drift between specification and runtime. Mentoring the associate architect who joined last month. Remembering, under pressure, which of these decisions can be reversed and which cannot.

The body of knowledge that organizes this work, IASA's BTABoK, recognizes the breadth. It distinguishes four models for the practice: Engagement (how the architect executes work across the lifecycle), Value (why the work was undertaken and whether the benefits are real), People (the structure and development of the architectural community), and Competency (the substrate of professional development, certified at four levels across nine pillars). Each model has its own working artifacts and named cadences, from weekly scorecard refreshes to annual principle reviews.

The breadth is the problem an agentic platform must respect. A tool that addresses one model and ignores the others either fails the practitioner or quietly absorbs work it has no authority to do. A platform that addresses all four equally, without distinguishing between them, makes the same mistake on a larger scale.

## 3. Why a platform, not a tool

The architect's work surface is heterogeneous in a way that resists single-tool design. Some work is deterministic and benefits from machine speed: a freshness sweep across a hundred specs at midnight, a Technical Debt Ratio computed from current portfolio data. Some work is enforcement: a commit that introduces a topology violation should be refused at the keyboard, not weeks later in review. Some work is calendrical: a quarterly leading-indicator review should not require the practitioner to remember it. Some work is conversational and benefits from a focused subagent with its own context. Some work is human-only, and any AI involvement misshapes it.

These are different modalities, not different applications. An agentic platform is a layered set of primitives, each calibrated to its modality. The platform reaches the architect not through one interface but through whichever primitive fits the work at hand: a tool when the answer is computable, a hook when the rule is non-negotiable, a scheduled task when the cadence is named, a subagent when the work is multi-step, a slash command when the practitioner initiates, a skill when guidance is welcomed but not imposed, a preview when the question is what something looks like, retrieval when the answer is in the corpus.

A platform-shaped solution is harder to design than a tool-shaped one because the primitives must agree on shared infrastructure: a single source of profile context, a single audit trail, a single privacy gate. The reward is that each primitive can do its job honestly, without pretending to be the whole.

## 4. The authority gradient

The platform's central design constraint is that AI's authority over the architect's work must be legible. A feature that blocks an action is doing something different from a feature that proposes one. The practitioner must always know which.

The platform divides authority into four tiers. *Enforce* blocks the action: the commit is refused, the merge is held. *Gate* requires acknowledgment: the practitioner must explicitly approve before proceeding. *Advise* offers and argues but does not decide. *Inform* presents facts without recommendation.

The tiers correspond to confidence in the AI's judgment for the work at hand. Enforcement is appropriate where the rule is exact and the cost of false negatives exceeds the cost of false positives, as with profile validators on a specification. Gating is appropriate where the work has irreversible consequences and the practitioner's signal is the safeguard, as with a waiver chain for an architecturally significant decision. Advice is appropriate where AI can compose a plausible candidate but the judgment is the practitioner's, as with a benefits-realization model or a mentoring pairing. Information is appropriate where the answer is fact, retrieved or computed, with no recommendation attached.

The gradient is not a feature ranking. It is an ethical commitment. A platform that misclassifies its own authority, advising when it should inform or enforcing when it should advise, erodes the practitioner's trust in the rest of the system. Each platform feature is assigned to exactly one tier at design time, and the assignment is visible to the practitioner at point of use. The principle is simple: the architect always knows what the agent is doing.

## 5. Model coverage

The four BTABoK models are not equally enforce-eligible, and the platform must say so.

The Engagement Model, the operating framework for how the architect executes work, has formal validators backed by the SpecChat specification language. Errors here are computable: a topology rule is violated or it is not, a freshness SLA has lapsed or it has not, a waiver chain is complete or it is broken. Enforcement is therefore available across the whole Engagement surface, and the platform takes it.

The other three models are different. Value asks whether the benefits proposed in a business case are being realized; the answer is judgment under uncertainty, not computation. People concerns relationships, mentoring, community health, and reporting structures; these are sites of human judgment that AI cannot mechanize without misshaping. Competency tracks practitioner development across pillars and proficiency levels, with self-assessment, peer assessment, mentor assessment, and certification distributing the judgment across four parties by design. AI authority over any of these would compress what is meant to be distributed.

The platform's response is a deliberate asymmetry. Engagement Model support runs across all four authority tiers including enforcement. Value, People, and Competency support runs at Advise and Inform only, never at Enforce or Gate. The decision is permanent. A platform that crossed this boundary, validating value-realization claims or rating mentor work, would have quietly become a different system, and a worse one. The constraint is not technical but architectural: the platform's discipline is what the discipline of the practice itself depends on.

## 6. The judgment boundary

The authority gradient classifies *what* the platform is doing. A second discipline classifies *what kinds of work AI should never do at all*, regardless of capability.

Across the practice, AI is well-suited to mechanical cadence work, to artifact drafting, and to retrieval across a structured corpus. It assembles review packets, drafts decision records and business cases, surfaces evidence, and watches for drift. It does these well, and the platform leans on them.

AI is poorly suited, and in some cases excluded, from work where judgment is itself the deliverable. The platform names this with seven safeguard patterns and four authority bands.

The authority bands sort every feature by how much of the work AI carries. *AI-strong* features have AI carrying the bulk of the labor with a named human confirming the result: the decision scribe drafts a record, the architect signs it. *AI-backstage* features prepare material for a human who must own a primary relationship: the mentor packet is assembled offstage; the mentor never sees AI in the room with the mentee. *AI-proposer* features rank or match candidates, leaving each decision to a human: the rotation coordinator proposes; the manager approves. *AI-excluded* features are off-limits regardless of capability: performance rating, mentor judgment, certification, compensation, hiring, firing, funding allocation. The platform produces no output that reads as a recommendation in any of these.

The seven safeguard patterns describe how AI and the practitioner share each piece of work. *Draft-and-review*: AI drafts; a named human owns the artifact. *Assemble-and-present*: AI gathers inputs; the human interprets and acts. *Propose-and-confirm*: AI suggests an action; the human confirms each one. *Monitor-and-alert*: AI watches signals; the human decides response. *Coach-and-capture*: AI guides a practitioner-owned process; data stays with the practitioner. *Shadow-and-record*: AI observes; the human acts; AI builds the audit trail. *Gate-and-block*: AI cannot proceed past a checkpoint without an explicit human signal.

These are not soft preferences. They are the platform's structural commitment to the practice it supports. The mechanics of architecture can be automated. The judgment of architecture is what makes the practitioner an architect, and the platform refuses to absorb it.

## 7. Where the architect ends and the agent begins

The platform draws one further boundary, this one between itself and SpecChat.

SpecChat is the formal medium where the architect's commitments live as machine-readable specification. Its validators run inside its profile; its grammar is exact; its rules apply uniformly to any collection that adopts them. ASAP consumes SpecChat through its MCP server interface and adds the practitioner's working surface around it: the cadences, the cross-references, the platform tasks that exceed any single specification.

The dependency points one way. ASAP depends on SpecChat. SpecChat does not depend on ASAP and ships independently. A team can use SpecChat for specification work without adopting ASAP. A team using ASAP will find SpecChat doing the load-bearing work in the spec layer underneath.

This boundary matters because it is the one Enquiry implies but does not name. Enquiry argues that the medium of specification is where the architect's commitments must live. Once that layer is honest, the question becomes what surrounds it. ASAP is the answer for the architecture practitioner specifically.

## 8. A working example

The platform's design becomes concrete against a worked enterprise. [Global Corp](https://realizationengine.net/spec-chat/docs/examples/global-corp/Global-Corp-Exemplar.html) is a fictional global supply-chain company specified completely in BTABoK terms: a strategic thesis with named objectives, a portfolio of capabilities and value streams, a multi-application architecture spec collection, a decision register, a waiver process, a view gallery, and the personas, ASRs, and governance bodies that organize them. The narrative document and the formal spec collection live alongside each other in the SpecChat repository.

Global Corp is the fixed point against which the platform's components are designed. Each subagent, scheduled task, and skill is shaped by what it would actually do for the architect responsible for Global Corp's evolution. The exemplar is not illustrative. It is the test.

## 9. Status

ASAP is in design. The platform's architecture is captured in the [Platform Design document](https://github.com/Realization-Engine/asap/blob/main/WIP/Architect-Support-Agentic-Platform.md) in this repository, organized as ten primitives, four cross-cutting concerns, a lifecycle-by-primitive matrix, BTABoK model coverage by primitive, and a six-wave delivery plan. The first four waves are SpecChat deliverables: profile, enforcement, governance mechanics, and rendering. The last two waves, Value-and-People support and Competency support, ship from this repository as ASAP proper.

The design is grounded in a direct read of the IASA BTABoK corpus. The lineage of arguments behind it is recorded in the [Citations](The-Architect-and-the-Agent_Citations.md) document.
