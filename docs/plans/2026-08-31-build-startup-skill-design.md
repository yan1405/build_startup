# Build Startup — especificação de design da skill

Data: 2026-08-31  
Status: aprovado para planejamento de implementação

## 1. Propósito e público

`build-startup` será uma skill orquestradora híbrida do ciclo de construção de produtos digitais interativos. Seu público principal será formado por fundadores técnicos solo e equipes pequenas.

Ela atenderá SaaS, aplicativos web e mobile, plataformas e marketplaces. Sites institucionais simples receberão um percurso reduzido e proporcional ao risco.

A skill deverá:

- diagnosticar projetos existentes antes de entrevistar o fundador;
- aproveitar evidências e documentos já produzidos;
- identificar o estágio real do produto;
- conduzir somente o trabalho necessário até o próximo gate;
- orquestrar o ciclo completo, da descoberta ao pós-lançamento;
- manter análise imparcial, crítica e baseada em evidências;
- registrar o trabalho em Markdown versionado e compatível com Obsidian.

## 2. Diagnóstico inicial

Toda execução começa pela inspeção dos materiais disponíveis, como repositório, documentos, pesquisas, protótipos, decisões e testes.

A skill propõe uma classificação em três dimensões:

1. estágio do produto;
2. categoria do produto;
3. nível de risco.

A classificação deve conter justificativa e evidências. Ela somente se torna oficial depois da confirmação do fundador.

O resultado inicial será um Mapa de Estado do Projeto contendo:

- estágio proposto;
- categoria do produto;
- nível de risco;
- evidências encontradas;
- lacunas;
- bloqueios;
- próximo gate recomendado.

## 3. Arquitetura da skill

O `SKILL.md` funcionará como orquestrador enxuto. Ele conterá as regras de diagnóstico, classificação, seleção do próximo gate, aprovação e carregamento progressivo.

Os procedimentos detalhados serão separados nos seguintes módulos:

```text
build-startup/
|-- SKILL.md
|-- agents/
|   `-- openai.yaml
|-- references/
|   |-- lifecycle-and-gates.md
|   |-- evidence-and-sources.md
|   |-- discovery-and-business.md
|   |-- value-flow-and-ux.md
|   |-- requirements-and-architecture.md
|   |-- engineering-and-quality.md
|   |-- launch-and-operations.md
|   `-- post-launch-and-scale.md
`-- assets/
    `-- document-templates/
```

Não haverá scripts na primeira versão, salvo se a implementação demonstrar uma transformação repetitiva que exija execução determinística.

## 4. Ciclo operacional e gates

Cada execução terá como unidade de sucesso a conclusão do próximo gate comprovável.

### Gate 1 — Problema comprovado

Deve haver evidência de comportamento real, intensidade do problema, público prioritário e alternativa atual.

### Gate 2 — Valor e solução compreendidos

A jornada atual, o fluxo de valor, o resultado desejado e o protótipo devem ter sido avaliados com usuários representativos.

### Gate 3 — Construção autorizada

MVP, critérios de aceite, métricas, dados, permissões, riscos e arquitetura mínima devem estar suficientemente definidos.

### Gate 4 — Publicação autorizada

Fluxos críticos, segurança proporcional, privacidade, testes, monitoramento, backup e rollback devem estar verificados.

### Gate 5 — Valor em produção comprovado

Devem existir dados reais de ativação, uso, entrega de valor, retenção e problemas operacionais.

### Gate 6 — Escala autorizada

Sinais combinados de retenção, receita, satisfação, capacidade operacional e demanda devem justificar o aumento de investimento ou complexidade.

Cada gate terá critérios obrigatórios, critérios condicionais e sinais de alerta. Uma falha crítica não poderá ser compensada por uma pontuação agregada.

Avançar para o gate seguinte exige aprovação explícita. Uma reprovação abre um ciclo de correção limitado às lacunas encontradas, sem reiniciar o processo inteiro.

