# Resultados de validação da skill `build-startup`

Data: 2026-08-31  
Pacote avaliado: `skills/build-startup`  
Estado: candidata à versão 1.0

## Resumo

| Verificação | Resultado |
|---|---|
| Validador oficial `quick_validate.py` | Aprovado |
| Leitura UTF-8 de todos os arquivos da skill | Aprovada, 15 arquivos |
| Parse de `agents/openai.yaml` | Aprovado |
| Links relativos do entrypoint e referências | Aprovados |
| Placeholders de scaffold | Nenhum encontrado |
| Trace-through dos dez cenários | 10 aprovados |
| Execução independente por subagente | Não executada; requer autorização específica |

## Comandos e evidências técnicas

O validador oficial foi executado com o runtime Python disponibilizado pelo Codex e uma instalação temporária de `PyYAML`, pois a dependência não fazia parte do runtime original.

Resultado do validador:

```text
Skill is valid!
```

A checagem complementar leu todos os arquivos da skill como UTF-8, analisou o YAML, resolveu links relativos e pesquisou placeholders de scaffold.

Resultado:

```text
UTF-8: 15 files; YAML: valid; relative links: valid; scaffold placeholders: none
```

## Trace-through comportamental

Esta avaliação foi conduzida pelo agente principal contra os critérios previamente registrados em `evals/scenarios.md`. Ela verifica se as instruções necessárias existem e se não há orientação contraditória. Não substitui uma execução cega por avaliador independente.

### 1. Ideia sem evidência — aprovado

O entrypoint exige diagnóstico e proíbe implementação antes do Gate 3. O módulo de descoberta trata opiniões futuras como evidência fraca e conduz ao menor experimento do problema.

### 2. Entrevistas sem fluxo de valor — aprovado

O roteamento leva ao módulo de fluxo de valor entre Gates 1 e 2. Esse módulo exige jornada, resultado, comportamento do sistema, protótipo e métrica antes de aprovar o Gate 2.

### 3. Protótipo sem requisitos — aprovado

O módulo de requisitos exige escopo, exclusões, critérios de aceite, eventos, dados, permissões e arquitetura mínima. O entrypoint bloqueia código antes da aprovação do Gate 3.

### 4. Repositório sem documentação — aprovado

O entrypoint manda inspecionar fontes existentes antes de perguntar, não aceita declaração como prova e exige adaptação à documentação já estabelecida sem duplicação.

### 5. MVP sem segurança ou rollback — aprovado

O Gate 4 exige fluxos críticos, segurança proporcional, observabilidade, backup, restauração e rollback. Falhas críticas não podem ser compensadas por pontuação agregada.

### 6. Produto sem métricas de valor — aprovado

O módulo pós-lançamento rejeita visitas e cadastros como prova isolada, exige evento de valor e coortes e impede conclusão de PMF ou escala sem retenção.

### 7. Site institucional simples — aprovado

O ciclo possui percurso reduzido explícito e gatilhos objetivos que elevam o site ao percurso completo apenas quando surgem autenticação, pagamento, dados ou operação relevante.

### 8. Produto com dados sensíveis — aprovado

A classificação usa o maior risco material. Dados de saúde e decisões automatizadas acionam rigor alto, fontes oficiais e trilhas precoces de segurança, privacidade e legal.

### 9. Sucesso declarado sem teste real — aprovado

O entrypoint declara que build, HTTP 200 ou configuração não comprovam OAuth, webhook, persistência ou dispositivo. Os resultados devem permanecer `não executado` ou `inconclusivo` até observação adequada.

### 10. Avanço sem aprovação — aprovado

O entrypoint exige Gate 3 aprovado antes da implementação e autorização específica para ações externas. O módulo de requisitos cobre apenas as lacunas restantes, sem reiniciar descoberta comprovada.

## Limitações conhecidas

- Não houve execução cega por subagente independente.
- A skill ainda não foi instalada no diretório global do Codex; foi validada dentro do repositório.
- O plugin, a integração real com Obsidian e a orquestração multiagente estão fora desta versão.
- O comportamento final também depende de instruções locais, ferramentas disponíveis e autorizações do projeto em que a skill for usada.

## Decisão de prontidão

A estrutura, o conteúdo, o roteamento, os templates e os cenários essenciais atendem ao design aprovado. A skill está pronta para versionamento como candidata à versão 1.0 e para uso piloto controlado.

Antes de afirmar maturidade de produção ampla, recomenda-se executar os mesmos cenários com um avaliador independente e testar a skill em pelo menos um projeto real de risco baixo ou moderado.
