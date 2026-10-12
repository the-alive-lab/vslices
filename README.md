> **Idiomas / Languages:** **Español (versión principal)** · [English](README.en.md)
>
> El español y el inglés son idiomas oficiales de comunicación de este repositorio. Se prioriza el español como idioma de entrada y comunicación predeterminado. Ambas versiones deben preservar el mismo significado conceptual.

# Suite VSlices

Este repositorio es la **fuente canónica de verdad para la Suite VSlices y todos sus productos** (Method, Design, Docs Standard, Framework, Tooling y otros). Preserva los significados fundamentales a partir de los cuales pueden desarrollarse distintas proyecciones posteriores.

Define conceptos transversales de la Suite y específicos de sus productos, identidades y responsabilidades de productos, procesos, intenciones y, cuando corresponde, restricciones normativas. Esto no significa que cada concepto deba convertirse en una especificación prescriptiva ni que todas las proyecciones posibles deban representarse aquí.

**No es** el sitio de documentación pública, un repositorio de implementación ni necesariamente el lugar donde se elabora cada realización posterior.

## Responsabilidad

Este repositorio puede:

- definir fundamentos compartidos;
- definir mecanismos cuya identidad pertenece a VSlices de manera transversal a sus productos;
- definir propósitos, responsabilidades, conceptos y procesos de productos, así como sus límites;
- preservar relaciones entre productos;
- registrar modelos candidatos de ciclo de vida o diseño que afectan a más de un producto mientras todavía se valida su pertenencia;
- preservar el historial de promoción y las preguntas de autoridad aún no resueltas.

No debe:

- eliminar la responsabilidad interna de un producto solo porque su fuente esté alojada aquí;
- duplicar una misma definición en rutas de la Suite y de sus productos;
- convertir una realización actual en una definición universal;
- promover una hipótesis útil a semántica estable únicamente porque ya tenga un nombre.

## Regla de autoridad

```text
semántica transversal de la Suite
    -> definida aquí, bajo responsabilidad de la Suite

semántica específica de un producto
    -> definida aquí, dentro del espacio conceptual de ese producto

investigación / pertenencia incierta
    -> preservada como evidencia candidata o pregunta explícita de pertenencia
```

Un producto puede utilizar, documentar, realizar, especializar, representar, validar u operacionalizar un mecanismo de VSlices sin convertirse por ello en la autoridad que define su semántica fundamental.

**El alojamiento canónico centralizado no elimina las responsabilidades propias de cada producto.** Design, Method, Tooling, etc., conservan una responsabilidad conceptual diferenciada aunque sus definiciones residan en un mismo repositorio.

**Autoridad según granularidad:** un repositorio oficialmente reconocido como específico de un producto puede mantener **especificaciones normativas** detalladas y versionadas (por ejemplo, contratos del lenguaje VSIR 0.1 o YAML de definición de artefactos de Docs Standard) que especialicen las definiciones conceptuales alojadas aquí. Esos contratos rigen la conformidad con la versión que declaran; no son simplemente código de implementación o documentación pública. No pueden redefinir silenciosamente la identidad del producto, las responsabilidades entre productos ni el significado de una versión anterior. Cualquier conflicto conceptual debe exponerse para revisión, con su procedencia, en lugar de borrarse eligiendo la ubicación más conveniente.

Del mismo modo, la ubicación física no determina la autoridad semántica.

## Madurez

Las definiciones deberían explicitar su madurez.

Entre los estados útiles se encuentran:

- `candidate` (candidato);
- `emerging` (emergente);
- `active` (activo);
- `stable` (estable);
- `superseded` (reemplazado).

Por ahora, estas etiquetas describen estados de trabajo; todavía no constituyen un esquema universal.

## Estructura actual

```text
the-alive-lab/vslices/
├── foundations/
├── mechanisms/
├── lifecycle/
├── forces/                # carpeta histórica; actualmente Orientation Factors
├── playgrounds/
├── products/
├── relationships/
├── promotion/
└── bootstrap/
```

### Fundamentos

Conceptos compartidos que necesitan varios productos sin redefinirlos independientemente.

### Mecanismos

Mecanismos reutilizables de VSlices y relaciones explícitas entre mecanismos de distintos productos.

Que un mecanismo sea aplicable a varios productos no convierte por sí solo a la Suite en su responsable conceptual. La pertenencia y la aplicabilidad deben registrarse por separado.

Candidatos actuales:

