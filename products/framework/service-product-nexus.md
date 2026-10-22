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

- Expone capacidades propias mediante contratos identificables.
- Puede servir a más de un producto, pero su reutilización potencial no lo define.
- No debe transferir sus invariantes al producto consumidor ni al nexo.
- No implica microservicio, repositorio, base de datos o despliegue independiente.

Pregunta: **¿qué responsabilidad funcional se resuelve y quién es su autoridad?**

## Producto (Product)

Ofrece una experiencia o línea de trabajo reconocible a consumidores y compone capacidades para cumplir intenciones de producto.

- Puede poseer interacción, BFF, consultas y modelos de lectura propios cuando correspondan.
- Sus procesos de producto pueden componer Features de servicios y aplicar reglas de producto justificadas.
- No debe duplicar autoridad de dominio perteneciente a servicios.
- No implica por sí mismo un proceso, repositorio o despliegue independiente.

Pregunta: **¿qué experiencia o resultado ofrece al consumidor y cómo compone las capacidades necesarias?**

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

## Límites y criterios

1. Primero distribuir **ownership**; separar ejecución solo cuando exista presión comprobable.
2. Repositorio, ensamblado, proceso, base de datos y deployment no equivalen automáticamente a fronteras semánticas.
3. Los productos componen capacidades y experiencia; los servicios conservan autoridad funcional; los nexos materializan escenarios.
4. El mismo servicio puede participar en varios nexos sin que cada nexo lo redefina.
5. La autenticación como mecanismo de plataforma puede usar Dependency/host; las reglas de cuentas, identidades y acceso permanecen en sus propietarios pertinentes.
6. Examinar coherencia, cohesión y acoplamiento antes de incorporar una abstracción o separar un deployment.

## Primer caso de presión: ticketera experimental

**Producto:** `atom-dev-serviu/ticket-support-product` — BFF, consultas, Views y procesos de producto.

**Servicios:** `atom-dev-serviu/ticket-service`, `folder-service`, `account-service`, `identity-service`, `monitoring-service`. Cada uno conserva su autoridad funcional; su participación exacta en cada escenario debe verificarse.

**Nexo:** `atom-dev-serviu/ticket-support-nexus` — composición para desarrollo y pruebas integradas del flujo completo, no duplicación de Features.

**Decisión operacional del caso:** usar PostgreSQL para habilitar despliegue experimental en Railway. Esto es una elección de realización, **no** una obligación semántica universal de VSIR ni del patrón.

**Objetivo investigativo:** obtener una realización ejecutable de inicio de sesión + ticketera y después someter sus garantías a Verification y Challenge, incluido testing de seguridad **solo en entornos propios y autorizados**, con datos sintéticos y aislamiento.

Los siete repositorios de caso están vacíos al establecer esta propuesta. La descripción de sus responsabilidades deriva de la delimitación acordada, no de implementaciones ya verificadas.

## Preguntas abiertas

- ¿Cuándo una composición entre servicios pertenece a un WorkProcess de producto y cuándo constituye mera coordinación operacional del nexo?
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
