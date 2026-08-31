# Build Startup — plano de implementação da skill

Data: 2026-08-31  
Base: `docs/plans/2026-08-31-build-startup-skill-design.md`  
Escopo: implementar e validar a primeira versão da skill `build-startup`  
Fora de escopo: plugin, integração real com Obsidian e execução multiagente

## 1. Resultado esperado

Ao final deste plano, o repositório deverá conter uma skill Codex instalável e validada que:

- diagnostica o estado de um produto digital existente antes de entrevistar o fundador;
- classifica estágio, categoria e risco com justificativa verificável;
- conduz o projeto até o próximo gate comprovável;
- carrega somente as referências necessárias à fase atual;
- mantém documentação Markdown progressiva e compatível com Obsidian;
- separa evidências, decisões, hipóteses, estimativas, bloqueios e conteúdo desatualizado;
- aplica pesquisa proporcional ao risco e uma hierarquia explícita de fontes;
- impede implementação antes do Gate 3 e publicação sem autorização específica;
- passa na validação estrutural oficial e nos cenários comportamentais essenciais.

## 2. Estrutura-alvo do repositório

```text
build_startup/
|-- docs/
|   `-- plans/
|       |-- 2026-08-31-build-startup-skill-design.md
|       `-- 2026-08-31-build-startup-skill-implementation.md
|-- skills/
|   `-- build-startup/
|       |-- SKILL.md
|       |-- agents/
|       |   `-- openai.yaml
|       |-- references/
|       |   |-- lifecycle-and-gates.md
|       |   |-- evidence-and-sources.md
|       |   |-- discovery-and-business.md
|       |   |-- value-flow-and-ux.md
|       |   |-- requirements-and-architecture.md
|       |   |-- engineering-and-quality.md
|       |   |-- launch-and-operations.md
|       |   `-- post-launch-and-scale.md
|       `-- assets/
|           `-- document-templates/
|               |-- status.md
|               |-- evidence.md
|               |-- decisions.md
|               |-- roadmap.md
|               `-- risks.md
`-- evals/
    |-- scenarios.md
    `-- validation-results.md
```

Os templates especializados, como PRD, ADR ou plano de métricas, somente serão adicionados se os módulos demonstrarem necessidade concreta durante a implementação. A primeira versão não terá scripts próprios.

## 3. Etapa 1 — Inicializar a skill

### Ações

1. Executar o inicializador oficial com o nome `build-startup`, destino `skills/` e recursos `references,assets`.
2. Remover qualquer exemplo ou placeholder gerado que não pertença ao design aprovado.
3. Confirmar que o scaffold criou `SKILL.md` e `agents/openai.yaml`.
4. Manter invocação implícita habilitada.

### Interface inicial

- `display_name`: `Build Startup`
- `short_description`: descrição curta entre 25 e 64 caracteres, voltada ao ciclo de produtos digitais.
- `default_prompt`: uma frase que mencione explicitamente `$build-startup` e peça diagnóstico do projeto até o próximo gate.

Ícones e cor de marca não entram na primeira versão, pois ainda não existe identidade visual aprovada.

### Critério de aceite

O scaffold deve existir sem placeholders não resolvidos e passar na validação estrutural inicial, mesmo antes de o conteúdo final ser escrito.

## 4. Etapa 2 — Implementar o orquestrador em `SKILL.md`

### Conteúdo obrigatório

O entrypoint deverá conter apenas as regras compartilhadas que mudam decisões:

1. propósito, público e limites de aplicação;
2. diagnóstico antes da entrevista;
3. classificação proposta e confirmada;
4. unidade de sucesso: próximo gate comprovável;
5. estados de informação;
6. exigência de aprovação nos gates;
7. bloqueio de implementação antes do Gate 3;
8. autorização específica para publicação, custos e ações externas;
9. roteamento para cada referência;
10. formato mínimo da saída de cada execução.

### Limites de descoberta

A descrição deverá acionar a skill para criação, auditoria ou continuidade de SaaS, web apps, mobile apps, plataformas e marketplaces. Deverá evitar ativação em alterações isoladas de código ou sites simples sem ciclo de produto, salvo quando o usuário pedir o percurso reduzido.

