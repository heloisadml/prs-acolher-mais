# Sprint Backlog — Sprint 1

## Observação sobre a organização atual

No GitHub, as histórias de usuário estão atualmente registradas como checklists dentro dos épicos. Para a documentação da Sprint, elas são apresentadas individualmente abaixo.

Os Story Points foram estimados utilizando uma escala relativa baseada na sequência de Fibonacci, considerando complexidade, esforço e incerteza.

## Situação dos épicos no GitHub Project

| Épico | Status |
|---|---|
| E01 — Autenticação e Usuários | Doing |
| E02 — Cadastro de Idosos e Responsáveis | To Do |
| E03 — Gestão de Medicamentos | To Do |
| E04 — Registro de Rotina | Doing |
| E05 — Consulta para Familiares | Product Backlog |
| E06 — Banco de Dados e Integração | Product Backlog |

---

## E01 — Autenticação e Usuários

Todas as histórias deste épico foram selecionadas para a Sprint.

| ID | História de usuário | Story Points | Situação |
|---|---|---:|---|
| E01-US01 | Como Administrador, quero me cadastrar no sistema com e-mail e senha, para ter acesso às funcionalidades de gestão. | 3 | Concluída |
| E01-US02 | Como Administrador, quero fazer login no sistema, para acessar o painel de controle com segurança. | 3 | Concluída |
| E01-US03 | Como Cuidador, quero fazer login com minhas credenciais, para acessar as informações dos idosos sob minha responsabilidade. | 3 | Concluída |
| E01-US04 | Como Administrador, quero criar contas para Cuidadores e Familiares, para controlar quem tem acesso ao sistema. | 5 | Concluída |

**Total planejado do E01: 14 Story Points**

### Situação do épico

No registro atual do GitHub:

- [x] Todas as histórias concluídas
- [x] Funcionalidade validada
- [x] Documentação atualizada

Como todos os critérios foram atendidos até o encerramento da Sprint, o épico E01 foi considerado **Done**.

---

## E02 — Cadastro de Idosos e Responsáveis

Foram selecionadas para a Sprint as histórias relacionadas ao cadastro e à consulta inicial dos residentes.

| ID | História de usuário | Story Points | Situação |
|---|---|---:|---|
| E02-US01 | Como Administrador, quero cadastrar um novo idoso com nome, data de nascimento e informações de saúde, para manter um registro organizado dos residentes. | 5 | Em andamento |
| E02-US02 | Como Administrador, quero editar os dados de um idoso já cadastrado, para manter as informações sempre atualizadas. | 3 | Não selecionada |
| E02-US03 | Como Administrador, quero listar todos os idosos cadastrados, para visualizar rapidamente os residentes do lar. | 3 | Pendente |
| E02-US04 | Como Administrador, quero cadastrar os contatos de emergência de cada idoso, para acionar os responsáveis quando necessário. | 3 | Não selecionada |
| E02-US05 | Como Administrador, quero registrar o valor e a data de vencimento da mensalidade de cada residente, para controlar os pagamentos do lar. | 5 | Não selecionada |

**Total planejado do E02 na Sprint: 8 Story Points**

---

## E03 — Gestão de Medicamentos

Foram selecionadas as funcionalidades iniciais de cadastro e consulta de medicamentos.

| ID | História de usuário | Story Points | Situação |
|---|---|---:|---|
| E03-US01 | Como Administrador, quero cadastrar os medicamentos de cada idoso com nome, dosagem e frequência, para garantir que o tratamento seja seguido corretamente. | 5 | Pendente |
| E03-US02 | Como Cuidador, quero visualizar a lista de medicamentos que devo ministrar em cada horário, para não esquecer nenhuma dose. | 3 | Pendente |
| E03-US03 | Como Cuidador, quero marcar uma dose como ministrada, para registrar que o medicamento foi dado ao idoso. | 3 | Não selecionada |
| E03-US04 | Como Administrador, quero visualizar o histórico de doses ministradas, para acompanhar se o tratamento está sendo seguido. | 5 | Não selecionada |

**Total planejado do E03 na Sprint: 8 Story Points**

---

## E04 — Registro de Rotina

Foram selecionadas as histórias relacionadas ao registro básico das atividades diárias do residente.

| ID | História de usuário | Story Points | Situação |
|---|---|---:|---|
| E04-US01 | Como Cuidador, quero acessar um checklist diário com as atividades de higiene do residente (banho, escovação, troca de roupa), para garantir que todos os cuidados foram realizados. | 5 | Em andamento |
| E04-US02 | Como Cuidador, quero marcar as refeições do dia (café, almoço, lanche, janta) como realizadas ou não, para registrar a alimentação do idoso. | 3 | Em andamento |
| E04-US03 | Como Cuidador, quero adicionar uma observação ao checklist diário, para registrar qualquer ocorrência relevante do dia. | 3 | Não selecionada |
| E04-US04 | Como Administrador, quero visualizar o histórico de rotina de cada idoso, para acompanhar a qualidade dos cuidados prestados. | 5 | Não selecionada |

