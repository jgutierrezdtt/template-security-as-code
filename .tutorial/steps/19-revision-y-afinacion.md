# Paso 19. Revision y afinacion

## Objetivo de aprendizaje

Este paso introduce la revisión y afinación del programa y debe dejar un cambio comprensible en `docs/security-as-code.md`.

## Que vas a cambiar y por que

En este paso vas a usar `docs/security-as-code.md` como instrumento de revisión final antes del cierre. La afinación consiste en observar el inventario, la cobertura, las excepciones activas y la siguiente iteración como un sistema: qué sobra, qué falta, qué está degradando el control y qué merece corregirse primero.

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
- Usa `## Excepciones activas` y `## Siguiente iteracion` para priorizar afinaciones reales del programa.
- Haz que la revisión apunte a decisiones concretas y no a un resumen complaciente.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- El documento ya sirve como revisión crítica antes del cierre del tutorial.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-19.py` comprueba este paso contra el archivo configurado.
- El workflow busca `## Inventario de controles` dentro de `docs/security-as-code.md`.
- El workflow busca `## Cobertura actual` dentro de `docs/security-as-code.md`.
- El workflow busca `## Excepciones activas` dentro de `docs/security-as-code.md`.
- El workflow busca `## Siguiente iteracion` dentro de `docs/security-as-code.md`.

## Criterio de finalizacion

El paso 19 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 20.
