# Levantamento, classificação e qualidade dos requisitos

Consulte [fontes.md](fontes.md) para localizar os PDFs A01–A04 e os complementos de A09. Esta referência se aplica ao trabalho com necessidades, requisitos e regras de negócio; os casos da biblioteca e da clínica são exemplos didáticos, não políticas transferíveis a outro sistema.

## Do problema ao requisito

- Um requisito descreve algo que o sistema deve fazer ou uma condição que deve atender. Comece pela necessidade real do interessado e por sua origem, não por uma solução técnica escolhida antes de entender o problema. [A01, pp. 4–5; A02, pp. 15, 18]
- Identifique quem usa, mantém ou é afetado pelo sistema. Elicitação é descobrir necessidades, inclusive as tácitas, implícitas e conflitantes; não basta copiar pedidos literais. [A02, pp. 7–8; A04, pp. 4–5]
- Registre a origem de cada requisito e conecte-o, quando possível, à implementação e aos testes. Requisitos podem mudar e precisam de controle para manter a rastreabilidade. [A03, pp. 4, 6; A02, p. 12]

## Classifique sem confundir origem e implementação

| Tipo | Critério da aula | Exemplos de conteúdo, não regras universais |
| --- | --- | --- |
| Funcional | Ação, cálculo, entrada, saída, mudança de estado ou comportamento observável do sistema. [A02, p. 3; A03, p. 9] | Registrar empréstimo; emitir relatório. |
| Não funcional | Qualidade do produto ou restrição de processo/implementação: desempenho, usabilidade, confiabilidade, segurança, portabilidade ou manutenibilidade. [A02, p. 4; A03, pp. 10–11] | Tempo de resposta; disponibilidade; restrição tecnológica justificada. |
| De domínio | Restrição trazida pelo contexto de negócio, política institucional ou regulação do setor. [A01, p. 5; A02, p. 5] | Limite de empréstimos definido pela biblioteca. |

Na abordagem de A04, uma **regra de negócio** é uma política, restrição ou definição que já existe independentemente do software. Registre-a como tal e derive dela um ou mais requisitos implementáveis, sem confundir a regra com o comportamento do sistema. [A04, pp. 6–7] A09 distingue essa categoria, chamada **crucial**, das **regras específicas da aplicação**, que organizam como o software realiza a política. Para rotulá-las no DERS, consulte [ders.md](ders.md); preserve o vínculo entre política e realização. [A09, pp. 8–10] Uma restrição tecnológica imposta pode ser um requisito não funcional; escolher uma tecnologia por iniciativa da equipe antes de investigar a necessidade é decisão de arquitetura, não requisito de negócio. [A03, p. 10; A02, p. 15]

## Escreva requisitos de qualidade

- Dê identificador estável aos requisitos que precisam ser rastreados; A03 exemplifica **RF001**, **RF002** etc. para funcionais. A09 usa **RF01** e **RNF01** e explicita a coluna **Origem** no DERS. Preserve a convenção já adotada no projeto sem renumerar artefatos só para reproduzir o exemplo. [A03, p. 9; A09, pp. 10, 16]
- Formule uma condição observável e completa, com contexto e limites quando necessários. Substitua adjetivos vagos, como “rápido” e “fácil”, por critérios verificáveis; para desempenho, a aula mostra medida, percentual e carga como dimensões possíveis, não valores padrão. [A03, pp. 6–8]
- Revise se cada requisito é **claro e não ambíguo, completo, consistente, verificável, rastreável, necessário e factível** no tempo, custo e tecnologia disponíveis. Cheque conflitos com outros requisitos. [A03, pp. 6, 12–13]
- Quando o usuário pedir uma especificação, detalhe o critério de aceitação apenas até onde as evidências sustentarem; marque medidas e políticas ainda não confirmadas como questões em aberto. A especificação deve permitir validação com interessados e verificação após a implementação. [A02, pp. 11–12, 17]

Uma forma útil de apresentar o trabalho, quando o usuário não exigir outra, é uma tabela com **ID, tipo, enunciado, origem, critério de verificação e dúvidas**. Essa tabela é uma organização de trabalho derivada da exigência de clareza e rastreabilidade; os PDFs não prescrevem essas colunas como modelo obrigatório. [A03, p. 6]

## Elicite e valide

Escolha técnicas conforme a informação que falta:

- **Entrevista estruturada** para comparar respostas; **semiestruturada** para seguir um roteiro com abertura; **aberta** para explorar um domínio pouco conhecido. Prefira perguntas abertas ancoradas no processo atual, sem induzir respostas; registre exceções e o que parece óbvio. [A04, pp. 8–9]
- **Brainstorming** no início para gerar ideias sem crítica durante a sessão; avalie-as depois e garanta participação de todos. [A04, p. 10]
- **Observação** para revelar trabalho tácito; **questionário** para muitos interessados, sabendo que perde detalhes; **workshop/JAD** para decidir e priorizar em grupo; **protótipo** para obter reação a algo concreto. [A04, p. 11]

Considere interesses divergentes e regras implícitas. Na análise, resolva conflitos e priorize; na validação, confirme com os interessados que os requisitos representam o problema real. Não chame de “validado” um requisito que ninguém confirmou. [A04, pp. 3–5; A02, pp. 12, 17]

## Entenda os dois recortes de processo das aulas

- **Visão ampla:** identificação, definição, análise, especificação, validação, gerenciamento e verificação; a última verifica se a entrega cumpre os requisitos. [A02, pp. 9–12]
- **Quatro etapas centrais:** elicitação, análise e negociação, especificação e validação. O trabalho é iterativo e pode retornar a etapas anteriores. [A04, p. 3]

Esses recortes se complementam. Se o usuário pedir “as etapas”, explicite qual aula ou nível de detalhe está sendo usado; não funde as listas em uma nova sequência supostamente prescrita pelas fontes.
