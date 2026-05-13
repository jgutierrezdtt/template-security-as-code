# Paso 14. Integracion multi herramienta

## Objetivo de aprendizaje

Este paso introduce la integración multi herramienta y debe dejar un cambio comprensible en `.github/workflows/policy-check.yml`.

## Que vas a cambiar y por que

En este paso vuelves a trabajar sobre `.github/workflows/policy-check.yml`, pero ahora con una lectura más amplia: el programa de seguridad no suele depender de una sola herramienta. La base del workflow debe ser lo bastante clara como para integrar más validaciones sin perder el foco de política como criterio central.

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
- Deja `opa` como unidad clara del workflow, aunque luego se complemente con otras herramientas.
- Haz que el archivo se lea como puerta común de validación y no como una colección desordenada de pasos.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- Se entiende que el workflow puede crecer hacia validaciones múltiples sin perder estructura.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-14.py` comprueba este paso contra el archivo configurado.
- El workflow busca `name: Policy Check` dentro de `.github/workflows/policy-check.yml`.
- El workflow busca `pull_request:` dentro de `.github/workflows/policy-check.yml`.
- El workflow busca `push:` dentro de `.github/workflows/policy-check.yml`.
- El workflow busca `opa:` dentro de `.github/workflows/policy-check.yml`.

## Criterio de finalizacion

El paso 14 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 15.
