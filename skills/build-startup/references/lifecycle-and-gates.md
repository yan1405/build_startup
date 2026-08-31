# Ciclo, classificação e gates

Use este arquivo para diagnosticar o estado do produto, dimensionar o rigor e decidir se um gate pode avançar.

## Classificação em três dimensões

### Estágio observado

Escolha o estágio mais alto sustentado por evidência, não o estágio declarado:

1. **Ideia:** problema, público ou proposta ainda são hipóteses.
2. **Descoberta do problema:** existem conversas ou dados, mas a relevância ainda não está comprovada.
3. **Descoberta da solução:** problema sustentado; jornada, valor ou solução ainda estão sendo testados.
4. **Pronto para construir:** solução e escopo mínimo compreendidos; falta aprovação formal do Gate 3.
5. **Em construção:** fatias verticais em implementação após Gate 3.
6. **Pronto para publicar:** MVP implementado; prontidão operacional ainda em avaliação.
7. **Em produção:** usuários reais usam o produto; valor e retenção ainda precisam ser comprovados.
8. **Em evolução ou escala:** valor sustentado; investimento, processo e arquitetura podem crescer.

### Categoria do produto

Registre a forma dominante e características que mudam o percurso:

- SaaS B2B ou B2C;
- app web;
- app mobile nativo ou híbrido;
- plataforma ou marketplace;
- produto com IA;
- site institucional com interações limitadas.

Marketplace, pagamentos, conteúdo gerado por usuários, IA, integrações críticas e distribuição em lojas adicionam critérios condicionais. Um site institucional simples usa o percurso reduzido descrito abaixo.

### Nível de risco

Avalie separadamente produto, negócio, tecnologia, segurança, privacidade, legal, operação e custo.

- **Baixo:** falha reversível, poucos dados, nenhum efeito financeiro ou operacional relevante.
- **Moderado:** autenticação, dados pessoais comuns, integrações externas, receita ou dependência operacional limitada.
- **Alto:** dados sensíveis, saúde, finanças, menores, decisões automatizadas relevantes, pagamentos, múltiplos locatários, obrigação regulatória, alto custo ou dano difícil de reverter.

O maior risco material determina o rigor mínimo. Explique a classificação e peça confirmação quando ela mudar o percurso.

## Gate 1 — Problema comprovado

### Obrigatório

- público prioritário delimitado;
- comportamentos passados ou dados observáveis mostram o problema;
- frequência, intensidade ou consequência compreendidas;
- alternativa atual e suas limitações conhecidas;
- distinção entre fato observado e opinião sobre a solução.

### Condicional

- evidência de disposição a pagar quando o modelo depende de compra direta;
- comprador, usuário e aprovador separados em B2B;
- restrições regulatórias ou de acesso ao mercado identificadas.

### Sinais de alerta

- entrevistas hipotéticas;
- elogios sem comportamento;
- amostra composta apenas por amigos ou equipe;
- problema formulado como ausência da solução desejada.

## Gate 2 — Valor e solução compreendidos

### Obrigatório

- jornada atual e resultado desejado;
- fluxo de valor do gatilho ao resultado percebido;
- proposta `TO BE` reduz esforço, tempo, custo ou risco de forma explícita;
- protótipo ou experimento testou o fluxo crítico;
- comportamento dos participantes registrado;
- métrica inicial de valor definida.

### Condicional

- oferta e liquidez para marketplaces;
- confiança, explicabilidade e avaliação para IA;
- acessibilidade crítica para o público;
- fluxos offline, dispositivo ou permissões nativas em mobile.

### Sinais de alerta

- protótipo validado apenas por stakeholders;
- sucesso medido por preferência estética;
- fluxo termina em clique ou cadastro, não em valor;
- exceções críticas ignoradas.

## Gate 3 — Construção autorizada

### Obrigatório

- MVP e exclusões explícitas;
- critérios de aceite dos fluxos críticos;
- eventos necessários para medir valor;
- dados, permissões e ciclo de vida conhecidos;
- arquitetura mínima e decisões caras registradas;
- riscos críticos tratados, aceitos ou bloqueados;
- custo e dependências compatíveis com o estágio.

### Condicional

- threat model para superfície relevante;
- requisitos legais e de plataforma;
- estratégia de migração ou compatibilidade;
- contrato de integração quando equipes ou sistemas evoluem em paralelo.

### Sinais de alerta

- stack escolhida antes do fluxo;
- microsserviços ou infraestrutura sem dor comprovada;
- requisito sem critério de aceite;
- coleta de dados sem finalidade.

## Gate 4 — Publicação autorizada

### Obrigatório

- fluxos críticos validados no ambiente relevante;
- autenticação, autorização e entradas revisadas quando aplicável;
- erros e sinais operacionais observáveis;
- backup e restauração proporcionais ao risco;
- caminho de rollback conhecido;
- privacidade e suporte mínimos disponíveis;
- riscos residuais documentados;
- autorização específica para publicar.

### Condicional

- revisão de lojas e políticas atuais;
- pagamentos reais e webhooks testados;
- matriz de dispositivos ou navegadores;
- plano de incidentes, continuidade ou comunicação;
- acessibilidade e performance com critérios formais.

### Sinais de alerta

- HTTP 200 usado como prova de fluxo;
- backup sem teste de restauração;
- segredos no repositório;
- produção diferente do que foi testado.

## Gate 5 — Valor em produção comprovado

### Obrigatório

- usuários reais e coorte identificável;
- ativação e evento de valor observados;
- retenção ou repetição coerente com a frequência natural;
- falhas e suporte analisados;
- comparação entre hipótese e comportamento real.

### Condicional

- receita recebida e reconciliada;
- qualidade de oferta e demanda em marketplace;
- avaliações de qualidade, custo e segurança para IA;
- métricas de confiabilidade para operação crítica.

### Sinais de alerta

- cadastros ou visitas tratados como valor;
- métricas agregadas sem coortes;
- usuários internos misturados aos clientes;
- crescimento pago mascarando baixa retenção.

## Gate 6 — Escala autorizada

### Obrigatório

- valor e retenção sustentados no segmento prioritário;
- economia e capacidade operacional compreendidas;
- demanda justifica o investimento;
- gargalo real identificado antes de aumentar complexidade;
- riscos de escala e gatilhos de revisão registrados.

### Condicional

- especialização de equipe;
- revisão de topologia e dados;
- automação de aquisição e suporte;
- SLOs, compliance ou governança formais.

### Sinais de alerta

- teste de 40% tratado como prova isolada;
- arquitetura escalada por previsão;
- aquisição aumentada antes da retenção;
- processo copiado de empresa maior sem necessidade local.

## Trilhas transversais

Em cada gate, verifique somente o rigor necessário para:

- segurança;
- privacidade e legal;
- acessibilidade;
- custos e limites;
- mensuração;
- operação e suporte.

Não espere uma fase tardia para descobrir um bloqueio transversal.

## Percurso reduzido para site institucional

Use quando o site não possuir conta, fluxo transacional, dados sensíveis ou regra de negócio central:

1. objetivo, público e ação desejada;
2. conteúdo e fluxo de navegação;
3. requisitos de marca, acessibilidade, privacidade e formulário;
4. implementação e QA responsivo;
5. domínio, analytics proporcional e publicação autorizada.

Eleve ao ciclo completo se surgirem autenticação, pagamento, área privada, dados relevantes, integrações críticas ou operação contínua.
