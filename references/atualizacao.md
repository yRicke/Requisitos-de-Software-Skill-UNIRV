# Atualização das fontes da skill

Este procedimento se aplica à manutenção da skill quando o usuário fornecer novos materiais da disciplina.

1. Inventarie todos os arquivos novos ou alterados: título, tipo, versão ou data explícita, quantidade de páginas, identificador e hash SHA-256. Registre-os em `references/fontes.md` sem copiar o PDF para um repositório público por padrão.
2. Leia o conteúdo integral relevante, incluindo tabelas, figuras, notas e exemplos. Diferencie prescrições, definições, recomendações e exemplos; anote as páginas exatas. Não deduza regras de um exemplo isolado.
3. Compare as regras com as já registradas. Preserve o que ainda é válido, acrescente o que é novo e marque conflitos ou escopos distintos. Se as fontes não estabelecerem precedência, não escolha uma silenciosamente.
4. Atualize somente os tópicos afetados nas referências e o roteamento em `SKILL.md`. Cada regra específica deve apontar para a fonte e página; cada referência deve ser descoberta pelo índice.
5. Valide a estrutura da skill e faça uma revisão prática com um pedido realista. Confira se a resposta resultante respeita as fontes, separa fatos de inferências e indica lacunas sem inventar conteúdo.
6. Registre em commit convencional, em português, as alterações da skill. Descreva na entrega quais fontes entraram, quais regras mudaram e quais conflitos permanecem.
