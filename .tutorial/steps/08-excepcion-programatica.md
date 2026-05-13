# Paso 8. Excepcion programatica

## Objetivo de aprendizaje

Este paso introduce una excepción programática y debe dejar un cambio comprensible en `docs/policy-exceptions.yml`.

## Que vas a cambiar y por que

En este paso vas a crear `docs/policy-exceptions.yml` para que una desviación del control no se gestione en conversaciones sueltas ni comentarios ad hoc. La excepción debe estar estructurada para que la política o el pipeline puedan interpretarla de forma consistente.

## Archivo y seccion que debes modificar

- Archivo objetivo: `docs/policy-exceptions.yml`.
- Aplícalo en la parte del archivo que corresponde al título del paso.
- Si el archivo aún no existe, créalo con este contenido inicial y luego evoluciona desde ahí en los siguientes pasos.

## Cambio base recomendado

Este bloque no es para pegar a ciegas: úsalo como punto de partida y ajústalo al contexto del repositorio.

```yaml
exceptions:
  - policy: deny_public_resource
    scope: resource/demo-public-bucket
    reason: "Excepcion temporal durante migracion controlada"
    expires_on: "2026-12-31"
```

## Como adaptarlo correctamente

- Mantén el cambio pequeño y centrado en una sola idea por paso.
- Usa `policy` y `scope` para que la excepción sea evaluable y no ambigua.
- Haz que `reason` explique por qué se acepta la desviación y no solo qué control se afecta.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- La excepción ya parece tratable por código y no solo por lectura humana.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-08.py` comprueba este paso contra el archivo configurado.
- El workflow busca `exceptions:` dentro de `docs/policy-exceptions.yml`.
- El workflow busca `policy:` dentro de `docs/policy-exceptions.yml`.
- El workflow busca `scope:` dentro de `docs/policy-exceptions.yml`.
- El workflow busca `reason:` dentro de `docs/policy-exceptions.yml`.
- El workflow busca `expires_on:` dentro de `docs/policy-exceptions.yml`.

## Criterio de finalizacion

El paso 8 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 9.
