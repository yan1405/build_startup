---
project: "{{project_name}}"
updated: "{{yyyy-mm-dd}}"
document: "decision-log"
---

# Decisões

## {{DECISION_ID}} — {{short_title}}

- Estado: `{{APPROVED|pending|rejected|superseded}}`
- Data: {{yyyy-mm-dd}}
- Responsável pela aprovação: {{responsible}}
- Gate relacionado: `{{gate}}`

### Contexto

{{context}}

### Evidências usadas

- [{{EVIDENCE_ID}}](EVIDENCE.md#{{evidence_anchor}})

### Alternativas consideradas

1. {{option_and_tradeoff}}
2. {{option_and_tradeoff}}

### Decisão e justificativa

{{decision_and_reasoning}}

### Consequências e riscos aceitos

{{consequences}}

### Gatilho de revisão

{{observable_condition_for_review}}
