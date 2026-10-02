# Backlog Inicial do Produto

## Acolher+ — Sistema de Gestão para Lares de Idosos

### Links

- **Repositório:** https://github.com/heloisadml/prs-acolher-mais
- **GitHub Project:** https://github.com/users/heloisadml/projects/1

---

## Objetivo

Estruturar o backlog inicial do produto Acolher+, apresentando o problema que será tratado, os usuários envolvidos e um conjunto inicial de histórias de usuário priorizadas, servindo de base para o planejamento das próximas etapas de desenvolvimento.

## Produto

O Acolher+ é um sistema de gestão voltado para Instituições de Longa Permanência para Idosos (ILPIs), com o objetivo de centralizar o cadastro de residentes, o controle de medicação, o registro da rotina de cuidados e o acompanhamento dessas informações pelos familiares responsáveis.

## Problema

Lares de idosos frequentemente dependem de processos manuais e registros em papel para controlar a administração de medicamentos e a rotina de cuidados dos residentes. Essa forma de trabalho gera riscos concretos: erros na administração de medicação, falta de rastreabilidade sobre o que foi efetivamente realizado, dificuldade dos familiares em acompanhar o cuidado prestado ao seu parente, e ausência de dados centralizados que apoiem auditorias e a conformidade com exigências regulatórias.

O Acolher+ propõe substituir esse processo fragmentado por um sistema único, acessível pelos diferentes perfis envolvidos no cuidado do idoso.

---

# Personas

## Sandra Oliveira

**Administradora — gestão do lar**

Responsável pela gestão operacional do lar de idosos. Cadastra residentes e cria as contas da equipe e dos familiares, e acompanha indicadores gerais de funcionamento da instituição.

**Principais necessidades:**

- Ter uma visão centralizada de todos os residentes e da equipe;
- Garantir que a documentação exigida por órgãos reguladores esteja em dia;
- Reduzir o tempo gasto com controles manuais e planilhas.

## Carlos Souza

**Cuidador — equipe de cuidados diretos**

Membro da equipe responsável pelos cuidados diários dos residentes: administração de medicamentos, registro de rotina e registro de observações relevantes do dia.

**Principais necessidades:**

- Registrar rapidamente doses administradas e atividades diárias, mesmo com pouco tempo disponível;
- Consultar com clareza quais medicamentos devem ser ministrados em cada horário;
- Registrar ocorrências relevantes de forma simples e rastreável;
- Receber alertas automáticos sobre horários de medicação *(necessidade identificada para evolução futura)*.

## Beatriz Lima

**Familiar — acompanhamento do residente**

Filha de uma residente do lar. Não trabalha na instituição, mas quer acompanhar de perto os cuidados prestados ao seu familiar, mesmo à distância.

**Principais necessidades:**

- Visualizar a medicação e a rotina diária do seu parente sem precisar ligar para o lar;
- Ter confiança de que as informações são atualizadas e confiáveis;
- Ser avisada rapidamente em caso de intercorrências *(necessidade identificada para evolução futura)*.

> As necessidades marcadas como evolução futura foram identificadas junto às personas, mas ainda não correspondem a histórias do backlog atual.

---

# Stakeholders

Além das personas que utilizam o sistema diretamente, o projeto envolve outras partes interessadas que influenciam requisitos e decisões, ainda que não interajam com a interface no dia a dia.

| Stakeholder | Interesse |
|---|---|
| Direção/gestão da instituição | Interessada em relatórios gerenciais, conformidade e redução de riscos operacionais. |
| Órgãos reguladores (ex.: Vigilância Sanitária) | Exigem rastreabilidade da medicação e da rotina de cuidados para fins de fiscalização. |
| Equipe de desenvolvimento (o grupo) | Responsável por construir, testar e evoluir o sistema ao longo do projeto de extensão. |
| Setor financeiro/administrativo | Interessado nas informações relacionadas às mensalidades dos residentes e em possíveis evoluções futuras da gestão financeira do sistema. |

---

# Backlog de Histórias de Usuário

O backlog atual possui **25 histórias distribuídas em 6 épicos**, priorizadas com a técnica MoSCoW.

Os identificadores, títulos, histórias e critérios de aceitação abaixo correspondem às issues registradas no repositório.

## ÉPICO 1 — Autenticação e Usuários

### E01-US01 — Cadastro de Administrador (#8) — MUST HAVE

Como **Administrador**, quero **me cadastrar no sistema com e-mail e senha**, para **ter acesso às funcionalidades de gestão**.

