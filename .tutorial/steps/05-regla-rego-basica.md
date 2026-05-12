# Paso 5. Regla rego basica

## Objetivo de aprendizaje

Una política aporta valor cuando traduce una regla de seguridad en lógica ejecutable. Este paso crea esa primera regla base.

## Que vas a cambiar y por que

Escribe una regla Rego que niegue un recurso público y devuelva un mensaje entendible para quien rompe la política.

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

- El mensaje debe explicar la infracción en lenguaje claro.
- Usa una condición simple para que el tutorial sea comprensible en la primera iteración.
- No metas varias políticas en el mismo paso; una regla bien explicada vale más que varias opacas.

## Que deberia verse al terminar

- Existe un `package` coherente y una regla `deny`.
- La condición es fácil de leer.
- El mensaje indica por qué el recurso no está permitido.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-05.py` comprueba este paso contra el archivo configurado.
- El workflow busca `package security` dentro de `policies/security.rego`.

## Criterio de finalizacion

El paso 5 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 6.