## 5. Fluxo de valor obrigatório

Entre a visão do produto e a descoberta da solução, a skill deverá exigir uma etapa explícita de fluxo de valor, jornada e funcionamento do produto.

Essa etapa deve identificar:

1. usuário prioritário e contexto;
2. resultado desejado;
3. jornada atual, ou `AS IS`;
4. jornada proposta, ou `TO BE`;
5. fluxo funcional do cliente;
6. comportamento interno do sistema;
7. dados e permissões envolvidos;
8. métrica que comprova valor entregue;
9. caminho principal, exceções e falhas relevantes.

O fluxo termina no resultado percebido pelo cliente, não apenas na ação realizada dentro da interface.

## 6. Documentação e fonte de verdade

A skill deverá adaptar-se à estrutura existente. Quando não houver fonte equivalente, sugerirá `docs/product-lifecycle/`.

O núcleo documental será progressivo:

- `STATUS.md`: estágio, gate, resumo factual, bloqueios e próxima ação;
- `EVIDENCE.md`: evidências internas e externas, origem, data, confiabilidade e conclusão sustentada;
- `DECISIONS.md`: decisões aprovadas, alternativas e consequências;
- `ROADMAP.md`: percurso até o próximo gate;
- `RISKS.md`: riscos de produto, negócio, tecnologia, segurança, privacidade e operação.

Documentos especializados serão criados somente quando necessários. Exemplos incluem fluxo de valor, pesquisa com usuários, PRD, modelo de dados, ADRs, plano de métricas, análise de ameaças, estratégia de testes e checklist de publicação.

Os estados padronizados serão:

- `VERIFIED`: sustentado por fonte ou teste verificável;
- `APPROVED`: decisão explicitamente aceita;
- `HYPOTHESIS`: ainda requer experimento;
- `ESTIMATE`: aproximação com premissas declaradas;
- `BLOCKER`: impede o gate atual;
- `STALE`: evidência possivelmente desatualizada.

Os arquivos usarão Markdown, frontmatter simples e links relativos, mantendo compatibilidade com Git e Obsidian.

## 7. Evidências, fontes e imparcialidade

A skill deverá ser crítica inclusive quando a conclusão contrariar a ideia inicial do fundador. Declarações do usuário, documentos existentes, código e respostas de agentes serão tratados como insumos verificáveis, não como verdade automática.

Para temas estruturais das fases, a preferência será por métodos publicados por fundadores, desenvolvedores, designers, pesquisadores e gestores com reconhecimento internacional e experiência prática comprovada.

Referências-base incluem:

- Steve Blank e Rob Fitzpatrick para validação;
- Alexander Osterwalder para modelo de negócio;
- Jeff Bezos e Working Backwards para visão de produto;
- Marty Cagan para descoberta de produto;
- Jake Knapp para prototipação;
- Eric Ries para experimentação;
- Martin Fowler e Michael Nygard para arquitetura;
- DORA, Jez Humble e Martin Fowler para engenharia e entrega;
- OWASP para segurança;
- Ryan Singer para execução;
- Paul Graham para tração;
- Marc Andreessen e Sean Ellis para product-market fit.

A lista não é fechada. Outra referência poderá ser usada quando tiver maior aderência ao contexto.

Para assuntos que não se encaixarem nessas referências, a prioridade será:

1. legislação, regulador ou autoridade pública competente;
2. documentação oficial do produto, plataforma ou padrão;
3. publicação original do criador do método;
4. instituição técnica ou acadêmica reconhecida globalmente;
5. pesquisa revisada por pares ou relatório transparente;
6. especialista reconhecido com experiência diretamente relevante;
7. fonte secundária, quando não houver fonte primária acessível.

Cada recomendação deverá distinguir a referência que sustenta o método dos dados que sustentam a conclusão aplicada ao projeto.

## 8. Roteamento dos módulos

