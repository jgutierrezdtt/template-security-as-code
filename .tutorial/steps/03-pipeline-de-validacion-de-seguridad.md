# Paso 3. Pipeline de validacion de seguridad

## Objetivo de aprendizaje

Este paso introduce el pipeline de validación de seguridad y debe dejar un cambio comprensible en `.github/workflows/policy-check.yml`.

## Que vas a cambiar y por que

En este paso vas a definir `.github/workflows/policy-check.yml` para que las políticas no vivan solo en el repositorio, sino también en la ruta normal de cambios. El valor del pipeline está en convertir una política escrita en una validación repetible sobre `push` y `pull_request`.

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
- Haz visible el job `opa` para que se entienda qué parte del workflow evalúa la política.
- Usa `push` y `pull_request` como señal de que el control ya vive en el flujo real del repositorio.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.
- Se reconoce una automatización mínima para validar políticas en el ciclo de desarrollo.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-03.py` comprueba este paso contra el archivo configurado.
- El workflow busca `name: Policy Check` dentro de `.github/workflows/policy-check.yml`.
- El workflow busca `pull_request:` dentro de `.github/workflows/policy-check.yml`.
- El workflow busca `push:` dentro de `.github/workflows/policy-check.yml`.
- El workflow busca `opa:` dentro de `.github/workflows/policy-check.yml`.

## Criterio de finalizacion

El paso 3 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 4.
