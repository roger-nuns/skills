# elegir-modelo

Hace que tu límite de uso de Claude dure más. Antes de cada tarea, Claude mira lo difícil e importante que es y elige el modelo y el esfuerzo que tocan, en vez de usar siempre el más caro.

| Tarea | Modelo | Esfuerzo |
|---|---|---|
| Fácil (buscar, resumir, renombrar) | Haiku 5.5 | low |
| Normal (código con pruebas, un análisis) | Sonnet 5.5 | medium |
| Difícil o importante (diseñar algo nuevo, decisiones caras) | Opus 5.5 | medium o high |
| Lo más difícil y largo | Fable 5.1 | high |

Además trae la regla que más ahorra: **una tarea, una conversación** (con `/clear` o una conversación nueva al cambiar de tema), y no cambiar de modelo a mitad de camino.

Todos los datos de la skill salen de la documentación oficial de Anthropic, con enlaces al final del `SKILL.md`. Comprobados el 27 de octubre de 2026.

## Ejemplos

- Le pides "resume este PDF": Claude te dice *"Haiku 5.5, esfuerzo low: es un resumen con receta clara"*.
- Le pides "arregla este error que nadie entiende": *"Opus 5.5, esfuerzo high: es difícil y hay casos raros"*.
- Le pides algo grande: lo parte en trozos y manda lo mecánico a un agente con Haiku.

## Instalar

Dentro de Claude Code:

```
/plugin install elegir-modelo --marketplace roger-nuns/skills
```

Más opciones en el [README principal](../../README.md#cómo-instalarlas).
