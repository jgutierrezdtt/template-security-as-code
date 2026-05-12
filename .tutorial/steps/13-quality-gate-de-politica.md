# Paso 13. Quality gate de politica

## Objetivo de aprendizaje

Ejecutar políticas como parte del pipeline y usar el resultado para gobernar cambios.

## Archivo y seccion que debes modificar

- Archivo objetivo: `.github/workflows/policy-check.yml`.
- Seccion donde aplicar el cambio: workflow de evaluación de políticas.
- Resultado esperado: el repositorio incorpora el control de este paso de forma legible y revisable.

## Cambio que debes introducir

Copia este bloque como base y adáptalo al contexto real del repositorio:

```yaml
name: Policy Check
on:
  pull_request:
  push:
jobs:
  opa:
    runs-on: ubuntu-latest
```

## Como adaptarlo correctamente

- Si el paso es notificación, añade una etapa posterior al fallo.
- Si el paso es integración multi-herramienta, separa validación de políticas de otros análisis.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-13.py` comprueba el archivo y los marcadores esperados de este paso.
- Debe encontrar el marcador `name: Policy Check` en `.github/workflows/policy-check.yml`.
- Debe encontrar el marcador `pull_request:` en `.github/workflows/policy-check.yml`.
- Debe encontrar el marcador `push:` en `.github/workflows/policy-check.yml`.
- Debe encontrar el marcador `opa:` en `.github/workflows/policy-check.yml`.

## Criterio de finalizacion

El paso 13 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 14.
