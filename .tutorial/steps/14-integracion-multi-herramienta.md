# Paso 14. Integracion multi herramienta

## Que vas a hacer en este paso?

Implementaras este control de POLICY de forma concreta sobre el archivo `.github/workflows/policy-check.yml` y registraras evidencia tecnica en `.tutorial/evidence/step-14.json`.

## Por que es importante

**En la practica real**:
- Este control reduce riesgo operativo y mejora trazabilidad.
- Permite validar avance real, no solo lectura del tutorial.

**Lo que logras**:
- Resultado tecnico verificable para el paso 14.
- Evidencia auditable para revisiones de seguridad.

---

## Instrucciones paso-a-paso

### Paso 14.1: Prepara el artefacto principal

Crea o actualiza el archivo objetivo de este paso:

```bash
mkdir -p "$(dirname .github/workflows/policy-check.yml)"
touch .github/workflows/policy-check.yml
```

### Paso 14.2: Registra evidencia del paso

Crea el archivo `.tutorial/evidence/step-14.json` con este contenido:

```bash
mkdir -p .tutorial/evidence
cat > .tutorial/evidence/step-14.json << 'EOF'
{
  "step": 14,
  "title": "Integracion multi herramienta",
  "status": "completed",
  "artifact": ".github/workflows/policy-check.yml"
}
EOF
```

---

## Verificacion local

```bash
test -f .github/workflows/policy-check.yml && echo "artifact ok"
python3 -c 'import json;json.load(open(".tutorial/evidence/step-14.json"));print("evidence ok")'
```

---

## Validacion automatica

`validate-step-14.py` verificara:
- Existe `.github/workflows/policy-check.yml`.
- Existe `.tutorial/evidence/step-14.json`.
- La evidencia marca `status=completed` y `step=14`.

---

## Criterio de finalizacion

Paso 14 esta completo cuando:
1. `.github/workflows/policy-check.yml` existe en el repositorio.
2. `.tutorial/evidence/step-14.json` existe y es JSON valido.
3. `.tutorial/state.json` muestra `"current_step": 15`.

**Siguiente paso**: Paso 15
