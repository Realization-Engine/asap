# Citations and references

Companion to [*The Architect and the Agent*](The-Architect-and-the-Agent.md).

This document organizes the source material the concept doc rests on. The references are grouped by their relationship to the argument: parent works in the Realization Engine sequence, the body of knowledge that organizes architecture practice, the companion artifacts that ground the platform's design, and the adjacent practice references the platform design document draws on.

---

## Parent works

The concept doc is the third in a sequence. Each parent work establishes a layer of the argument that *The Architect and the Agent* extends.

**[P1]** Landi, Dennis. *The Multiplier and the Mirror.* The Realization Engine, 2026. <https://realizationengine.net/fstar/docs/The_Multiplier_and_the_Mirror.html>

The foundational argument. Establishes that human capability scales through collaborative systems, and that those systems, in turn, reshape the practitioners working inside them. Provides the general frame from which the specification and platform arguments descend.

**[P2]** Landi, Dennis. *Enquiry Into Specification as Meaningful Struggle.* The Realization Engine, 2026. <https://realizationengine.net/spec-chat/docs/theory/Enquiry-Into-Specification-as-Meaningful-Struggle.html>

Applies the Multiplier and Mirror thesis to software work. Argues that as language models absorb implementation labor, the human's value migrates to specification, evaluation, and architecture under ambiguity, and that the medium of specification therefore matters. Provides the immediate intellectual basis for the platform's discipline at the spec-language layer.

---

## Body of knowledge

The platform takes its working surface, vocabulary, and named cadences from the IASA Body of Knowledge. The references below are direct sources for the practice ASAP supports.

**[B1]** IASA Global. *Business Technology Architecture Body of Knowledge (BTABoK), version 3.x.* IASA Global, ongoing. <https://btabok.iasaglobal.org/>

The corpus that organizes architecture practice into the four models (Engagement, Value, People, Competency), the Architecture Development Life Cycle, the canvas catalog, and the certification structure the concept doc references. The platform's model-coverage decision in §5 is grounded in BTABoK's own framing, including its statements that "the engagement model is the how, the value model is the why" and "architects should be governed, not doing the governing."

**[B2]** IASA Global. *Concept Definition Language (CoDL) and Canvas Definition Language (CaDL).* BTABoK 3.2 Education Portal, IASA Global, 2026.

Companion to BTABoK 3.x. Defines the structured concept and canvas languages the SpecChat profile mirrors and the platform's preview layer renders.

**[B3]** IASA Global. *CITA Certification: Foundation, Associate, Professional, Distinguished.* IASA Global. <https://iasaglobal.org/architect-training/cita/>

The four-level certification structure referenced by the platform's Competency Model coverage. The asymmetry between five proficiency levels and four certification levels noted in the design doc traces to this material.

**[B4]** IASA Global. *Architect Skills Framework: BIISS specializations.* IASA Global.

The Business / Information / Infrastructure / Software / Solution specialization taxonomy used in the platform's role and team-coverage features.

---

## Companion artifacts

The concept doc points to three companion artifacts in the Realization Engine corpus. They make the platform's design concrete.

**[C1]** *Architect Support Agentic Platform: Platform Design.* This repository. <https://github.com/Realization-Engine/asap/blob/main/WIP/Architect-Support-Agentic-Platform.md>

The full platform design. Covers ten components (deterministic core, enforcement, automation, integration, specialist workers, human entry points, advisory, rendering, knowledge, infrastructure), eight cross-cutting concerns, a lifecycle-by-primitive matrix, model-by-model agentic coverage, the human-in-the-loop role architecture across all three out-of-profile models, and a six-wave delivery plan with a fork point at SpecChat GA exit. The concept doc's §3, §4, §5, and §6 each summarize a layer of this document.

**[C2]** *ASAP Acronym and Term Glossary.* This repository. <https://github.com/Realization-Engine/asap/blob/main/WIP/ASAP-Acronym-and-Term-Glossary.md>

Working vocabulary across the ASAP corpus. Useful when reading the platform design or the BTABoK source material.

**[C3]** *Global Corp Enterprise Architecture: A Fictional BTABOK-Complete Enterprise Architecture for Global Supply Chain Tracking.* SpecChat repository. <https://realizationengine.net/spec-chat/docs/examples/global-corp/Global-Corp-Exemplar.html>

The narrative architecture document and its companion spec collection. Functions as the fixed point against which the platform's components are designed and tested. Referenced in §8.

---

## SpecChat design notes

The platform's design depends on several SpecChat design records. These remain repository-only material, cited here for traceability.

**[S1]** *SpecLang-Design.md.* SpecChat repository. <https://github.com/Realization-Engine/spec-chat/blob/main/docs/design-notes/SpecLang-Design.md>

The consolidated design covering Core SpecLang, the BTABOK profile, CoDL and CaDL alignment, and the Engagement Model scope.

**[S2]** *Spec-Type-System.md.* SpecChat repository. <https://github.com/Realization-Engine/spec-chat/blob/main/docs/design-notes/Spec-Type-System.md>

Spec type taxonomy, rationale, and validation architecture.

**[S3]** *MCP-Server-Integration-Design.md.* SpecChat repository. <https://github.com/Realization-Engine/spec-chat/blob/main/docs/design-notes/MCP-Server-Integration-Design.md>

The MCP server surface ASAP consumes. Integration phases referenced in the platform's six-wave delivery plan.

**[S4]** *SpecChat-BTABOK-Implementation-Plan.md.* SpecChat repository. <https://github.com/Realization-Engine/spec-chat/blob/main/docs/design-notes/btabok/SpecChat-BTABOK-Implementation-Plan.md>

Phased plan for SpecChat's BTABOK profile, validators, and canvas rendering. Phases 1 through 4 underwrite the enforcement layer the concept doc's §4 and §5 describe.

**[S5]** *BTABOK-Out-of-Scope-Models.md.* SpecChat repository. <https://github.com/Realization-Engine/spec-chat/blob/main/docs/design-notes/btabok/BTABOK-Out-of-Scope-Models.md>

The scope discipline that places Value, People, and Competency models out of the SpecLang profile. The model-coverage asymmetry the concept doc defends in §5 traces to this decision.

---

## Adjacent practice references

The platform design draws on practice frameworks and methods adjacent to BTABoK. These are not load-bearing for the concept doc itself but ground the design's references in §3 and §6.

**[A1]** Westrum, Ron. "A Typology of Organisational Cultures." *Quality and Safety in Health Care*, 2004. The typology underlying the Westrum Culture Diagnostic referenced in the platform's People Model coverage.

**[A2]** *SFIA: Skills Framework for the Information Age.* SFIA Foundation. <https://sfia-online.org/>. Referenced in the platform's Competency Model integrations.

**[A3]** *TOGAF Standard, Architecture Skills Framework.* The Open Group. Referenced alongside SFIA and BTABoK in the Competency Model index.

**[A4]** *European e-Competence Framework (e-CF).* CEN Workshop, European Standard EN 16234-1. Referenced alongside SFIA and TOGAF in the Competency Model index.

**[A5]** Christensen, Clayton M., et al. "Know Your Customers' 'Jobs to Be Done.'" *Harvard Business Review*, September 2016. The Jobs-to-be-Done method referenced in the stakeholder concern miner subagent and in BTABoK's own discovery practices.

**[A6]** Carlson, Curtis R., and William W. Wilmot. *Innovation: The Five Disciplines for Creating What Customers Want.* Crown Business, 2006. Source of the NABC (Needs / Approach / Benefits / Considerations) framing the platform's business case drafter uses.
