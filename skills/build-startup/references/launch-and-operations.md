# Beta, publicação e operação

Carregue este módulo ao preparar ou avaliar o Gate 4 e durante o período entre publicação e comprovação de valor em produção.

## Resultado esperado

Colocar o produto diante de usuários reais com risco controlado, capacidade de diagnóstico, suporte e reversão.

## Beta antes do lançamento amplo

Escolha o menor grupo capaz de revelar falhas relevantes. Defina:

- público e critério de entrada;
- fluxos e ambientes testados;
- canal de suporte;
- eventos e métricas;
- duração ou condição de encerramento;
- tratamento de dados e consentimentos aplicáveis;
- critério de expansão ou rollback.

Não chame teste interno de validação com clientes. Diferencie alfa, beta controlado e disponibilidade pública.

## Checklist proporcional de prontidão

### Produto

- fluxos críticos e estados de falha;
- onboarding, suporte e recuperação;
- conteúdo, termos e comunicações coerentes;
- acessibilidade e dispositivos relevantes.

### Engenharia

- versão identificável;
- migrações e compatibilidade;
- erros, logs e métricas;
- backup e restauração;
- rollback conhecido e, quando o risco exigir, testado;
- segredos e permissões revisados.

### Negócio e operação

- responsável por incidentes e suporte;
- custos, limites e alertas;
- canal de aquisição inicial;
- política de cancelamento, reembolso ou exclusão quando aplicável.

### Privacidade e legal

- inventário e finalidade dos dados;
- política e termos adequados ao fluxo real;
- fornecedores e compartilhamentos;
- direitos, retenção e eliminação;
- resposta a incidentes proporcional.

Use autoridade e documentação oficial atuais. Não ofereça conclusão jurídica definitiva sem profissional qualificado quando houver particularidade relevante.

## Web e domínio

Verifique domínio, DNS, TLS, variáveis, ambiente, indexação quando desejada, analytics proporcional e política de cookies quando aplicável. Prefira recursos nativos do provedor para rollback antes de introduzir sistemas próprios.

## Lojas de aplicativos

Antes da submissão, consulte a documentação oficial atual da Apple ou Google. Verifique conforme a plataforma:

- conta e contratos do desenvolvedor;
- assinatura, identificadores e builds;
- metadados, capturas e classificação etária;
- privacidade, Data Safety e SDKs terceiros;
- permissões e justificativas;
- exclusão de conta;
- compras dentro do app;
- acesso ou credenciais para revisão;
- TestFlight ou trilhas de teste;
- nível de API e requisitos de versão.

Não prometa prazo fixo de revisão. Registre a data da consulta e trate rejeição como risco externo.

## Lançamento inicial

Recrute usuários de forma compatível com o estágio. Suporte manual pode produzir aprendizado antes de automação. Não escale aquisição antes de observar ativação e retenção coerentes.

Deploy e lançamento são eventos diferentes. Feature flags são opcionais; use-as quando reduzirem risco ou permitirem exposição controlada.

## Evidência para Gate 4

O gate exige comportamento observado no ambiente relevante, não apenas configuração. Quando uma validação real depender de autorização, conta, dispositivo ou terceiro, registre `não executado` ou `BLOCKER` com precisão.

## Bloqueios comuns

- fluxo crítico não testado em ambiente realista;
- política diverge da coleta real;
- backup sem restauração;
- ausência de suporte ou dono operacional;
- requisito de loja desatualizado;
- publicação confundida com autorização para marketing, cobrança ou transmissão de dados.

## Referências preferenciais

Use documentação oficial do provedor, Apple, Google, autoridades de proteção de dados e padrões aplicáveis. Para primeiros usuários, Paul Graham pode orientar a execução manual sem torná-la regra universal.