- [Action Flow](mechanisms/action-flow.md)
- [Semantic Pressure](mechanisms/semantic-pressure.md) — pertenece a Method, con aplicabilidad transversal a la Suite
- [Value Orientations](mechanisms/value-orientations.md) — modelo candidato actual para tres prioridades de valor de negocio; las fuentes históricas [Least Resistance](mechanisms/path-of-least-resistance.md), [Most Continuity](mechanisms/path-of-most-continuity.md) y [Most Value](mechanisms/path-of-most-value.md) Path se conservan por procedencia
- [Documentary Reinterpretation](mechanisms/documentary-reinterpretation.md) — candidato de reinterpretación de impacto mediante relaciones del front matter de Docs Standard; todavía no es ejecutable en Tooling

### Ciclo de vida

El ciclo de vida iterativo aprobado de cinco fases pertenece ahora a **Design**, en [products/design/lifecycle.md](products/design/lifecycle.md). La superficie de ciclo de vida de la Suite preserva el contexto entre productos y las transiciones históricas, no una autoridad competidora sobre las fases. [Orientation](products/method/orientation.md) pertenece a Method; sus mecanismos operacionales detallados siguen en revisión.

### Factores de orientación

La ruta existente `forces/` preserva la continuidad con el nombre anterior **Work Forces**. [Orientation Factors](forces/README.md) es el término candidato revisado para las clasificaciones Semántica, Técnica, de Entrega y de Recursos de la evidencia interpretada. Sus cambios justificados pueden informar a [Value Orientations](mechanisms/value-orientations.md); [Documentary Reinterpretation](mechanisms/documentary-reinterpretation.md) explora el impacto iterativo mediante relaciones documentales.

Su afinidad actual de pertenencia más fuerte es con Design.

### Productos

Definiciones canónicas de productos y límites de sus responsabilidades, incluido [VSlices Design](products/design/README.md). Los significados específicos de cada producto se definen aquí, bajo el espacio de nombres del producto responsable; los repositorios de realización independientes son proyecciones, no fuentes de verdad competidoras.

### Relaciones

Cómo se define la pertenencia de las definiciones y cómo estas se utilizan, realizan, preservan, representan, operacionalizan, respaldan o cuestionan.

### Promoción

Cómo las ideas pasan de la observación al conocimiento canónico sin reescribir su historia.

### Bootstrap

Evidencia histórica que condujo a esta superficie, incluida la propuesta original de conocimiento interno y las instantáneas de fuentes de contexto del proyecto preservadas antes de que este repositorio se volviera canónico.

Véase [`bootstrap/`](bootstrap/README.md).

El material de bootstrap constituye evidencia, no autoridad vigente.

## Definición, intención, especificación y proyección

El repositorio canónico es la **fuente** de conceptos, productos, procesos y otros elementos que pueden justificar una proyección posterior. Varias categorías útiles pueden superponerse:

- **Definición**: establece qué significa un concepto, responsabilidad, producto o proceso.
- **Intención**: establece qué resultado busca una realización y por qué.
- **Especificación**: hace examinables las restricciones u obligaciones de una realización.
- **Proyección**: interpreta, expresa o materializa significados e intenciones canónicas seleccionadas en un contexto específico.

Son distinciones de responsabilidad, **no** un formato obligatorio de cuatro documentos ni un proceso lineal. «Especificación» no es sinónimo de todo lo canónico: los conceptos explicativos, los objetivos y las preguntas abiertas pueden ser fuentes importantes sin constituir contratos de implementación.

Ejemplos:

- **La definición canónica de Tooling** describe las capacidades y restricciones que debería proporcionar. Su implementación es una realización o proyección técnica, y los detalles de esa implementación no redefinen automáticamente la fuente.
- **La documentación pública** proyecta conceptos de VSlices con una intención pedagógica, y una implementación web realiza además esa intención mediante páginas, navegación e interacción.
- **TDidacta** puede aportar metodologías pedagógicas, diseño y examen de esa intención sin adquirir autoridad para redefinir conceptos de VSlices. Que la intención pedagógica sea canónica para una publicación concreta o pertenezca a un artefacto separado con su propia gobernanza depende de la responsabilidad en cuestión; no se implica ninguna transferencia automática de pertenencia.

```text
the-alive-lab/vslices
  conceptos + productos + procesos + intenciones + restricciones
       |                            |
       +--> realización de Tooling  +--> proyección pedagógica
                                           |
                                           +--> publicación web (vslices/docs)
```

Las ramas son ilustrativas, no exhaustivas ni necesariamente secuenciales. Las fuentes y proyecciones deberían conservar vínculos con los significados y las intenciones que las justifican. La nueva evidencia procedente de una realización puede **cuestionar** una fuente, pero no sobrescribe silenciosamente su autoridad.

## Principio de la Suite — proyección fundamentada

