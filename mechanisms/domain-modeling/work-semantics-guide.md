# Guía de modelado de Work Semantics

**Estado:** guía inicial candidata — 2026-11-10.  
**Mecanismo propietario de la orientación:** [Domain Modeling](README.md).  
**Alcance:** comprender cómo una organización reconoce, organiza y coordina su trabajo, **antes** de decidir sus realizaciones de sistema. No es un estándar universal de diagramas ni un contrato de Framework.

## Propósito

Orientar el inicio de Domain Modeling mediante **Work Semantics**, sin confundir procesos con estados del software, actores con cuentas o perfiles con permisos.

El primer movimiento no es diseñar funcionalidades de sistema: es **reconocer quiénes participan en el trabajo, qué procesos semánticos reconoce la organización y qué perfiles realizan sus acciones**.

## Recorrido inicial de modelado

### 1. Reconocer actores

Identificar los tipos de **actor** que participan en el ámbito estudiado y la relación desde la que intervienen. Distinguir:

- **Participante:** persona, organización o sistema concreto que interviene.
- **Actor:** calidad o posición desde la que participa en un contexto de trabajo.
- **Perfil:** responsabilidad o función que puede desempeñar un actor dentro de un contexto particular.
- **Identidad/cuenta y permiso técnico:** mecanismos de reconocimiento y autorización, que **no** se infieren automáticamente del actor o perfil organizacional.

Un mismo participante puede actuar en diferentes calidades y desempeñar perfiles distintos en procesos diferentes. Los tipos de actores se documentan **una sola vez en su superficie propietaria** y se referencian desde procesos y perfiles.

**Preguntas:** ¿quiénes se relacionan con el trabajo?, ¿desde qué posición participan?, ¿qué distinciones reconoce realmente la organización?, ¿cuáles son conjeturas?

**Salida esperada:** un catálogo contextual de tipos de actor con sus límites y fuentes, **no** una tabla de roles de autorización.

### 2. Reconocer los procesos semánticos de trabajo

Investigar cómo la organización **comprende y coordina sus esfuerzos**. Identificar las cadenas de trabajo relevantes y los **Work Processes** que contribuyen a ellas; no deducirlos de un conjunto de endpoints, pantallas o estados.

- **Work Chain:** cadena reconocible de trabajo o prestación de servicio.
- **Work Process:** parte reconocible de esa cadena, caracterizada por las acciones de negocio que coordina y las relaciones significativas entre ellas.
- **Work Flow:** acción semántica específica que forma parte del proceso.

Comenzar por el **propósito y el resultado reconocible** de cada proceso, sus participantes y las acciones que lo componen. Al elaborar el diagrama de un Work Process, representar **las acciones y relaciones necesarias para comprender ese nivel**, sin introducir automáticamente cada decisión o paso interno de sus Work Flows.

Una condición que dirige una relación entre acciones puede expresarse en la **relación** sin añadir un nodo de decisión redundante. No ocultar, sin embargo, una decisión que sea semánticamente importante a nivel del proceso.

**Preguntas:** ¿qué trabajo realiza la organización?, ¿qué resultado reconoce?, ¿qué acciones articulan el proceso?, ¿cuándo cambia su relación?, ¿qué detalles corresponden a cada Work Flow?

**Salida esperada:** mapa navegable de cadenas/procesos y un documento propietario por proceso, con acciones candidatas y relaciones examinables.

### 3. Identificar los perfiles que ejecutan o participan en los Work Flows

Una vez reconocidos los procesos y las acciones que los componen, identificar los **perfiles organizacionales** que realizan, coordinan o participan en cada Work Flow.

- Definir cada perfil **una vez dentro del contexto al que pertenece**, indicando con qué tipos de actor puede relacionarse.
- Distinguir el **perfil que ejecuta o responde por la acción** de otros perfiles participantes, cuando la evidencia permita hacer esa distinción.
- Referenciar las definiciones propietarias de actores y perfiles; no repetirlas en el Work Process.
- No derivar permisos de software, cargos contractuales ni exclusividad de responsabilidades a partir del nombre de un perfil.
- Si no está comprobado quién realiza una acción, **marcar la responsabilidad como pendiente**, sin asignarla por conveniencia visual.

**Preguntas:** ¿qué perfil realiza cada Work Flow?, ¿intervienen otros?, ¿hay cambio de responsabilidad entre acciones?, ¿qué evidencia confirma cada asignación?