**Critérios de aceitação:**

- O cadastro deve exigir e-mail e senha.
- O sistema deve impedir o cadastro de e-mail já utilizado.
- Após um cadastro válido, a conta do Administrador deve ficar disponível para autenticação.

### E01-US02 — Login de Administrador (#9) — MUST HAVE

Como **Administrador**, quero **fazer login no sistema**, para **acessar o painel de controle com segurança**.

**Critérios de aceitação:**

- Credenciais válidas devem permitir o acesso.
- Credenciais inválidas devem ser rejeitadas.
- Após a autenticação, o Administrador deve acessar o painel correspondente ao seu perfil.

### E01-US03 — Login de Cuidador (#10) — MUST HAVE

Como **Cuidador**, quero **fazer login com minhas credenciais**, para **acessar as informações dos idosos sob minha responsabilidade**.

**Critérios de aceitação:**

- Credenciais válidas de Cuidador devem permitir o acesso.
- Credenciais inválidas devem ser rejeitadas.
- O Cuidador deve acessar apenas as funcionalidades compatíveis com seu perfil.

### E01-US04 — Criação de contas de Cuidadores e Familiares (#11) — MUST HAVE

Como **Administrador**, quero **criar contas para Cuidadores e Familiares**, para **controlar quem tem acesso ao sistema**.

**Critérios de aceitação:**

- O Administrador deve poder informar os dados necessários da nova conta.
- A conta deve ser criada com o perfil selecionado.
- O novo usuário deve poder utilizar as credenciais criadas para acessar o sistema.

---

## ÉPICO 2 — Cadastro de Idosos e Responsáveis

### E02-US01 — Cadastro de novo idoso com pelo menos um contato de emergência (#12) — MUST HAVE

Como **Administrador**, quero **cadastrar um novo idoso com nome, data de nascimento, informações de saúde e pelo menos um contato de emergência**, para **manter um registro organizado e garantir que exista uma referência de contato associada ao residente**.

**Critérios de aceitação:**

- O cadastro deve permitir informar nome, data de nascimento e informações de saúde.
- Deve ser informado pelo menos um contato de emergência.
- O sistema não deve concluir o cadastro sem um contato de emergência válido.
- O contato de emergência deve permanecer associado ao residente cadastrado.
- Os campos obrigatórios devem ser validados antes da gravação.
- Após salvar, o residente deve possuir apenas um registro válido no sistema.

### E02-US02 — Editar dados de um idoso (#37) — SHOULD HAVE

Como **Administrador**, quero **editar os dados de um idoso já cadastrado**, para **manter as informações sempre atualizadas**.

**Critérios de aceitação:**

- O Administrador deve poder acessar os dados de um residente já cadastrado.
- Deve ser possível atualizar os dados permitidos do residente.
- O sistema deve validar os campos obrigatórios antes de salvar as alterações.
- As alterações devem permanecer associadas ao residente correto.
- O residente deve continuar possuindo ao menos um contato de emergência válido.

### E02-US03 — Listagem de idosos cadastrados (#13) — SHOULD HAVE

Como **Administrador**, quero **listar todos os idosos cadastrados**, para **visualizar rapidamente os residentes do lar**.

**Critérios de aceitação:**

- A listagem deve exibir os residentes cadastrados.
- Cada item deve apresentar informações suficientes para identificação do residente.
- Novos cadastros válidos devem aparecer na listagem.

### E02-US04 — Gestão de contatos de emergência (#36) — SHOULD HAVE

Como **Administrador**, quero **gerenciar os contatos de emergência de um idoso após o cadastro inicial**, para **manter atualizadas as referências que podem ser acionadas quando necessário**.

**Critérios de aceitação:**

- Deve ser possível visualizar os contatos de emergência associados ao residente.
- Deve ser possível adicionar contatos de emergência adicionais.
- Deve ser possível atualizar os dados de um contato existente.
- O sistema deve manter pelo menos um contato de emergência válido associado ao residente.
- Cada contato deve permanecer vinculado ao residente correto.

### E02-US05 — Registrar mensalidade do residente (#38) — COULD HAVE

Como **Administrador**, quero **registrar o valor e a data de vencimento da mensalidade de cada residente**, para **controlar os pagamentos do lar**.

**Critérios de aceitação:**

- A mensalidade deve estar associada a um residente cadastrado.
- Deve ser possível informar valor e data de vencimento.
- O sistema deve validar os campos obrigatórios antes da gravação.
- Os dados registrados devem ficar disponíveis para consulta posterior.

