# Paso 7. Test de politica

## Objetivo de aprendizaje

Este paso introduce un control de Security as Code y debe dejar un cambio comprensible en policies/security_test.rego.

## Que vas a cambiar y por que

Actualiza policies/security_test.rego para que el control de "test de politica" quede explícito y revisable.

## Archivo y seccion que debes modificar

- Archivo objetivo: `policies/security_test.rego`.
- Aplícalo en la parte del archivo que corresponde al título del paso.
- Si el archivo aún no existe, créalo con este contenido inicial y luego evoluciona desde ahí en los siguientes pasos.

## Cambio base recomendado

Este bloque no es para pegar a ciegas: úsalo como punto de partida y ajústalo al contexto del repositorio.

```rego
package security_test
test_public_resource_denied
```

## Como adaptarlo correctamente

- Mantén el cambio pequeño y centrado en una sola idea por paso.
- Usa nombres claros para secciones, reglas o jobs.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-07.py` comprueba este paso contra el archivo configurado.
- El workflow busca `package security_test` dentro de `policies/security_test.rego`.
- El workflow busca `test_public_resource_denied` dentro de `policies/security_test.rego`.

## Criterio de finalizacion

El paso 7 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 8.
