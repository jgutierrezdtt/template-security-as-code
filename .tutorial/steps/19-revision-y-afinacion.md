# Paso 19. Revision y afinacion

## Objetivo de aprendizaje

Explicar cómo evoluciona y gobierna el conjunto de controles codificados.

## Archivo y seccion que debes modificar

- Archivo objetivo: `docs/security-as-code.md`.
- Seccion donde aplicar el cambio: documentación operativa del programa.
- Resultado esperado: el repositorio incorpora el control de este paso de forma legible y revisable.

## Cambio que debes introducir

Copia este bloque como base y adáptalo al contexto real del repositorio:

```markdown
## Inventario de controles
## Cobertura actual
## Excepciones activas
## Siguiente iteracion
```

## Como adaptarlo correctamente

- Usa esta documentación para mostrar qué controles ya están codificados y cuáles faltan.
- Relaciona cada control con su política o workflow asociado.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-19.py` comprueba el archivo y los marcadores esperados de este paso.
- Debe encontrar el marcador `## Inventario de controles` en `docs/security-as-code.md`.
- Debe encontrar el marcador `## Cobertura actual` en `docs/security-as-code.md`.
- Debe encontrar el marcador `## Excepciones activas` en `docs/security-as-code.md`.
- Debe encontrar el marcador `## Siguiente iteracion` en `docs/security-as-code.md`.

## Criterio de finalizacion

El paso 19 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 20.
