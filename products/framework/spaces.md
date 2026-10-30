# Spaces — superficie de conceptos

**Producto propietario:** VSlices Framework.  
**Estado:** responsabilidad organizacional acordada; contratos detallados sujetos a sus fuentes y revisión.

## Responsabilidad
**Spaces** organiza las definiciones de los espacios de conceptos utilizados por el dominio. Un **Space** define un concepto y las condiciones bajo las cuales sus **Points** son admisibles. Spaces (plural, superficie organizacional) no constituye un Space superior.

## Fronteras
- No posee la ejecución de funcionalidades, la selección de mecanismos concretos ni el ensamblaje operacional.
- No equivale a Domain de DDD ni exige un despliegue o proyecto físico universal. La organización `[dominio].Spaces` es una convención de implementación actualmente elegida para los servicios.
- Las funcionalidades de Work consumen los conceptos sin apropiarse de su significado.
- La expresión de estos conceptos en Language Specification no transfiere su autoridad conceptual fuera de Framework.

## Preguntas pendientes
Contratos precisos de reglas, admisibilidad, evolución de Points y correspondencia entre conceptos Framework y expresiones del lenguaje. Consultar [Space](https://github.com/vslices/lang-specification/blob/main/concepts/C-002-space.md) y [Spaces](https://github.com/vslices/lang-specification/blob/main/concepts/C-021-spaces.md) como articulaciones disponibles, no como sustitución de la responsabilidad de Framework.
