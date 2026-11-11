# Paso 3 — Reconocer perfiles organizacionales

**Estado:** guía candidata, elaborada a partir del modelado organizacional de Serviu (2026-11-10).  
**Pertenece a:** [Guía de uso de Work Semantics](README.md).  
**Definición del mecanismo:** [Domain Modeling](../README.md).

## Propósito

Reconocer **qué funciones y responsabilidades organizacionales tienen significado propio en el trabajo** y qué tipos de [actor](../concepts/actor.md) pueden desempeñarlas en el contexto estudiado.

Un [perfil](../concepts/profile.md) no es una cuenta, permiso o clase de usuario. En este paso buscamos **comprender qué perfiles existen y qué expresan**, sin exigir todavía su asignación a todos los [Work Flows](../concepts/work-flow.md). Relacionarlos con acciones concretas corresponde al [paso 4](04-relacionar-perfiles-con-work-flows.md).

## Preguntas que orientan

- ¿Qué funciones distingue la organización en este ámbito de trabajo y qué significado tiene cada una?
- ¿Qué responsabilidades permiten reconocer esas funciones sin definirlas a partir de un permiso técnico?
- ¿Qué tipos de actor pueden asumir una misma función? ¿Puede una persona desempeñar diferentes perfiles?
- ¿Qué ejemplos reales permiten distinguir dos perfiles que parecen similares?
- ¿Qué perfiles están sustentados y cuáles son solamente nombres o hipótesis?

## Evidencia y límites

Usar situaciones reales, procedimientos y testimonios pertinentes; distinguir **responsabilidad observada**, **responsabilidad declarada** y **suposición**.

Una etiqueta como «interno» o «externo» **no constituye un [perfil](../concepts/profile.md) por sí sola**: caracteriza una forma contextual de participación. Evitar inferir [perfiles](../concepts/profile.md) de nombres de grupos de seguridad, pantallas o cargos contractuales. **No traducir [perfiles](../concepts/profile.md) a permisos** durante este paso.

Si no conocemos quién ejecuta una acción, **reconocer esa responsabilidad como pendiente**; no atribuirla por conveniencia ni suponer que corresponde al [perfil](../concepts/profile.md) aparentemente más cercano.

## Cómo elaborar el modelo

1. **Reconocer funciones organizacionales** en situaciones conocidas, sin exigir partir de un proceso completo ni recorrer cada Work Flow.
2. **Distinguir perfiles con significado propio** por sus responsabilidades contextuales, no por personas, cargos, pantallas o grupos de acceso.
3. **Relacionar perfiles con tipos de [actor](../concepts/actor.md)** cuando sea pertinente, sin confundir ambas clasificaciones.
4. **Contrastar casos de frontera**: responsabilidades compartidas, una misma persona en funciones distintas o funciones que cambian según el contexto.
5. **Reconocer límites e incertidumbres** de la clasificación, evitando inventar responsabilidades para completar una lista.
6. **Revisar las distinciones** cuando la evidencia del trabajo muestre que dos funciones se confundieron o que falta reconocer alguna.

## Límites de la comprensión

Reconocer un [perfil](../concepts/profile.md) no implica asignarle exclusividad sobre un [Work Flow](../concepts/work-flow.md), ni determinar los permisos necesarios para una realización de sistema. Un mismo participante puede desempeñar distintas funciones; la colaboración y los cambios de responsabilidad deben examinarse según el trabajo real.

## Claridad esperada sobre el dominio

Deberíamos poder **explicar qué perfiles organizacionales reconocemos, qué funciones o responsabilidades representan y desde qué tipos de actor pueden ejercerse**, diferenciando la comprensión sustentada de las hipótesis y vacíos todavía abiertos.

No necesitamos haber asignado cada perfil a un Work Flow: **esa relación se examina en el [paso 4](04-relacionar-perfiles-con-work-flows.md)**. Tampoco necesitamos un catálogo, matriz, documento ni diagrama para considerar alcanzada esta claridad.

**Cómo examinar la comprensión:** ¿definimos un perfil por su función o por permisos técnicos?, ¿lo confundimos con un tipo de actor o cargo?, ¿podemos distinguir perfiles por evidencia sin depender de sus nombres?, ¿sabemos qué perfiles permanecen hipotéticos o insuficientemente comprendidos?

## Relación con los pasos siguientes

El [paso 4](04-relacionar-perfiles-con-work-flows.md) relaciona los perfiles reconocidos con los Work Flows estudiados. Esa relación puede revelar nuevos perfiles o cuestionar sus definiciones; las identidades y autorizaciones técnicas se examinarán en la sistematización sin sustituir retrospectivamente los perfiles organizacionales.

## Evidencia de referencia

[Perfiles de la ticketera de Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/profiles/README.md). Las asignaciones y el alcance de esos [perfiles](../concepts/profile.md) pertenecen a su contexto, no se generalizan a todo Domain Modeling.
