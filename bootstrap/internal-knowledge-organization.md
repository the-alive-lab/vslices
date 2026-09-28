> **Bootstrap evidence**
>
> Este documento fue la propuesta monolítica que precedió a la superficie provisional `future-steps/suite/`.
> Se conserva como evidencia histórica. Las definiciones distribuidas bajo `suite/` tienen prioridad cuando exista diferencia de organización o ownership.
>
> Ruta original: `future-steps/internal-knowledge-organization.md`

# Organización interna del conocimiento de VSlices

## Estado

Propuesta de siguiente paso.

Este documento no define todavía la estructura pública de la documentación ni una taxonomía definitiva de VSlices.

Su objetivo es preservar el entendimiento actual sobre cómo se relacionan los productos, conceptos, técnicas y evidencia de la suite, y proponer una forma de organizar ese conocimiento internamente antes de decidir cómo presentarlo al mundo.

## Motivación

El problema actual no es solamente que existan documentos desactualizados.

Durante la evolución reciente de VSlices se han hecho más explícitas varias distinciones que atraviesan más de un producto:

- qué entendemos por `Domain`, `Domain Knowledge` y `Domain Model`;
- la separación entre semántica, autoridad, mecanismo y realización;
- la aparición de `Space`, `Work` y `Grounding` como superficies semánticas emergentes;
- el uso de evidencia explícita cuando un hecho no puede derivarse desde el conocimiento disponible;
- la identificación de `Semantic Pressure` como una técnica base de trabajo;
- y una separación más clara de responsabilidades entre Design, Method, Docs Standard, Framework y Tooling.

Si estas ideas se documentan únicamente dentro de cada producto, existe riesgo de duplicar definiciones, introducir matices incompatibles y perder trazabilidad sobre quién tiene autoridad para definir cada concepto.

Antes de rediseñar la documentación pública conviene organizar primero el conocimiento interno de VSlices.

## Distinciones de base

### Domain

`Domain` es el ámbito de realidad, conocimiento o actividad acerca del cual una responsabilidad de software necesita comprender, representar, apoyar o actuar.

El dominio no es una capa arquitectónica ni equivale al antiguo namespace `VSlices.Domain`.

El abandono de `Domain`, `Application` e `Infrastructure` como descomposición semántica primaria del Framework no implica abandonar el concepto de dominio.

### Domain Knowledge

`Domain Knowledge` es el conocimiento que un actor o sistema posee, adquiere, infiere o preserva acerca de un dominio.

### Domain Model

`Domain Model` es una representación selectiva y estructurada de `Domain Knowledge` construida para un propósito.

No pretende agotar el dominio ni convertir todo conocimiento disponible en software.

Una relación útil es:

```text
Domain
    -> knowledge about it
Domain Knowledge
    -> selective formalization
Domain Model
```

## Semantic-Oriented Domain Modeling

`Semantic-Oriented Domain Modeling` continúa siendo un nombre de trabajo.

Describe provisionalmente una dirección donde la representación se deja determinar progresivamente por las distinciones semánticas descubiertas —significado, estructura, relaciones, admisibilidad, transformación, trabajo, autoridad y evidencia requerida— en vez de partir desde una taxonomía arquitectónica o de programación prefijada.

No debe presentarse todavía como disciplina cerrada, taxonomía completa ni afirmación de novedad académica.

Su ubicación conceptual exacta dentro de la suite todavía debe seguir validándose. Actualmente se manifiesta con especial fuerza en la evolución de Framework, pero sus consecuencias alcanzan también Design, Method y Docs Standard.

## Space, Work y Grounding

Las superficies `Space`, `Work` y `Grounding` no deben entenderse como reemplazos mecánicos de `Domain`, `Application` e `Infrastructure` ni como particiones exhaustivas del dominio.

Son superficies semánticas emergentes utilizadas para representar fenómenos distintos descubiertos durante el modelado.

### Space

`Space` representa espacios de valores, estructura semántica o algebraica, relaciones, admisibilidad y transformaciones puras.

### Work

`Work` representa trabajo ejecutable: comportamiento, coordinación, capacidades, efectos, errores esperados y cambios relevantes.

### Grounding

`Grounding` representa la adquisición de evidencia requerida cuando un hecho no puede derivarse únicamente desde el conocimiento actualmente disponible para el razonamiento o la computación.

La evidencia no tiene por qué ser externa al dominio.

Puede tratarse de un hecho perteneciente al propio dominio cuyo valor concreto debe observarse o establecerse mediante una fuente con autoridad suficiente.

