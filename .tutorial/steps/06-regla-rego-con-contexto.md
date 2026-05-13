# Paso 6. Regla rego con contexto

## Objetivo de aprendizaje

Este paso introduce la idea de una regla Rego con contexto y debe dejar un cambio comprensible en `policies/security.rego`.

## Que vas a cambiar y por que

En este paso sigues trabajando sobre la misma política base, pero con una lectura más madura: una regla no vale solo por su condición, sino por el contexto que aporta al resultado. Aunque el validador mantenga la misma estructura, el aprendizaje es que `deny[msg]` representa una decisión con sentido operativo y no una comparación aislada.

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
- Usa el mensaje para aportar contexto de decisión y no solo para repetir el nombre del campo evaluado.
- Piensa esta regla como base para añadir más adelante atributos del recurso, entorno o criticidad.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- La política ya sugiere cómo crecer hacia decisiones más contextuales sin perder claridad.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-06.py` comprueba este paso contra el archivo configurado.
- El workflow busca `package security` dentro de `policies/security.rego`.
- El workflow busca `deny[msg]` dentro de `policies/security.rego`.
- El workflow busca `input.resource.public == true` dentro de `policies/security.rego`.
- El workflow busca `Recurso publico no permitido` dentro de `policies/security.rego`.

## Criterio de finalizacion

El paso 6 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 7.
