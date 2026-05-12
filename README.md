# Security as Code

Tutorial avanzado de Security as Code: codificar, versionar y automatizar controles de seguridad como parte del ciclo de desarrollo.

## Objetivo

Aprender a tratar la seguridad como código: políticas versionadas, controles automatizados en pipeline, validación continua, gestión de excepciones programática y gobierno de seguridad reproducible.

## Audiencia

Equipos de AppSec y DevSecOps que quieran escalar controles de seguridad de forma sistemática, tratable y automatizable en toda la organización.

## Requisitos previos

- Experiencia con GitHub Actions.
- Nociones de SAST, SCA o IaC security.
- Conocimientos intermedios de Python o scripting.

## Herramientas utilizadas

- Open Policy Agent (OPA) / Rego
- GitHub Actions
- Scripts de validación del curso
- SARIF

## Inicio del tutorial

[![Empezar tutorial](https://img.shields.io/badge/Empezar%20tutorial-0b69ff?style=for-the-badge&logo=github&logoColor=white)](https://github.com/new?template_name=template-security-as-code&template_owner=jgutierrezdtt)

## Acceso al repositorio

- [Crear mi repositorio desde este template](https://github.com/new?template_name=template-security-as-code&template_owner=jgutierrezdtt)
- [Volver al portal general](https://github.com/jgutierrezdtt/security-learning-portal)

## Gestión del progreso

- [Validar progreso](../../actions/workflows/validate.yml)
- [Probar integridad del tutorial](../../actions/workflows/test-tutorial.yml)
- [Ejecutar tests funcionales del tutorial](../../actions/workflows/functional-tests.yml)
- [Reiniciar tutorial](../../actions/workflows/reset-tutorial.yml)
- [Ver pasos del tutorial](./.tutorial/steps/)

## Tabla de pasos

| Paso | Tema |
| --- | --- |
| 0 | Introducción |
| 1 | Primer control codificado |
| 2 | Control versionado en Git |
| 3 | Pipeline de validación de seguridad |
| 4 | Política como código con OPA |
| 5 | Regla Rego básica |
| 6 | Regla Rego con contexto |
| 7 | Test de política |
| 8 | Excepción programática |
| 9 | Excepción con trazabilidad |
| 10 | Excepción con caducidad |
| 11 | Inventario de controles |
| 12 | Evolución de controles |
| 13 | Quality gate de política |
| 14 | Integración multi-herramienta |
| 15 | Notificación automatizada |
| 16 | Reporting programático |
| 17 | Gobierno centralizado |
| 18 | Métricas de cobertura de controles |
| 19 | Revisión y afinación |
| 20 | Medalla final Security as Code |

## Paso 0

El paso 0 describe el entorno, permisos y limitaciones del laboratorio. No bloquea el flujo: el botón principal abre directamente el paso 1.

## Actualización desde template

Este repositorio incluye `.template-version` y workflow de actualización para revisar cambios del template sin sobrescribir trabajo del usuario.

## Badge final

Al cerrar el curso se generan artefactos de finalización en:

- `.tutorial/badges/completion-badge.md`
- `.tutorial/badges/completion-badge.svg`
- `.tutorial/evidence/completion.json`

## Referencias

- [Open Policy Agent](https://www.openpolicyagent.org/)
- [GitHub Actions](https://docs.github.com/actions)
- [SARIF](https://sarifweb.azurewebsites.net/)