- Antes do Gate 1: `discovery-and-business.md`.
- Entre os Gates 1 e 2: `value-flow-and-ux.md`.
- Entre os Gates 2 e 3: `requirements-and-architecture.md`.
- Entre os Gates 3 e 4: `engineering-and-quality.md` e `launch-and-operations.md` quando necessário.
- Entre os Gates 4 e 5: `launch-and-operations.md`.
- Entre os Gates 5 e 6: `post-launch-and-scale.md`.

`lifecycle-and-gates.md` e `evidence-and-sources.md` sustentam o processo geral. Segurança, privacidade, acessibilidade, custos e mensuração são trilhas transversais.

## 9. Execução e autorizações

A skill poderá executar alterações técnicas somente depois da aprovação do Gate 3. Antes disso, poderá inspecionar, pesquisar, documentar, elaborar protótipos conceituais e propor experimentos.

Durante a engenharia, deverá:

1. identificar a fatia vertical e critérios de aceite;
2. verificar instruções locais;
3. preservar alterações preexistentes;
4. implementar somente o escopo aprovado;
5. executar validações proporcionais ao risco;
6. registrar resultados e limitações;
7. atualizar o estado do gate.

Orquestração completa não significa autorização automática para publicar, criar contas, contratar serviços, transmitir dados, alterar produção ou gerar custos. Essas ações exigem autorização específica.

## 10. Bloqueios e resultados de validação

Os bloqueios serão classificados como:

- informação;
- evidência;
- técnico;
- externo;
- risco.

Um bloqueio interrompe somente o trabalho afetado. Tarefas independentes e seguras poderão continuar quando produzirem progresso real.

Resultados de teste serão registrados como:

- validado;
- não validado;
- não executado;
- inconclusivo.

Evidência indireta não deverá comprovar um fluxo real quando a conclusão depender de autenticação, pagamento, webhook, banco de dados, dispositivo ou outra integração ponta a ponta.

## 11. Validação da própria skill

A primeira versão será testada com cenários realistas:

1. ideia sem evidência;
2. entrevistas sem fluxo de valor;
3. protótipo sem requisitos técnicos;
4. repositório parcialmente desenvolvido sem documentação;
5. MVP sem segurança ou rollback;
6. produto publicado sem métricas suficientes;
7. site institucional simples;
8. produto regulado ou com dados sensíveis;
9. projeto que declara sucesso sem teste real;
10. pedido para avançar sem aprovação do gate.

Os testes verificarão decisões, não correspondência literal de texto. A skill deverá classificar o estágio, perguntar apenas o necessário, separar estados, encontrar bloqueios, selecionar módulos, evitar burocracia, preservar autorizações e produzir documentos coerentes.

A estrutura e o frontmatter serão verificados pelo validador oficial. Cenários independentes serão executados em ambientes temporários.

## 12. Preparação para o plugin

O plugin será uma camada operacional sobre a skill e não uma segunda metodologia.

Ele terá um agente orquestrador e agentes especializados em:

- estratégia e validação;
- fluxo de valor e pesquisa;
- UX e acessibilidade;
- arquitetura e dados;
- engenharia e testes;
- segurança e privacidade;
- lançamento e operação;
- métricas e crescimento.

Agentes especializados entregarão evidências, conclusões, incertezas e recomendações. Somente o orquestrador poderá consolidar o estado oficial do projeto.

O Obsidian será a primeira integração documental planejada. Os arquivos Markdown continuarão portáveis, sem formato proprietário. Git será o mecanismo preferencial de versionamento quando houver repositório.

Integrações adicionais serão incluídas somente diante de fluxos concretos e deverão operar com permissões mínimas, separação entre leitura e escrita e confirmação para ações externas relevantes.

## 13. Critério de conclusão do design

Esta especificação foi aprovada incrementalmente pelo usuário. A próxima etapa é produzir um plano de implementação detalhado e, após nova autorização, inicializar e implementar a skill `build-startup`.
