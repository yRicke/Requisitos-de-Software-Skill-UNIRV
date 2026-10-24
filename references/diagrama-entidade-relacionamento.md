# Diagrama Entidade-Relacionamento (DER)

Fonte: A08 no [índice](fontes.md). Modele os dados que o sistema precisa guardar para sustentar o comportamento descrito nos casos de uso e na sequência. O DER desta aula é conceitual, anterior à escolha de banco de dados; não converta o pedido automaticamente em tabelas ou SQL. [A08, pp. 3–5, 14]

## Elementos e notação

| Elemento | Como identificar e representar |
| --- | --- |
| Entidade | Coisa sobre a qual o sistema guarda dados; substantivo candidato, representado por retângulo em Chen. |
| Atributo | Característica de uma entidade; elipse em Chen. |
| Relacionamento | Ligação entre entidades, nomeada por verbo e lida nos dois sentidos; losango em Chen. |
| Identificador | Atributo único que distingue ocorrências; sublinhado em Chen. Se nenhum atributo natural servir, use um código próprio, explicitando essa decisão. |

Elementos: [A08, pp. 5–7, 9]. A aula adota **Chen** para ensinar os conceitos e menciona **pé de galinha (crow's foot)** como alternativa com atributos dentro da caixa. Preserve o formato pedido pelo usuário; se a ferramenta usar outra notação, identifique-a e não apresente seu resultado como Chen. A08 não detalha os símbolos de pé de galinha. [A08, p. 6]

## Atributos

- **Simples:** uma característica sem decomposição no modelo, como nome no exemplo da aula.
- **Composto:** dividido em componentes, como endereço em rua e cidade.
- **Multivalorado:** pode ter vários valores para uma ocorrência, como telefone; elipse dupla em Chen.
- **Derivado:** calculado de outros dados, como idade a partir da data de nascimento; elipse tracejada. No exemplo, guarde a data de nascimento e calcule a idade, evitando duas informações que podem divergir.

Tipos e exemplo: [A08, pp. 8, 16]. Telefone não vira entidade apenas por ser multivalorado: investigue se o sistema precisa guardar dados sobre o próprio telefone. Os identificadores CPF, CRO e número de consulta pertencem ao exemplo da clínica; não os imponha a outro domínio. [A08, pp. 7, 16]

## Cardinalidade e participação

Determine **1:1, 1:N ou N:N** perguntando, nos dois sentidos, a quantas ocorrências uma ocorrência se liga. Toda ligação precisa informar a cardinalidade em ambos os lados. Determine também se a participação é **total (obrigatória)** ou **parcial (opcional)** a partir das regras e dos casos de uso; o máximo N não responde se zero é permitido. Não invente obrigatoriedade quando o enunciado não a define. [A08, pp. 10–11, 14, 16]

No exemplo, toda Consulta exige um Paciente, mas um Paciente pode estar cadastrado sem consulta. Isso justifica participação total de Consulta e parcial de Paciente; não transfira essa regra automaticamente para outros relacionamentos. [A08, p. 11]

## Relacionamento N:N e entidade associativa

Quando um N:N possui informação própria do encontro entre entidades, introduza uma **entidade associativa** e substitua o N:N por dois 1:N. No exemplo Consulta–Procedimento, `quantidade` e `valorCobrado` pertencem a Item de consulta: não descrevem a consulta inteira nem o catálogo de procedimentos. Distinga o `valorBase` do procedimento do valor cobrado naquela ocorrência. [A08, pp. 12–13, 15–17]

A receita da aula orienta resolver N:N por entidade associativa; sua justificativa explícita é a informação própria da associação. Não atribua atributos ou uma chave composta à associativa sem evidência de que identificam suas ocorrências. Confira seu identificador, assim como o de qualquer entidade; se faltar informação para defini-lo, registre a lacuna. [A08, pp. 7, 12–14, 16]

## Do texto ao modelo e revisão

1. Extraia candidatos a entidades dos substantivos sobre os quais o sistema guarda dados.
2. Liste atributos, identificadores e os atributos especiais pertinentes.
3. Ligue as entidades com verbos que expressem o relacionamento.
4. Determine cardinalidade e participação, resolva os N:N pertinentes e confronte o resultado com as descrições dos casos de uso.

Procedimento: [A08, pp. 11, 14]. Revise atributos tratados como entidades sem justificativa, ligações sem cardinalidade, N:N com dados próprios sem associativa, dados derivados redundantes e entidades sem identificador. [A08, p. 16]

No DERS, confira se os dados e restrições sustentam as regras e os comportamentos descritos. Nem toda política cabe apenas nas linhas do desenho: registre restrições textuais necessárias, sem afirmar que a cardinalidade sozinha implementa a política. Veja [ders.md](ders.md). [A09, pp. 14–16]

## Limite da fonte

A08 apenas anuncia, para uma próxima aula, entidades fracas e a passagem do modelo para tabelas. Essas explicações não estão nos materiais cadastrados; não as apresente como regras verificadas da disciplina. Se o pedido exigir esse aprofundamento, diferencie conhecimento complementar das orientações presentes nas fontes. [A08, p. 18]