### Critério de aceite

Outro agente deve conseguir selecionar o módulo correto sem carregar todos os arquivos de referência. Toda referência necessária deve estar ligada diretamente a partir do `SKILL.md` ou de uma referência já carregada.

## 5. Etapa 3 — Implementar as referências compartilhadas

### `lifecycle-and-gates.md`

Definir:

- as três dimensões de classificação;
- os seis gates;
- critérios obrigatórios, condicionais e sinais de alerta;
- regras de avanço, reprovação e correção;
- trilhas transversais de segurança, privacidade, acessibilidade, custo e mensuração;
- percurso reduzido para sites institucionais.

### `evidence-and-sources.md`

Definir:

- estados `VERIFIED`, `APPROVED`, `HYPOTHESIS`, `ESTIMATE`, `BLOCKER` e `STALE`;
- distinção entre fonte conceitual, evidência do projeto e inferência;
- hierarquia de fontes aprovada;
- registro de autoria, data, consulta, afirmação e limitação;
- tratamento de fontes conflitantes e informação desatualizada;
- proibição de inventar entrevistas, métricas, usuários ou resultados.

### Critério de aceite

Os módulos compartilhados devem permitir justificar qualquer decisão de gate sem depender de regras duplicadas nos módulos de fase.

## 6. Etapa 4 — Implementar os módulos de fase

Cada módulo deverá conter: objetivo, quando carregar, entradas esperadas, perguntas mínimas, entregáveis possíveis, critérios do gate relacionados, bloqueios comuns e evidências aceitáveis.

### `discovery-and-business.md`

- problema, público, comportamento passado e alternativa atual;
- intensidade, frequência e disposição a pagar;
- modelo de negócio e distribuição;
- referências preferenciais: Blank, Fitzpatrick, Osterwalder e Bezos.

### `value-flow-and-ux.md`

- jornada `AS IS` e `TO BE`;
- fluxo funcional do cliente e comportamento do sistema;
- dados, permissões, caminho principal e falhas;
- métrica de valor;
- prototipação e testes com usuários;
- referências preferenciais: Cagan e Knapp.

### `requirements-and-architecture.md`

- MVP, exclusões explícitas e critérios de aceite;
- requisitos funcionais e não funcionais;
- eventos de mensuração;
- modelo de dados, permissões e integrações;
- ADRs, topologia e riscos;
- referências preferenciais: Nygard e Fowler.

### `engineering-and-quality.md`

- fatias verticais;
- ambiente, CI e testes proporcionais;
- segurança, observabilidade e custos;
- preservação do trabalho existente;
- evidência direta de fluxos críticos;
- referências preferenciais: DORA, Humble, Fowler e OWASP.

### `launch-and-operations.md`

- beta controlado e prontidão;
- QA, privacidade, backup, restauração e rollback;
- domínio, lojas e requisitos atuais;
- suporte, alertas e autorização para publicação;
- referências primárias obrigatórias para plataformas e regulação.

### `post-launch-and-scale.md`

- ativação, retenção, valor entregue e receita;
- interpretação contextual do teste de 40%;
- métrica norte e métricas de proteção;
- dívida técnica e sinais reais de escala;
- referências preferenciais: Ries, Graham, Andreessen, Ellis e Singer.

### Critério de aceite

Nenhum módulo poderá transformar um framework em regra universal. Números e práticas fixas devem declarar contexto, limitações ou condições de adaptação.

## 7. Etapa 5 — Implementar templates documentais

Criar cinco templates mínimos em `assets/document-templates/`:

### `status.md`

- frontmatter com projeto, data, estágio, gate e status;
- resumo factual;
- bloqueios;
- próxima ação;
- links para evidências e decisões.

### `evidence.md`

- identificador;
- estado;
- afirmação;
- fonte;
- data da fonte e da consulta;
- evidência observada;
- inferência;
- confiabilidade e limitações.

### `decisions.md`

- decisão;
- estado de aprovação;
- contexto;
- alternativas;
- justificativa;
- consequências;
- gatilho de revisão.

### `roadmap.md`

- gate atual;
- resultado pretendido;
- atividades somente até o próximo gate;
- dependências;
- critérios de conclusão.