---

## ÉPICO 3 — Gestão de Medicamentos

### E03-US01 — Cadastro de medicamentos (#14) — MUST HAVE

Como **Administrador**, quero **cadastrar os medicamentos de cada idoso com nome, dosagem e frequência**, para **garantir que o tratamento seja seguido corretamente**.

**Critérios de aceitação:**

- O medicamento deve ser associado a um residente.
- O cadastro deve permitir informar nome, dosagem e frequência.
- Os dados cadastrados devem ficar disponíveis para consulta posterior.

### E03-US02 — Consulta de medicamentos por horário (#15) — MUST HAVE

Como **Cuidador**, quero **visualizar a lista de medicamentos que devo ministrar em cada horário**, para **não esquecer nenhuma dose**.

**Critérios de aceitação:**

- A consulta deve apresentar os medicamentos previstos para cada horário.
- Devem ser exibidos o residente, o medicamento e a dosagem correspondente.
- As informações exibidas devem refletir os medicamentos cadastrados.

### E03-US03 — Marcar dose como ministrada (#39) — MUST HAVE

Como **Cuidador**, quero **marcar uma dose como ministrada**, para **registrar que o medicamento foi dado ao idoso**.

**Critérios de aceitação:**

- O Cuidador deve poder selecionar a dose prevista correspondente.
- O registro deve permanecer associado ao residente e ao medicamento corretos.
- A administração deve registrar data e horário.
- Após o registro, a dose deve ficar disponível no histórico.

### E03-US04 — Visualizar histórico de doses ministradas (#40) — SHOULD HAVE

Como **Administrador**, quero **visualizar o histórico de doses ministradas**, para **acompanhar se o tratamento está sendo seguido**.

**Critérios de aceitação:**

- O histórico deve apresentar o residente, medicamento, dose, data e horário registrados.
- As informações devem corresponder aos registros de administração existentes.
- O Administrador deve poder consultar o histórico de forma organizada.
- Os dados devem permanecer vinculados ao residente correto.

---

## ÉPICO 4 — Registro de Rotina

### E04-US01 — Checklist diário de higiene (#16) — MUST HAVE

Como **Cuidador**, quero **acessar um checklist diário com as atividades de higiene do residente**, para **garantir que todos os cuidados foram realizados**.

**Critérios de aceitação:**

- O checklist deve apresentar as atividades de higiene previstas.
- O Cuidador deve poder marcar cada atividade como realizada.
- O registro deve permanecer associado ao residente e à data correspondente.

### E04-US02 — Registro de refeições (#17) — MUST HAVE

Como **Cuidador**, quero **marcar as refeições do dia como realizadas ou não**, para **registrar a alimentação do idoso**.

**Critérios de aceitação:**

- O sistema deve apresentar as refeições previstas do dia.
- O Cuidador deve poder marcar cada refeição como realizada ou não realizada.
- O registro deve permanecer associado ao residente e à data correspondente.

### E04-US03 — Adicionar observação à rotina diária (#41) — MUST HAVE

Como **Cuidador**, quero **adicionar uma observação ao checklist diário**, para **registrar qualquer ocorrência relevante do dia**.

**Critérios de aceitação:**

- O Cuidador deve poder registrar uma observação textual.
- A observação deve permanecer associada ao residente e à data correspondente.
- O registro deve identificar o responsável pela observação.
- A observação deve ficar disponível para consulta posterior.

### E04-US04 — Visualizar histórico de rotina (#42) — SHOULD HAVE

Como **Administrador**, quero **visualizar o histórico de rotina de cada idoso**, para **acompanhar a qualidade dos cuidados prestados**.

**Critérios de aceitação:**

- O histórico deve apresentar os registros de rotina do residente.
- Os registros devem estar organizados por data.
- Devem ser exibidas informações de higiene, alimentação e observações existentes.
- Os dados apresentados devem permanecer vinculados ao residente correto.

---

## ÉPICO 5 — Consulta para Familiares

### E05-US01 — Visualizar medicamentos e horários (#28) — MUST HAVE

Como **Familiar**, quero **visualizar os medicamentos do meu familiar e os horários em que foram ministrados**, para **ter tranquilidade sobre o tratamento**.

**Critérios de aceitação:**

- O Familiar deve visualizar apenas informações do residente ao qual possui acesso.
- A consulta deve apresentar medicamento e horário correspondente.
- As informações devem refletir os registros disponíveis no sistema.