Una factorización actualmente útil es:

```text
effectful acquisition
    -> explicit evidence
    -> pure transformation
```

## Semantic Pressure

`Semantic Pressure` es actualmente una técnica candidata de VSlices Method.

Consiste en interrogar deliberadamente el significado de un fenómeno hasta hacer visibles supuestos, distinciones, restricciones, autoridad y evidencia requerida que permanecían implícitos.

Ejemplos de preguntas de presión semántica:

- ¿Qué significa exactamente este término?
- ¿Qué lo distingue de otro concepto parecido?
- ¿Quién tiene autoridad para establecer este hecho?
- ¿Qué debe ser cierto antes o después?
- ¿Qué evidencia se necesita?
- ¿De dónde puede obtenerse esa evidencia?
- ¿Qué puede derivarse y qué debe observarse?
- ¿Qué puede fallar de forma esperada?
- ¿Qué cambia como consecuencia?

La presión semántica no existe para maximizar la cantidad de preguntas.

Debe aplicarse hasta reducir la incertidumbre relevante o hasta hacer explícito que falta conocimiento que no puede inventarse responsablemente.

Una formulación útil es:

> Formalizar mediante comprensión, usando presión semántica.

## Responsabilidades actuales de los productos

La evolución reciente sugiere una separación más clara de responsabilidades.

### Independencia de los productos y rol de Method

Una propiedad importante de la suite es que sus productos deberían conservar valor independiente dentro de su propia responsabilidad.

En particular:

- VSlices Design puede utilizarse sin adoptar VSlices Method, Docs Standard o Framework;
- VSlices Docs Standard puede utilizarse para organizar y preservar conocimiento sin requerir Method o Framework;
- VSlices Framework puede utilizarse para modelar y materializar semántica de software sin exigir la adopción de Method o Docs Standard;
- VSlices Tooling puede utilizarse para operar capacidades soportadas de otros productos sin depender de Method.

VSlices Method es la excepción intencional.

Su responsabilidad es actuar como nexo metodológico entre los demás productos durante trabajo real: seleccionar, combinar y navegar sus capacidades según la incertidumbre, el conocimiento disponible y las necesidades del esfuerzo.

Esto tampoco implica que Method deba utilizar todos los productos en cada caso. Puede coordinar sólo los que aporten valor en una situación concreta.

Una regla candidata es:

> Cada producto de VSlices debería proporcionar valor independientemente dentro de su responsabilidad. VSlices Method es la excepción intencional porque su responsabilidad consiste en componer y navegar los demás productos durante trabajo real.

Tooling tampoco debe interpretarse como subordinado a Method.

Method conecta productos desde la organización del trabajo humano. Tooling operacionaliza capacidades soportadas directamente allí donde corresponda.


### VSlices Design

VSlices Design define estructuras, modalidades y herramientas de razonamiento que permiten organizar cómo abordar un problema de ingeniería.

Actualmente incluye formas de trabajo como:

- `Context-First`;
- `Problem-First`;
- `Slice-First`.

Design describe estas formas y los criterios conceptuales que las hacen útiles.

No debería absorber la navegación metodológica completa entre ellas.

### VSlices Method

VSlices Method organiza cómo se realiza y navega el trabajo real utilizando los demás productos.

Method puede:

- seleccionar una estructura de trabajo definida por Design;
- navegar entre `Context-First`, `Problem-First` y `Slice-First` según cambie la incertidumbre;
- aplicar técnicas de trabajo como `Semantic Pressure`;
- organizar colaboración y coordinación de equipos;
- decidir qué conocimiento necesita preservarse mediante Docs Standard;
- utilizar Framework cuando exista semántica suficientemente entendida para materializar;
- incorporar feedback de implementación, validación y operación de vuelta al entendimiento.

Una representación aproximada es:

```text
Design
    -> ofrece formas de razonar y abordar el trabajo

Method
    -> selecciona, combina y navega esas formas durante trabajo real
    -> aplica técnicas como Semantic Pressure
    -> coordina el uso de los productos que resulten necesarios
```

### VSlices Docs Standard

VSlices Docs Standard define cómo organizar, relacionar y preservar conocimiento.

Sus artefactos no son solamente plantillas.

La estructura de preguntas observada en Alive Lab muestra que pueden funcionar como superficies de exploración y preservación del conocimiento descubierto durante el trabajo.

