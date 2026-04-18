# ASAP

**Architect Support Agentic Platform**

An agentic support platform for the BTABoK practitioner across all four BTABoK models (Engagement, Value, People, Competency). ASAP wraps the practice around a practitioner rather than around a spec, delivering advisory guidance, calendar-driven automation, and knowledge retrieval while preserving strict human-in-the-loop boundaries for every role that requires judgment.

## Status

Pre-implementation. The founding design is in [WIP/Architect-Support-Agentic-Platform.md](WIP/Architect-Support-Agentic-Platform.md).

## Relationship to SpecChat

ASAP depends on [SpecChat](../spec-chat) and consumes its MCP server surface. SpecChat owns the SpecLang language, the BTABOK profile, validators, and canvas rendering. ASAP adds:

- Agentic primitives (skills, subagents, scheduled tasks, webhooks, preview, RAG) over SpecChat's deterministic core.
- Four-band authority gradient with human-in-the-loop role architecture for the non-Engagement BTABoK models.
- Deployed-service concerns: stores (`CompetencyStore`), privacy enforcement (`PrivacyGate`), retention, diagnostics bus, integrations with directory, HRIS, PMO, incident, and PR-webhook boundaries.

SpecChat ships independently and is unaware of ASAP. ASAP does not modify SpecLang.

## Design documents

- [Architect Support Agentic Platform](WIP/Architect-Support-Agentic-Platform.md): the founding design. Covers framing, ten platform components, BTABoK-model-by-model support, HITL role architecture, and a six-wave delivery plan with a fork point at SpecChat GA exit.
- [ASAP Acronym and Term Glossary](WIP/ASAP-Acronym-and-Term-Glossary.md): acronyms and terminology used across the ASAP corpus.

## License

See [LICENSE](LICENSE).
