# Skills de Claude en español

Skills gratis, en español sencillo, para usar Claude mejor y gastar menos de tu límite. Pensadas para gente que empieza: no hace falta saber programar.

## Skills disponibles

| Skill | Qué hace |
|---|---|
| [elegir-modelo](plugins/elegir-modelo) | Elige el modelo (Haiku 5.5, Sonnet 5.5, Opus 5.5 o Fable 5.1) y el esfuerzo según la tarea, para que tu límite dure más. |

## Cómo instalarlas

### Opción 1: Claude Code, con un comando (recomendada)

Escribe esto dentro de Claude Code:

```
/plugin install elegir-modelo --marketplace roger-nuns/skills
```

Si tu Claude Code es más antiguo, usa estos dos:

```
/plugin marketplace add roger-nuns/skills
/plugin install elegir-modelo@roger-nuns
```

Así también recibes las mejoras cuando las publique.

### Opción 2: Claude Code, copiando la carpeta

1. Descarga este repositorio (botón verde **Code** → **Download ZIP**).
2. Copia la carpeta `plugins/elegir-modelo/skills/elegir-modelo-y-esfuerzo` dentro de `~/.claude/skills/`.
3. Abre una sesión nueva.

### Opción 3: app de Claude (web o escritorio)

1. Comprime la carpeta `plugins/elegir-modelo/skills/elegir-modelo-y-esfuerzo` en un `.zip`.
2. En Ajustes, busca el apartado de Skills y sube el `.zip`.

## ¿Son fiables?

Cada dato sale de la documentación oficial de Anthropic, con el enlace al final de cada skill y la fecha en que se comprobó.

## ¿Es segura?

Sí. Cada skill es sólo texto con instrucciones: no ejecuta programas, no se conecta a internet y no pide claves. Puedes leer el archivo `SKILL.md` antes de instalarla.

## Licencia

[MIT](LICENSE): úsalas, cámbialas y compártelas libremente.
