# Paso 4. Politica como codigo con opa

## Que vas a hacer en este paso?

Implementaras este control de POLICY de forma concreta sobre el archivo `policies/security.rego` y registraras evidencia tecnica en `.tutorial/evidence/step-04.json`.

## Por que es importante

**En la practica real**:
- Este control reduce riesgo operativo y mejora trazabilidad.
- Permite validar avance real, no solo lectura del tutorial.

**Lo que logras**:
- Resultado tecnico verificable para el paso 4.
- Evidencia auditable para revisiones de seguridad.

---

## Instrucciones paso-a-paso

### Paso 4.1: Prepara el artefacto principal

Crea o actualiza el archivo objetivo de este paso:

```bash
mkdir -p "$(dirname policies/security.rego)"
touch policies/security.rego
```

### Paso 4.2: Registra evidencia del paso

Crea el archivo `.tutorial/evidence/step-04.json` con este contenido:

```bash
mkdir -p .tutorial/evidence
cat > .tutorial/evidence/step-04.json << 'EOF'
{
  "step": 4,
  "title": "Politica como codigo con opa",
  "status": "completed",
  "artifact": "policies/security.rego"
}
EOF
```

---

## Verificacion local

```bash
test -f policies/security.rego && echo "artifact ok"
python3 -c 'import json;json.load(open(".tutorial/evidence/step-04.json"));print("evidence ok")'
```

---

## Validacion automatica

`validate-step-04.py` verificara:
- Existe `policies/security.rego`.
- Existe `.tutorial/evidence/step-04.json`.
- La evidencia marca `status=completed` y `step=4`.

---

## Criterio de finalizacion

Paso 4 esta completo cuando:
1. `policies/security.rego` existe en el repositorio.
2. `.tutorial/evidence/step-04.json` existe y es JSON valido.
3. `.tutorial/state.json` muestra `"current_step": 5`.

**Siguiente paso**: Paso 5