**Salida esperada:** relación navegable entre perfiles, tipos de actor, procesos y Work Flows. La representación visual puede mostrar la distribución de responsabilidades cuando aporte claridad.

### 4. Profundizar cada Work Flow por separado

Con el Work Process y los perfiles reconocidos, elaborar **un documento propietario por Work Flow**. Examinar su intención, disparador, participantes, información necesaria, condiciones, decisiones internas, resultados y consecuencias observables.

No repetir el diagrama general del proceso dentro de cada Work Flow. Enlazar al proceso padre, al perfil correspondiente y a las fuentes que justifican el significado de la acción.

El nombre de una Feature o una operación CRUD no basta para demostrar que exista un Work Flow autónomo. Una acción que no cambia de etapa también puede tener significado de negocio.

### 5. Relacionar la comprensión con System Realizations

Solo cuando exista una comprensión suficiente para tomar decisiones examinables, estudiar cómo sistematizar el trabajo. En esa elaboración pueden descubrirse **Spaces, Points, Features, Capabilities**, restricciones y operaciones, mediante las definiciones y autoridades propias de VSlices.

Consultar [Domain Modeling](README.md) para la relación candidata `Work Flow → System Process` y la elaboración `System Process → System Action → System Step`. **No asumir mapeos uno a uno**.

La realización puede aportar evidencia que motive la revisión de actores, perfiles, procesos y flujos. Registrar **posición anterior → evidencia → revisión → posición posterior** sin presentar la implementación como autoridad automática sobre el trabajo organizacional.

## Convenciones de representación

Un diagrama es una **proyección de un modelo**, no el modelo mismo.

Para un Work Process puede usarse un diagrama de actividades con **carriles por perfil** si se conoce quién actúa y el renderizador lo soporta. `swimlane-beta` con `redux-color` en Mermaid es una opción visual **comprobada para el caso de documentación de Serviu en GitHub (2026-11-10)**, no una obligación técnica o conceptual para VSlices.

El diagrama debería conservar acciones semánticas, relaciones y condiciones relevantes. **No confundir tipos de actor (p. ej. interno/externo) con perfiles ejecutores**. No introducir carriles de perfiles ficticios como si fueran definiciones organizacionales aprobadas; marcar expresamente la incertidumbre cuando haga falta.

Las notaciones, colores y configuración del renderizador pueden cambiar sin cambiar el significado del trabajo.

## Organización documental y trazabilidad

- **Índices / README de ámbito:** orientan hacia documentos propietarios; no duplican diagramas, listas detalladas ni definiciones.
- **Actores:** tipos de participación, con su procedencia y clasificación contextual.
- **Perfiles:** catálogo contextual y una definición por perfil; relacionan tipos de actores y responsabilidades sin asumir permisos.
- **Procesos:** documento propietario de cada Work Process y su representación general.
- **Work Flows:** documentos propietarios de cada acción semántica, referenciados desde el proceso.
- **Evidencia técnica:** separar los comportamientos de sistema observados de las definiciones del trabajo.

Al crear o revisar documentos, registrar fuentes, fecha de observación si importa, decisiones acordadas, hipótesis y preguntas abiertas. Conservar enlaces y trayectoria de cambios en Git. Una decisión no se vuelve verdadera por aparecer en un diagrama.

## Ejemplo de referencia sin duplicación

En Serviu se inició por tipos de [actores](https://github.com/atom-dev-serviu/documentation/blob/main/actors/README.md), luego el [Work Process de gestión de solicitud de soporte](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md), y se estableció un catálogo contextual de [perfiles de ticketera](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/profiles/README.md). Sus [Work Flows](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/flows/README.md) serán profundizados por separado.

Este caso es **evidencia para revisar la guía**, no una definición obligatoria de todos los dominios ni una copia de sus diagramas.

## Preguntas abiertas

- Cuánto detalle corresponde a un Work Process o Work Flow en contextos distintos.
- Cuándo resulta útil formalizar más de un perfil participante o más de una responsabilidad por acción.
- Cómo representar variantes y condiciones sin imponer una notación universal.
- Qué otros conceptos de Domain Modeling requiere la evidencia más allá de este recorrido inicial de Work Semantics.

Esta guía describe el **primer recorrido de estudio**; no afirma que los actores, procesos o perfiles se descubran en un orden inmutable.
