# Paso 3 — Identificar [perfiles](../concepts/profile.md) [participantes](../concepts/participant.md) en los [Work Flows](../concepts/work-flow.md)

**Estado:** guía candidata, elaborada a partir del modelado organizacional de Serviu (2026-11-10).  
**Pertenece a:** [Guía de uso de Work Semantics](README.md).  
**Definición del mecanismo:** [Domain Modeling](../README.md).

## Propósito

Identificar **desde qué función o responsabilidad organizacional los [actores](../concepts/actor.md) ejecutan, coordinan o participan en los [Work Flows](../concepts/work-flow.md)** reconocidos. Un [perfil](../concepts/profile.md) describe una posición funcional en un contexto de trabajo; no define por sí solo una cuenta, un permiso ni una clase de usuario.

Este paso relaciona los [actores](01-reconocer-actores.md) y los [procesos y Work Flows](02-reconocer-procesos.md) ya reconocidos, sin volverlos definiciones subordinadas a un mismo archivo.

## Preguntas que orientan

- ¿Qué [perfil](../concepts/profile.md) realiza la acción? ¿Quién responde por su resultado, si es distinto?
- ¿Qué otros [perfiles](../concepts/profile.md) intervienen, asesoran, autorizan o reciben sus consecuencias?
- ¿Puede un tipo de [actor](../concepts/actor.md) desempeñar este [perfil](../concepts/profile.md) en el contexto estudiado? ¿Puede hacerlo más de un tipo?
- ¿Cambian las responsabilidades según el proceso, condición o etapa?
- ¿Qué asignaciones están confirmadas por la organización y cuáles son hipótesis?
- ¿Existe un caso en el que una misma persona desempeñe varios [perfiles](../concepts/profile.md) sin alterar las definiciones?

## Evidencia y límites

Usar situaciones reales, procedimientos y testimonios pertinentes; distinguir **responsabilidad observada**, **responsabilidad declarada** y **suposición**.

Una etiqueta como «interno» o «externo» **no constituye un [perfil](../concepts/profile.md) por sí sola**: caracteriza una forma contextual de participación. Evitar inferir [perfiles](../concepts/profile.md) de nombres de grupos de seguridad, pantallas o cargos contractuales. **No traducir [perfiles](../concepts/profile.md) a permisos** durante este paso.

Si no conocemos quién ejecuta una acción, **reconocer esa responsabilidad como pendiente**; no atribuirla por conveniencia ni suponer que corresponde al [perfil](../concepts/profile.md) aparentemente más cercano.

## Cómo elaborar el modelo

1. **Recorrer cada [Work Flow](../concepts/work-flow.md)** del proceso e identificar quién efectivamente actúa y quién participa.
2. **Reconocer funciones recurrentes** que merecen un [perfil](../concepts/profile.md) contextual propio; no crear uno nuevo por cada persona o pantalla.
3. **Relacionar [perfiles](../concepts/profile.md) con tipos de [actor](../concepts/actor.md)**: comprender qué posiciones permiten asumir cada función, sin confundir ambas clasificaciones.
4. **Distinguir participación y responsabilidad** en cada [Work Flow](../concepts/work-flow.md) cuando la evidencia lo permita; no imponer exclusividad, un único ejecutor ni categorías universales de responsabilidad.
5. **Contrastar casos de frontera** y asignaciones discutidas; conservar preguntas abiertas.
6. **Revisar las atribuciones de responsabilidad** ante casos reales, distinguiendo lo comprendido, lo hipotético y lo aún desconocido.

## Límites de la comprensión

Reconocer un [perfil](../concepts/profile.md) no implica asignarle exclusividad sobre un [Work Flow](../concepts/work-flow.md), ni determinar los permisos necesarios para una realización de sistema. Un mismo participante puede desempeñar distintas funciones; la colaboración y los cambios de responsabilidad deben examinarse según el trabajo real.

## Claridad esperada sobre el dominio

Al recorrer este paso, deberíamos poder **comprender qué funciones y responsabilidades participan en las acciones semánticas, qué tipos de actor pueden asumirlas y cómo se distribuyen, comparten o transfieren durante el trabajo**. Deberíamos distinguir a quien ejecuta una acción de otros participantes, cuando la evidencia permita hacerlo, y reconocer sin inventarlas las responsabilidades todavía inciertas.

Esta claridad no depende de producir un catálogo de perfiles, una matriz de responsabilidades o un diagrama por carriles. Tampoco requiere resolver permisos ni identidades de sistema.

**Cómo examinar la comprensión:** ¿un [perfil](../concepts/profile.md) fue definido como permiso o grupo técnico?, ¿confundimos [actor](../concepts/actor.md) con [perfil](../concepts/profile.md)?, ¿inventamos responsables por necesidades visuales?, ¿el mismo [perfil](../concepts/profile.md) está definido de distintas maneras en dos documentos?, ¿es reconstruible la evidencia detrás de cada asignación?

## Relación con los pasos siguientes

Al profundizar cada [Work Flow](../concepts/work-flow.md) se podrán identificar condiciones y [participantes](../concepts/participant.md) adicionales; al sistematizar el trabajo se estudiarán identidades y autorizaciones técnicas **sin sustituir retrospectivamente** los [perfiles](../concepts/profile.md) organizacionales.

## Evidencia de referencia

[Perfiles de la ticketera de Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/profiles/README.md). Las asignaciones y el alcance de esos [perfiles](../concepts/profile.md) pertenecen a su contexto, no se generalizan a todo Domain Modeling.
