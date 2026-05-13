# Paso 9. Excepcion con trazabilidad

## Objetivo de aprendizaje

Este paso introduce la trazabilidad de excepciones y debe dejar un cambio comprensible en `docs/policy-exceptions.yml`.

## Que vas a cambiar y por que

En este paso sigues trabajando sobre `docs/policy-exceptions.yml`, pero ahora con un objetivo más maduro: que la excepción no sea solo interpretable por código, sino también rastreable por personas y proceso. La trazabilidad aparece cuando la excepción deja clara la política afectada, el alcance concreto, el motivo y la fecha de revisión.

## Archivo y seccion que debes modificar

- Archivo objetivo: `docs/policy-exceptions.yml`.
- Aplícalo en la parte del archivo que corresponde al título del paso.
- Si el archivo aún no existe, créalo con este contenido inicial y luego evoluciona desde ahí en los siguientes pasos.

## Cambio base recomendado

Este bloque no es para pegar a ciegas: úsalo como punto de partida y ajústalo al contexto del repositorio.

```yaml
exceptions:
  - policy: deny_public_resource
    scope: resource/demo-public-bucket
    reason: "Excepcion temporal documentada para caso legado identificado"
    expires_on: "2026-12-31"
```

## Como adaptarlo correctamente

- Mantén el cambio pequeño y centrado en una sola idea por paso.
- Redacta `reason` de forma que otra persona pueda revisar si la excepción sigue siendo válida.
- Usa `scope` para evitar excepciones demasiado amplias que nadie pueda cerrar después.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- La excepción ya parece un elemento revisable del programa y no una nota olvidada.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-09.py` comprueba este paso contra el archivo configurado.
- El workflow busca `exceptions:` dentro de `docs/policy-exceptions.yml`.
- El workflow busca `policy:` dentro de `docs/policy-exceptions.yml`.
- El workflow busca `scope:` dentro de `docs/policy-exceptions.yml`.
- El workflow busca `reason:` dentro de `docs/policy-exceptions.yml`.
- El workflow busca `expires_on:` dentro de `docs/policy-exceptions.yml`.

## Criterio de finalizacion

El paso 9 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 10.
