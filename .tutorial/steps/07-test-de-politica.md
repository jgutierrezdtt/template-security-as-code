# Paso 7. Test de politica

## Objetivo de aprendizaje

Probar la política para evitar regresiones al evolucionarla.

## Archivo y seccion que debes modificar

- Archivo objetivo: `policies/security_test.rego`.
- Seccion donde aplicar el cambio: pruebas automatizadas de la politica.
- Resultado esperado: el repositorio incorpora el control de este paso de forma legible y revisable.

## Cambio que debes introducir

Copia este bloque como base y adáptalo al contexto real del repositorio:

```rego
package security_test

test_public_resource_denied {
  deny with input as {"resource": {"public": true}}
}
```

## Como adaptarlo correctamente

- Incluye al menos un caso permitido y uno denegado.
- Mantén los tests cortos y vinculados a una regla concreta.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-07.py` comprueba el archivo y los marcadores esperados de este paso.
- Debe encontrar el marcador `package security_test` en `policies/security_test.rego`.
- Debe encontrar el marcador `test_public_resource_denied` en `policies/security_test.rego`.

## Criterio de finalizacion

El paso 7 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 8.
