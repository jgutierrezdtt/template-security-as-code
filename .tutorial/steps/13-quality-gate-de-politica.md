# Paso 13. Quality gate de politica

## Que vas a hacer en este paso?

Implementaras este control de POLICY de forma concreta sobre el archivo `.github/workflows/policy-check.yml` y registraras evidencia tecnica en `.tutorial/evidence/step-13.json`.

## Por que es importante

**En la practica real**:
- Este control reduce riesgo operativo y mejora trazabilidad.
- Permite validar avance real, no solo lectura del tutorial.

**Lo que logras**:
- Resultado tecnico verificable para el paso 13.
- Evidencia auditable para revisiones de seguridad.

---

## Instrucciones paso-a-paso

### Paso 13.1: Prepara el artefacto principal

Crea o actualiza el archivo objetivo de este paso:

```bash
mkdir -p "$(dirname .github/workflows/policy-check.yml)"
touch .github/workflows/policy-check.yml
```

### Paso 13.2: Registra evidencia del paso

Crea el archivo `.tutorial/evidence/step-13.json` con este contenido:

```bash
mkdir -p .tutorial/evidence
cat > .tutorial/evidence/step-13.json << 'EOF'
{
  "step": 13,
  "title": "Quality gate de politica",
  "status": "completed",
  "artifact": ".github/workflows/policy-check.yml"
}
EOF
```

---

## Verificacion local

```bash
test -f .github/workflows/policy-check.yml && echo "artifact ok"
python3 -c 'import json;json.load(open(".tutorial/evidence/step-13.json"));print("evidence ok")'
```

---

## Validacion automatica

`validate-step-13.py` verificara:
- Existe `.github/workflows/policy-check.yml`.
- Existe `.tutorial/evidence/step-13.json`.
- La evidencia marca `status=completed` y `step=13`.

---

## Criterio de finalizacion

Paso 13 esta completo cuando:
1. `.github/workflows/policy-check.yml` existe en el repositorio.
2. `.tutorial/evidence/step-13.json` existe y es JSON valido.
3. `.tutorial/state.json` muestra `"current_step": 14`.

**Siguiente paso**: Paso 14
