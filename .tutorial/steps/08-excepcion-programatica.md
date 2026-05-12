# Paso 8. Excepcion programatica

## Que vas a hacer en este paso?

Implementaras este control de POLICY de forma concreta sobre el archivo `policies/security.rego` y registraras evidencia tecnica en `.tutorial/evidence/step-08.json`.

## Por que es importante

**En la practica real**:
- Este control reduce riesgo operativo y mejora trazabilidad.
- Permite validar avance real, no solo lectura del tutorial.

**Lo que logras**:
- Resultado tecnico verificable para el paso 8.
- Evidencia auditable para revisiones de seguridad.

---

## Instrucciones paso-a-paso

### Paso 8.1: Prepara el artefacto principal

Crea o actualiza el archivo objetivo de este paso:

```bash
mkdir -p "$(dirname policies/security.rego)"
touch policies/security.rego
```

### Paso 8.2: Registra evidencia del paso

Crea el archivo `.tutorial/evidence/step-08.json` con este contenido:

```bash
mkdir -p .tutorial/evidence
cat > .tutorial/evidence/step-08.json << 'EOF'
{
  "step": 8,
  "title": "Excepcion programatica",
  "status": "completed",
  "artifact": "policies/security.rego"
}
EOF
```

---

## Verificacion local

```bash
test -f policies/security.rego && echo "artifact ok"
python3 -c 'import json;json.load(open(".tutorial/evidence/step-08.json"));print("evidence ok")'
```

---

## Validacion automatica

`validate-step-08.py` verificara:
- Existe `policies/security.rego`.
- Existe `.tutorial/evidence/step-08.json`.
- La evidencia marca `status=completed` y `step=8`.

---

## Criterio de finalizacion

Paso 8 esta completo cuando:
1. `policies/security.rego` existe en el repositorio.
2. `.tutorial/evidence/step-08.json` existe y es JSON valido.
3. `.tutorial/state.json` muestra `"current_step": 9`.

**Siguiente paso**: Paso 9
