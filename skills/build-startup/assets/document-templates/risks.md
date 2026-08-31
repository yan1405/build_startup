---
project: "{{project_name}}"
updated: "{{yyyy-mm-dd}}"
document: "risk-register"
---

# Riscos

## {{RISK_ID}} — {{short_title}}

- Categoria: `{{product|business|technical|security|privacy|legal|operations|cost}}`
- Estado: `{{open|accepted|mitigated|blocked|closed}}`
- Probabilidade: `{{low|moderate|high}}`
- Impacto: `{{low|moderate|high}}`
- Gate relacionado: `{{gate}}`
- Responsável: {{responsible}}

### Evidência

{{evidence_or_uncertainty}}

### Consequência

{{credible_failure_or_damage}}

### Tratamento

{{avoid|reduce|transfer|accept}} — {{action}}

### Gatilho de escalonamento

{{observable_trigger}}

### Risco residual

{{remaining_risk_after_treatment}}