**Total planejado do E04 na Sprint: 8 Story Points**

---

## BUG01 — Registro de idosos duplicado

Durante a Sprint foi identificado o seguinte bug relacionado ao cadastro de residentes.

| ID | Descrição | Story Points | Situação |
|---|---|---:|---|
| BUG01 | Registro de idosos duplicado após atualização da página. | 3 | Pendente |

### Descrição do problema

Ao registrar um idoso no sistema e atualizar a página de residentes, o mesmo registro aparece duplicado.

### Resultado esperado

O idoso deve ser registrado apenas uma vez no sistema.

### Resultado observado

O registro aparece duplicado após a atualização da página.

### Impacto

A duplicação pode gerar inconsistências nos dados dos residentes e afetar outras funcionalidades relacionadas ao cadastro.

### Critérios de correção

- [ ] Bug reproduzido pela equipe;
- [ ] Correção implementada;
- [ ] Testes realizados;
- [ ] Teste de regressão executado;
- [ ] Bug validado após correção.

### Relação com o Sprint Backlog

O BUG01 está relacionado ao épico:

- E02 — Cadastro de Idosos e Responsáveis

E à história:

- E02-US01 — Como Administrador, quero cadastrar um novo idoso com nome, data de nascimento e informações de saúde, para manter um registro organizado dos residentes.

---

## Resumo do Sprint Backlog

| Item | Story Points planejados |
|---|---:|
| E01 — Autenticação e Usuários | 14 |
| E02 — Cadastro de Idosos e Responsáveis | 8 |
| E03 — Gestão de Medicamentos | 8 |
| E04 — Registro de Rotina | 8 |
| BUG01 | 3 |
| **Total** | **41** |

Foram planejados inicialmente **38 Story Points** para a Sprint 1.

Durante a execução, o BUG01 foi adicionado ao Sprint Backlog com estimativa de **3 Story Points**, elevando o escopo final para **41 Story Points**.

---

## Tarefas técnicas

As tarefas técnicas representam o trabalho necessário para implementar, testar e validar as histórias selecionadas.

| Tarefa | História relacionada | Responsável | Estimativa | Status |
|---|---|---|---:|---|
| T01 — Implementar cadastro de Administrador | E01-US01 | Heloisa de Moraes Lira | 3 SP | Concluída |
| T02 — Implementar autenticação e login | E01-US02 / E01-US03 | Mileni Savily de Souza Alves | 5 SP | Concluída |
| T03 — Implementar criação de contas de usuários | E01-US04 | Sandrine de Araújo Azevedo | 5 SP | Concluída |
| T04 — Estruturar cadastro de residentes | E02-US01 | Danylo Vieira de Melo Barros Falcão | 5 SP | Em andamento |
| T05 — Estruturar listagem de residentes | E02-US03 | Heloisa de Moraes Lira | 3 SP | Pendente |
| T06 — Estruturar cadastro de medicamentos | E03-US01 | Mileni Savily de Souza Alves | 5 SP | Pendente |
| T07 — Estruturar consulta de medicamentos por horário | E03-US02 | Sandrine de Araújo Azevedo | 3 SP | Pendente |
| T08 — Estruturar checklist de higiene | E04-US01 | Danylo Vieira de Melo Barros Falcão | 5 SP | Em andamento |
| T09 — Estruturar registro de refeições | E04-US02 | Heloisa de Moraes Lira | 3 SP | Em andamento |
| T10 — Investigar e corrigir duplicação de residentes | BUG01 / E02-US01 | Danylo Vieira de Melo Barros Falcão | 3 SP | Pendente |


---

## Itens fora da Sprint

Os seguintes épicos permaneceram no Product Backlog e não foram priorizados para execução nesta Sprint:

- E05 — Consulta para Familiares
- E06 — Banco de Dados e Integração

Também permaneceram fora desta Sprint as seguintes histórias dos épicos parcialmente selecionados:

- E02-US02 — Editar os dados de um idoso;
- E02-US04 — Cadastrar contatos de emergência;
- E02-US05 — Registrar mensalidade;
- E03-US03 — Marcar dose como ministrada;
- E03-US04 — Visualizar histórico de doses;
- E04-US03 — Adicionar observações à rotina;
- E04-US04 — Visualizar histórico de rotina.

Esses itens permanecem disponíveis para priorização em Sprints posteriores.