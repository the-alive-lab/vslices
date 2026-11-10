# Work Modeling — comprensión del trabajo y continuidad hacia su realización

**Estado:** `candidate` — nombre **Work Modeling** acordado el 2026-11-10; alcance y frontera con la realización sistematizada sujetos a examen; vocabulario de acción de sistema aún candidato.  
**Responsabilidad conceptual:** VSlices Suite.  
**Procedencia:** evolución de la definición candidata «Action Flow» en conversación de Hernán y Limen (2026-11-10), contrastada con el modelado de la ticketera de Serviu. Conserva el antecedente del caso «Crear solicitud de pago DS 49» y la arquitectura Producto/Servicio/Composition.

## Propósito

**Work Modeling** permite comprender y representar el trabajo organizacional mediante actividades, participantes, responsabilidades, condiciones, relaciones y consecuencias, preservando su significado cuando se estudian o diseñan sus realizaciones sistematizadas.

El trabajo puede reconocerse aunque no exista una secuencia lineal ni un flujo explícito. Una **acción**, un **proceso** y una **cadena de trabajo** expresan niveles distintos: ninguno debe utilizarse automáticamente como nombre de todo el mecanismo.

**Límite abierto:** esta definición conserva por continuidad la perspectiva de realización de sistema que ya trataba Action Flow; aún debemos decidir si dicha perspectiva forma parte de Work Modeling o se articula como un modelado relacionado de **System Realization**. El cambio de nombre no decide esa frontera ni crea mecanismos separados.

Un flujo no es necesariamente una secuencia técnica de instrucciones ni una operación CRUD genérica: representa una acción con significado propio. Por ejemplo, «Actualizar subtítulo» y «Actualizar tipo» son acciones distintas aunque puedan compartir mecanismos de actualización.

## Dos perspectivas

### Perspectiva organizacional — trabajo

Representa trabajo sin comprometerse con una realización técnica. Puede expresar acciones, condiciones, alternativas, cardinalidad, responsables, derivaciones, repetición y consecuencias.

Se distinguen tres niveles de elaboración organizacional:

- **Work Chain (cadena de trabajo):** cadena de producción o servicio que atraviesa áreas o departamentos. Ejemplo: «Servicio de financiamiento de proyectos relacionados al DS 49».
- **Work Process (proceso de trabajo):** parte reconocible de esa cadena, que contribuye a su producción. Ejemplo: «Proceso de creación de solicitudes asociadas al DS 49».
- **Work Flow (flujo de trabajo):** **acción semántica específica** dentro de un proceso. Ejemplo: «Crear solicitud de pago DS 49».

**Work Chain reemplaza a Work Line en esta jerarquía candidata revisada.** La denominación histórica `Work Line` se conserva en la trayectoria de revisión y no se debe tratar como un nivel adicional silencioso.

### Perspectiva de realización — sistema (alcance por revisar)

Describe cómo un sistema y sus participantes realizan acciones identificables.

- **System Process (proceso de sistema):** coordinación de acciones de sistema para realizar una intención reconocible, por ejemplo «Crear solicitud de pago DS 49» en la frontera operacional del producto.
- **System Action (acción de sistema; nombre candidato):** capacidad o acción semántica específica participante del proceso, por ejemplo «Crear solicitud de pago», «Notificar solicitante», «Notificar revisor» o «Registrar auditoría de la acción», cada una dentro de la responsabilidad funcional que corresponda.
- **System Step (paso de sistema):** operación más concreta de realización de una acción, por ejemplo «Validar solicitud de pago» o «Persistir cambios realizados».

La etiqueta **`System Action` es candidata**: en la discusión también se consideró `System Section` / «sección», todavía sin contrato terminológico definitivo. Se prefiere provisionalmente «acción» porque nombra comportamiento con intención, no solamente una partición estructural. **No introducir nuevos tipos de VSIR ni exigir nombres de clases o interfaces por este cambio documental.**

La identidad semántica de una acción **no obliga** a crear un endpoint, Feature, clase, repositorio o servicio separado.

## Matriz de correspondencia revisada

| Nivel | Organización | Sistema | Ejemplo |
|---|---|---|---|
| Cadena | **Work Chain** | — | Servicio de financiamiento de proyectos relacionados al DS 49 |
| Proceso organizacional | **Work Process** | — | Proceso de creación de solicitudes asociadas al DS 49 |
| Flujo organizacional / realización coordinada | **Work Flow** | **System Process** | «Crear solicitud de pago DS 49» como intención de negocio y su coordinación sistematizada |
| Acción funcional | — | **System Action** *(candidato)* | Crear solicitud; notificar solicitante; notificar revisor; registrar auditoría |
| Paso de realización | — | **System Step** | Validar solicitud; persistir cambios |

