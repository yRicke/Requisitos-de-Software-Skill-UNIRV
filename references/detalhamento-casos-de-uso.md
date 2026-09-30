# Descrição textual de casos de uso

Fonte: A06 no [índice](fontes.md). A UML padroniza o diagrama, mas a aula usa um **modelo textual da disciplina**, que transforma cada elipse em um roteiro verificável. Use-o quando for solicitado detalhar casos de uso e mantenha identificação e nome iguais aos do diagrama. [A06, pp. 3, 5–6]

## Campos do modelo da aula

| Campo | Registre |
| --- | --- |
| Identificação | Código e nome do caso, iguais aos da elipse. |
| Ator principal e atores secundários | Quem inicia e quem é acionado no percurso. |
| Pré-condições | Estados já verdadeiros antes do início, assumidos pelo caso. |
| Pós-condições | Estados garantidos quando o objetivo termina com sucesso. |
| Fluxo principal | Passos numerados do percurso comum até o objetivo. |
| Fluxos alternativos (FA) | Outros caminhos que alcançam o mesmo objetivo. |
| Fluxos de exceção (FE) | Caminhos que terminam sem alcançar o objetivo. |
| Regras de negócio (RN) | Políticas em tabela separada, referenciadas pelos passos. |

Campos e distinções: [A06, pp. 5–6, 10–14]. Não confunda pré-condição com checagem executada pelo sistema: se o sistema precisa verificar algo durante a interação, registre a verificação no fluxo e trate a falha no desvio. A pós-condição de sucesso não vale automaticamente após uma exceção; declare o estado final da exceção quando necessário. [A06, pp. 7, 13]

## Escreva o fluxo principal

Numere os passos para permitir referências dos desvios. Cada passo deve dizer **quem faz o quê** (sujeito, verbo e objeto) e expressar a intenção, sem detalhes de botão ou tela. Mostre as respostas do sistema às ações do ator. O fluxo principal representa o caminho usual de sucesso e termina quando o objetivo é alcançado. Não coloque condições “se” nele: encaminhe-as a FA ou FE. [A06, pp. 8–9, 16]

## Escreva e conecte os desvios

- **FA:** indique o passo de origem, a condição, as ações diferentes e o passo exato ao qual o caso retorna. O objetivo e a pós-condição de sucesso continuam alcançáveis. [A06, pp. 11–12, 14]
- **FE:** indique o passo de origem, a condição, a comunicação do motivo e o encerramento sem o objetivo. Registre o que não foi alterado ou o estado que permanece. [A06, pp. 11, 13–14, 16]
- **RN:** mantenha o texto completo de cada política em tabela própria com identificador e origem; cite seu identificador nos passos que a usam. Assim, uma mudança de política não obriga a reescrever o número em diversos fluxos. [A06, p. 10; A03, p. 6]

Um `«include»` obrigatório aparece no fluxo principal como chamada ao caso incluído, cuja descrição é mantida uma vez e reutilizada. Um `«extend»` condicional é representado por ponto de extensão no caso base e condição no caso estendido; o caso base continua funcional sem ele. [A06, p. 15]

## Conferência cruzada

Cada caso desenhado deve ter descrição correspondente quando o pedido for uma especificação completa; confira se os atores, nomes, relações, regras e estados combinam. Compare o passo e seus desvios com o diagrama de sequência, se existir. Não preencha lacunas do enunciado com decisões de implementação: registre perguntas que precisam ser respondidas pelo interessado. [A06, pp. 3–5, 17, 19]
