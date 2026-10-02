# Gestão de Mudança — Sprint 1

## Identificação

- **Projeto:** Acolher+
- **Sprint:** Sprint 1
- **Data da mudança:** 29/09/2026
- **Integrantes:**
  - Heloisa de Moraes Lira
  - Sandrine de Araújo Azevedo
  - Mileni Savily de Souza Alves
  - Danylo Vieira de Melo Barros Falcão

## Requisito original

O requisito original estava relacionado ao épico **E02 — Cadastro de Idosos e Responsáveis** e era dividido em duas histórias distintas:

- **E02-US01 — Cadastro de novo idoso:** previa o cadastro do residente com nome, data de nascimento e informações de saúde;
- **E02-US04 — Cadastro de contatos de emergência:** previa o registro de contatos de emergência como funcionalidade separada.

Na versão original do backlog, a necessidade de manter ao menos um contato de emergência por idoso já existia, mas não fazia parte do fluxo inicial da E02-US01.

## Mudança solicitada

Foi solicitada uma alteração de organização do requisito: o primeiro contato de emergência, antes tratado em uma história separada, passa a ser **obrigatório dentro do próprio fluxo de cadastro inicial do idoso**.

Com a mudança, a E02-US01 deixa de representar apenas os dados básicos do residente e passa a incluir também a associação inicial obrigatória de um contato de emergência. A E02-US04 permanece responsável pela gestão posterior dos contatos.

## Motivo da mudança

A mudança foi motivada pela necessidade de garantir que todo residente possua uma referência de contato disponível desde o primeiro momento em que é inserido no sistema.

Separar o cadastro do residente do cadastro do contato de emergência poderia permitir a existência de registros incompletos, dificultando o acionamento de familiares ou responsáveis em situações que demandem contato imediato.

A alteração busca, portanto:

- aumentar a consistência dos dados cadastrados;
- reduzir a possibilidade de residentes sem contato responsável associado;
- melhorar a segurança operacional do fluxo de atendimento;
- tornar o cadastro inicial mais completo.

## Análise de impacto

A mudança afeta diferentes elementos do backlog e do planejamento.

### E02-US01 — Cadastro de novo idoso

A história precisa incorporar a obrigatoriedade do contato de emergência como parte do cadastro inicial.

Os critérios de aceitação passam a incluir:

- o cadastro deve permitir informar nome, data de nascimento e informações de saúde;
- deve ser informado pelo menos um contato de emergência;
- o sistema não deve concluir o cadastro sem um contato de emergência válido;
- o contato deve permanecer associado ao residente cadastrado.

### E02-US04 — Cadastro de contatos de emergência

A funcionalidade deixa de ser totalmente independente do cadastro inicial.

Parte do seu escopo passa a ser incorporada à E02-US01.

A história E02-US04 continua relevante para permitir que contatos adicionais sejam incluídos, editados ou mantidos após o cadastro inicial do residente.

### T04 — Estruturar cadastro de residentes

A tarefa técnica passa a incluir:

- campos para contato de emergência;
- validação da obrigatoriedade do contato;
- associação entre residente e contato;
- tratamento de erros de preenchimento.

### Testes

Os testes da funcionalidade passam a verificar também:

- tentativa de cadastro sem contato de emergência;
- cadastro com contato válido;
- associação correta entre residente e contato;
- persistência dos dados após o cadastro.

### Estimativa e planejamento

A alteração aumenta a complexidade da E02-US01, pois amplia o número de campos, validações e relacionamentos envolvidos.

A história estava estimada em **5 Story Points**. Após análise, a equipe decidiu manter a estimativa atual nesta Sprint e registrar o aumento de complexidade para consideração em planejamentos futuros, uma vez que a história já estava em andamento.

## Decisão tomada

A equipe decidiu **aceitar a mudança** e incorporar a obrigatoriedade de um contato de emergência ao fluxo de cadastro de residentes.

A decisão foi tomada porque a alteração melhora a integridade das informações e reduz o risco de registros incompletos.

A E02-US01 passa a contemplar o cadastro inicial de pelo menos um contato de emergência, enquanto a E02-US04 permanece no Product Backlog para tratar a gestão posterior de contatos adicionais.

## Alterações realizadas no backlog

| Item | Situação anterior | Alteração |
|---|---|---|
| E02-US01 | Cadastro de nome, data de nascimento e informações de saúde | Passa a exigir pelo menos um contato de emergência |
| E02-US04 | Cadastro de contatos de emergência como funcionalidade separada | Reformulada para gestão posterior dos contatos após o cadastro inicial |
| T04 | Estruturar cadastro básico do residente | Passa a incluir campos, validações e associação do contato de emergência |
| Critérios de aceitação de E02-US01 | Não incluíam o contato de emergência no fluxo inicial | Passam a exigir pelo menos um contato válido durante o cadastro |

## Rastreabilidade

A mudança mantém rastreabilidade com os seguintes itens:

- **Épico:** E02 — Cadastro de Idosos e Responsáveis;
- **História principal afetada:** E02-US01 — Cadastro de novo idoso;
- **História relacionada:** E02-US04 — Gestão de contatos de emergência (#36);
- **Tarefa técnica afetada:** T04 — Estruturar cadastro de residentes;
- **Sprint:** Sprint 1.

A relação entre o requisito original e a alteração foi preservada por meio da manutenção dos identificadores dos itens e do registro explícito dos impactos no backlog.

## Justificativa técnica

A decisão de incorporar um contato de emergência obrigatório ao cadastro inicial foi considerada adequada porque reduz estados incompletos no sistema e melhora a consistência dos dados.

Do ponto de vista de modelagem, a alteração estabelece uma relação necessária entre o residente e ao menos um contato responsável desde a criação do registro. Isso reduz a necessidade de validações posteriores para identificar residentes sem referência de emergência.

A reformulação da E02-US04 como história de gestão posterior preserva a separação de responsabilidades: a E02-US01 garante o primeiro contato obrigatório no cadastro inicial, enquanto a E02-US04 trata inclusão de contatos adicionais e atualização das informações existentes.

A mudança também demonstra a necessidade de revisar critérios de aceitação e tarefas técnicas quando um requisito é alterado, mantendo a rastreabilidade entre a necessidade original, a decisão tomada e os itens afetados no backlog.