**La fila compartida no representa identidad automática ni una correspondencia uno a uno.** Indica una relación de **sistematización** entre una acción organizacional reconocible (`Work Flow`) y un proceso que coordina su realización (`System Process`). Un mismo nombre de acción puede aparecer en ambos niveles y significar cosas distintas por su responsabilidad.

La organización no adquiere automáticamente un nivel «Paso» y la realización de sistema no infiere por sí sola una «Cadena» completa.

## Ejemplo: crear una solicitud de pago DS 49

**Organización:**

```text
Work Chain: Servicio de financiamiento DS 49
  Work Process: Creación de solicitudes DS 49
    Work Flow: Crear solicitud de pago DS 49
```

**Sistema (realización candidata):**

```text
System Process: Atender «Crear solicitud de pago DS 49»
  System Action: Crear solicitud de pago (servicio propietario de solicitudes)
    System Step: Validar solicitud de pago
    System Step: Persistir cambios
  System Action: Notificar solicitante (capacidad correspondiente)
  System Action: Notificar revisor (capacidad correspondiente)
  System Action: Registrar auditoría (capacidad correspondiente)
```

La descomposición es **semántica**, no un orden obligatorio de transacciones. Las notificaciones podrían representar consecuencias o eventos posteriores, y la auditoría podría requerir garantías distintas. El modelo aquí **no decide** sincronía, orden de confirmación, idempotencia, atomicidad, compensación ni propiedad de datos.

«Crear solicitud de pago DS 49» como **Work Flow** expresa el trabajo de negocio; como **System Process** expresa la coordinación de su realización. «Crear solicitud de pago» como **System Action** es una responsabilidad funcional más acotada: no equivale a la coordinación completa.

## Relaciones con arquitectura de solución

La [arquitectura de Servicio, Producto y Composition](../products/framework/service-product-nexus.md) proporciona un **caso de referencia**, no una asignación universal:

- Un **Producto/BFF** puede expresar un `System Process` que interpreta la acción solicitada y coordina capacidades privadas.
- Un **Servicio** puede ofrecer una o varias `System Actions`, preservando la autoridad funcional, reglas y garantías que le correspondan.
- Los `System Steps` pueden formar parte de la realización interna de una acción; no exigen frontera de servicio.
- **Composition** reúne y verifica participantes; no se convierte en dueño de la coordinación funcional.

Una acción iniciada por un usuario, actor automatizado u otro participante puede ser ejecutada por un producto bajo la identidad y autoridad de su proceso, conservando la identidad del originador cuando corresponda.

Esto **no demuestra** que todo proceso de sistema deba residir en un BFF, ni que toda acción de sistema pertenezca siempre a un Service distinto. No transformar esta matriz de comprensión en taxonomía obligatoria de despliegues.

### Distinción respecto de un gestor de instancias de proceso

El `System Process` que coordina acciones de sistema **no debe equipararse automáticamente** con una **instancia de proceso administrada por un orquestador**.

Una entidad de negocio puede relacionarse simultáneamente con varias instancias de proceso independientes (por ejemplo, solicitud DS 49 y ticket de soporte). La identidad, estado e historia de esas instancias no se reducen al estado de la entidad.

La autoridad sobre definición de flujos, reglas, transiciones y persistencia de instancias del futuro orquestador **permanece abierta**. La presente revisión de Work Modeling no resuelve esa arquitectura.

## Proyecciones y carriles

Un diagrama puede distinguir personas y responsabilidades de sistema:

```text
Humano: Usuario externo / Usuario interno / Revisor
Sistema: Views / Producto-BFF / Servicio / Worker / Provider
```

Los carriles se seleccionan por su utilidad para la decisión y **no** establecen por sí mismos repositorios, procesos ejecutables, despliegues o servicios.

## Movimientos candidatos revisados

Los movimientos expresan preguntas de elaboración y reconstrucción; no constituyen transformaciones automáticas ni conversiones uno a uno.

- **Concretizar (organización):** `Work Chain → Work Process → Work Flow`. ¿Qué acciones reconocibles realizan esta cadena y sus procesos?
- **Abstraer (organización):** `Work Flow → Work Process → Work Chain`. ¿Qué proceso o cadena explican estas acciones?
- **Sistematizar (entre perspectivas; antes «Digitize»):** `Organization / Work Flow → System / System Process`. ¿Qué coordinación de capacidades realizaría esta acción de negocio? Pueden intervenir otros flujos y procesos organizacionales; no asumir equivalencia estructural.
- **Reconocer trabajo organizacional desde el sistema (antes «Materialize», nombre aún abierto):** `System Process → Organization / Work Flow`, cuando la evidencia permita identificar qué trabajo organizacional realiza. No inferirlo solo por semejanza nominal.
- **Componer (sistema):** `System Action → System Process`. ¿Qué acciones semánticas y consecuencias coordinamos para satisfacer la intención?
- **Descomponer (sistema; antes «Segment»):** `System Process → System Action → System Step`. ¿Qué responsabilidades funcionales y pasos de realización se distinguen dentro de esa coordinación?

