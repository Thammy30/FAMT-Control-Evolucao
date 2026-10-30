# FAMT Control — Projeto de Transição (Waterfall → Scrum)

## 📌 Identificação do Projeto e Governança

**Universidade:** Universidade de Mogi das Cruzes (UMC)  
**Curso:** Engenharia de Software  
**Disciplina:** Gestão de Projetos de Software (Semestre 2026/2)  
**Professor Orientador:** Prof. Renato  
**Sistema:** FAMT Control — Aplicativo de Controle de Gastos Pessoais  
**Abordagem Metodológica:** Hibridismo Metodológico (Preditivo/Waterfall + Ágil/Scrum)

---

## 👥 Squad FAMT de Desenvolvimento

| Integrante | RA | Papel Técnico | Atribuições Principais |
|---|---|---|---|
| Franciellen Moreira Santos | 11261403634 | Gerente de Projetos (PM) | Coordenação geral, cronograma CPM/Gantt, TAP/EAP, documentação e comunicação. |
| Maria Augusta S. Toledo | 11241102057 | Product Owner (PO) / QA | Priorização do Backlog, critérios de aceite das User Stories, BDD e qualidade. |
| André Mitchel Ruiz Santos | 11231102531 | Tech Lead / Desenvolvedor | Arquitetura Python/Streamlit, regras de negócio, interface e gráficos Plotly. |
| Thamirys Matos da Silva | 11261403155 | Engenheira de Dados (DBA) | Modelagem relacional, estrutura do banco de dados, constraints e chaves estrangeiras. |

---

## 🔄 Contextualização da Transição Metodológica (Waterfall → Scrum)

O projeto FAMT Control foi desenvolvido inicialmente na M1, utilizando uma abordagem preditiva baseada nos conceitos do PMI (Waterfall). Nessa etapa, foi realizado o planejamento do projeto por meio do Termo de Abertura do Projeto (TAP), da Estrutura Analítica do Projeto (EAP/WBS), do Diagrama de Precedência (PDM), da identificação do Caminho Crítico (CPM) e da definição da linha de base orçamentária de R$ 11.913,00, com BAC de R$ 12.454,50.

Na etapa de transição, o planejamento inicialmente estruturado foi aproveitado como base para a organização do trabalho utilizando o Scrum Framework. O escopo definido na EAP foi convertido em um Product Backlog, organizado em Histórias de Usuário (User Stories), permitindo dividir as funcionalidades em entregas menores e priorizadas.

Além da mudança na organização do trabalho, a aplicação também passou por uma evolução técnica. Na versão inicial, o sistema utilizava SQLite para armazenar os dados. Durante a transição, foi realizada a migração para MySQL, permitindo utilizar um banco de dados externo à aplicação e configurado para conexão com o ambiente de implantação.

Também foi acrescentada a funcionalidade de redefinição de senha, ampliando as opções disponíveis na tela de autenticação.

Dessa forma, a transição representou tanto uma evolução na organização do projeto quanto uma atualização técnica da aplicação.

---

## 🗺️ Mapeamento Hierárquico de Tradução (EAP → Scrum)

Para manter a relação entre o planejamento inicial e a execução ágil, foi utilizada a seguinte correspondência entre os elementos da EAP e os elementos do Scrum:

| Nível Preditivo (PMI / EAP) | Nível Ágil (Scrum) | Definição no FAMT Control |
|---|---|---|
| Projeto / Módulo | Épico | Grandes conjuntos de funcionalidades da aplicação, como Gestão Financeira e Painel de Alertas. |
| Pacote de Trabalho (EAP) | Funcionalidade / Feature | Conjunto de funcionalidades que gera valor ao usuário. |
| Requisitos Detalhados | História de Usuário (User Story) | Descrição de uma necessidade do usuário e do resultado esperado. |
| Atividades do Cronograma | Tarefas Técnicas (Tasks) | Atividades de desenvolvimento, banco de dados, interface e qualidade. |

