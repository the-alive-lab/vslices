# Paso 3 — Identificar perfiles participantes en los Work Flows

**Estado:** guía candidata, elaborada a partir del modelado organizacional de Serviu (2026-11-10).  
**Pertenece a:** [Guía de uso de Work Semantics](README.md).  
**Definición del mecanismo:** [Domain Modeling](../README.md).

## Propósito

Identificar **desde qué función o responsabilidad organizacional los actores ejecutan, coordinan o participan en los Work Flows** reconocidos. Un perfil describe una posición funcional en un contexto de trabajo; no define por sí solo una cuenta, un permiso ni una clase de usuario.

Este paso relaciona los [actores](01-reconocer-actores.md) y los [procesos y Work Flows](02-reconocer-procesos.md) ya reconocidos, sin volverlos definiciones subordinadas a un mismo archivo.

## Preguntas que orientan

- ¿Qué perfil realiza la acción? ¿Quién responde por su resultado, si es distinto?
- ¿Qué otros perfiles intervienen, asesoran, autorizan o reciben sus consecuencias?
- ¿Puede un tipo de actor desempeñar este perfil en el contexto estudiado? ¿Puede hacerlo más de un tipo?
- ¿Cambian las responsabilidades según el proceso, condición o etapa?
- ¿Qué asignaciones están confirmadas por la organización y cuáles son hipótesis?
- ¿Existe un caso en el que una misma persona desempeñe varios perfiles sin alterar las definiciones?

## Evidencia y límites

Usar situaciones reales, procedimientos y testimonios pertinentes; distinguir **responsabilidad observada**, **responsabilidad declarada** y **suposición**.

Una etiqueta como «interno» o «externo» **no constituye un perfil por sí sola**: caracteriza una forma contextual de participación. Evitar inferir perfiles de nombres de grupos de seguridad, pantallas o cargos contractuales. **No traducir perfiles a permisos** durante este paso.

Si una acción no tiene ejecutor comprobado, registrarlo como **perfil por determinar**; no asignársela al perfil más cercano solo para colorear un carril.

## Cómo elaborar el modelo

1. **Recorrer cada Work Flow** del proceso e identificar quién efectivamente actúa y quién participa.
2. **Reconocer funciones recurrentes** que merecen un perfil contextual propio; no crear uno nuevo por cada persona o pantalla.
3. **Relacionar perfiles con tipos de actor**: registrar qué posiciones permiten asumir cada función, sin confundir ambas clasificaciones.
4. **Distinguir participación y responsabilidad** en cada Work Flow cuando la evidencia lo permita; no imponer exclusividad, un único ejecutor ni categorías universales de responsabilidad.
5. **Contrastar casos de frontera** y asignaciones discutidas; conservar preguntas abiertas.
6. **Documentar cada perfil en su superficie propietaria** y enlazarlo desde la matriz o proyección del proceso; no duplicar definiciones.

Una matriz de apoyo puede relacionar **Work Flow → perfil ejecutor/participantes → tipos de actor compatibles → evidencia/estado**. No prescribe un esquema de almacenamiento ni un mecanismo de autorización.

## Representación y ejemplos

Una proyección de Work Process **con carriles por perfil** puede ayudar a reconocer traspasos de responsabilidad, siempre que las asignaciones estén sustentadas. En Serviu se exploró Mermaid `swimlane-beta` con `redux-color` para diferenciar carriles: es una posibilidad de visualización, no una convención obligatoria del modelo.

No hacer del diagrama la única autoridad documental: el modelo de perfiles y sus relaciones se conserva en documentos enlazados.

## Resultado examinable

Un catálogo contextual de perfiles, cada uno con su significado, responsabilidades conocidas, tipos de actor relacionados y procedencia; además de relaciones documentadas entre perfiles y Work Flows, con asignaciones **comprobadas, candidatas o pendientes**.

**Comprobaciones:** ¿un perfil fue definido como permiso o grupo técnico?, ¿confundimos actor con perfil?, ¿inventamos responsables por necesidades visuales?, ¿el mismo perfil está definido de distintas maneras en dos documentos?, ¿es reconstruible la evidencia detrás de cada asignación?

## Relación con los pasos siguientes

Al profundizar cada Work Flow se podrán identificar condiciones y participantes adicionales; al sistematizar el trabajo se estudiarán identidades y autorizaciones técnicas **sin sustituir retrospectivamente** los perfiles organizacionales.

## Evidencia de referencia

[Perfiles de la ticketera de Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/profiles/README.md). Las asignaciones y el alcance de esos perfiles pertenecen a su contexto, no se generalizan a todo Domain Modeling.
