# Servicio, Producto y Nexo — arquitectura de solución y composición operacional

**Estado:** propuesta reconstruida y delimitada; pendiente de validación con consumidores reales.
**Fecha:** 2026-10-22
**Responsabilidad conceptual candidata:** VSlices Framework, arquitectura de solución.
**Fuente histórica principal:** `vslices/ideas/proyectos/v-slices/Framework/arquitecturas/solucion/productos-y-servicios/` y `vslices/ideas/servicios/serviu/lecciones/leccion-1/lado-tecnico/06-dependencies-y-nexus.md`.

## Propósito

Distinguir la responsabilidad funcional, la responsabilidad de producto y la composición operacional necesaria para desarrollar, ejecutar y validar escenarios reales, sin confundir límites lógicos con repositorios, procesos o despliegues.

No se afirma que esta división sea una taxonomía universal de software. Se conserva como patrón de arquitectura de solución que debe contrastarse con casos reales.

## Servicio (Service)

Es propietario de una responsabilidad funcional reutilizable: conocimiento, reglas, comportamiento, garantías y, cuando corresponda, estado o datos bajo su autoridad.

- Expone **privadamente** capacidades reutilizables a productos autorizados mediante contratos identificables; no es una superficie de acceso directo del usuario final.
- El producto consumidor actúa con su identidad y autoridad de proceso, conservando por separado la identidad del usuario que originó una operación cuando corresponde.
- Puede servir a más de un producto, pero su reutilización potencial no lo define.
- No debe transferir sus invariantes al producto consumidor ni al nexo.
- No implica microservicio, repositorio, base de datos o despliegue independiente.

Pregunta: **¿qué responsabilidad funcional se resuelve y quién es su autoridad?**

## Producto (Product)

Ofrece una experiencia o línea de trabajo reconocible a consumidores y compone capacidades para cumplir intenciones de producto.

- En la realización de referencia diferencia **Views**, **BFF** y **Queries**, con responsabilidades semánticas propias descritas a continuación.
- Sus procesos de producto pueden componer Features de servicios y aplicar reglas de producto justificadas.
- No debe duplicar autoridad de dominio perteneciente a servicios.
- No implica por sí mismo un proceso, repositorio o despliegue independiente.

Pregunta: **¿qué experiencia o resultado ofrece al consumidor y cómo compone las capacidades necesarias?**

### Responsabilidades internas del producto (caso de referencia)

- **Views:** superficies públicas de interacción y representación (Blazor en el caso Serviu). El usuario consume el producto, no invoca los servicios directamente.
- **BFF:** frontera de operaciones del producto. Puede actuar como proxy y además expresa WorkFlows/WorkProcesses propios que coordinan capacidades privadas genéricas y específicas de servicios, interpretan la intención y producen feedback. La coordinación entre Ticket Service y Monitoring Service pertenece al BFF, no a Ticket Service ni al nexo.
- **Queries:** **dominio de lectura y representación propio del producto**, no un conjunto de sentencias SQL. Define los significados y estructuras que la presentación necesita, componiendo información de diversos propietarios funcionales (por ejemplo, tickets, archivos e historial transversal). Puede realizarse con proyecciones, vistas o vistas materializadas, sin que un mecanismo particular defina universalmente su semántica. No es una API directamente consumida por el usuario; su acceso está dentro del producto, incluido el consumo por el BFF según el caso.

Aquí *dominio* significa un ámbito de conocimiento e información sobre un tema; no presupone adoptar Domain-Driven Design ni sus patrones estructurales.

### Orientación funcional y límite de extrapolación

Para **servicios** se utiliza una aproximación funcional: las definiciones establecen **espacios de valores válidos** (Space); las instancias representan **puntos admisibles** (Point); las funcionalidades expresan operaciones o transformaciones sobre esos puntos, y pueden componer otras funcionalidades (Work); Grounding aporta realizaciones de capacidades y efectos frente al mundo externo. Esta descripción es una orientación de trabajo y no congela una geometría matemática formal única.

**No está demostrado ni acordado extrapolar esa estructura a Queries o Views.** Queries tiene una responsabilidad representacional reconocida, pero cómo formalizarla mediante espacios, proyecciones, observaciones u otro vocabulario se investigará desde casos reales. No imponer simetrías ni nuevas categorías de VSIR por anticipado.

## Nexo operacional (Nexus)

Reúne productos, servicios y recursos **ya existentes** en un escenario reconocible de desarrollo, integración, ejecución o prueba.

- Puede reunir procesos, PostgreSQL u otras bases de datos, almacenamiento, configuración, observabilidad, dependencias externas y sustitutos controlados.
- Explicita disponibilidad, orden de arranque, configuración y relaciones operacionales.
- Favorece escenarios mínimos, reproducibles y observables.
- No posee lógica de negocio, casos de uso funcionales ni los datos o garantías de sus componentes.
- No convierte una dependencia de ejecución en propietario conceptual.
- Aparece bajo demanda, no obligatoriamente para cada servicio o producto.

Pregunta: **¿qué debe estar disponible para ejecutar y examinar este escenario?**

La palabra *Nexus* aquí refiere a la **composición operacional**, no al artefacto documental `Nexus` de VSlices Docs Standard. Ambos pueden relacionarse, pero no se deben confundir.

## Dependency y recurso operacional