Esse mapeamento foi utilizado para orientar a organização do Product Backlog, mantendo a relação entre o escopo planejado na M1 e as funcionalidades trabalhadas na transição.

---

## 📋 Product Backlog Ordenado do FAMT Control

O escopo inicial foi organizado em seis Histórias de Usuário (US-001 a US-006), contemplando as principais funcionalidades do sistema. Durante a transição, a funcionalidade de redefinição de senha foi acrescentada como uma nova necessidade.

### 1. US-001 — Cadastro de Transações Financeiras

**User Story:** Como estudante universitário, quero cadastrar minhas receitas e despesas com descrição, valor e categoria, para manter minha contabilidade pessoal atualizada.

- Prioridade PO: Alta / Essencial
- Estimativa técnica: 5 Story Points (SP)

### 2. US-002 — Painel de Saldos e Indicadores

**User Story:** Como usuário do sistema, quero visualizar meus cartões de Receita, Despesa e Saldo Atualizado no painel principal, para compreender minha situação financeira.

- Prioridade PO: Alta / Essencial
- Estimativa técnica: 3 Story Points (SP)

### 3. US-003 — Central de Notificações e Alertas Contábeis

**User Story:** Como usuário do FAMT Control, quero receber alertas sobre minha situação financeira e confirmações de lançamentos, para acompanhar melhor minhas receitas e despesas.

- Prioridade PO: Média / Valor
- Estimativa técnica: 5 Story Points (SP)

### 4. US-004 — Gestão de Metas Financeiras Mensais

**User Story:** Como estudante, quero definir uma meta de economia e acompanhar a porcentagem atingida, para planejar meu orçamento de forma disciplinada.

- Prioridade PO: Média
- Estimativa técnica: 3 Story Points (SP)

### 5. US-005 — Visualização de Gráficos e Ranking de Despesas

**User Story:** Como usuário, quero analisar gráficos comparativos de receitas e despesas e a distribuição por categoria, para identificar meus maiores gastos.

- Prioridade PO: Média
- Estimativa técnica: 5 Story Points (SP)

### 6. US-006 — Autenticação e Troca de Senha no Primeiro Acesso

**User Story:** Como usuário cadastrado, quero alterar minha senha provisória no primeiro acesso, para personalizar minhas credenciais de entrada.

- Prioridade PO: Alta / Segurança
- Estimativa técnica: 2 Story Points (SP)

### 7. US-007 — Redefinição de Senha

**User Story:** Como usuário cadastrado que esqueceu sua senha, quero informar meu e-mail e cadastrar uma nova senha, para recuperar o acesso à minha conta.

- Prioridade PO: Alta / Segurança
- Funcionalidade acrescentada durante a transição.

---

## 🧪 Critérios de Aceitação em BDD (Behavior-Driven Development)

Os critérios de aceitação foram organizados utilizando a estrutura Gherkin (Dado / Quando / Então), para descrever o comportamento esperado das funcionalidades.

### Cenário 1: Cadastro de Receita com Atualização e Notificação (US-001)

**Dado** que o usuário está autenticado e acessa a área "Lançar".

**Quando** preencher o tipo "Receita", valor "150.00", descrição "Bolsa Estágio" e categoria "Salário".

**E** clicar no botão "Salvar Transação no Banco de Dados".

**Então** o sistema deverá salvar a transação na tabela `Transacoes` do MySQL.

**E** atualizar as informações apresentadas no painel.

**E** gerar a notificação correspondente no sistema.

### Cenário 2: Alerta Contábil por Saldo Devedor (US-003)

**Dado** que o total de despesas cadastradas supera o total de receitas acumuladas.

**Quando** o usuário acessar o Painel Principal ou a Central de Alertas.

**Então** o sistema deverá apresentar um alerta visual sobre a situação financeira.

