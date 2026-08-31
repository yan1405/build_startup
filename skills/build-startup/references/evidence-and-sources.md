# Evidências, fontes e imparcialidade

Use este arquivo ao avaliar afirmações, pesquisar referências ou justificar um gate.

## Estados de informação

- `VERIFIED`: uma fonte confiável ou teste observável sustenta a afirmação.
- `APPROVED`: o responsável aceitou explicitamente uma decisão e suas consequências conhecidas.
- `HYPOTHESIS`: afirmação plausível ainda dependente de experimento.
- `ESTIMATE`: aproximação com premissas, intervalo ou base declarados.
- `BLOCKER`: lacuna que impede o gate atual.
- `STALE`: evidência com risco relevante de desatualização.

Não use `APPROVED` como sinônimo de verdadeiro. Uma decisão pode ser aprovada com risco aceito. Não converta ausência de evidência em evidência negativa.

## Três camadas obrigatórias

Ao justificar uma conclusão, separe:

1. **Referência conceitual:** método ou princípio usado para raciocinar.
2. **Evidência do projeto:** dado que demonstra o caso específico.
3. **Inferência:** conclusão obtida ao aplicar a referência à evidência.

Um especialista pode orientar o método, mas não valida sozinho o produto analisado.

## Referências preferenciais por tema estrutural

Priorize publicações originais, entrevistas diretas ou organizações mantidas pelos autores:

- validação: Steve Blank e Rob Fitzpatrick;
- modelo de negócio: Alexander Osterwalder;
- visão: Jeff Bezos e Working Backwards;
- descoberta: Marty Cagan;
- prototipação: Jake Knapp;
- experimentação: Eric Ries;
- arquitetura: Martin Fowler e Michael Nygard;
- entrega: DORA, Jez Humble e Martin Fowler;
- segurança: OWASP;
- execução: Ryan Singer e Shape Up;
- tração: Paul Graham;
- product-market fit: Marc Andreessen e Sean Ellis.

Esses nomes são referências iniciais, não autoridades infalíveis. Escolha outra fonte quando ela tiver maior aderência, experiência relevante ou evidência melhor.

## Hierarquia para demais assuntos

1. legislação, regulador ou autoridade pública competente;
2. documentação oficial do produto, plataforma ou padrão;
3. publicação original do criador do método;
4. instituição técnica ou acadêmica reconhecida globalmente;
5. pesquisa revisada por pares ou relatório metodologicamente transparente;
6. especialista reconhecido com experiência diretamente relevante;
7. fonte secundária quando não houver fonte primária acessível.

Avalie autoridade, experiência, atualidade, transparência e aplicabilidade. Popularidade, cargo ou quantidade de links não substituem qualidade.

## Quando pesquisar ou atualizar

Pesquise fontes atuais quando houver chance material de mudança, especialmente:

- legislação, regulação e obrigações de privacidade;
- políticas de lojas e plataformas;
- versões, APIs, preços e limites de serviços;
- segurança e vulnerabilidades;
- padrões técnicos ou requisitos de publicação;
- recomendações que gerem custo, risco ou compromisso relevante.

Não pesquise novamente um fato estável já sustentado por fonte adequada sem motivo. Se a verificação atual for impossível, marque `STALE` ou limitação em vez de confirmar.

## Registro mínimo de uma fonte

Para cada fonte relevante, registre:

- título;
- autor, organização ou autoridade;
- URL ou localização interna;
- data de publicação ou atualização, quando disponível;
- data da consulta;
- afirmação sustentada;
- evidência observada;
- inferência aplicada;
- confiabilidade e limitações.

## Evidência adequada por decisão

### Problema e mercado

Prefira comportamento passado, transações, esforço atual, frequência, intensidade, retenção e disposição a pagar. Opinião hipotética é evidência fraca.

### Usabilidade e valor

Prefira observação de tarefa, conclusão do fluxo, tempo, erros, abandono e relato contextual. Aprovação estética de stakeholder não prova usabilidade.

### Engenharia

Prefira código, configuração, testes executados, logs, consultas, artefatos de build e comportamento do sistema. README ou status declarado não comprovam operação real.

### Produção

Prefira o fluxo real no ambiente e dispositivo relevantes, métricas, eventos, transações reconciliadas e restauração testada. HTTP 200 é apenas um sinal parcial.

## Conflito entre fontes

Quando houver conflito:

1. confirme se tratam do mesmo contexto e período;
2. priorize a autoridade competente para o assunto;
3. compare data e versão;
4. examine método, amostra e incentivos;
5. apresente a divergência e a incerteza residual;
6. evite conclusão definitiva quando a base não permitir.

## Linguagem imparcial

Use formulações como:

- “A evidência disponível sustenta...”
- “Ainda não foi demonstrado...”
- “A decisão foi aprovada, com os seguintes riscos...”
- “Esta é uma estimativa baseada em...”
- “A fonte define o método; os dados do projeto ainda não confirmam o resultado.”

Evite usar prestígio, entusiasmo do fundador ou volume de documentação como substitutos de prova.