### E05-US02 — Visualizar checklist de rotina diária (#29) — SHOULD HAVE

Como **Familiar**, quero **ver o checklist de rotina diária do meu familiar**, para **acompanhar os cuidados de higiene e alimentação**.

**Critérios de aceitação:**

- O Familiar deve visualizar o checklist diário do residente autorizado.
- O checklist deve apresentar registros de higiene e alimentação.
- Os dados devem estar vinculados à data correspondente.

### E05-US03 — Visualizar observações dos cuidadores (#30) — SHOULD HAVE

Como **Familiar**, quero **visualizar as observações registradas pelos cuidadores**, para **ficar por dentro de qualquer ocorrência relevante**.

**Critérios de aceitação:**

- O Familiar deve visualizar apenas observações do residente autorizado.
- Cada observação deve indicar a data do registro.
- As observações devem ser apresentadas de forma legível e organizada.

### E05-US04 — Visualizar dados de contato do lar (#31) — COULD HAVE

Como **Familiar**, quero **ver os dados de contato do lar**, para **conseguir falar com a equipe quando necessário**.

**Critérios de aceitação:**

- Os dados de contato devem estar disponíveis na área do Familiar.
- As informações exibidas devem incluir ao menos um canal de contato.
- Os dados apresentados devem corresponder às informações cadastradas pelo lar.

---

## ÉPICO 6 — Banco de Dados e Integração

### E06-US01 — Criar estrutura de tabelas do banco de dados (#32) — MUST HAVE

Como **Desenvolvedor**, quero **criar as tabelas de usuários, idosos, medicamentos, rotinas e mensalidades no banco de dados**, para **que o sistema tenha uma base estruturada**.

**Critérios de aceitação:**

- Devem existir estruturas para usuários, idosos, medicamentos, rotinas e mensalidades.
- Os relacionamentos necessários entre as entidades devem ser definidos.
- A estrutura deve permitir persistência consistente dos dados.

### E06-US02 — Criar rotas da API (#33) — MUST HAVE

Como **Desenvolvedor**, quero **criar as rotas da API para cadastro, edição e listagem de dados**, para **que o front-end consiga se comunicar com o back-end**.

**Critérios de aceitação:**

- Devem existir rotas para cadastro dos dados necessários.
- Devem existir rotas para edição dos registros suportados.
- Devem existir rotas para listagem e consulta dos dados.

### E06-US03 — Implementar autenticação via JWT (#34) — MUST HAVE

Como **Desenvolvedor**, quero **implementar autenticação via token (JWT)**, para **garantir que apenas usuários autorizados acessem o sistema**.

**Critérios de aceitação:**

- Usuários autenticados devem receber um token válido.
- Rotas protegidas devem exigir autenticação.
- Requisições sem token válido devem ter o acesso negado.

### E06-US04 — Integrar formulários do front-end à API (#35) — MUST HAVE

Como **Desenvolvedor**, quero **conectar os formulários do front-end às rotas da API**, para **que os dados inseridos sejam salvos no banco**.

**Critérios de aceitação:**

- Os formulários devem enviar dados para as rotas corretas da API.
- Os dados enviados com sucesso devem ser persistidos no banco.
- Erros de integração devem ser tratados e informados adequadamente.

---

# Priorização — Técnica MoSCoW

