# Paso 1. Primer control codificado

## Objetivo de aprendizaje

En este paso vas a practicar un control de Security as Code para entender que decision de configuracion aplicar y por que.

## Que debe hacer la persona participante

1. Revisar el contexto del control en este paso.
2. Editar la configuracion esperada en `policies/security.rego`.
3. Guardar y subir el cambio en el flujo normal del repositorio (commit/push o PR).

## Que configurar exactamente

- Campo o seccion objetivo: relacionado con "Primer control codificado".
- Ubicacion principal: `policies/security.rego`.
- Resultado esperado: que la configuracion refleje el control del paso 1.

## Checklist de configuracion

- El cambio del paso 1 esta presente en `policies/security.rego`.
- El cambio es coherente con el objetivo del paso.
- El repositorio incluye la evidencia de progreso para este paso.

## Validacion automatica (sin ejecucion manual)

- `validate-steps.yml` se ejecuta automaticamente por eventos `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-01.py` valida que el control de este paso esta aplicado.
- El estado de progreso se refleja en `.tutorial/state.json`.

## Criterio de finalizacion

El paso 1 se marca como completado cuando GitHub Actions reporta exito para `validate-step-01.py`.

Siguiente paso: Paso 2.
