---
name: build-startup
description: Diagnostique, planeje, construa, valide, publique ou evolua produtos digitais interativos de startups. Use quando um fundador técnico solo ou uma equipe pequena quiser conduzir um SaaS, app web ou mobile, plataforma ou marketplace do estado atual até o próximo gate comprovável, ou auditar a prontidão de um projeto existente. Não use para alterações isoladas de código ou sites informativos simples, salvo quando o usuário pedir uma revisão do ciclo de produto.
---

# Build Startup

Conduza o produto até o próximo gate com evidências suficientes. Não transforme o método em uma esteira rígida nem force todos os artefatos em todo projeto.

## Comece pelo estado real

1. Leia instruções locais e fontes de verdade do projeto.
2. Inspecione documentos, repositório, protótipos, pesquisas, testes e resultados disponíveis antes de entrevistar o fundador.
3. Separe afirmações de evidências observáveis. Um documento que declara sucesso não comprova o fluxo.
4. Proponha e justifique uma classificação em três dimensões:
   - estágio atual do ciclo;
   - categoria do produto;
   - nível de risco.
5. Peça confirmação da classificação quando ela alterar materialmente o percurso. Pergunte somente o que não puder ser descoberto e que seja necessário para decidir o próximo gate.

Para classificar o ciclo e aplicar os seis gates, leia [references/lifecycle-and-gates.md](references/lifecycle-and-gates.md). Para avaliar fontes ou evidências, leia [references/evidence-and-sources.md](references/evidence-and-sources.md).

## Escolha o próximo gate

Trabalhe para um único gate comprovável por vez:

1. problema comprovado;
2. valor e solução compreendidos;
3. construção autorizada;
4. publicação autorizada;
5. valor em produção comprovado;
6. escala autorizada.

Não use uma pontuação agregada para compensar uma falha crítica. Segurança, privacidade, legalidade, custo ou ausência de evidência essencial podem bloquear o avanço apesar de outros resultados positivos.

## Carregue somente o módulo necessário

- Antes do Gate 1, leia [references/discovery-and-business.md](references/discovery-and-business.md).
- Entre os Gates 1 e 2, leia [references/value-flow-and-ux.md](references/value-flow-and-ux.md).
- Entre os Gates 2 e 3, leia [references/requirements-and-architecture.md](references/requirements-and-architecture.md).
- Entre os Gates 3 e 4, leia [references/engineering-and-quality.md](references/engineering-and-quality.md). Leia também [references/launch-and-operations.md](references/launch-and-operations.md) quando preparar beta, produção ou lojas.
- Entre os Gates 4 e 5, leia [references/launch-and-operations.md](references/launch-and-operations.md).
- Entre os Gates 5 e 6, leia [references/post-launch-and-scale.md](references/post-launch-and-scale.md).

Carregue mais de um módulo somente quando um risco transversal exigir. Segurança, privacidade, acessibilidade, custos e mensuração acompanham todo o ciclo.

## Preserve a imparcialidade

Marque informações relevantes como:

- `VERIFIED`: sustentada por fonte ou teste observável;
- `APPROVED`: decisão explicitamente aceita;
- `HYPOTHESIS`: ainda precisa de experimento;
- `ESTIMATE`: aproximação com premissas declaradas;
- `BLOCKER`: impede o gate atual;
- `STALE`: pode estar desatualizada.

Não invente entrevistas, usuários, métricas, testes ou resultados. Diferencie ausência de evidência de evidência negativa. Indique separadamente o que a fonte diz, o que o projeto demonstra e o que foi inferido.

## Registre sem criar burocracia

Adapte-se à documentação existente. Quando não houver fonte equivalente, sugira `docs/product-lifecycle/` e crie somente os arquivos necessários. Use os modelos em [assets/document-templates](assets/document-templates) para status, evidências, decisões, roadmap e riscos.

Use Markdown, links relativos e frontmatter simples para manter compatibilidade com Git e Obsidian. Preserve documentos e alterações preexistentes. Não duplique uma fonte de verdade já estabelecida.

## Execute dentro do gate autorizado

Antes do Gate 3, limite-se a inspeção, pesquisa, documentação, protótipos conceituais e experimentos de validação. Não implemente uma hipótese instável como produto de produção.

Depois da aprovação do Gate 3, implemente por fatias verticais com critérios de aceite, validações proporcionais ao risco e registro de resultados. Respeite instruções locais e preserve mudanças do usuário.

Orquestração completa não autoriza automaticamente publicação, criação de contas, contratação, custos, transmissão de dados, alterações em produção ou operações irreversíveis. Obtenha a autorização específica exigida no momento da ação.

## Trate bloqueios precisamente

Classifique bloqueios como informação, evidência, técnico, externo ou risco. Interrompa apenas o trabalho afetado e continue tarefas independentes quando produzirem progresso seguro.

Registre testes como `validado`, `não validado`, `não executado` ou `inconclusivo`. Build concluído, HTTP 200 ou configuração presente não comprovam autenticação, pagamento, webhook, persistência, dispositivo ou outro fluxo ponta a ponta.

## Encerre cada execução com um contrato claro

Entregue:

1. classificação confirmada ou ainda pendente;
2. gate atual e decisão sobre o avanço;
3. evidências usadas e limitações;
4. documentos criados ou modificados;
5. riscos e bloqueios;
6. próxima ação recomendada;
7. aprovação necessária antes do próximo gate.

Se o gate falhar, proponha o menor experimento ou correção capaz de resolver a lacuna. Não reinicie fases já comprovadas.