### `risks.md`

- categoria;
- probabilidade e impacto qualitativos;
- evidência;
- mitigação;
- responsável;
- gatilho de escalonamento.

### Critério de aceite

Os templates devem funcionar em Markdown comum e no Obsidian, sem depender de plugin específico, URI proprietária ou banco de dados externo.

## 8. Etapa 6 — Validação estrutural e revisão de qualidade

### Validações automáticas

1. Executar `quick_validate.py` na pasta `skills/build-startup`.
2. Verificar frontmatter, nome, descrição e placeholders.
3. Verificar que `agents/openai.yaml` usa strings entre aspas e que `default_prompt` menciona `$build-startup`.
4. Confirmar que todos os links relativos apontam para arquivos existentes.
5. Pesquisar duplicações desnecessárias de regras entre `SKILL.md` e referências.

### Revisão manual

- descrição discriminante;
- entrypoint enxuto;
- referências carregadas progressivamente;
- requisitos proporcionais ao risco;
- autorizações preservadas;
- nenhuma promessa de acesso a ferramentas inexistentes;
- plugin e Obsidian descritos somente como evolução futura.

### Critério de aceite

Validador oficial aprovado, links íntegros, nenhum placeholder e nenhuma inconsistência conhecida entre gates, módulos e templates.

## 9. Etapa 7 — Avaliações comportamentais

Registrar em `evals/scenarios.md` os dez cenários aprovados no design. Para cada cenário, definir:

- contexto mínimo entregue à skill;
- evidências presentes e ausentes;
- classificação esperada ou faixa aceitável;
- gate máximo permitido;
- comportamento proibido;
- artefato ou decisão observável esperada.

Executar primeiro cinco cenários prioritários:

1. ideia sem evidência;
2. entrevistas sem fluxo de valor;
3. repositório desenvolvido sem documentação;
4. MVP sem segurança ou rollback;
5. pedido de avanço sem aprovação do gate.

Depois executar os cinco cenários restantes. Usar espaços temporários para que os resultados não alterem o pacote da skill.

Uma avaliação independente por subagente ficará condicionada a autorização explícita do usuário. Sem essa autorização, a validação será conduzida no agente principal com entradas isoladas e critérios previamente registrados.

### Critério de aceite

- nenhum cenário crítico avança indevidamente;
- ausência de evidência não é tratada como evidência negativa;
- a skill não inventa dados;
- o percurso reduzido não recebe burocracia do percurso completo;
- bloqueios críticos permanecem visíveis;
- documentos gerados são coerentes entre si.

## 10. Etapa 8 — Resultado e versionamento

Registrar em `evals/validation-results.md`:

- versão ou commit testado;
- comandos executados;
- cenários aprovados e reprovados;
- limitações;
- correções aplicadas;
- decisão de prontidão.

Sequência de commits recomendada:

1. `chore: scaffold build-startup skill`
2. `feat: add lifecycle and evidence framework`
3. `feat: add phase modules and document templates`
4. `test: add build-startup evaluation scenarios`
5. `docs: record skill validation results`

Somente publicar cada commit após verificar que ele não inclui arquivos não relacionados.

## 11. Definição de pronto da versão 1.0

A skill estará pronta quando:

- todos os arquivos planejados existirem e estiverem ligados corretamente;
- `quick_validate.py` passar;
- os dez cenários estiverem documentados;
- os cinco cenários críticos e os cinco complementares tiverem resultado registrado;
- nenhum gate crítico puder ser pulado sem aprovação;
- o percurso reduzido estiver funcional;
- a documentação gerada for compatível com Markdown, Git e Obsidian;
- limitações e capacidades futuras estiverem explícitas;
- o repositório estiver limpo e sincronizado com `origin/main`.

## 12. Ordem de execução imediata

Quando a implementação for autorizada:

1. criar o scaffold oficial;
2. validar o scaffold;
3. escrever `SKILL.md`;
4. escrever as duas referências compartilhadas;
5. validar o roteamento;
6. escrever os seis módulos de fase;
7. criar os cinco templates;
8. executar validação estrutural;
9. escrever e executar os cenários;
10. registrar resultados, revisar e versionar.
