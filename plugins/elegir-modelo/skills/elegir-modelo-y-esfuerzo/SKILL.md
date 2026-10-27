---
name: elegir-modelo-y-esfuerzo
description: Úsala al empezar cada tarea en Claude Code. Elige el modelo (Haiku 5.5, Sonnet 5.5, Opus 5.5 o Fable 5.1) y el nivel de esfuerzo según lo difícil e importante que sea la tarea, para que tu límite de uso dure más.
---

# Elegir modelo y esfuerzo según la tarea

## Lo que dice Anthropic (datos comprobados el 27-oct-2026)

**Los modelos actuales**, del más potente al más ligero:

| Modelo | Para qué lo recomienda Anthropic | Precio en la API (entrada / salida, por millón de tokens) |
|---|---|---|
| **Fable 5.1** | Las tareas más difíciles y largas | 10 $ / 50 $ |
| **Opus 5.5** | Razonamiento complejo, decisiones de arquitectura | 4 $ / 20 $ |
| **Sonnet 5.5** | El trabajo diario: la mayoría de tareas de código | 2 $ / 10 $ |
| **Haiku 5.5** | Tareas simples, rápido y eficiente | 0,10 $ / 0,50 $ |

En la API, Opus 5.5 cuesta el doble que Sonnet 5.5, y Haiku 5.5 veinte veces menos que Sonnet. En los planes de suscripción (Pro, Max) Anthropic no publica la proporción exacta, pero sí dice que Sonnet gasta menos que Opus.

**El esfuerzo** es cuánto piensa el modelo antes de responder. Niveles: `low`, `medium`, `high`, `xhigh`, `max`. En Opus 5.5, Sonnet 5.5 y Haiku 5.5 viene en `medium`; en Fable 5.1, en `high`. Anthropic recomienda bajarlo en tareas simples para gastar menos.

**Otros hechos oficiales:**

- Claude Code reenvía toda la conversación en cada mensaje. Por eso recomienda `/clear` al cambiar a un tema distinto: el contexto viejo gasta en cada mensaje siguiente. `/clear` no cuesta nada.
- Cada modelo tiene su propia memoria rápida (caché). Cambiar de modelo a mitad de una conversación obliga a procesar todo otra vez: ese mensaje sale más lento y más caro.
- Cambiar el esfuerzo a mitad de conversación en Opus 5.5, Sonnet 5.5, Haiku 5.5 y Fable 5.1 no rompe esa caché (con suscripción o clave de API).
- Los agentes que lanza Claude usan el modelo de la sesión si no se les pone otro. Si la sesión está en Opus, ellos también. Para tareas simples de agentes, Anthropic recomienda ponerles Haiku.

## Cómo aplicarlo (recomendación)

| Tarea | Ejemplos | Modelo | Esfuerzo |
|---|---|---|---|
| Fácil, con receta clara | buscar en archivos, contar, dar formato, resumir un documento, renombrar | **Haiku 5.5** | low |
| Normal | escribir código con pruebas, un análisis con un script, revisar un cambio | **Sonnet 5.5** | medium |
| Difícil o importante | diseñar algo nuevo, decisiones que cuestan dinero si salen mal, un error que nadie entiende | **Opus 5.5** | medium (high si hay casos raros) |
| Lo más difícil y largo | un proyecto entero de muchas horas, un problema en el que ya falló Opus | **Fable 5.1** (si tu plan lo incluye) | high |

Reglas:

- Ante la duda, sube un escalón sólo si equivocarse costaría dinero o rehacer todo.
- Baja un escalón cuando la receta ya está escrita y el resultado se comprueba fácil.
- El esfuerzo `max` sólo cuando lo pide la persona.
- Di en una línea qué modelo y esfuerzo elegiste y por qué.
- Elige el modelo al abrir la sesión y no lo cambies a mitad. Si hace falta otro modelo, abre otra sesión o lanza un agente con ese modelo.
- Una tarea por sesión. Al cambiar de tema, `/clear` o sesión nueva.
- En tareas grandes, lo mecánico va a un agente con Haiku; el análisis, a Sonnet; la decisión final, a Opus.

## Comandos útiles en Claude Code

- `/model` para elegir modelo. Los nombres cortos `haiku`, `sonnet`, `opus` y `fable` siempre apuntan a la versión más nueva.
- `/effort` para elegir el esfuerzo (por ejemplo `/effort low`).
- `/usage` para ver cuánto llevas gastado y qué lo está gastando.

## Fuentes oficiales

- Modelos, alias y esfuerzo: https://code.claude.com/docs/en/model-config
- Ahorrar uso (`/clear`, elegir modelo, agentes): https://code.claude.com/docs/en/costs
- Caché al cambiar de modelo o esfuerzo: https://code.claude.com/docs/en/prompt-caching
- Precios: https://platform.claude.com/docs/en/about-claude/pricing
