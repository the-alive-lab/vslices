# Docs Standard — root-question inventory from normative definitions

**Source:** [vslices/docs-standard](https://github.com/vslices/docs-standard) (main; reviewed 2026-10-09).  
**Status:** bounded source extraction for canonical review; **not** a promotion of question branches or of candidate vocabularies to installed-standard status.

This inventory records **only root questions** of particular Documents and Continuity Paths. It does not transplant child questions, recommendations, YAML implementation, scope lists or historical path ranks.

## Documents — root questions

The following 16 Document definitions are registered in the source repository's `manifest.yaml`.

| Type | Root question |
| --- | --- |
| context | ¿Dónde existe? |
| structure | ¿Cómo se organiza? |
| domain-vocabulary | ¿Cómo hablamos? |
| consistency | ¿Qué debe mantenerse coherente? |
| update | ¿Qué cambia? |
| behavior | ¿Qué debe ocurrir? |
| decision-record | ¿Qué se decidió? |
| feedback | ¿Qué recibimos al aplicar algo? |
| navigation | ¿Cómo exploramos? |
| scope | ¿Hasta dónde llega? |
| viability | ¿Es viable? |
| constraint | ¿Qué condiciona la realización? |
| realization | ¿Cómo se realiza? |
| drift | ¿Qué divergencia sigue sin reconciliarse? |
| diagnostic | ¿Qué tensión, fragilidad o contradicción revela lo que observamos? |
| validation | ¿Sigue siendo válida esta representación? |

## Nexus — current particular definitions

The source defines two candidate Nexus types:

| Type | Declared base question |
| --- | --- |
| capability | **Not declared** in its YAML |
| service-consumption | **Not declared** in its YAML |

**Do not infer or invent root question wording.** Their source files currently express the composition via `recommendations` and do not contain `nexus.questions`. The [Nexus language](https://github.com/vslices/docs-standard/blob/main/nexus/README.md) allows questions but does not require them. The current conceptual interpretation here is **a collection of large questions about a given concept**; stabilizing each particular Nexus's base organizing question, if warranted, remains an explicit gap. Neither Nexus definition is registered in the source manifest.

## Continuity Paths — root continuity questions

The source has 13 candidate definitions, not registered in its manifest.

| Type | Root continuity question |
| --- | --- |
| business-driver | ¿Qué situación de negocio origina, justifica o condiciona esto? |
| business-scenario | ¿Dónde ocurre el trabajo y qué elementos ayudan a entender este escenario? |
| client-product | ¿Qué experiencia visible ofrece este producto y qué aprendizaje la cambia o confirma? |
| consumable-service | ¿Qué capacidad ofrece este servicio y cómo debe consumirse? |
| domain-context | ¿Qué lenguaje, conceptos, reglas y comportamientos pertenecen a este contexto? |
| evolution | ¿Cómo cambió esto sin perder su intención? |
| impact | ¿Qué se ve afectado si esto cambia, falla, aparece, se elimina o evoluciona? |
| knowledge-handoff | ¿Qué conocimiento debe quedar disponible para que el equipo pueda continuar? |
| ownership | ¿Quién entiende, decide, valida, mantiene u opera esto? |
| software-initiative | ¿Qué intenta cubrir esta iniciativa y qué piezas participan? |
| software-project | ¿Cómo está organizada esta solución de software? |
| traceability | ¿De dónde viene esto, qué lo transformó y dónde terminó materializándose? |
| viability | ¿Puede sostenerse esto bajo las condiciones actuales? |

**No inherent priority classes:** `core`, `supporting`, `contextual`, primary and secondary are legacy classifications and are **not** part of the current type definition. Any number of Paths may be selected according to the continuities that actually need preserving.

## Semantic interpretation and limits

- **Support Note:** a detail about a specific concept.
- **Document:** a large question about a specific concept.
- **Nexus:** a collection of large questions about a specific concept.
- **Continuity Path:** a map of question-bearing routes preserving the continuity of a specific topic.

Root questions give each particular type its current focus. **Branches are not part of this inventory.** They are progressively discovered, tested and stabilized through Semantic Pressure as actual use reveals distinctions necessary for an increasingly informative corpus. A branch is neither a required checklist item nor a measure of maturity. This summary does **not** prescribe all artifacts originate in explicit Semantic Pressure sessions.

The historical research under `vslices/docs/es/alive-lab/research/notes/docs-standard/artifacts` is relevant evidence; the documentary definitions under `vslices/docs/es/products/docs-standard` are legacy and must not override the above normative source. Other non-documentary concepts in that public product surface remain worth examining separately.

**Authority boundary:** `vslices/docs-standard` is currently the normative machine-consumable definition source for Tooling. This file is a **review/extraction inside the developing shared canonical Suite source**, not a silent change of Tooling's installed manifest or an assertion that unpublished candidate types have already been promoted. The transition of semantic authority must be explicit.
