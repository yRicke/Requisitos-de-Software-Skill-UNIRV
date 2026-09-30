# Atualização das fontes da skill

Este procedimento se aplica quando o usuário fornecer novos materiais da disciplina ou uma versão diferente de algum PDF cadastrado.

1. Inventarie cada arquivo novo ou alterado: título, nome exato, data ou versão explícita, quantidade de páginas e SHA-256. Compare o hash e o conteúdo com [fontes.md](fontes.md); não trate uma cópia com outro nome como aula adicional.
2. Leia as páginas integralmente, incluindo tabelas, figuras, notas e exemplos relevantes. Diferencie definição, regra, recomendação, exemplo e instrução de atividade. Não transforme um exemplo ou exercício isolado em obrigação geral.
3. Registre a fonte em `fontes.md` e acrescente regras específicas somente à referência pertinente. Aponte o ID e as páginas de cada regra; explique em `fontes.md` as divergências ou complementaridades que mudem decisões do agente.
4. Compare regras novas com as anteriores. Se os PDFs antigos não estiverem disponíveis, use as sínteses rastreáveis como base e não afirme ter relido os originais; solicite o arquivo anterior quando um conflito exigir confronto direto. Preserve as regras ainda válidas, delimite escopos distintos e exponha conflitos sem escolher pela ordem de inclusão. Se a precedência não estiver clara nas fontes nem nas instruções do usuário, solicite decisão.
5. Atualize o roteamento em `SKILL.md` apenas quando surgir um novo tipo de tarefa ou referência. Evite duplicar explicações em vários arquivos. Não publique o PDF original em um repositório público por padrão; a skill contém sínteses rastreáveis.
6. Valide a estrutura com `quick_validate.py` da skill `skill-creator`, confira links internos e teste um pedido realista ligado ao material novo. Registre as alterações em commit convencional com mensagem em português.
