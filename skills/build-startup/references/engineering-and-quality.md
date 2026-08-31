# Engenharia e qualidade

Carregue este módulo somente após o Gate 3 aprovado, ou para auditar uma implementação existente que deveria ter passado por esse gate.

## Resultado esperado

Entregar fatias verticais utilizáveis, testadas e observáveis, preservando a capacidade de aprender e reverter.

## Antes de alterar código

1. Leia instruções locais e fontes de verdade.
2. Inspecione o estado real do repositório e alterações preexistentes.
3. Relacione a tarefa a uma fatia e critérios de aceite aprovados.
4. Identifique dados, integrações e riscos envolvidos.
5. Confirme que a ação está dentro do Gate 3 e das autorizações concedidas.

Não use a skill para ampliar silenciosamente o escopo ou “melhorar” áreas não relacionadas.

## Fatias verticais

Uma fatia deve atravessar somente as camadas necessárias para produzir comportamento testável. Prefira uma jornada estreita completa a grandes blocos separados de frontend, backend e infraestrutura.

Para cada fatia, registre:

- resultado do usuário;
- critérios de aceite;
- estados relevantes;
- evento de mensuração;
- estratégia de teste;
- rollout ou reversão quando necessário.

## Ambiente e integração contínua

Comece com validação automática mínima útil: instalação ou build, lint ou tipos e testes relevantes. Adicione staging, matrizes extensas ou deployment contínuo quando o risco justificar.

Trunk-based development e mudanças pequenas são preferências úteis para times pequenos, não obrigação quando o contexto exige outro fluxo.

## Estratégia de testes

Combine testes pelo risco:

- unitários para regras isoladas;
- integração para banco, contratos e serviços;
- ponta a ponta para jornadas críticas;
- manuais para experiência, dispositivo e casos difíceis de automatizar;
- segurança, acessibilidade e performance quando aplicáveis.

Não persiga cobertura percentual sem relação com risco. Teste a fronteira onde a falha seria cara ou silenciosa.

## Segurança

Inclua desde a implementação:

- autenticação e autorização;
- validação de entrada e saída;
- segredos fora do código;
- dependências e superfícies expostas;
- menor privilégio;
- logs sem dados indevidos;
- backup e recuperação proporcionais.

Use OWASP e documentação oficial como base; adapte ao produto.

## Observabilidade

Comece com:

- captura de erros;
- logs estruturados úteis;
- eventos do fluxo de valor;
- métricas operacionais essenciais;
- alertas para falhas prováveis e acionáveis.

Tracing distribuído, plataforma complexa de observabilidade e SLOs formais são condicionais. Não os imponha a um monólito inicial sem necessidade.

## Evidência de conclusão

Registre comandos e resultados. Refaça a verificação após alterações relevantes. Diferencie:

- `validado`;
- `não validado`;
- `não executado`;
- `inconclusivo`.

Build ou HTTP 200 não comprovam OAuth, webhook, pagamento, persistência, notificação ou fluxo em dispositivo. Teste a realidade quando autorizado e necessário.

## Bloqueios comuns

- implementação sem critérios aprovados;
- ambiente ou dependência não reproduzível;
- mock usado como prova de produção;
- segredo ou dado sensível exposto;
- teste passa sem exercitar integração real;
- alteração preexistente do usuário seria sobrescrita;
- custo ou limite de serviço desconhecido.

## Referências preferenciais

Use DORA, Jez Humble e Martin Fowler para entrega; OWASP para segurança. Para frameworks, provedores e plataformas, use documentação oficial da versão em uso.
