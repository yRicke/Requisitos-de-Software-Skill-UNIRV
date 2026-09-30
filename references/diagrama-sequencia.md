# Diagrama de sequência no nível do sistema

Fonte: A07 no [índice](fontes.md). Derive o diagrama da descrição textual do caso de uso, preservando a ordem dos passos e as regras citadas. O desenho explicita participantes, mensagens, dados transportados e respostas; ele **testa** a descrição e não cria requisitos novos. Se houver lacuna ou desacordo, corrija o texto ou registre uma pergunta antes de inventar uma mensagem. [A07, pp. 3–4, 14]

## Participantes e notação

- Coloque o **ator principal** à esquerda, o **`:Sistema`** no centro como caixa-preta e os sistemas ou serviços externos acionados à direita. Não introduza tela, controller, classe ou banco de dados interno como participante nesta fase. [A07, p. 7]
- A linha de vida é tracejada e vertical; o tempo passa de cima para baixo. Mensagem de pedido usa seta cheia e nome com intenção e dados; retorno usa seta tracejada; auto-mensagem volta à mesma linha de vida; ativação marca o período de trabalho. [A07, pp. 4–6]
- Nomeie mensagens pela intenção de negócio, com verbo e dados quando houver, como `validarMatricula(matricula)`. Não use nomes de interação de interface nem comandos de banco de dados. [A07, pp. 8, 14]

## Converta os passos, sem perder correspondência

| Passo da descrição | Representação |
| --- | --- |
| Ator informa ou pede algo | Mensagem do ator para `:Sistema`. |
| Sistema consulta ator secundário | Mensagem para o sistema externo e retorno correspondente. |
| Sistema verifica ou calcula internamente | Auto-mensagem em `:Sistema`. |
| Sistema informa resultado ao ator | Retorno ao ator. |
| Passo chama `«include»` | Represente a execução do caso incluído e suas interações pertinentes, sem criar um participante artificial apenas com o nome do caso. |

Derivação e exemplo: [A07, pp. 8–10]. Preserve a numeração dos passos quando ajudar a confrontar texto e desenho. Verifique se toda mensagem tem um passo ou justificativa e se cada passo relevante tem representação. [A07, pp. 9, 14]

## Cenários e fragmentos

- Faça primeiro um diagrama limpo do **fluxo principal**, sem fragmentos. Depois represente desvios importantes separadamente. Um desvio curto pode caber em fragmento; se tiver vários passos ou atravessar o caso inteiro, faça outro diagrama. [A07, p. 13]
- Use **`alt`** para dois ou mais caminhos mutuamente exclusivos, cada qual com guarda; **`opt`** para trecho que ocorre ou não, típico de extensão condicional; **`loop`** para repetição enquanto a guarda valer. A condição fica na guarda do fragmento, não no nome da mensagem. [A07, pp. 11–12, 14]
- Fluxos alternativos e de exceção da descrição devem manter seus desfechos: alternativo alcança o objetivo; exceção termina sem ele. A guarda e a mensagem final precisam refletir isso. [A06, pp. 12–14; A07, pp. 11–12]

Mermaid, ferramenta gráfica ou desenho manual são meios aceitáveis quando o usuário não exigir um formato específico; a notação e a coerência importam mais que a ferramenta. [A07, p. 15]

## Revisão

Confira a ordem temporal, os participantes externos, os dados e retornos das mensagens, as guardas exclusivas do `alt` e a correspondência exata com o caso de uso. Não abra a caixa-preta nem aninhe todos os FA e FE em um único desenho ilegível. [A07, pp. 4, 7, 12–14, 17]
