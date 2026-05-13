# Paso 13. Quality gate de politica

## Objetivo de aprendizaje

Este paso introduce el quality gate de política y debe dejar un cambio comprensible en `.github/workflows/policy-check.yml`.

## Que vas a cambiar y por que

En este paso vas a reforzar `.github/workflows/policy-check.yml` para que la validación de políticas funcione como puerta de calidad. La diferencia importante es de intención: el workflow ya no solo ejecuta OPA, sino que representa una condición previa para aceptar cambios que rompen el baseline definido por el repositorio.

## Archivo y seccion que debes modificar

- Archivo objetivo: `.github/workflows/policy-check.yml`.
- Aplícalo en la parte del archivo que corresponde al título del paso.
- Si el archivo aún no existe, créalo con este contenido inicial y luego evoluciona desde ahí en los siguientes pasos.

## Cambio base recomendado

Este bloque no es para pegar a ciegas: úsalo como punto de partida y ajústalo al contexto del repositorio.

```yaml
name: Policy Check
on:
pull_request:
push:
jobs:
  opa:
```

## Como adaptarlo correctamente

- Mantén el cambio pequeño y centrado en una sola idea por paso.
- Usa el job `opa` como la unidad visible del gate para que el control sea fácil de auditar.
- Piensa en `pull_request` y `push` como puntos de aplicación de la política, no solo como triggers técnicos.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- Se reconoce un gate mínimo de política dentro del flujo de desarrollo.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-13.py` comprueba este paso contra el archivo configurado.
- El workflow busca `name: Policy Check` dentro de `.github/workflows/policy-check.yml`.
- El workflow busca `pull_request:` dentro de `.github/workflows/policy-check.yml`.
- El workflow busca `push:` dentro de `.github/workflows/policy-check.yml`.
- El workflow busca `opa:` dentro de `.github/workflows/policy-check.yml`.

## Criterio de finalizacion

El paso 13 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 14.
