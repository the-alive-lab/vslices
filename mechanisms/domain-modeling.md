# Domain Modeling — comprensión del dominio y elaboración de realizaciones

**Estado:** `candidate` — revisión conceptual del 2026-11-10.  
**Responsabilidad conceptual:** VSlices Suite; la propiedad de los conceptos técnicos utilizados continúa en sus superficies correspondientes.  
**Procedencia:** evolución explícita de `Action Flow → Work Modeling → Domain Modeling`, discutida por Hernán y Limen a partir de la reconstrucción de los procesos de Serviu. [Trayectoria histórica](#trayectoria-de-revisión).

## Propósito

**Domain Modeling** es la práctica de comprender y representar un dominio partiendo de **cómo la organización entiende, estructura y coordina su trabajo**, para luego descubrir y desarrollar realizaciones sistematizadas que conserven su significado.

Se emplea **domain** en el sentido de ámbito de conocimiento, influencia o actividad asociado a Eric Evans y Domain-Driven Design. VSlices **comparte esa noción de dominio**, pero no queda subordinado al catálogo de construcciones, las capas ni la metodología de modelado de DDD: la aproximación y los mecanismos de VSlices deben examinarse por su propia evidencia.

El modelado es **progresivo y revisable**: comprender el trabajo orienta la sistematización; la realización y sus resultados pueden revelar tensiones que exijan revisar la comprensión anterior. No es una traducción automática del trabajo a componentes técnicos, ni una secuencia rígida en la cual toda pregunta se resuelve definitivamente antes de avanzar.

## Dos ámbitos relacionados

### Work Semantics — semántica del trabajo

**Work Semantics** expresa **cómo la organización comprende su propio trabajo y coordina sus esfuerzos**: actividades, participantes, perfiles, responsabilidades, acciones, condiciones, relaciones y consecuencias. «Organización» designa aquí al sujeto/contexto que reconoce y organiza el trabajo; **no** es el nombre del ámbito de modelado ni una clasificación de tipos de trabajador.

Esta comprensión **no presupone software**, automatización ni una secuencia de acciones.

La jerarquía organizacional candidata es:

- **Work Chain:** cadena de producción o prestación de servicios que puede atravesar áreas y responsabilidades. Ejemplo: servicio de financiamiento de proyectos relacionados al DS 49.
- **Work Process:** parte reconocible de una cadena, que coordina acciones semánticas y sus relaciones para contribuir a su resultado. Ejemplo: gestión de una solicitud de soporte.
- **Work Flow:** acción semántica específica dentro de un Work Process. Ejemplo: registrar una solicitud de soporte o crear una solicitud de pago DS 49.

Un **Work Process no debe reproducir exhaustivamente las decisiones y pasos internos de cada Work Flow**: contiene las acciones y relaciones necesarias para expresar el proceso en ese nivel. Una condición que dirige relaciones entre acciones puede pertenecer al proceso; una condición interna de ejecución puede detallarse en el flujo. La pertinencia del detalle depende de lo que queremos comprender, no de una regla de sintaxis.

Actores y perfiles se relacionan con el trabajo; no equivalen automáticamente a identidades, cuentas ni permisos técnicos. Un diagrama de carriles es una **proyección posible** de esa relación, no la definición del proceso.

### System Realizations — realizaciones de sistema

**System Realizations** comprende la elaboración de cómo los sistemas y sus participantes **pueden realizar el trabajo comprendido**.

Durante el paso desde Work Semantics hacia System Realizations **se descubren, precisan y expresan conceptos, restricciones, comportamientos y capacidades**. No son una tercera rama paralela de Domain Modeling.

En VSlices esos descubrimientos pueden expresarse mediante construcciones como:

- **Spaces y Points:** conceptos y admisibilidad, cuya autoridad conceptual corresponde a [Framework / Spaces](../products/framework/spaces.md).
- **Features:** comportamientos funcionales identificables, con intención y promesa de resultado; y **Capabilities** requeridas, según [Framework / Work](../products/framework/work.md).
- **Grounding y Hosting:** mecanismos y configuración de la realización, cuando corresponda; consultar [Framework](../products/framework/README.md).

**Que Domain Modeling permita descubrir la necesidad de un Space o Feature no transfiere la autoridad de su definición ni obliga a crearlo.** No todo Work Flow genera una sola Feature, ni toda Feature representa un Work Flow organizacional.

La elaboración de sistema utiliza actualmente tres niveles **candidatos**:

- **System Process:** coordinación de acciones de sistema para realizar una intención reconocible; por ejemplo, atender «Crear solicitud de pago DS 49».
- **System Action:** acción semántica funcional que participa en esa coordinación; por ejemplo, crear la solicitud, notificar al solicitante o registrar una actuación. **Nombre aún candidato**; se consideró anteriormente `System Section`.
- **System Step:** operación más concreta dentro de una acción, por ejemplo validar información o persistir cambios.

Estos niveles describen **intención y realización**, no una obligación de separar proyectos, endpoints, clases, Features, servicios o transacciones.

## Continuidad entre ámbitos

| Comprensión / elaboración | Work Semantics | System Realizations |
|---|---|---|
| Cadena de trabajo | Work Chain | — |
| Proceso de trabajo | Work Process | — |
| Acción organizacional y su posible sistematización | Work Flow | System Process |
| Acción funcional en el sistema | — | System Action (candidato) |
| Paso de realización | — | System Step |

**La fila compartida no implica igualdad estructural ni cardinalidad uno a uno**. Un Work Flow puede requerir coordinación de varias capacidades, y diferentes situaciones pueden necesitar realizaciones distintas o ninguna.

Una orientación de elaboración **no obligatoria** es:

```text
Comprender Work Semantics
  → examinar la sistematización
  → descubrir conceptos, comportamientos, restricciones y capacidades
  → expresarlos mediante construcciones pertinentes de VSlices
  → desarrollar y examinar System Realizations
  → revisar lo comprendido cuando exista evidencia
```

La última relación **retroalimenta** las anteriores. No equivale a generar código automáticamente ni a declarar correcta una interpretación por el solo hecho de haberla implementado.

### Ejemplo: crear solicitud de pago DS 49

**Work Semantics:**

```text
Work Chain: Servicio de financiamiento DS 49
  Work Process: Creación de solicitudes DS 49
    Work Flow: Crear solicitud de pago DS 49
```

**System Realizations (descomposición candidata):**

```text
System Process: Atender «Crear solicitud de pago DS 49»
  System Action: Crear solicitud de pago
    System Step: Validar solicitud
    System Step: Persistir cambios
  System Action: Notificar solicitante
  System Action: Notificar revisor
  System Action: Registrar auditoría
```

Esta ilustración **no decide** coordinación síncrona/asíncrona, identidad de servicios, transacciones, consistencia, idempotencia, orden de confirmación, permisos ni autoridad de los datos o del proceso.

### Modelos, actores y diagramas

Las representaciones visuales pueden diferenciar perfiles responsables de las acciones y registrar condiciones o derivaciones cuando aporten significado. La selección de notación (por ejemplo, flowcharts o swimlanes Mermaid) es una decisión de **representación**, no un nuevo nivel de Domain Modeling.

Cada documento debe definir su propio objeto de conocimiento y enlazar a las definiciones propietarias de los demás, evitando diagramas duplicados y fuentes competidoras.

## Arquitectura de solución y límites de autoridad

[Servicio, Producto y Composition](../products/framework/service-product-nexus.md) ofrece una realización de referencia, no una asignación universal:

- Un **Producto/BFF** puede coordinar un System Process a partir de capacidades pertinentes.
- Un **Servicio** conserva sus responsabilidades funcionales, reglas y garantías, sin que ello implique necesariamente un microservicio o repositorio distinto.
- **Composition** ensambla e integra participantes; no se convierte por ello en dueño del comportamiento de negocio.

**System Process no equivale automáticamente a la instancia persistida de un proceso administrada por un orquestador.** Una misma entidad de negocio puede participar en varias instancias de proceso independientes, con sus propias identidades e historias.

La autoridad de definiciones, reglas, transiciones, estados, eventos y persistencia del gestor de flujos compartido **sigue abierta**; este documento no establece un contrato ni decide dónde residirá.

## Movimientos de elaboración candidatos

Los siguientes movimientos expresan **preguntas de estudio y revisión**, no transformaciones automáticas:

- **Concretizar trabajo:** `Work Chain → Work Process → Work Flow`. ¿Qué acciones reconocibles realizan estos procesos y cadenas?
- **Abstraer trabajo:** `Work Flow → Work Process → Work Chain`. ¿Qué proceso o cadena da contexto y propósito a estas acciones?
- **Sistematizar:** `Work Flow → System Process` como posible relación de realización. ¿Qué capacidades, conceptos y restricciones son necesarios?
- **Descubrir y expresar:** durante System Realizations, ¿qué Spaces, Points, Features y Capabilities se justifican, y con qué evidencia?
- **Descomponer realización:** `System Process → System Action → System Step`. ¿Qué responsabilidades y operaciones deben distinguirse?
- **Reexaminar la comprensión:** desde las realizaciones y la observación, ¿qué hipótesis de Work Semantics deben revisarse?

No hay correspondencia universal obligatoria entre niveles, ni inferencia de significado organizacional a partir de nombres de APIs o clases.

## Relación con VSlices Suite

- **Design** puede apoyar el descubrimiento, la delimitación y la revisión de modelos, decisiones y evidencias.
- **Method** puede orientar cuándo profundizar, sistematizar o revisar.
- **Docs Standard** puede apoyar su documentación trazable y navegable.
- **Framework** conserva la autoridad de sus conceptos de Spaces, Work, Grounding y Hosting.
- **Tooling** puede explorar representaciones o validaciones, sin que esta definición implique una implementación existente.

Domain Modeling **no sustituye** esos productos ni les impone contratos técnicos nuevos. Su responsabilidad aquí es preservar la continuidad del significado entre la comprensión del dominio y las realizaciones estudiadas.

## Límites y preguntas abiertas

- La jerarquía y los nombres de Work Semantics y System Realizations son modelos **candidatos**, sujetos a evidencia de casos reales.
- `System Action` sigue siendo una denominación provisional; también pueden revisarse `Work Flow` y otros nombres.
- Está abierta la cardinalidad y el alcance preciso de las relaciones entre acciones organizacionales, funcionalidades, capacidades y realizaciones.
- No existe aquí especificación ejecutable, generación automática ni garantía de universalidad.
- La comprensión organizacional no es infalible; una realización tampoco se convierte automáticamente en autoridad para reescribirla.

## Trayectoria de revisión

**Posición original — Action Flow:** se entendía el mecanismo principalmente como representación de acciones semánticas, sus relaciones y consecuencias, con niveles de trabajo organizacional y de sistema. El nombre sugería que la existencia de un flujo era condición de todo el modelado.

**Primera revisión — Work Modeling (2026-11-10):** se reconoció que el trabajo puede modelarse sin una secuencia de acciones y que un Work Process no necesita reproducir el interior de cada Work Flow. Se adoptó temporalmente [Work Modeling](work-modeling.md) y se conservó la entrada de [Action Flow](action-flow.md).

**Tensión posterior:** Work Modeling tampoco expresaba plenamente el alcance: al examinar cómo sistematizar el trabajo se **descubren conceptos, comportamientos y capacidades** que deben modelarse y expresarse con construcciones propias de VSlices. Tratar Spaces y Features como una tercera perspectiva paralela separaba artificialmente ese descubrimiento de la realización.

**Revisión acordada — Domain Modeling (2026-11-10):** se toma la acepción de `Domain` compartida con Eric Evans y DDD, **sin adoptar obligatoriamente sus procedimientos ni taxonomía**. El modelo parte de **Work Semantics** —cómo la organización entiende y coordina su trabajo— y avanza, con revisión iterativa, hacia **System Realizations**, descubriendo y elaborando en ese avance los conceptos pertinentes. No son dos catálogos aislados.

**Estado posterior:** `Domain Modeling` es el nombre vigente del mecanismo candidato. Los nombres anteriores permanecen como entradas históricas y en Git; el razonamiento sobre límites, alternativas y denominaciones previas no se reescribe como si siempre se hubiera adoptado el modelo actual.

**Evidencia que motivó el cambio:** la revisión de «Gestión de solicitud de soporte» y su distinción entre Work Process, Work Flows, actores/perfiles y realización de Ticket Service; además de las definiciones ya vigentes de Framework para Spaces y Work.
