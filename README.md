# ASAP

**Architect Support Agentic Platform**

An agentic support platform for the BTABoK practitioner across all four BTABoK models (Engagement, Value, People, Competency). ASAP wraps the practice around a practitioner rather than around a spec, delivering advisory guidance, calendar-driven automation, and knowledge retrieval while preserving strict human-in-the-loop boundaries for every role that requires judgment.

## Status

Pre-implementation. The concept is introduced in [*The Architect and the Agent*](docs/theory/The-Architect-and-the-Agent.md). The platform's full architecture is captured in [WIP/Architect-Support-Agentic-Platform.md](WIP/Architect-Support-Agentic-Platform.md).

## Relationship to SpecChat

ASAP depends on [SpecChat](../spec-chat) and consumes its MCP server surface. SpecChat owns the SpecLang language, the BTABOK profile, validators, and canvas rendering. ASAP adds:

- Agentic primitives (skills, subagents, scheduled tasks, webhooks, preview, RAG) over SpecChat's deterministic core.
- Four-band authority gradient with human-in-the-loop role architecture for the non-Engagement BTABoK models.
- Deployed-service concerns: stores (`CompetencyStore`), privacy enforcement (`PrivacyGate`), retention, diagnostics bus, integrations with directory, HRIS, PMO, incident, and PR-webhook boundaries.

SpecChat ships independently and is unaware of ASAP. ASAP does not modify SpecLang.

## Documents

- [*The Architect and the Agent*](docs/theory/The-Architect-and-the-Agent.md): the concept doc. Introduces ASAP as the third in the Realization Engine sequence (after *The Multiplier and the Mirror* and *Enquiry Into Specification as Meaningful Struggle*) and names the platform's authority gradient, model-coverage asymmetry, and judgment boundary.
  - [Citations and references](docs/theory/The-Architect-and-the-Agent_Citations.md): companion to the concept doc.
- [Architect Support Agentic Platform](WIP/Architect-Support-Agentic-Platform.md): the founding design. Covers framing, ten platform components, BTABoK-model-by-model support, HITL role architecture, and a six-wave delivery plan with a fork point at SpecChat GA exit.
- [ASAP Acronym and Term Glossary](WIP/ASAP-Acronym-and-Term-Glossary.md): acronyms and terminology used across the ASAP corpus.

## License

See [LICENSE](LICENSE).