**E** disponibilizar o aviso na Central de Notificações.

### Cenário 3: Primeiro Acesso com Troca Obrigatória de Senha (US-006)

**Dado** que um novo usuário realiza o login utilizando a senha provisória.

**E** o campo `primeiro_acesso` na tabela `Usuarios` possui o valor 1.

**Quando** o sistema identificar que se trata do primeiro acesso.

**Então** deverá apresentar a tela de alteração de senha.

**E** exigir a definição de uma nova senha antes de liberar o acesso ao painel principal.

### Cenário 4: Redefinição de Senha (US-007)

**Dado** que o usuário possui um e-mail cadastrado no sistema.

**Quando** acessar a aba "Redefinir Senha", informar o e-mail, digitar uma nova senha e confirmar a senha.

**E** clicar no botão "Salvar Nova Senha".

**Então** o sistema deverá verificar se o e-mail está cadastrado e se as senhas informadas coincidem.

**E** atualizar o hash da senha na tabela `Usuarios` do MySQL.

**E** apresentar uma mensagem de confirmação da redefinição.

**Observação:** Na implementação atual, a redefinição é feita diretamente pelo formulário, mediante o e-mail cadastrado. Não há envio de código ou link de confirmação por e-mail.

---

## ⚙️ Decomposição Técnica em Sprint Tasks e Estimativas

As atividades técnicas foram organizadas de acordo com as Histórias de Usuário e as necessidades de evolução da aplicação.

| ID Task | Descrição da Atividade Técnica | História Vinculada | Especialidade | Estimativa |
|---|---|---|---|---|
| TSK-101 | Modelagem das tabelas `Usuarios` e `Transacoes`, com chaves estrangeiras no MySQL. | US-001 | Backend / Banco de Dados | 3 horas |
| TSK-102 | Desenvolvimento do formulário de lançamento de receitas e despesas no Streamlit. | US-001 | Frontend | 4 horas |
| TSK-103 | Implementação do cálculo de saldos e organização das transações por data. | US-002 | Backend | 3 horas |
| TSK-104 | Construção do componente de notificações e alertas. | US-003 | Frontend | 5 horas |
| TSK-105 | Geração dos gráficos de barras e rosca utilizando Plotly Express. | US-005 | Frontend / Dados | 4 horas |
| TSK-106 | Implementação do hash SHA-256 e validação de primeiro acesso. | US-006 | Segurança | 4 horas |
| TSK-107 | Desenvolvimento do formulário de redefinição de senha e atualização no MySQL. | US-007 | Backend / Segurança | Atividade acrescentada na transição |

*As estimativas representam o planejamento das atividades e não necessariamente o tempo efetivamente utilizado para sua execução.*

---

## 🏆 Governança e Critérios de Qualidade: DoR e DoD

### Definition of Ready (DoR) — Critérios para Entrar na Sprint

- Requisito funcional claro e alinhado com a regra de negócio do FAMT Control.
- Critérios de aceitação definidos no formato BDD (Dado / Quando / Então).
- Dependências relacionadas ao banco de dados MySQL e aos componentes visuais identificadas.
- Estimativa relativa definida pela equipe por meio de Planning Poker.
- História de Usuário compreendida pela equipe e com condições para desenvolvimento.

### Definition of Done (DoD) — Critérios para Considerar Concluído

- Código Python integrado à aplicação Streamlit.
- Operações de persistência executadas utilizando o banco de dados MySQL.
- Gráficos Plotly apresentados corretamente na interface.
- Navegação entre as funcionalidades testada.
- Validações dos formulários e mensagens de retorno implementadas.
- Critérios de aceitação da História de Usuário atendidos.
- Revisão e validação da entrega pela equipe.

---

## 🔗 Matriz de Rastreabilidade (EAP x Product Backlog)

A matriz relaciona os pacotes de trabalho definidos na EAP inicial às Histórias de Usuário organizadas no Product Backlog.

