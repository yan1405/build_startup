# Fluxo de valor, jornada e UX

Carregue este módulo depois do Gate 1 e antes do Gate 2, ou quando o produto tiver funcionalidades sem conexão clara com valor percebido.

## Resultado esperado

Explicar e testar como o cliente sai da situação problemática e alcança um resultado valioso, conectando jornada, interface, comportamento do sistema, dados e métrica.

## Insumos úteis

- evidência aprovada do problema e público;
- jornada ou processo atual;
- protótipos, telas ou produto existente;
- regras de negócio e integrações conhecidas;
- feedback e testes de usabilidade;
- métricas de ativação ou uso.

## Construa o fluxo de valor

Documente:

1. **Gatilho:** evento que inicia a necessidade.
2. **Ator:** usuário, comprador ou operador que age.
3. **Jornada `AS IS`:** passos, ferramentas, pessoas, espera, custo e falhas atuais.
4. **Resultado desejado:** progresso que a pessoa quer alcançar.
5. **Jornada `TO BE`:** como a proposta reduz esforço, tempo, custo ou risco.
6. **Frontstage:** ações e respostas visíveis ao cliente.
7. **Backstage:** regras, integrações, persistência e operações necessárias.
8. **Dados e permissões:** entradas, finalidade, acesso, retenção e saída.
9. **Métrica de valor:** comportamento que demonstra o resultado.

O fluxo não termina no clique, cadastro ou mensagem de sucesso. Termine no valor percebido, como atendimento concluído, pagamento reconciliado ou tarefa resolvida.

## Caminhos e estados

Comece pelo caminho principal. Depois cubra somente exceções que alterem valor, risco ou arquitetura:

- entrada inválida;
- permissão negada;
- ausência de dados ou oferta;
- falha de integração;
- abandono e retomada;
- conflito de estado;
- cancelamento, estorno ou exclusão;
- operação humana necessária.

Não refine microinterações antes de compreender os estados críticos.

## Prototipação

Escolha a fidelidade mais barata capaz de testar a dúvida:

- storyboard ou esboço para sequência e proposta;
- wireframe para hierarquia e navegação;
- protótipo navegável para usabilidade;
- concierge ou Wizard of Oz para valor sem backend completo;
- spike técnico para viabilidade difícil.

Design Sprint é uma opção, não uma obrigação de cinco dias. Reduza ou expanda conforme risco, time e acesso a usuários.

## Teste com usuários

Defina antes:

- público representativo;
- tarefa e contexto;
- comportamento que indica sucesso;
- sinais de confusão ou abandono;
- aprendizado que mudaria a decisão.

Observe comportamento antes de pedir opinião. Separe problemas de proposta de valor, compreensão, navegação e estética.

## Fundação visual

Para o MVP, defina somente tokens e componentes necessários aos fluxos aprovados. Não exija um design system completo. Registre tipografia, cores, espaçamento, estados e acessibilidade suficientes para consistência e evolução.

## Entregáveis possíveis

- jornada `AS IS` e `TO BE`;
- mapa de fluxo de valor ou service blueprint enxuto;
- diagrama funcional do sistema;
- matriz inicial de dados e permissões;
- protótipo;
- roteiro e resultado de teste;
- métrica de valor e eventos candidatos.

## Bloqueios comuns

- solução definida antes do resultado;
- protótipo testado apenas internamente;
- sucesso medido por gosto;
- dados coletados sem finalidade;
- métrica de vaidade no lugar de valor;
- caminho crítico depende de operação ou integração não mapeada.

## Referências preferenciais

Use Marty Cagan para riscos de produto e descoberta; Jake Knapp para prototipação estruturada. Prefira métodos de jornada ou service blueprint de fontes reconhecidas quando ajudarem a conectar frontstage e backstage.
