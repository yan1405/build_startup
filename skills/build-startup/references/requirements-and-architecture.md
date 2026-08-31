# Requisitos e arquitetura

Carregue este módulo depois do Gate 2 e antes do Gate 3, ou quando uma decisão estrutural precisar ser revisada por mudança de evidência.

## Resultado esperado

Transformar o fluxo de valor aprovado em um MVP implementável, mensurável e proporcional ao risco, sem prever escala ou flexibilidade sem evidência.

## Insumos necessários

- problema e público aprovados;
- fluxo de valor e protótipo testados;
- métrica de valor;
- riscos conhecidos;
- restrições reais de prazo, orçamento, equipe e plataformas;
- repositório e arquitetura existente, quando houver.

## Defina o MVP

Registre:

- resultado que o MVP precisa demonstrar;
- menor conjunto de fatias verticais;
- critérios de aceite observáveis;
- exclusões explícitas;
- experimento ou métrica que encerra a hipótese;
- dependências e operação manual aceita.

Priorize pelo risco que precisa ser reduzido, não por quantidade de funcionalidades. MoSCoW, RICE ou outro método podem apoiar, mas não substituem julgamento e evidência.

## Requisitos

Para cada fluxo crítico, descreva:

- ator e permissão;
- pré-condição;
- ação e regra de negócio;
- resultado esperado;
- estados de erro relevantes;
- dados lidos, criados, alterados ou eliminados;
- evento analítico necessário;
- critério de aceite.

Inclua requisitos não funcionais apenas quando houver motivo: disponibilidade, latência, volume, compatibilidade, acessibilidade, privacidade, segurança, auditabilidade, custo ou recuperação.

## Arquitetura mínima

Comece pelo sistema mais simples que atende os fluxos e riscos aprovados. Para uma startup inicial, prefira monólito bem delimitado ou serviço gerenciado quando isso reduzir operação. Não trate essa preferência como regra se houver restrição real que a invalide.

Decida com base em:

- padrões de leitura e escrita;
- consistência e transações;
- isolamento entre clientes;
- integrações e falhas;
- requisitos de identidade e autorização;
- ciclo de vida dos dados;
- custo e capacidade operacional;
- reversibilidade.

## Decisões e contratos

Crie ADR somente para decisão cara, controversa ou com consequência duradoura. Registre contexto, opções, decisão, consequências e gatilho de revisão.

Use contrato de API quando frontend e backend, equipes ou sistemas precisarem evoluir em paralelo. Trate o contrato como versionado e evolutivo, não imutável.

## Riscos transversais

Antes do Gate 3, verifique:

- threat model proporcional;
- base e finalidade de dados pessoais;
- permissões e menor privilégio;
- dependência de fornecedor e saída possível;
- orçamento, limites e alertas de custo;
- requisitos de loja, navegador ou dispositivo;
- acessibilidade necessária;
- estratégia de teste e observabilidade.

Para assuntos legais ou políticas atuais, consulte fontes oficiais e registre a data.

## Entregáveis possíveis

- PRD enxuto;
- mapa de escopo e exclusões;
- critérios de aceite;
- plano de eventos e métricas;
- modelo de dados;
- matriz de papéis e permissões;
- diagrama de contexto;
- ADRs;
- registro de riscos e custo.

## Bloqueios comuns

- requisito sem vínculo com o fluxo de valor;
- arquitetura escolhida por preferência;
- coleta de dados sem finalidade ou retenção;
- integração crítica não validada;
- custo desconhecido para uso esperado;
- critério de aceite subjetivo;
- Gate 2 ainda sustentado apenas por opinião.

## Referências preferenciais

Use Michael Nygard para ADRs e Martin Fowler para arquitetura e entrega evolutiva. Para padrões, serviços e APIs, use documentação oficial atual.