Por ejemplo, un `Domain Vocabulary` puede aplicar presión sobre significado y ambigüedad; un `Behavior Document` puede hacer explícito qué debe ocurrir; un `Continuity Path` puede preservar relaciones entre perspectivas sin convertir cada nodo en documentación obligatoria.

Una relación útil es:

```text
Semantic Pressure
    -> discovers distinctions

Docs Standard
    -> preserves and relates discovered knowledge
```

### VSlices Framework

VSlices Framework define cómo conocimiento suficientemente explícito puede materializarse como semántica ejecutable y, mediante realizaciones tecnológicas, convertirse progresivamente en software.

Framework no debe confundirse con una única biblioteca, con .NET, con LanguageExt, con DDD ni con programación funcional.

La realización .NET es actualmente un laboratorio especialmente importante para validar conceptos como `Space`, `Work`, `Grounding`, transformaciones, autoridad y evidencia.

### VSlices Tooling

VSlices Tooling hace operables, repetibles y verificables mecanismos soportados por la suite.

Su relación con los demás productos es transversal y no pasa necesariamente por Method.

Actualmente esta relación es especialmente visible con:

- **VSlices Docs Standard**, donde Tooling puede apoyar generación, validación, navegación, visualización, identidad, relaciones, metadata y otras operaciones sobre artifacts documentales;
- **VSlices Framework**, donde Tooling puede apoyar VSIR, Rulesets, lowering, rebase, validación, target context y materialización;
- otras superficies de la suite cuando aparezcan capacidades operables suficientemente definidas y exista evidencia para automatizarlas.

Tooling puede apoyar un producto sin convertirse en dueño de su semántica.

La autoridad permanece en el producto o superficie que define el concepto; Tooling implementa o coordina mecanismos que lo hacen operable.

Una relación útil es:

```text
Method
    -> connects products through human engineering work

Tooling
    -> operationalizes supported capabilities across products
```

Por lo tanto, Tooling no debería modelarse como una dependencia subordinada a Method.

Tooling no debería convertirse en la fuente de semántica únicamente porque automatiza una operación.

Debe conservar la separación entre:

- semántica;
- autoridad;
- mecanismo;
- realización;
- evidencia.

## Consecuencia para la organización interna

La documentación actual está organizada principalmente por producto, pero el conocimiento de VSlices no tiene una única naturaleza.

Antes de reorganizar las carpetas públicas conviene reconocer al menos estas categorías candidatas:

### Foundations

Conceptos compartidos por la suite que ningún producto debería redefinir de manera independiente.

Candidatos actuales:

- Domain;
- Domain Knowledge;
- Domain Model;
- Semantics;
- Semantic Authority;
- Evidence;
- Representability;
- Admissibility;
- Continuity;
- Transformation;
- Realization;
- Materialization;
- Unknown / Underdetermination.

### Product knowledge

Conocimiento cuya autoridad pertenece principalmente a un producto.

Ejemplos:

- Design modes;
- Method navigation;
- Docs Standard artifacts;
- Framework semantic surfaces;
- Tooling lowering mechanisms.

### Techniques

Acciones o prácticas repetibles utilizadas durante el trabajo.

Candidato actual principal:

- Semantic Pressure.

Otros candidatos deberán descubrirse desde uso real antes de crear una taxonomía extensa.

### Principles

Criterios que orientan decisiones sin describir necesariamente una acción concreta.

Ejemplos actuales incluyen preservar intención, hacer visible la incertidumbre, preferir evidencia antes de generalizar y evitar inventar conocimiento faltante.

### Research and hypotheses

Ideas todavía bajo validación que no deberían presentarse como conocimiento canónico sólo porque resultan prometedoras.

Alive Lab ya cumple parcialmente esta responsabilidad.

### Evidence

Casos, migraciones, experimentos, observaciones y resultados que soportan, tensionan o contradicen conceptos y técnicas.

La evidencia debería permanecer distinguible de la definición que ayuda a sostener.

```text
definition
    != history
    != evidence
```

## Ownership explícito

Cada concepto importante debería poder responder:

- ¿Qué clase de conocimiento es?
- ¿Quién tiene autoridad principal para definirlo?
- ¿Qué productos lo utilizan?
- ¿Cuál es su estado de madurez?
- ¿Dónde está su definición canónica?
- ¿Qué evidencia lo sostiene o tensiona?

Una forma mínima candidata de representarlo podría ser:

```yaml
concept:
  name: Semantic Pressure
  owner: method
  kind: technique
  status: candidate
```

Otro ejemplo:

```yaml
concept:
  name: Grounding
  owner: framework
  kind: semantic-surface
  status: emerging
```

