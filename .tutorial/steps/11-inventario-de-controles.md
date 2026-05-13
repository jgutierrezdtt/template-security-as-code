# Paso 11. Inventario de controles

## Objetivo de aprendizaje

Este paso introduce el inventario de controles y debe dejar un cambio comprensible en `docs/security-as-code.md`.

## Que vas a cambiar y por que

En este paso vas a reforzar `docs/security-as-code.md` como inventario vivo del programa. La idea es que el equipo pueda ver qué controles existen, cuánto cubren, qué excepciones siguen abiertas y cuál es la siguiente iteración de mejora sin tener que reconstruir esa información a partir de varios archivos dispersos.

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
- Usa `## Inventario de controles` para enumerar controles reales y no conceptos abstractos.
- Haz que `## Cobertura actual` y `## Excepciones activas` aporten estado del programa y no solo descripción.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- El documento ya funciona como referencia rápida del programa Security as Code.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-11.py` comprueba este paso contra el archivo configurado.
- El workflow busca `## Inventario de controles` dentro de `docs/security-as-code.md`.
- El workflow busca `## Cobertura actual` dentro de `docs/security-as-code.md`.
- El workflow busca `## Excepciones activas` dentro de `docs/security-as-code.md`.
- El workflow busca `## Siguiente iteracion` dentro de `docs/security-as-code.md`.

## Criterio de finalizacion

El paso 11 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 12.
