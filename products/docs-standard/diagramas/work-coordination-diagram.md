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

Un **nodo** representa un Work Flow reconocido. Su denominación preserva el significado de la acción, sin transformarlo en una operación técnica.

### Posición lógica

Cada nodo exhibe un **número de paso** delante de su nombre: `1. [Work Flow]`, `2. [Work Flow]`, etc.

- **Números diferentes** indican posiciones diferentes en el orden lógico representado. No son marcas de tiempo, duraciones ni identificadores intrínsecos de los Work Flows.
- **El mismo número en dos o más nodos declara simultaneidad** en el modelo. Por ahora, esta declaración **no especifica** cómo comienzan, se completan o se sincronizan esas acciones: la lógica se estudiará posteriormente junto con los conectores pertinentes.
- Un **salto numérico** no significa que necesariamente deban ejecutarse todos los pasos intermedios: una ruta condicional puede omitirlos.
- La alineación visual de los nodos **no define por sí sola** simultaneidad. La declaración corresponde al número compartido.

El número no reemplaza la relación entre acciones: la posición lógica y los conectores son dimensiones complementarias.

### Conectores definidos inicialmente

| Conector | Significado documental |
|---|---|
| **Secuencial** | Relación conocida de precedencia lógica entre Work Flows, sin inferir duración o comunicación técnica. |
| **Condicional** | Relación de precedencia aplicable bajo una condición expresada. No implica por sí misma concurrencia entre alternativas. |

**No se definen todavía** conectores de sincronización, unión paralela u otras modalidades de simultaneidad. Tampoco se infieren de las capacidades disponibles en el motor de diagramación.

## Límites y conocimiento incompleto

El diagrama debe permitir reconocer **qué relaciones conocemos y dónde termina nuestro conocimiento**. La falta de una relación representada no prueba que dicha relación sea inexistente; tampoco los números obligan a completar todos los pasos o las ramas.

Distinguir lo **sustentado**, lo **candidato** y lo **desconocido**, sin atribuir perfiles o conexiones por conveniencia visual. Una relación nueva puede extender la representación sin desautorizar automáticamente el conocimiento previo.

## Realización inicial en Mermaid

La notación utilizada inicialmente es `swimlane-beta LR` con carriles `subgraph`, nodos numerados y conexiones `-->` (secuencial) o `-->|condición|` (condicional).

```mermaid
---
config:
  theme: redux-color
---
swimlane-beta LR
    subgraph solicitante ["Solicitante de soporte"]
        registrar["1. Registro y<br/>seguimiento"]
    end

    subgraph analista ["Analista operacional"]
        evaluar["2. Evaluación de<br/>solicitudes"]
    end

    subgraph agente ["Agente de supervisión"]
        aprobar["3. Aprobar solución<br/>operacional"]
        sync@{ shape: fork }
        supervisar["4. Supervisado y<br/>cierre de soluciones"]
    end

    registrar --> evaluar
    evaluar -->|"Si es soporte"| sync
    evaluar -->|"Si es mejora"| aprobar
    aprobar --> sync
    sync --> supervisar
```

Este ejemplo proviene del [Work Process «Gestión de solicitud de soporte» de Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md). Ilustra **dos conexiones condicionales** y un salto del paso 2 al paso 4 en la ruta «Soporte». **No hay Work Flows declarados simultáneos en este ejemplo**. Las acciones internas «Registrar seguimiento de solución» y «Cerrar solicitud de soporte» pertenecen al cuarto Work Flow; no son nodos adicionales en esta representación.

La ubicación física automática de Mermaid no constituye una segunda autoridad sobre el orden ni sobre la simultaneidad. `swimlane-beta` es una realización de la representación, **no la definición de Work Coordination Diagram**; otras notaciones futuras podrían preservar su semántica.

## Separación de responsabilidades

- **Domain Modeling** define Work Flows, Work Processes, perfiles y el conocimiento que buscamos obtener sobre el trabajo.
- **Docs Standard** define la lectura de este diagrama y cómo expresar mediante él relaciones conocidas y límites de comprensión.
- **La realización visual** (actualmente Mermaid) materializa la representación sin determinar el significado de sus elementos.

El uso de este diagrama es **opcional**. La comprensión de un dominio no depende de elaborar ningún artefacto específico.

## Preguntas abiertas

- ¿Qué conectores adicionales se necesitan para describir la lógica de simultaneidad y sincronización?
- ¿Cómo distinguir, cuando sea necesario, tipos distintos de concurrencia sin confundirlos con alternativas condicionales?
- ¿Qué otras notaciones pueden preservar estas convenciones sin depender del posicionamiento automático de Mermaid?
