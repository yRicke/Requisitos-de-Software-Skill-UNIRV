# Documento de Especificação de Requisitos de Software (DERS)

Fonte: A09 no [índice](fontes.md). A aula apresenta o DERS como a **SRS (Software Requirements Specification)** na abordagem de SWEBOK adotada pelo professor. Consolide o que foi decidido sobre comportamentos e restrições em um documento verificável para cliente, equipe e projeto. Ele serve de base para implementação, testes e controle de mudanças; não trate uma proposta ainda não validada como compromisso aprovado. As sete seções abaixo são o modelo da disciplina, não uma estrutura universal imposta a toda SRS. [A09, pp. 3–6]

## As sete seções

| Seção | Conteúdo e conferência |
| --- | --- |
| 1. Problema e contexto | Negócio, problema, stakeholders, escopo e fora de escopo. O leitor deve entender a necessidade antes da solução. [A09, p. 7] |
| 2. Regras de negócio | Políticas e regras de aplicação identificadas, rotuladas nas duas categorias abaixo e relacionadas à sua realização. [A09, pp. 8–9] |
| 3. Requisitos (RF/RNF) | IDs, tipo, enunciado verificável e origem. Use [requisitos.md](requisitos.md) para elicitação, classificação e qualidade. [A09, p. 10] |
| 4. Diagrama de casos de uso | Visão geral de atores e funções, usada como índice visual da seção 5. Veja [diagrama-casos-de-uso.md](diagrama-casos-de-uso.md). [A09, p. 11] |
| 5. Especificação dos casos de uso | Identificação, atores, pré/pós-condições, fluxo principal, alternativos e exceções. Use o modelo completo de [detalhamento-casos-de-uso.md](detalhamento-casos-de-uso.md); o exemplo resumido de A09 não elimina seus campos e conexões. [A09, p. 12; A06, pp. 5–6, 11–14] |
| 6. Diagramas de sequência | Interações derivadas dos passos e regras dos casos de uso. Preserve participantes, ordem e correspondência; consulte [diagrama-sequencia.md](diagrama-sequencia.md). [A09, pp. 12–13] |
| 7. Diagrama Entidade-Relacionamento | Dados e restrições que sustentam comportamentos e políticas; confronte com [diagrama-entidade-relacionamento.md](diagrama-entidade-relacionamento.md). [A09, p. 14] |

Estrutura: [A09, p. 6]. Reutilize e refine os artefatos já existentes, mantendo nomes e IDs; não reúna versões contraditórias apenas para preencher as seções. [A09, pp. 3, 15–17]

## Duas categorias de regras

A09 apresenta a distinção atribuída a Robert C. Martin (Uncle Bob):

- **Cruciais (Core / Enterprise):** existiriam sem computador; representam políticas intrínsecas ao negócio. No modelo didático, aparecem nas entidades, atributos e restrições do DER. A regra de não haver dois agendamentos no mesmo horário para um dentista é um exemplo da clínica.
- **Específicas da aplicação:** definem como o software viabiliza o negócio, como confirmar a disponibilidade antes de registrar ou acionar um serviço de mensagens. Aparecem nos casos de uso e na sequência.

Distinção e exemplos: [A09, pp. 8–9, 14]. Rotule cada regra e mantenha seu ID. A aula usa **RN** para cruciais e **RA** para aplicação; preserve uma convenção existente que permita distinguir as categorias. Política e realização podem expressar a mesma necessidade em níveis diferentes: registre o vínculo, sem tratá-las como duplicação nem como categorias RF/RNF. [A09, pp. 9–10, 16]

Essa distinção amplia a abordagem de A04, em que regra de negócio é a política independente do software; não reclassifique essa política como regra de aplicação apenas porque o sistema a verifica. Os valores de duração, taxa, antecedência e desempenho da clínica são exemplos, não parâmetros padrão para novos projetos. [A04, pp. 6–7; A09, pp. 9–10]

## Rastreabilidade e consistência

Use o fio **problema → regra → requisito → caso de uso → sequência → DER** para confrontar os artefatos. Todo requisito deve ter origem identificável em regra, caso de uso ou restrição; não crie requisitos para completar uma tabela. Dê IDs aos elementos referenciados e confira se os vínculos apontam para elementos existentes. [A09, pp. 10, 15–16]

Uma matriz com regra, requisito, caso de uso, cenário/mensagem e entidade/atributo/restrição pode ajudar na revisão; é uma organização de trabalho derivada da rastreabilidade, não uma oitava seção exigida pela aula. Registre vínculos quando pertinentes, sem inventar uma correspondência de um para um para cada requisito. [A09, pp. 6, 10, 15]

Revise especialmente:

- Regras sem realização correspondente e requisitos sem origem.
- Casos de uso que usam dados persistidos ausentes no DER ou políticas que o modelo não sustenta.
- Divergências de atores, nomes, IDs, fluxos, mensagens, estados finais e restrições entre seções.
- RNFs vagos, como “rápido”, sem medida verificável; se a medida não foi fornecida, marque-a como pendente.
- Escopo sem limites e regras de validação da aplicação rotuladas como políticas cruciais.

Conferência: [A09, pp. 10, 12–16]. No exemplo, RN01 aparece tanto como verificação na sequência quanto como restrição sobre Consulta no DER. Um desenho de cardinalidade não basta para provar que uma regra temporal ou cobrança está atendida; explicite a restrição e a realização necessárias. [A09, pp. 13–15]

Depois de estabelecida a baseline, registre e versione mudanças e revise seus impactos nos artefatos ligados. A aula relaciona validação e gestão de mudanças ao DERS; não afirme que consolidar o documento encerra essas atividades. [A09, pp. 4–5]

## Atividade avaliativa de A09

Aplique os itens a seguir somente quando o pedido tratar da atividade de **A09, p. 17**:

- Trabalho em dupla, com as sete seções; é permitido reutilizar e refinar as atividades 05–08.
- Domínio: Clínica Sorriso Feliz, biblioteca de empréstimos ou domínio escolhido pela dupla com aprovação do professor.
- Pelo menos duas regras de cada categoria; requisitos RF e RNF numerados e rastreados por origem.
- Entrega indicada: um PDF por dupla no Classroom, em **22/10/2026 às 23h59**; o roteiro completo é mencionado como disponível no Classroom, mas não foi fornecido.

Esses itens descrevem a atividade, não mínimos universais para todo DERS. Não presuma que o prazo foi prorrogado nem que o domínio foi aprovado. O slide não instrui a skill a enviar arquivos ou executar ações no Classroom.
