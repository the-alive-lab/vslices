# Work Coordination Diagram

**Responsabilidad documental:** VSlices Docs Standard.  
**Estado:** definición inicial candidata, elaborada a partir de la representación de trabajo de Serviu (2026-11-10).  
**Conceptos representados:** [Domain Modeling](../../../mechanisms/domain-modeling/README.md).  
**Navegación:** [Diagramas](README.md).

## Definición

Un **Work Coordination Diagram** representa, de forma examinable, **qué [Work Flows](../../../mechanisms/domain-modeling/concepts/work-flow.md) participan en el trabajo estudiado, desde qué [perfiles](../../../mechanisms/domain-modeling/concepts/profile.md), en qué posiciones del orden lógico y mediante qué relaciones conocidas**.

Es una **representación del conocimiento del trabajo**, no una definición de Work Flow, Work Process, perfil o ejecución técnica. Puede proyectar una parte del trabajo sin exigir que todo el proceso o su cadena estén descubiertos.

## Elementos de lectura

### Perfil

Los **carriles** identifican los perfiles organizacionales desde los cuales se participa en las acciones representadas. No representan necesariamente personas, cargos, cuentas ni permisos.

### Work Flow

Un **nodo de flujo** con notación Mermaid `A["Sample"]` representa un Work Flow reconocido. Su denominación preserva el significado de la acción, sin transformarlo en una operación técnica.

### Sincronización de acciones

Un **nodo de sincronización** con notación `A@{ shape: fork }` representa un punto explícito de coordinación entre recorridos o acciones. Permite mostrar dónde se encuentran o coordinan conexiones antes de continuar.

**No implica automáticamente esperar a que se completen todas las ramas entrantes**: su condición de habilitación depende de la semántica reconocida en el proceso. En particular, una convergencia de caminos alternativos no debe confundirse con una unión que exige completar actividades paralelas. Tampoco es un Work Flow adicional ni tiene un número de paso propio.

### Posición lógica

Cada nodo exhibe un **número de paso** delante de su nombre: `1. [Work Flow]`, `2. [Work Flow]`, etc.

- **Números diferentes** indican posiciones diferentes en el orden lógico representado. No son marcas de tiempo, duraciones ni identificadores intrínsecos de los Work Flows.
- **El mismo número en dos o más nodos declara simultaneidad** en el modelo. Por ahora, esta declaración **no especifica** cómo comienzan, se completan o se sincronizan esas acciones: la lógica se estudiará posteriormente junto con los conectores pertinentes.
- Un **salto numérico** no significa que necesariamente deban ejecutarse todos los pasos intermedios: una ruta condicional puede omitirlos.
- La alineación visual de los nodos **no define por sí sola** simultaneidad. La declaración corresponde al número compartido.

El número no reemplaza la relación entre acciones: la posición lógica y los conectores son dimensiones complementarias.

### Conectores definidos

| Conector Mermaid | Significado documental |
|---|---|
| `A --> B` | **Secuencial:** continuidad o precedencia lógica entre elementos, sin inferir mecanismo de ejecución. |
| `A -->|Sample| B` | **Secuencial con texto:** la misma continuidad, acompañada de una descripción para facilitar su lectura. El texto no cambia por sí mismo la naturaleza del conector. |
| `A -.-> B` | **Condicional:** continuidad aplicable bajo una condición reconocida, aunque esta no se escriba sobre el conector. |
| `A -.->|Sample| B` | **Condicional con texto:** continuidad condicionada, acompañada de una descripción de la condición o alternativa. |

La **diferencia entre secuencial y condicional la determina el estilo del conector**, no la presencia o ausencia de texto. Un conector secuencial con texto **no se vuelve condicional** por llevar una etiqueta.

Por ahora no se definen otros conectores. El nodo `fork` expresa una **sincronización o convergencia reconocida**: su presencia no establece por sí sola concurrencia, simultaneidad o una espera de todas las entradas.

## Límites y conocimiento incompleto

El diagrama debe permitir reconocer **qué relaciones conocemos y dónde termina nuestro conocimiento**. La falta de una relación representada no prueba que dicha relación sea inexistente; tampoco los números obligan a completar todos los pasos o las ramas.

Distinguir lo **sustentado**, lo **candidato** y lo **desconocido**, sin atribuir perfiles o conexiones por conveniencia visual. Una relación nueva puede extender la representación sin desautorizar automáticamente el conocimiento previo.

## Realización inicial en Mermaid

La realización inicial utiliza `swimlane-beta LR`, carriles `subgraph`, nodos de Work Flow `A["Sample"]`, nodos de sincronización `A@{ shape: fork }` y conectores `-->` (secuencial) o `-.->` (condicional), con sus variantes etiquetadas.

```mermaid
---
config:
  theme: redux-color
---
swimlane-beta LR
    subgraph solicitante ["Solicitante de soporte"]
        dudaInicio@{ shape: notch-rect, label: "¿Que procesos activan este?" }
        inicio(("Inicio))
        registrar["1. Registro y<br/>seguimiento"]
    end

    subgraph analista ["Analista operacional"]
        evaluar["2. Evaluación de<br/>solicitudes"]
    end

    subgraph agente ["Agente de supervisión"]
        aprobar["3. Aprobar solución<br/>operacional"]
        sync@{ shape: fork }
        supervisar["4. Supervisado y<br/>cierre de soluciones"]
        fin((("Fin")))
    end

    dudaInicio ~~~ inicio --> registrar --> evaluar
    evaluar -.->|"Si es soporte"| sync
    evaluar -.->|"Si es mejora"| aprobar
    aprobar --> sync --> supervisar --> fin
```

Este ejemplo proviene del [Work Process «Gestión de solicitud de soporte» de Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md). Ilustra **dos conexiones condicionales** (Soporte y Mejora), un salto del paso 2 al paso 4 en la ruta «Soporte» y la **convergencia de ambos recorridos mediante el nodo `sync`** antes de supervisión. Como las rutas son alternativas, `sync` representa aquí su reunión para continuar, **no una barrera que espere ambas**. **No hay Work Flows declarados simultáneos en este ejemplo**. Las acciones internas «Registrar seguimiento de solución» y «Cerrar solicitud de soporte» pertenecen al cuarto Work Flow; no son nodos adicionales en esta representación.

La ubicación física automática de Mermaid no constituye una segunda autoridad sobre el orden ni sobre la simultaneidad. `swimlane-beta` es una realización de la representación, **no la definición de Work Coordination Diagram**; otras notaciones futuras podrían preservar su semántica.

## Separación de responsabilidades

- **Domain Modeling** define Work Flows, Work Processes, perfiles y el conocimiento que buscamos obtener sobre el trabajo.
- **Docs Standard** define la lectura de este diagrama y cómo expresar mediante él relaciones conocidas y límites de comprensión.
- **La realización visual** (actualmente Mermaid) materializa la representación sin determinar el significado de sus elementos.

El uso de este diagrama es **opcional**. La comprensión de un dominio no depende de elaborar ningún artefacto específico.

## Preguntas abiertas

- ¿Qué nuevas convenciones serían necesarias si un caso real exigiera sincronización de actividades paralelas, además de la convergencia de alternativas representada aquí?
- ¿Cómo distinguir con mayor precisión diferentes condiciones de habilitación de una sincronización, sin inferirlas de la figura?
- ¿Qué otras notaciones pueden preservar estas convenciones sin depender del posicionamiento automático de Mermaid?
