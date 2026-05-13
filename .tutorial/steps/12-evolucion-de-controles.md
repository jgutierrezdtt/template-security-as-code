# Paso 12. Evolucion de controles

## Objetivo de aprendizaje

Este paso introduce la evolución de controles y debe dejar un cambio comprensible en `docs/security-as-code.md`.

## Que vas a cambiar y por que

En este paso vuelves a trabajar sobre `docs/security-as-code.md`, pero con una intención distinta: usar el documento para mostrar cómo madura el programa. No basta con saber qué controles existen hoy; también importa dejar claro qué cobertura falta, qué excepciones condicionan el estado actual y cuál es la siguiente iteración prioritaria.

## Archivo y seccion que debes modificar

- Archivo objetivo: `docs/security-as-code.md`.
- Aplícalo en la parte del archivo que corresponde al título del paso.
- Si el archivo aún no existe, créalo con este contenido inicial y luego evoluciona desde ahí en los siguientes pasos.

## Cambio base recomendado

Este bloque no es para pegar a ciegas: úsalo como punto de partida y ajústalo al contexto del repositorio.

```markdown
## Inventario de controles
## Cobertura actual
## Excepciones activas
## Siguiente iteracion
```

## Como adaptarlo correctamente

- Mantén el cambio pequeño y centrado en una sola idea por paso.
- Usa `## Siguiente iteracion` como punto de planificación y no como frase genérica de cierre.
- Haz que `## Cobertura actual` y `## Excepciones activas` expliquen por qué ciertos controles aún no están cerrados.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- El documento ya sirve para hablar de evolución del programa y no solo de su estado actual.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-12.py` comprueba este paso contra el archivo configurado.
- El workflow busca `## Inventario de controles` dentro de `docs/security-as-code.md`.
- El workflow busca `## Cobertura actual` dentro de `docs/security-as-code.md`.
- El workflow busca `## Excepciones activas` dentro de `docs/security-as-code.md`.
- El workflow busca `## Siguiente iteracion` dentro de `docs/security-as-code.md`.

## Criterio de finalizacion

El paso 12 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 13.
