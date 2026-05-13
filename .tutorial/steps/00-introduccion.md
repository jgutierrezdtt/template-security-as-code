# Paso 0. Introducción

Este laboratorio está pensado para practicar Security as Code como disciplina operativa, no solo como concepto. La idea central es tratar controles, políticas, excepciones, evidencias y decisiones de gobierno igual que cualquier otro activo técnico: versionados, revisables, automatizables y sujetos a mejora continua.

## Qué vas a trabajar

Durante el recorrido vas a combinar varias piezas que en muchos equipos aparecen separadas:

- controles expresados directamente como archivos y reglas
- políticas evaluables en pipeline
- excepciones registradas con criterio y trazabilidad
- inventario, reporting y métricas para operar el programa
- gobierno centralizado para evitar decisiones dispersas o contradictorias

## Qué problema intenta resolver este laboratorio

Cuando la seguridad se gestiona fuera del código, suelen aparecer los mismos problemas:

- controles difíciles de reproducir entre equipos
- excepciones acordadas pero no registradas
- pipelines que validan cosas distintas según el repositorio
- reporting que llega tarde o sin contexto suficiente

Security as Code busca precisamente lo contrario: que la seguridad tenga una representación explícita, tratable y verificable dentro del mismo ciclo de desarrollo.

## Cómo se recorre el tutorial

El orden del laboratorio importa. Primero defines controles y su soporte versionado, luego introduces políticas y tests, después gestionas excepciones y finalmente cierras con inventario, reporting y gobierno. Esa secuencia convierte reglas sueltas en un programa mantenible.

## Qué conviene tener claro antes de empezar

- una política útil no es solo correcta; también tiene que ser operable
- una excepción sin responsable ni fecha termina erosionando el control
- un quality gate sin criterio degrada la confianza igual que la ausencia de gate
- métricas y reporting solo aportan valor si ayudan a decidir qué hacer después

## Siguiente paso

El botón **Empezar tutorial** abre directamente el paso 1.
