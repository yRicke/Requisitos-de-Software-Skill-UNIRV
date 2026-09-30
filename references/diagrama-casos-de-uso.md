# Diagrama de casos de uso

Fonte: A05 no [índice](fontes.md). Use este modelo para conversar sobre **quem** interage com o sistema e **quais objetivos completos** ele alcança. O diagrama complementa a especificação escrita; não mostra a ordem temporal e não substitui a descrição de cada caso. [A05, pp. 4–6, 11, 20]

## Escolha o que entra

- **Ator** é um papel externo à fronteira: usuário, outro sistema ou tempo que dispara uma rotina. Não represente uma pessoa específica nem componentes internos como banco de dados. [A05, pp. 7, 9]
- **Caso de uso** é um objetivo concluído com valor para o ator. Nomeie com verbo no infinitivo e objeto, na linguagem do negócio. Passos de tela, validações internas, operações de banco e substantivos soltos não são casos de uso por si. [A05, pp. 6, 10, 18]
- **Fronteira** delimita as responsabilidades do sistema: casos dentro, atores fora. **Associação** é linha simples, sem seta, entre ator e caso; indica participação, nunca sequência. [A05, pp. 7–8, 11]
- Parta dos requisitos funcionais e do enunciado, mas decida caso a caso: alguns RFs viram objetivos, outros viram passos ou relações. Não crie uma elipse para cada RF automaticamente. [A05, p. 16]
- Evite quatro elipses genéricas de CRUD para cada entidade. Quando o objetivo for manter um cadastro, a aula prefere um caso de uso de manutenção, preservando os detalhes de cada operação na descrição. [A05, pp. 10, 18]

## Relacionamentos

| Relação | Use quando | Sentido da seta |
| --- | --- | --- |
| `«include»` | Um comportamento obrigatório e reutilizado ocorre sempre no caso base; evita repetir trecho comum. [A05, pp. 12, 14] | Do caso base para o incluído. |
| `«extend»` | Um comportamento excepcional entra somente sob uma condição; o caso base continua completo sem ele. [A05, pp. 13–14] | Do caso de extensão para o caso base. |
| Generalização de atores | Um papel especializado herda **todas** as interações do papel mais genérico e ainda pode fazer mais. [A05, p. 15] | Triângulo vazado aponta para o ator genérico. |

As relações `include` e `extend` são tracejadas e rotuladas. Não as use para simular a ordem de uma tarefa ou decorar o diagrama. Se houver muitos cruzamentos, mantenha o objetivo principal no diagrama e detalhe os passos na descrição textual. [A05, pp. 12–14, 18]

## Revisão

1. Leia cada associação como frase de negócio: o ator realmente participa do objetivo? [A05, p. 11]
2. Para cada elipse, confira valor concluído e nome em verbo no infinitivo; elimine passos de interface e decomposição excessiva. [A05, pp. 6, 10, 18]
3. Para cada `include`, confirme que é obrigatório; para cada `extend`, escreva a condição. Confira as direções das setas. [A05, pp. 12–14]
4. Confira se a fronteira e os atores externos estão corretos, se a generalização representa herança total e se o desenho permanece legível. [A05, pp. 7, 9, 15, 18]
5. Compare diagrama, requisitos e descrições: o que for passo deve ficar no texto; nenhum objetivo sustentado pelo enunciado deve desaparecer. [A05, pp. 4, 16, 20]

A atividade da clínica pede quantidades específicas de atores e casos e o uso de `include`/`extend` para **aquele exercício**. Não imponha essas quantidades a outros sistemas. [A05, p. 19]
