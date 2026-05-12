# Paso 8. Excepcion programatica

## Objetivo de aprendizaje

Evitar que una excepción de política se convierta en una supresión opaca.

## Archivo y seccion que debes modificar

- Archivo objetivo: `docs/policy-exceptions.yml`.
- Seccion donde aplicar el cambio: registro de excepciones de política.
- Resultado esperado: el repositorio incorpora el control de este paso de forma legible y revisable.

## Cambio que debes introducir

Copia este bloque como base y adáptalo al contexto real del repositorio:

```yaml
exceptions:
  - policy: public-resource
    scope: namespace/dev
    reason: "entorno temporal de pruebas"
    expires_on: "2026-12-31"
```

## Como adaptarlo correctamente

- Usa el scope más pequeño posible.
- Caduca la excepción en cuanto el caso temporal desaparezca.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-08.py` comprueba el archivo y los marcadores esperados de este paso.
- Debe encontrar el marcador `exceptions:` en `docs/policy-exceptions.yml`.
- Debe encontrar el marcador `policy:` en `docs/policy-exceptions.yml`.
- Debe encontrar el marcador `scope:` en `docs/policy-exceptions.yml`.
- Debe encontrar el marcador `reason:` en `docs/policy-exceptions.yml`.
- Debe encontrar el marcador `expires_on:` en `docs/policy-exceptions.yml`.

## Criterio de finalizacion

El paso 8 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 9.
