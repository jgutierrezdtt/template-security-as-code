# Paso 20. Medalla final security as code

## Objetivo de aprendizaje

Cerrar el recorrido Security as Code con una vista final del programa y dejar un cambio comprensible en `docs/security-as-code.md`.

## Que vas a cambiar y por que

En este último paso vas a usar `docs/security-as-code.md` como resumen final del programa: qué controles están inventariados, cuál es su cobertura actual, qué excepciones siguen abiertas y cuál es la siguiente iteración recomendada. Esa estructura permite cerrar el tutorial con una visión de sistema y no con una lista de piezas sueltas.

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
- Usa cada sección como criterio de cierre y no como encabezado vacío.
- Haz que `## Siguiente iteracion` deje visible qué faltaría para madurar después del tutorial.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- El documento puede leerse como checklist final del nivel alcanzado en el repositorio.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-20.py` comprueba este paso contra el archivo configurado.
- El workflow busca `## Inventario de controles` dentro de `docs/security-as-code.md`.
- El workflow busca `## Cobertura actual` dentro de `docs/security-as-code.md`.
- El workflow busca `## Excepciones activas` dentro de `docs/security-as-code.md`.
- El workflow busca `## Siguiente iteracion` dentro de `docs/security-as-code.md`.

## Criterio de finalizacion

El paso 20 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Este es el ultimo paso del tutorial.