**Los artefactos y las realizaciones deberían surgir como proyecciones justificadas de problemas, necesidades y requisitos comprendidos, mediante la continuidad preservada acerca de ellos.**

Las historias de usuario, pantallas, API, tablas de bases de datos, tareas de implementación, modelos, documentos y comportamientos ejecutables no son simplemente nombres distintos para requisitos o problemas. Son **proyecciones** potenciales de significados, decisiones y restricciones comprendidos progresivamente, en formas adecuadas a sus propias responsabilidades.

Es una expectativa **transversal a la Suite**, no una restricción que pertenezca solamente a Design:

- **Comprensión y continuidad** permiten reconstruir el problema de origen, los requisitos pertinentes, la incertidumbre, la evidencia y la intención.
- **Design** explora y justifica respuestas sin dar por hecho que un artefacto solicitado o una funcionalidad de software ya estén justificados.
- **Method** coordina cómo contribuyen las responsabilidades de los productos participantes y cómo se conserva el contexto en que se sitúan.
- **Docs Standard** puede preservar las distinciones y sus relaciones sin exigir un documento por cada proyección.
- **Framework y Tooling** pueden expresar o realizar semánticas seleccionadas de forma ejecutable u operacional sin heredar autoridad para redefinir su origen.

Una proyección **no es una copia mecánica**. Puede especializar o transformar significados y revelar nuevas restricciones o evidencia. Esa evidencia puede justificar la revisión de la comprensión y de los requisitos anteriores; no debe cambiar silenciosamente su autoridad ni borrar la razón de ser de una proyección.

El principio **no** exige que cada artefacto de bajo nivel tenga una traza escrita independiente, que cada resultado sea software ni que toda solicitud observada se convierta en un requisito validado. Exige que **las decisiones materiales sigan siendo explicables a partir de los problemas y requisitos que abordan**, con un nivel de continuidad proporcional a sus consecuencias.

### Superficies de proyección más allá de los productos de VSlices

Una proyección no se limita a la implementación de un producto de la Suite ni a la documentación publicada. **Surreal Atlas** y posibles aplicaciones de gestión de trabajo (incluidos sistemas funcionalmente análogos a Jira) pueden proporcionar distintas **superficies de proyección** sobre problemas, requisitos, decisiones y su continuidad fundamentados.

Algunos ejemplos de vistas posibles son mapas semánticos y relaciones navegables, elementos de trabajo y estados de asignación, explicaciones pedagógicas y representaciones operacionales. Son **posibilidades ilustrativas**, no afirmaciones de que ya exista una integración concreta o un modelo de almacenamiento compartido.

Una superficie de proyección puede registrar nuevas observaciones, asignaciones o cambios de estado del trabajo dentro de su propia autoridad. Estos hechos pueden convertirse en evidencia que informe la comprensión subyacente; no redefinen automáticamente el problema, requisito o intención proyectados.

**No deben confundirse la autoridad conceptual, la representación, el almacenamiento y la responsabilidad operacional.** El principio no exige una base de datos central universal, un mecanismo prescrito de sincronización bidireccional ni esquemas idénticos entre superficies. Cada implementación concreta debe establecer cómo preserva la procedencia y evita significados competidores cuando corresponda.

### Trayectoria de la decisión

El planteamiento anterior de Design advertía contra la confusión de historias de usuario, pantallas, API, tablas y tareas de implementación con problemas o requisitos. La reformulación transversal a la Suite fortalece esa advertencia: pasa de prohibir la confusión a establecer una **relación positiva de proyección fundamentada**, compartida entre productos. Design conserva su metodología de comprensión y justificación, pero no es propietario del principio general.

## Documentación pública

`vslices/docs` es una **proyección didáctica y web** de los significados canónicos de VSlices, no la autoridad que establece esos significados. Su intención pedagógica y la realización de su sitio web pueden distinguirse aun cuando estén alojadas en un mismo proyecto.

## Regla de reconstrucción

1. Consultar **este repositorio** para los significados canónicos de la Suite **y de cada producto VSlices**.
2. Consultar las **especificaciones especializadas oficiales** para conocer sus contratos detallados y versionados, y los repositorios de implementación o publicación para obtener evidencia de las realizaciones efectivas y de la retroalimentación. Ni una implementación concreta ni una publicación cambian automáticamente la autoridad conceptual subyacente.
3. Utilizar Research y los artefactos históricos para reconstruir la emergencia de conceptos, poner a prueba afirmaciones y señalar preguntas de pertenencia aún no resueltas.
4. Registrar explícitamente las revisiones sustantivas de las fuentes canónicas y propagar sus resultados a las proyecciones pertinentes, en lugar de reescribir silenciosamente la historia.
