# Fontes verificadas

Conjunto inicial recebido em 30/09/2026 (A01–A07), ampliado em 24/10/2026 com A08 e A09: nove PDFs da disciplina **ESW208 — Requisitos de Software**, turma A, professor Gustavo Martins Lima. As páginas indicadas nas referências são as páginas do PDF, começando em 1. O conteúdo foi analisado a partir dos arquivos enviados pelo usuário; os PDFs não fazem parte deste repositório.

| ID | PDF recebido | Data indicada | Páginas | Regras extraídas em |
| --- | --- | --- | ---: | --- |
| A01 | `2026-2 Aula 01 - Apresentação da Disciplina.pdf` | 30/07/2026 | 9 | [requisitos.md](requisitos.md) |
| A02 | `2026-2 Aula 02 - Identificando Requisitos em Sistemas Reais (1).pdf` | 01/08/2026 | 19 | [requisitos.md](requisitos.md) |
| A03 | `2026-2 Aula 03 - Características e Classificação de Requisitos (1).pdf` | 06/08/2026 | 14 | [requisitos.md](requisitos.md) |
| A04 | `2026-2 Aula 04 - Processo de Engenharia de Requisitos (Elicitação e Técnicas).pdf` | 20/08/2026 | 14 | [requisitos.md](requisitos.md) |
| A05 | `2026-2 Aula 05 - Diagrama de Casos de Uso.pdf` | 10/09/2026 | 21 | [diagrama-casos-de-uso.md](diagrama-casos-de-uso.md) |
| A06 | `2026-2 Aula 06 - Detalhamento de Casos de Uso.pdf` | 17/09/2026 | 20 | [detalhamento-casos-de-uso.md](detalhamento-casos-de-uso.md) |
| A07 | `2026-2 Aula 07 - Diagrama de Sequência.pdf` | 24/09/2026 | 18 | [diagrama-sequencia.md](diagrama-sequencia.md) |
| A08 | `2026-2 Aula 08 - Diagrama Entidade-Relacionamento.pdf` | 01/10/2026 | 18 | [diagrama-entidade-relacionamento.md](diagrama-entidade-relacionamento.md) |
| A09 | `2026-2 Aula 09 - Documento de Especificação de Requisitos (DERS).pdf` | 08/10/2026 | 19 | [ders.md](ders.md), [requisitos.md](requisitos.md) |

## Identidade dos arquivos (SHA-256)

| ID | SHA-256 |
| --- | --- |
| A01 | `5222945FBC92C93398B4A5B75C83AFE292E239F087793242FF776654724EB61C` |
| A02 | `9FF43312008252B70550CCB8D3BB0647755DD29BB9F8A4BC60B92854A1330496` |
| A03 | `061F2DA1B38CD91C7F344CE916ACD6056BFC0BE1737474213CCC0BA6E86AC828` |
| A04 | `9A8FD1329FA49E7D85F8583FA11C4D46943A0227C76492F083B493ADAABD3380` |
| A05 | `8EB525CB73207F94F91F23601C1784FACEAEFF9A2AD41BC906EA2D23F8E6A7B5` |
| A06 | `DE3DBBDC29335FA2369995EEA56AF2D1170C9B3388C7F579479F278A47499122` |
| A07 | `A48555CCDDE01DB6C6648FC43F0F38E98B3C992B9EA2BAD19FD0ED1D5B449B15` |
| A08 | `086E08229AD35E6D6B03D379635E9A45DCF096A8B7E04EFB914DBEF06350BFC4` |
| A09 | `E4AA70AD5C4AB9293C0D15D39B7B43A5522E1F81D65F6DD57F73D304544E2715` |

## Limites e leitura conjunta

- [A02, pp. 9–12] apresenta um ciclo didático amplo em **sete etapas**; [A04, p. 3] detalha **quatro etapas centrais** de forma iterativa. Use a enumeração adequada ao contexto, sem tratar uma como correção da outra.
- [A02, p. 15] alerta que escolher MySQL antes de entender o problema é decisão de arquitetura, não requisito de negócio. [A03, p. 10] admite uma restrição tecnológica imposta como requisito não funcional. Investigue a origem da restrição antes de classificá-la.
- Os exemplos da biblioteca e da clínica demonstram regras, mas seus números, prazos e políticas não se transferem para outros sistemas. Atividades de sala também não definem quantidades obrigatórias para toda entrega.
- A ementa de [A01, p. 3] apenas menciona DER; [A08, pp. 5–17] passa a ensinar entidades, atributos, Chen, cardinalidade, participação e entidade associativa. A08, p. 18 apenas anuncia entidades fracas e transformação para tabelas: esse aprofundamento não está nas fontes recebidas.
- [A04, pp. 6–7] trata regra de negócio como política independente do software. [A09, pp. 8–9] chama essa categoria de crucial e acrescenta regras específicas da aplicação, ligadas aos casos de uso e à sequência. Preserve a distinção entre política e realização; não trate a ampliação como invalidação da definição anterior.
- [A03, p. 9] exemplifica RF001; [A09, pp. 9–12, 16] usa RN, RA, RF01, RNF01 e UC01 e explicita a origem dos requisitos. Os exemplos reforçam IDs e rastreabilidade, sem exigir renumeração de artefatos existentes.
- [A06, pp. 5–6, 11–14] detalha o modelo textual e as conexões dos desvios; o exemplo resumido de [A09, p. 12] não substitui essas orientações. A sequência em [A09, p. 13] mantém o sistema como caixa-preta e explicita os vínculos às regras.
- [A09, pp. 5–6] apresenta o DERS/SRS e suas sete seções na abordagem didática da disciplina; não é uma consulta externa ao SWEBOK nem uma imposição dessa estrutura a toda SRS. As quantidades, opções de domínio e entrega em 22/10/2026 de [A09, p. 17] são exigências daquela atividade. O roteiro adicional do Classroom não foi fornecido.
