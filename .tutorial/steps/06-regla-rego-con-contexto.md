# Paso 6. Regla rego con contexto

## Objetivo de aprendizaje

Codificar una política que pueda evaluarse automáticamente en CI.

## Archivo y seccion que debes modificar

- Archivo objetivo: `policies/security.rego`.
- Seccion donde aplicar el cambio: reglas OPA/Rego del control.
- Resultado esperado: el repositorio incorpora el control de este paso de forma legible y revisable.

## Cambio que debes introducir

Copia este bloque como base y adáptalo al contexto real del repositorio:

```rego
package security

deny[msg] {
  input.resource.public == true
  msg := "Recurso publico no permitido"
}
```

## Como adaptarlo correctamente

- Haz que el mensaje de deny explique claramente la infracción.
- Si el paso es con contexto, añade condiciones adicionales sobre labels, owner o entorno.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-06.py` comprueba el archivo y los marcadores esperados de este paso.
- Debe encontrar el marcador `package security` en `policies/security.rego`.
- Debe encontrar el marcador `deny[msg]` en `policies/security.rego`.
- Debe encontrar el marcador `input.resource.public == true` en `policies/security.rego`.
- Debe encontrar el marcador `Recurso publico no permitido` en `policies/security.rego`.

## Criterio de finalizacion

El paso 6 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 7.
