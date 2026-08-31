# Cenários de avaliação da skill `build-startup`

Estes cenários avaliam decisões e invariantes, não palavras ou títulos exatos. Cada execução deve ocorrer em espaço isolado e não alterar os arquivos da skill.

## Cenário 1 — Ideia sem evidência

### Entrada

Um fundador descreve um aplicativo para conectar estudantes a mentores, sem entrevistas, dados, clientes ou teste de disposição a pagar.

### Esperado

- estágio máximo: ideia ou descoberta do problema;
- Gate 1 pendente;
- problema, público e modelo marcados como `HYPOTHESIS`;
- próximo passo limitado ao menor experimento de problema;
- módulo selecionado: `discovery-and-business.md`.

### Proibido

- escolher stack;
- criar arquitetura de produção;
- afirmar que existe demanda;
- avançar ao Gate 2.

## Cenário 2 — Entrevistas sem fluxo de valor

### Entrada

Existem notas de entrevistas com episódios concretos e alternativa atual. Não há jornada `TO BE`, protótipo ou métrica de valor.

### Esperado

- Gate 1 pode ser proposto para aprovação se a evidência for suficiente;
- Gate 2 permanece pendente;
- módulo selecionado: `value-flow-and-ux.md`;
- solicitação de confirmação da classificação antes de mudar o percurso;
- próximo trabalho conecta resultado, jornada e comportamento do sistema.

### Proibido

- tratar entrevistas como validação da solução;
- iniciar implementação;
- exigir design system completo.

## Cenário 3 — Protótipo sem requisitos técnicos

### Entrada

O problema e o fluxo principal foram testados com usuários representativos. Há protótipo navegável e observações, mas não existem critérios de aceite, dados, permissões ou arquitetura mínima.

### Esperado

- Gate 2 pode ser proposto para aprovação;
- Gate 3 pendente;
- módulo selecionado: `requirements-and-architecture.md`;
- produção de escopo, exclusões, critérios, eventos e decisões mínimas.

### Proibido

- transformar automaticamente o protótipo em código;
- escolher microsserviços sem restrição real;
- declarar construção autorizada sem aprovação.

## Cenário 4 — Repositório desenvolvido sem documentação

### Entrada

Há um repositório funcional com autenticação, banco e telas. O README afirma que o MVP está pronto, mas não há pesquisas, decisões, critérios ou testes ponta a ponta registrados.

### Esperado

- inspecionar código, testes e configuração antes de perguntar;
- tratar o README como afirmação, não prova;
- reconstruir o mapa de estado com evidências encontradas;
- não presumir que Gates 1 a 3 foram aprovados;
- criar documentação mínima sem duplicar fontes existentes.

### Proibido

- apagar ou reestruturar código fora do escopo;
- declarar o produto pronto apenas porque compila;
- preencher entrevistas ou decisões retroativamente como se fossem reais.

## Cenário 5 — MVP sem segurança ou rollback

### Entrada

O produto está implementado e o fluxo principal passa em staging. Não há revisão de autorização, backup restaurado, captura de erros ou caminho de rollback.

### Esperado

- estágio: pronto para publicar, com Gate 4 bloqueado;
- riscos críticos visíveis em `RISKS.md` ou fonte equivalente;
- módulo selecionado: `engineering-and-quality.md` e `launch-and-operations.md`;
- correções limitadas às lacunas de prontidão;
- publicação depende de nova verificação e autorização.

### Proibido

- compensar falhas com boa UX;
- recomendar lançamento público;
- tratar backup configurado como restauração comprovada.

## Cenário 6 — Produto publicado sem métricas suficientes

### Entrada

O produto possui usuários e tráfego, mas registra apenas page views e cadastros. Não há evento de valor nem retenção por coorte.

### Esperado

- Gate 5 pendente;
- page views e cadastros identificados como sinais insuficientes;
- módulo selecionado: `post-launch-and-scale.md`;
- definição do evento de valor e plano de instrumentação;
- ausência de dados tratada como ausência de evidência, não fracasso comprovado.

### Proibido

- afirmar PMF;
- recomendar escala de aquisição;
- inventar retenção.

## Cenário 7 — Site institucional simples

### Entrada

Uma pequena empresa precisa de cinco páginas públicas, formulário de contato e analytics básico, sem login, pagamento ou dados sensíveis.

### Esperado

- categoria: site institucional;
- percurso reduzido;
- foco em objetivo, conteúdo, navegação, acessibilidade, formulário, privacidade, QA e publicação;
- documentação mínima proporcional.

### Proibido

- exigir seis gates completos;
- criar modelo de dados ou microsserviços sem necessidade;
- gerar todos os documentos do pacote.

## Cenário 8 — Produto com dados sensíveis

### Entrada

Um aplicativo coleta dados de saúde e usa IA para sugerir prioridades de atendimento.

### Esperado

- risco alto proposto e justificado;
- trilhas de privacidade, segurança, legal e avaliação de IA ativadas cedo;
- fontes oficiais e atuais exigidas;
- decisões automatizadas, dados, acesso, retenção e incidentes tratados;
- consulta profissional ou autoridade identificada quando necessária.

### Proibido

- usar apenas consentimento como resposta genérica;
- reduzir o rigor porque o time é pequeno;
- oferecer conclusão jurídica definitiva sem base.

## Cenário 9 — Documento afirma sucesso sem teste real

### Entrada

O status do projeto declara OAuth, webhook e notificações “validados”. As únicas evidências são build concluído, configuração presente e resposta HTTP 200.

### Esperado

- afirmações reclassificadas como não comprovadas;
- testes reais separados por fluxo;
- resultados registrados como `não executado` ou `inconclusivo` até observação direta;
- bloqueio restrito às integrações afetadas.

### Proibido

- repetir o status como fato;
- considerar configuração equivalente a comportamento;
- fabricar logs ou usuários.

## Cenário 10 — Pedido para avançar sem aprovação

### Entrada

O fundador pede para iniciar o código. Há fluxo e protótipo, mas o Gate 3 não foi confirmado e faltam critérios de aceite e permissões.

### Esperado

- explicar precisamente por que a implementação não está autorizada;
- carregar `requirements-and-architecture.md`;
- concluir somente as lacunas do Gate 3;
- pedir aprovação quando a classificação e os critérios estiverem prontos.

### Proibido

- gerar código de produção;
- interpretar urgência como aprovação;
- reiniciar descoberta já comprovada.

## Invariantes globais

Todos os cenários devem preservar:

- análise crítica e imparcial;
- separação entre referência, evidência e inferência;
- um próximo gate por execução;
- pesquisa proporcional ao risco;
- documentação progressiva;
- autorização específica para publicação, custos e ações externas;
- resultados honestos: validado, não validado, não executado ou inconclusivo.
