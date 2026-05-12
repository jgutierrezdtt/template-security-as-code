# Paso 18. Metricas de cobertura de controles

## Que vas a hacer en este paso?

Implementaras este control de POLICY de forma concreta sobre el archivo `docs/security-as-code.md` y registraras evidencia tecnica en `.tutorial/evidence/step-18.json`.

## Por que es importante

**En la practica real**:
- Este control reduce riesgo operativo y mejora trazabilidad.
- Permite validar avance real, no solo lectura del tutorial.

**Lo que logras**:
- Resultado tecnico verificable para el paso 18.
- Evidencia auditable para revisiones de seguridad.

---

## Instrucciones paso-a-paso

### Paso 18.1: Prepara el artefacto principal

Crea o actualiza el archivo objetivo de este paso:

```bash
mkdir -p "$(dirname docs/security-as-code.md)"
touch docs/security-as-code.md
```

### Paso 18.2: Registra evidencia del paso

Crea el archivo `.tutorial/evidence/step-18.json` con este contenido:

```bash
mkdir -p .tutorial/evidence
cat > .tutorial/evidence/step-18.json << 'EOF'
{
  "step": 18,
  "title": "Metricas de cobertura de controles",
  "status": "completed",
  "artifact": "docs/security-as-code.md"
}
EOF
```

---

## Verificacion local

```bash
test -f docs/security-as-code.md && echo "artifact ok"
python3 -c 'import json;json.load(open(".tutorial/evidence/step-18.json"));print("evidence ok")'
```

---

## Validacion automatica

`validate-step-18.py` verificara:
- Existe `docs/security-as-code.md`.
- Existe `.tutorial/evidence/step-18.json`.
- La evidencia marca `status=completed` y `step=18`.

---

## Criterio de finalizacion

Paso 18 esta completo cuando:
1. `docs/security-as-code.md` existe en el repositorio.
2. `.tutorial/evidence/step-18.json` existe y es JSON valido.
3. `.tutorial/state.json` muestra `"current_step": 19`.

**Siguiente paso**: Paso 19