Y para conceptos compartidos:

```yaml
concept:
  name: Domain
  owner: suite
  kind: foundation
  status: active
```

Este formato es sólo una hipótesis de organización. No debería convertirse en schema antes de validarlo contra conceptos reales.

## Rol de Alive Lab

Alive Lab debería continuar funcionando como superficie de observación, experimentación y preservación de evidencia antes de promover conocimiento a una definición canónica.

Un flujo posible es:

```text
observation
    -> candidate idea
    -> repeated evidence
    -> conceptual stabilization
    -> promotion
    -> canonical VSlices knowledge
```

Una técnica como `Semantic Pressure` puede preservar inicialmente sus observaciones y casos en Alive Lab mientras su definición canónica permanece pequeña y revisable.

Esto permite conservar por qué creemos algo sin convertir toda la historia de descubrimiento en parte de la definición pública del concepto.

## Propuesta de reestructuración interna

No se propone todavía mover masivamente archivos.

Primero conviene construir y validar un modelo mínimo de organización del conocimiento.

Una estructura conceptual candidata es:

```text
VSlices Knowledge
|
|-- Foundations
|-- Principles
|-- Product Concepts
|-- Modes
|-- Techniques
|-- Artifacts
|-- Mechanisms
|-- Hypotheses
`-- Evidence
```

Las relaciones relevantes podrían incluir:

```text
owned-by
used-by
realized-by
preserved-by
supported-by
challenged-by
derived-from
supersedes
```

Esta lista no debe tratarse como taxonomía final.

Debe ser presionada contra casos reales antes de establecer una estructura física de carpetas o schemas.

## Caso mínimo de validación

Antes de reorganizar el repositorio completo, conviene intentar clasificar un conjunto pequeño pero diverso de conceptos:

- Domain;
- Domain Knowledge;
- Domain Model;
- Context-First;
- Problem-First;
- Slice-First;
- Semantic Pressure;
- Document;
- Continuity Path;
- Semantic-Oriented Domain Modeling;
- Space;
- Work;
- Grounding;
- Evidence.

Para cada uno deberíamos poder responder:

1. ¿Qué significa?
2. ¿Qué clase de conocimiento es?
3. ¿Quién tiene autoridad para definirlo?
4. ¿Quién lo utiliza?
5. ¿Dónde está definido hoy?
6. ¿Qué evidencia lo sostiene?
7. ¿Qué tan estable está?
8. ¿Qué relaciones tiene con otros conceptos?

Si el modelo organiza estos casos sin forzarlos, tendremos mejor evidencia para convertirlo en estructura documental.

## Documentación interna y presentación pública

La estructura interna del conocimiento no tiene por qué ser idéntica a la navegación que finalmente vea un usuario externo.

Primero necesitamos una superficie interna donde las definiciones sean consistentes, trazables y tengan ownership claro.

Después podremos diseñar distintas proyecciones públicas según la necesidad:

- aprender VSlices desde cero;
- entender un producto;
- aplicar VSlices a un proyecto;
- consultar una técnica;
- comprender una abstracción de Framework;
- revisar evidencia o decisiones históricas.

La documentación pública debería ser una proyección deliberada de conocimiento internamente organizado, no la fuente accidental de su estructura conceptual.

## Próximos pasos propuestos

1. Corregir las definiciones de responsabilidad de Design, Method, Docs Standard, Framework y Tooling en las superficies internas que todavía mezclen sus funciones.
2. Registrar `Semantic Pressure` como técnica candidata de Method sin declarar todavía una taxonomía completa de técnicas.
3. Construir el inventario mínimo de conceptos descrito en este documento.
4. Identificar para cada concepto su definición actual, ownership, estado y evidencia.
5. Detectar duplicaciones y contradicciones entre la documentación existente.
6. Validar la clasificación candidata contra casos reales y contra Alive Lab.
7. Sólo después proponer una nueva estructura física para el conocimiento canónico.
8. Diseñar posteriormente cómo ese conocimiento se proyectará hacia documentación pública.

## Criterio de cierre

La reestructuración no debería buscar una jerarquía más elegante por sí misma.

Debería lograr que podamos reconstruir con claridad:

```text
qué significa algo
    -> quién lo define
    -> dónde se preserva
    -> cómo se utiliza
    -> cómo se materializa
    -> qué evidencia lo sostiene
    -> cómo evolucionó
```

Si una nueva organización no mejora esa continuidad, no justifica el costo de reestructurar la documentación.