**La antigua transformación `Organization / Process → System / Process` no se conserva como mapeo obligatorio.** Puede seguir siendo objeto de investigación, pero la revisión actual toma como caso central la realización de un **Work Flow** mediante un **System Process**.

Movimientos con fuentes distintas pueden converger en una misma decisión de diseño: la necesidad organizacional de una acción y las capacidades sistematizadas disponibles pueden justificar conjuntamente un proceso de sistema.

## Relación con productos de VSlices

- **Design:** examina acciones, límites, alternativas y relaciones entre organización y realización.
- **Method:** decide cuándo profundizar o revisar Work Modeling.
- **Docs Standard:** puede dar forma documental, visual y trazable al mecanismo.
- **Tooling:** puede explorar autoría, validación, transformaciones o representación, sin que ello esté implementado por esta definición.
- **Framework:** puede relacionar acciones de sistema con semántica ejecutable cuando haya evidencia; **no** asumir equivalencia automática entre `Work Flow`, `System Action`, `Feature` o el `Flow` de runtime.

## Límites y madurez

Esta revisión del **10 de noviembre de 2026** modifica la orientación candidata anterior:

1. Sustituye `Work Line` por `Work Chain` para la cadena organizacional.
2. Distingue `Work Process` de un `System Process` que coordina la realización de un `Work Flow`.
3. Introduce provisionalmente `System Action` entre proceso y paso de sistema, separando coordinación de acción funcional.
4. Reemplaza la matriz previa, que alineaba procesos y flujos de ambas perspectivas con el mismo nombre, por relaciones de sistematización **sin igualdad estructural**.

**No se ha validado universalidad ni conformidad ejecutable.** Hay que examinar estos nombres y relaciones contra casos reales, incluidos Ticket Service, Refrendación y procesos DS 49, y revisar las propuestas si la evidencia las contradice.

### Cambio de nombre y alcance — 2026-11-10

**Posición anterior:** `Action Flow` describía un mecanismo para representar acciones semánticas, relaciones y condiciones, tanto desde la organización como desde el sistema. El nombre enfatizaba un **flujo de acciones**, aunque la definición incluía cadenas, procesos, participantes y responsabilidades.

**Tensión:** al simplificar el Work Process de «Gestión de solicitud de soporte» y estudiar sus participantes/perfiles, se hizo evidente que un proceso organizacional no debe contener todas las decisiones internas de sus Work Flows y que el trabajo puede modelarse sin exigir una secuencia. El flujo es una posible relación entre acciones, no la totalidad de aquello que se modela.

**Revisión acordada:** `Work Modeling` sustituye a `Action Flow` como nombre del mecanismo candidato. La representación parte del significado del trabajo y distingue la perspectiva organizacional de su posible realización. La jerarquía `Work Chain → Work Process → Work Flow` y las categorías `System Process → System Action → System Step` se conservan por ahora, con sus incertidumbres previas.

**Consecuencias:** diagramas y notaciones (por ejemplo, Mermaid y swimlanes) son proyecciones del modelo y no definiciones de `Work Modeling`. Una guía de elaboración de Work Processes puede apoyarse en este mecanismo sin confundirlo con un estándar de diagramación. El término histórico `Action Flow` se conserva en la trayectoria y en [su entrada de redirección](action-flow.md).

**Abierto:** relación exacta entre `Work Modeling` y `System Realization`; si `Work Flow` es el mejor nombre del nivel de acción organizacional; y alcance universal de las correspondencias. Ninguna de estas cuestiones se cierra por renombrar el mecanismo.

### Trayectoria preservada

**Posición anterior:** `Scenario → Work Line → Work Process → Work Flow → Work Step`; la matriz situaba `Work Process` y `Work Flow` en organización y sistema, y proponía `System / Flow → System / Process`.

**Tensión observada:** un flujo organizacional es una **acción semántica**, mientras un `WorkProcess` de sistema comienza con acciones funcionales y las coordina. La matriz no distinguía con claridad la intención organizacional de la acción concreta de servicio.

**Revisión:** `Work Chain → Work Process → Work Flow` en organización, relacionado con `System Process → System Action → System Step` en sistema. `Work Flow` puede sistematizarse mediante `System Process`, sin equivalencia universal.

**Estado posterior:** candidato revisado, con el nombre `System Action` y las transformaciones aún examinables. La posición anterior queda preservada en esta sección y en la historia Git, no como segunda autoridad vigente.