| Cód. EAP | Pacote de Trabalho Original (PMI) | Histórias de Usuário Vinculadas |
|---|---|---|
| EAP 2.1 | Módulo de Gestão de Transações | US-001, US-002 |
| EAP 2.2 | Módulo de Alertas e Notificações | US-003 |
| EAP 2.3 | Módulo de Planejamento de Metas | US-004 |
| EAP 3.1 | Módulo de Análise Gráfica e Segurança | US-005, US-006 |

A US-007 foi acrescentada durante a transição como uma evolução da funcionalidade de autenticação, relacionada à redefinição de senha.

A matriz demonstra a relação entre o planejamento inicial e a organização das funcionalidades no Scrum. A conclusão individual de cada História de Usuário deve ser registrada conforme sua validação pela equipe.

---

## 🗄️ Arquitetura da Aplicação e Banco de Dados

O FAMT Control utiliza Python e Streamlit para a aplicação web, com MySQL para persistência dos dados e Plotly para a apresentação dos gráficos.

### Tecnologias Utilizadas

| Tecnologia | Finalidade |
|---|---|
| Python | Linguagem de programação principal. |
| Streamlit | Desenvolvimento da interface web. |
| MySQL | Armazenamento e gerenciamento dos dados. |
| MySQL Connector/Python | Comunicação entre a aplicação Python e o banco MySQL. |
| Pandas | Manipulação e organização dos dados. |
| Plotly Express | Construção de gráficos e visualizações. |
| Plotly Graph Objects | Criação de elementos gráficos personalizados. |
| Hashlib | Geração do hash SHA-256 das senhas. |
| HTML e CSS | Personalização visual da aplicação. |

### Estrutura do Banco de Dados

Durante a transição, o banco de dados SQLite foi substituído pelo MySQL.

A aplicação utiliza duas tabelas principais:

**Tabela `Usuarios`**

| Campo | Descrição |
|---|---|
| id | Identificador do usuário, com incremento automático. |
| email | E-mail cadastrado, único e obrigatório. |
| senha_hash | Hash da senha do usuário. |
| primeiro_acesso | Indicador de primeiro acesso, utilizado para exigir a troca da senha provisória. |

**Tabela `Transacoes`**

| Campo | Descrição |
|---|---|
| id | Identificador da transação, com incremento automático. |
| usuario_id | Identificador do usuário relacionado à transação. |
| valor | Valor financeiro da transação. |
| tipo | Tipo de movimentação: Receita ou Despesa. |
| data | Data e horário do lançamento. |
| descricao | Descrição da movimentação. |
| categoria | Categoria financeira da movimentação. |

A tabela `Transacoes` possui uma chave estrangeira (`usuario_id`) relacionada à tabela `Usuarios`, com exclusão em cascata (`ON DELETE CASCADE`).

### Conexão com o MySQL

A aplicação utiliza a biblioteca `mysql.connector` para realizar a conexão com o banco de dados.

As informações de conexão são obtidas por meio do recurso `st.secrets` do Streamlit, utilizando as configurações de host, usuário, senha, banco de dados e porta.

No ambiente Streamlit Cloud, as credenciais devem ser configuradas na seção **Secrets**, seguindo a estrutura:

```toml
[mysql]
host = "SEU_HOST"
user = "SEU_USUARIO"
password = "SUA_SENHA"
database = "SEU_BANCO"
port = 3306
```

As credenciais reais não devem ser publicadas no repositório.

---

## 🔐 Segurança e Autenticação

O sistema possui mecanismos de autenticação e controle de acesso, incluindo:

- Cadastro de usuários por e-mail.
- Armazenamento de senhas utilizando hash SHA-256.
- Validação das credenciais durante o login.
- Troca obrigatória da senha provisória no primeiro acesso.
- Funcionalidade de redefinição de senha.
- Separação das transações por usuário.
- Utilização de chave estrangeira para relacionar usuários e transações.
- Validação dos dados informados nos formulários.

