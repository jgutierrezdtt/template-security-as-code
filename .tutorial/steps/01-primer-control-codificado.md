# Paso 1. Primer control codificado

## Objetivo de aprendizaje

Este paso introduce un primer control real de Security as Code y debe dejar un cambio comprensible en `policies/security.rego`.

## Que vas a cambiar y por que

En este paso vas a crear una política Rego mínima pero útil: una regla `deny[msg]` que rechace recursos públicos. La idea es que el laboratorio arranque con un control pequeño, comprensible y claramente evaluable, no solo con un fichero vacío o un `package` sin lógica.

## Archivo y seccion que debes modificar

- Archivo objetivo: `policies/security.rego`.
- Aplícalo en la parte del archivo que corresponde al título del paso.
- Si el archivo aún no existe, créalo con este contenido inicial y luego evoluciona desde ahí en los siguientes pasos.

## Cambio base recomendado

Este bloque no es para pegar a ciegas: úsalo como punto de partida y ajústalo al contexto del repositorio.

```rego
package security

deny[msg] {
  input.resource.public == true
  msg := "Recurso publico no permitido"
}
```

## Como adaptarlo correctamente

- Mantén el cambio pequeño y centrado en una sola idea por paso.
- Usa `deny[msg]` como patrón base para que la política produzca un resultado interpretable.
- Expresa la condición de forma directa; aquí importa más el criterio del control que la sofisticación de la sintaxis.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- Ya existe una política capaz de rechazar un caso sencillo de exposición pública.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-01.py` comprueba este paso contra el archivo configurado.
- El workflow busca `package security` dentro de `policies/security.rego`.
- El workflow busca `deny[msg]` dentro de `policies/security.rego`.
- El workflow busca `input.resource.public == true` dentro de `policies/security.rego`.
- El workflow busca `Recurso publico no permitido` dentro de `policies/security.rego`.

## Criterio de finalizacion

El paso 1 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 2.