A técnica de priorização utilizada é o **MoSCoW** (*Must Have, Should Have, Could Have, Won't Have*).

## Resumo da distribuição

| Prioridade | Quantidade |
|---|---:|
| Must Have | 16 |
| Should Have | 7 |
| Could Have | 2 |
| Won't Have (nesta versão) | 0 |
| **Total** | **25** |

## MUST HAVE — 16 histórias

- E01-US01 — Cadastro de Administrador
- E01-US02 — Login de Administrador
- E01-US03 — Login de Cuidador
- E01-US04 — Criação de contas de Cuidadores e Familiares
- E02-US01 — Cadastro de novo idoso com pelo menos um contato de emergência
- E03-US01 — Cadastro de medicamentos
- E03-US02 — Consulta de medicamentos por horário
- E03-US03 — Marcar dose como ministrada
- E04-US01 — Checklist diário de higiene
- E04-US02 — Registro de refeições
- E04-US03 — Adicionar observação à rotina diária
- E05-US01 — Visualizar medicamentos e horários
- E06-US01 — Criar estrutura de tabelas do banco de dados
- E06-US02 — Criar rotas da API
- E06-US03 — Implementar autenticação via JWT
- E06-US04 — Integrar formulários do front-end à API

## SHOULD HAVE — 7 histórias

- E02-US02 — Editar dados de um idoso
- E02-US03 — Listagem de idosos cadastrados
- E02-US04 — Gestão de contatos de emergência
- E03-US04 — Visualizar histórico de doses ministradas
- E04-US04 — Visualizar histórico de rotina
- E05-US02 — Visualizar checklist de rotina diária
- E05-US03 — Visualizar observações dos cuidadores

## COULD HAVE — 2 histórias

- E02-US05 — Registrar mensalidade do residente
- E05-US04 — Visualizar dados de contato do lar

## WON'T HAVE (nesta versão) — 0 histórias

Nenhuma história foi classificada nesta categoria na versão revisada do backlog.

---

# Justificativa Técnica

A técnica de priorização escolhida para o backlog do Acolher+ foi o MoSCoW (*Must have, Should have, Could have, Won't have*), por ser simples de comunicar tanto para a equipe técnica quanto para interlocutores não técnicos — como a direção do lar de idosos e, eventualmente, familiares consultados durante a validação do produto.

Diferente de escalas numéricas ou pontuação por esforço, o MoSCoW permite classificar rapidamente cada história em função do impacto que sua ausência causaria no produto, o que é especialmente útil em um projeto de extensão com prazo definido e escopo que precisa ser justificado de forma objetiva.

As histórias classificadas como **Must Have (16)** concentram-se nas funcionalidades que sustentam o funcionamento mínimo do sistema e a rastreabilidade do cuidado: autenticação e controle de usuários (E01-US01 a E01-US04); cadastro inicial seguro de residentes, já com ao menos um contato de emergência obrigatório (E02-US01); cadastro de medicamentos, consulta por horário e registro das doses ministradas (E03-US01 a E03-US03); registro de higiene, alimentação e observações da rotina (E04-US01 a E04-US03); visualização básica de medicamentos e horários pelo Familiar (E05-US01); e a base técnica que viabiliza tudo isso — estrutura do banco de dados, rotas da API, autenticação via JWT e integração entre front-end e back-end (E06-US01 a E06-US04). Essas histórias atacam diretamente os riscos descritos no problema — erros de medicação e falta de rastreabilidade — e as demais funcionalidades dependem delas para existir.

As histórias classificadas como **Should Have (7)** são importantes para a usabilidade, a manutenção dos dados e o acompanhamento do cuidado, mas não impedem a primeira operação básica do sistema: edição dos dados do residente (E02-US02), listagem de idosos (E02-US03), gestão posterior dos contatos de emergência (E02-US04), histórico de doses ministradas (E03-US04), histórico de rotina (E04-US04) e, na área do Familiar, a visualização do checklist de rotina (E05-US02) e das observações dos cuidadores (E05-US03). Elas ampliam o valor do produto em iterações seguintes, sem comprometer o núcleo operacional caso sejam adiadas.

As histórias classificadas como **Could Have (2)** agregam valor administrativo e de comunicação, mas não comprometem o núcleo de cuidado se forem adiadas: o registro da mensalidade de cada residente (E02-US05) e a visualização dos dados de contato do lar pelo Familiar (E05-US04). Cabe destacar que o escopo de mensalidades é deliberadamente limitado ao registro de valor e data de vencimento associados ao residente; o Acolher+ não se propõe, nesta versão, a ser um sistema financeiro, e integrações financeiras ou fiscais permanecem fora do que está definido.

Nesta versão revisada do backlog, nenhuma história foi classificada como **Won't Have**. A categoria foi mantida na priorização para evidenciar que o método foi aplicado de forma completa.

Os três perfis de persona definidos — Administrador, Cuidador e Familiar — refletem papéis distintos dentro do sistema. O Administrador gerencia cadastros, contas de usuários e a operação geral; o Cuidador consulta e registra o dia a dia do cuidado, incluindo doses, higiene, refeições e observações; e o Familiar acompanha as informações do residente ao qual possui acesso, sem poder alterá-las.

Essa separação de perfis orienta diretamente os critérios de aceitação relacionados a acesso — como o login por perfil (E01-US02 e E01-US03), a criação de contas com perfil definido (E01-US04), a proteção de rotas por token (E06-US03) e a restrição do Familiar ao residente autorizado (E05-US01 a E05-US03) — e deverá ser refinada com a evolução do projeto.
