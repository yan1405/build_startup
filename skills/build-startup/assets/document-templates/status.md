---
project: "{{project_name}}"
updated: "{{yyyy-mm-dd}}"
product_stage: "{{stage}}"
current_gate: "{{gate}}"
gate_status: "{{pending|approved|blocked|rejected}}"
---

# Estado do produto

## Resumo factual

Registre somente o estado sustentado pelas evidências ligadas abaixo.

## Classificação

- Categoria: `{{category}}`
- Nível de risco: `{{low|moderate|high}}`
- Classificação confirmada por: `{{responsible}}`
- Data da confirmação: `{{yyyy-mm-dd}}`

## Decisão do gate

- Resultado: `{{pending|approved|blocked|rejected}}`
- Justificativa: {{reasoning}}
- Aprovação necessária: {{approval}}

## Bloqueios

- `{{BLOCKER_ID}}` — {{description}}

## Próxima ação

{{single_next_action}}

## Ligações

- Evidências: [EVIDENCE.md](EVIDENCE.md)
- Decisões: [DECISIONS.md](DECISIONS.md)
- Roadmap: [ROADMAP.md](ROADMAP.md)
- Riscos: [RISKS.md](RISKS.md)