Una **Dependency** ofrece mecanismos técnicos reutilizables (por ejemplo, integración de autenticación, observabilidad o componentes visuales) sin adquirir la responsabilidad funcional que habilita.

Un **recurso operacional** es algo necesario durante la ejecución (por ejemplo, PostgreSQL o almacenamiento), sin que ello lo convierta en una biblioteca compartida ni en un servicio de dominio.

Ni la reutilización ni la coincidencia de repositorio justifican por sí mismas una extracción.

## Flujo observable de composición de producto

En el ejemplo Ticket Support:

1. **Usuario → Ticket Support Product:** solicita una acción funcional por Views/BFF.
2. **Ticket Support BFF → Ticket Service:** ejecuta la capacidad funcional y obtiene el resultado de la transición, bajo reglas del servicio.
3. **Ticket Support BFF → Monitoring Service:** registra la acción y evolución observada como capacidad transversal distinta de `Tickets.UpdateMonitoring`, que pertenece al workflow de tickets.
4. **Ticket Support Product → Usuario:** comunica el resultado del proceso.

Esta secuencia es una **obligación de proceso por representar en VSIR**; todavía no acredita atomicidad, retries, compensación ni qué feedback corresponde ante una falla de Monitoring. Monitoring es un servicio genérico y transversal, análogo en papel arquitectónico a Folder Service; el producto coordina ambos. Las Queries del producto pueden construir una representación enriquecida desde datos de tickets, archivos y monitoreos.

## Límites y criterios

1. Primero distribuir **ownership**; separar ejecución solo cuando exista presión comprobable.
2. Repositorio, ensamblado, proceso, base de datos y deployment no equivalen automáticamente a fronteras semánticas.
3. Los productos componen capacidades y experiencia; los servicios conservan autoridad funcional; los nexos materializan escenarios.
4. El mismo servicio puede participar en varios nexos sin que cada nexo lo redefina.
5. La autenticación como mecanismo de plataforma puede usar Dependency/host; las reglas de cuentas, identidades y acceso permanecen en sus propietarios pertinentes.
6. Examinar coherencia, cohesión y acoplamiento antes de incorporar una abstracción o separar un deployment.

## Primer caso de presión: ticketera experimental

**Productos:** `atom-dev-serviu/ticket-support-product` (Views, BFF, Queries) y `atom-dev-serviu/landing-product` (entrada, inicio de sesión, perfil, recuperación de cuenta y elección manual de aplicación, inicialmente Tickets).

**Servicios:** `atom-dev-serviu/ticket-service`, `folder-service`, `account-service`, `identity-service`, `monitoring-service`. `account-service` se delimita inicialmente a autenticación, recuperación, cambio y contraseña temporal de un solo uso; `monitoring-service` registra transversalmente la acción de cada operación sobre tickets. Sus participaciones concretas deben verificarse.

**Dependency:** `atom-dev-serviu/auth-dependency`, responsable de integración SSO compartida y validación de cookies, propuesta para consumo mediante submódulo Git. La reutilización de código no sustituye los requisitos operacionales de protección de cookies ni configuración compartida.

**Nexo:** `atom-dev-serviu/ticket-support-nexus` — composición para desarrollo y pruebas integradas del flujo completo, no duplicación de Features.

**Decisión operacional del caso:** usar PostgreSQL para habilitar despliegue experimental en Railway. Esto es una elección de realización, **no** una obligación semántica universal de VSIR ni del patrón.

**Objetivo investigativo:** obtener una realización ejecutable de inicio de sesión + ticketera y después someter sus garantías a Verification y Challenge, incluido testing de seguridad **solo en entornos propios y autorizados**, con datos sintéticos y aislamiento.

Los nueve repositorios de destino (dos productos, cinco servicios, una dependencia y un nexo) fueron verificados vacíos el 2026-10-22. La descripción de responsabilidades deriva de acuerdos y evidencia del monolito original, **no** de implementaciones verificadas en esos destinos.

## Preguntas abiertas

- El BFF es propietario del WorkProcess funcional; ¿cómo garantizar su registro transversal ante fallos parciales sin atribuirlo al nexo?
- ¿Qué representación semántica corresponde al dominio de Queries, sin extrapolar prematuramente la orientación Space/Point/Work usada en servicios?
- ¿Qué obligaciones de identidad, sesión y autorización se representan en VSIR, y cuáles corresponden a reglas de plataforma o mecanismos de ejecución?
- ¿Qué perfil mínimo de despliegue y aislamiento permite evaluar Challenge sin exponer terceros ni datos reales?
- ¿Qué evidencia de un segundo caso mostraría que esta separación es más que una organización conveniente para Serviu?

## Procedencia y autoridad

Esta propuesta reconstruye el patrón discutido históricamente en VSlices y Serviu; no promueve automáticamente archivos históricos de `vslices/ideas` a autoridad actual.

Fuentes de reconstrucción:
- [Nexus operacional histórico](https://github.com/vslices/ideas/blob/main/proyectos/v-slices/Framework/arquitecturas/solucion/productos-y-servicios/nexus.md)
- [Dependencies y Nexus en Serviu](https://github.com/vslices/ideas/blob/main/servicios/serviu/lecciones/leccion-1/lado-tecnico/06-dependencies-y-nexus.md)
- [Framework conceptual actual](./README.md)

Esta página estabiliza una **propuesta examinable**, no una norma cerrada. Los casos y la evidencia pueden modificarla.