A função `hashlib.sha256()` é utilizada para gerar o hash das senhas antes de seu armazenamento no banco de dados. SHA-256 é uma função de hash, e não um método de criptografia reversível.

**Observação de segurança:** para uma aplicação em produção, recomenda-se utilizar algoritmos específicos para armazenamento de senhas, como Argon2 ou bcrypt, além de implementar uma etapa de verificação de identidade na redefinição de senha.

---

## 💻 Como Executar a Aplicação

### Pré-requisitos

- Python 3.10 ou superior.
- MySQL disponível e configurado.
- Gerenciador de pacotes pip.
- Acesso às credenciais do banco de dados.

### 1. Clonar o Repositório

```bash
git clone URL_DO_REPOSITORIO
```

Acesse a pasta do projeto:

```bash
cd NOME_DA_PASTA
```

### 2. Criar o Ambiente Virtual

```bash
python -m venv venv
```

Ativar no Windows:

```bash
venv\Scripts\activate
```

### 3. Instalar as Dependências

```bash
pip install streamlit mysql-connector-python pandas plotly
```

### 4. Configurar o Banco de Dados

Configure as credenciais de conexão com o MySQL no ambiente de execução.

Na implantação pelo Streamlit Cloud, utilize a seção Secrets com a estrutura apresentada anteriormente.

A aplicação possui uma rotina de inicialização que cria as tabelas `Usuarios` e `Transacoes` caso ainda não existam.

### 5. Executar a Aplicação Web

```bash
python -m streamlit run famt-control-app-com-logo-transicao.py
```

Após iniciar, acesse o endereço local apresentado no terminal, normalmente:

```text
http://localhost:8501
```

---

## 🧪 Qualidade e Validação

Os critérios BDD foram utilizados para descrever os comportamentos esperados das funcionalidades, orientando a validação das entregas.

Entre os principais pontos de verificação estão:

- Cadastro e armazenamento de receitas e despesas.
- Atualização dos indicadores financeiros.
- Exibição dos alertas e notificações.
- Funcionamento das metas e visualizações gráficas.
- Autenticação e troca de senha no primeiro acesso.
- Redefinição de senha.
- Conexão e persistência de dados no MySQL.

Os cenários descritos nesta documentação representam critérios de aceitação. A execução de uma suíte automatizada com Pytest deve ser documentada separadamente, caso os respectivos arquivos de testes estejam implementados e disponíveis no projeto.

---

## 🎯 Conclusão do Hibridismo

A transição do FAMT Control demonstra como o planejamento preditivo realizado na M1 pode servir como base para uma organização ágil do desenvolvimento.

A EAP inicialmente elaborada foi utilizada como referência para estruturar o Product Backlog e organizar as Histórias de Usuário, permitindo uma visão mais detalhada das funcionalidades e atividades técnicas.

Além da adaptação metodológica, o sistema passou por uma evolução técnica com a migração do SQLite para o MySQL e a inclusão da funcionalidade de redefinição de senha.

Dessa forma, o projeto manteve a continuidade do escopo inicialmente planejado e avançou em sua implementação, incorporando melhorias na estrutura de dados, na autenticação e na organização do trabalho da equipe.

## 📄 Licença e Direitos Autorais

Este projeto foi desenvolvido pela **Squad FAMT** para fins acadêmicos, como parte das atividades do curso de Engenharia de Software da Universidade de Mogi das Cruzes (UMC).

© 2026 Squad FAMT. Todos os direitos reservados.

---

<p align="center">
  💜 <strong>FAMT CONTROL</strong><br>
  <em>Seu dinheiro sob controle.</em><br><br>
  Desenvolvido com dedicação pela Squad FAMT.
</p>

---

**Projeto acadêmico desenvolvido pelo Squad FAMT — Engenharia de Software | UMC | 2026/2.**
