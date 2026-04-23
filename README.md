# ASAP

**Architect Support Agentic Platform**

An agentic support platform for the BTABoK practitioner across all four BTABoK models (Engagement, Value, People, Competency). ASAP wraps the practice around a practitioner rather than around a spec, delivering advisory guidance, calendar-driven automation, and knowledge retrieval while preserving strict human-in-the-loop boundaries for every role that requires judgment.

## Status

Pre-implementation. The platform's full architecture is captured in [WIP/Architect-Support-Agentic-Platform.md](WIP/Architect-Support-Agentic-Platform.md). The theoretical groundwork for an upcoming concept paper, *The Architect and the Agent*, is in [docs/notes/](docs/notes/).

## Relationship to SpecChat

ASAP depends on [SpecChat](../spec-chat) and consumes its MCP server surface. SpecChat owns the SpecLang language, the BTABOK profile, validators, and canvas rendering. ASAP adds:

- Agentic primitives (skills, subagents, scheduled tasks, webhooks, preview, RAG) over SpecChat's deterministic core.
- Four-band authority gradient with human-in-the-loop role architecture for the non-Engagement BTABoK models.
- Deployed-service concerns: stores (`CompetencyStore`), privacy enforcement (`PrivacyGate`), retention, diagnostics bus, integrations with directory, HRIS, PMO, incident, and PR-webhook boundaries.

SpecChat ships independently and is unaware of ASAP. ASAP does not modify SpecLang.

## Documents

**Design**

- [Architect Support Agentic Platform](WIP/Architect-Support-Agentic-Platform.md): the founding platform design. Covers framing, ten platform components, BTABoK-model-by-model support, HITL role architecture, and a six-wave delivery plan with a fork point at SpecChat GA exit.
- [ASAP Acronym and Term Glossary](WIP/ASAP-Acronym-and-Term-Glossary.md): acronyms and terminology used across the ASAP corpus.

**Notes** (preparatory analytical material; concept paper forthcoming)

- [Notes for *The Architect and the Agent*](docs/notes/Notes-for-The-Architect-and-the-Agent.md): a section-by-section corollary analysis of *The Multiplier and the Mirror* applied to enterprise architecture practice. Derives the theoretical foundation for ASAP's design: BTABoK as the operationalized FORCE taxonomy; the Mirror at two scales (individual and enterprise); three commitments (FORCE-form coverage, formalizability-asymmetric authority, atrophy-defense via HITL); the architectural Collapse of Execution; the cohort discontinuity; the cascade and the platform's brakes; the decision bottleneck and architectural moats; sovereignty; three trajectories for the profession; and the platform's explicit bet on Future 1 + Future 4. Comprehensive (twenty sections, ~9,000 words) by design.
  - [Citations](docs/notes/Notes-for-The-Architect-and-the-Agent_Citations.md): companion citations record, organised in the parent paper's own section order.

## License

See [LICENSE](LICENSE).
