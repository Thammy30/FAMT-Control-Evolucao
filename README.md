# 💜 FAMT Control — Projeto de Transição (Waterfall → Scrum)

## 📌 Identificação do Projeto

**Projeto:** FAMT Control  
**Instituição:** Universidade de Mogi das Cruzes (UMC)  
**Curso:** Engenharia de Software  
**Disciplina:** Gestão de Projetos de Software  
**Semestre:** 2026/2  
**Professor:** Renato  
**Metodologia:** Transição híbrida de Waterfall para Scrum  

---

## 👥 Squad FAMT

| Integrante | RA | Responsabilidade |
|---|---|---|
| Franciellen Moreira Santos | 11261403634 | Product Manager (PM) |
| Maria Augusta S. Toledo | 11241102057 | Product Owner (PO) / QA |
| André Mitchel Ruiz Santos | 11231102531 | Tech Lead / Developer |
| Thamirys Matos da Silva | 11261403155 | DBA |

---

## 📖 1. Contextualização do Projeto

O FAMT Control é um sistema de controle financeiro pessoal, desenvolvido com o objetivo de auxiliar os usuários na organização de suas finanças, permitindo o gerenciamento de receitas, despesas, metas financeiras e acompanhamento de informações por meio de gráficos e indicadores.

Inicialmente, o projeto foi planejado utilizando a metodologia tradicional Waterfall (Cascata), com a elaboração dos documentos de gerenciamento de projetos, incluindo:

- Termo de Abertura do Projeto (TAP);
- Estrutura Analítica do Projeto (EAP);
- Diagrama de Precedência (PDM);
- Método do Caminho Crítico (CPM);
- Definição da linha de base de custos.

**Linha de base de custos:** R$ 11.913,00  
**Orçamento total (BAC):** R$ 12.454,50

Na segunda etapa, o projeto passou por uma transição para a metodologia ágil Scrum, transformando a estrutura inicialmente planejada em um Product Backlog, composto por Histórias de Usuário, critérios de aceitação e tarefas técnicas.

Durante essa transição, também ocorreu uma evolução técnica do sistema, com a migração do banco de dados SQLite para MySQL, agora hospedado na nuvem por meio da plataforma Aiven, além da inclusão da funcionalidade de redefinição de senha.

---

## 🔄 2. Transição de Waterfall para Scrum

A transição teve como objetivo adaptar o planejamento tradicional à abordagem ágil, organizando as funcionalidades do sistema de acordo com as necessidades dos usuários.

A EAP foi utilizada como referência para estruturar as funcionalidades em Histórias de Usuário.

### 2.1. Mapeamento da EAP para o Product Backlog

| Estrutura da EAP | Elemento no Scrum |
|---|---|
| Planejamento do projeto | Product Backlog |
| Levantamento de requisitos | Histórias de Usuário |
| Desenvolvimento das funcionalidades | Sprint Backlog |
| Atividades técnicas | Tasks |
| Entregas do projeto | Incrementos do produto |
| Validação do sistema | Critérios de aceitação e Definition of Done |

---

## 📋 3. Product Backlog — Histórias de Usuário

O escopo inicial foi organizado em seis Histórias de Usuário (US-001 a US-006), contemplando as principais funcionalidades do sistema. Durante a transição, foi acrescentada a US-007, referente à redefinição de senha.

| ID | História de Usuário | Prioridade |
|---|---|---|
| US-001 | Como usuário, quero cadastrar receitas e despesas para controlar minhas movimentações financeiras. | Alta |
| US-002 | Como usuário, quero visualizar um dashboard com informações financeiras para acompanhar minha situação financeira. | Alta |
| US-003 | Como usuário, quero receber notificações e alertas para acompanhar informações importantes sobre minhas finanças. | Média |
| US-004 | Como usuário, quero cadastrar e acompanhar metas financeiras para organizar meus objetivos. | Média |
| US-005 | Como usuário, quero visualizar gráficos financeiros para compreender melhor meus gastos e receitas. | Média |
| US-006 | Como usuário, quero alterar minha senha no primeiro acesso para garantir maior controle sobre minha conta. | Alta |
| US-007 | Como usuário, quero redefinir minha senha caso a esqueça, para recuperar o acesso ao sistema. | Média |

---

## 🧪 4. Critérios de Aceitação — BDD

Os critérios de aceitação foram estruturados utilizando o formato BDD (Behavior-Driven Development), com os elementos:

- **Dado:** contexto inicial;
- **Quando:** ação realizada;
- **Então:** resultado esperado.

### 4.1. US-001 — Cadastro de movimentações financeiras

**Cenário: Cadastro de uma nova movimentação**

- **Dado** que o usuário esteja autenticado no sistema;
- **Quando** preencher as informações de uma receita ou despesa e confirmar o cadastro;
- **Então** o sistema deverá registrar a movimentação e atualizar as informações financeiras correspondentes.

### 4.2. US-003 — Alertas de dívidas

**Cenário: Exibição de alerta financeiro**

- **Dado** que existam informações financeiras cadastradas pelo usuário;
- **Quando** o sistema identificar uma situação que necessite de atenção;
- **Então** deverá apresentar um alerta ou dica financeira na interface.

### 4.3. US-006 — Alteração de senha no primeiro acesso

**Cenário: Primeiro acesso do usuário**

- **Dado** que o usuário esteja realizando seu primeiro acesso ao sistema;
- **Quando** efetuar o login com a senha inicial;
- **Então** o sistema deverá solicitar a alteração da senha antes de permitir o acesso às demais funcionalidades.

### 4.4. US-007 — Redefinição de senha

**Cenário: Usuário deseja redefinir sua senha**

- **Dado** que o usuário esteja na tela de redefinição de senha;
- **Quando** informar seu e-mail cadastrado, uma nova senha e a confirmação da nova senha;
- **Então** o sistema deverá validar as informações e atualizar a senha vinculada à conta, permitindo o acesso com a nova credencial.

**Observação:** A funcionalidade implementada realiza a redefinição diretamente por meio do e-mail cadastrado e da nova senha informada. Não utiliza envio de código de confirmação ou link por e-mail.

---

## 🏃 5. Sprint Backlog — Tarefas Técnicas

As histórias de usuário foram desmembradas em tarefas técnicas para organizar o desenvolvimento e facilitar o acompanhamento das atividades.

| ID | Tarefa | Descrição |
|---|---|---|
| TSK-101 | Estruturação do banco de dados | Configuração do banco de dados MySQL na Aiven e criação das tabelas necessárias. |
| TSK-102 | Gerenciamento de usuários | Implementação do cadastro, autenticação e gerenciamento de usuários. |
| TSK-103 | Gerenciamento de transações | Implementação das operações de cadastro e gerenciamento de receitas e despesas. |
| TSK-104 | Dashboard financeiro | Apresentação dos indicadores e informações financeiras do usuário. |
| TSK-105 | Gráficos e metas | Implementação da visualização gráfica e do acompanhamento das metas financeiras. |
| TSK-106 | Notificações e primeiro acesso | Implementação dos alertas e da alteração obrigatória de senha no primeiro acesso. |
| TSK-107 | Redefinição de senha | Implementação da funcionalidade de redefinição de senha utilizando o e-mail cadastrado. |

---

## 📌 6. Definition of Ready (DoR) e Definition of Done (DoD)

### 6.1. Definition of Ready (DoR)

Uma História de Usuário está pronta para ser desenvolvida quando:

- Possui descrição clara e compreensível;
- Apresenta valor para o usuário;
- Possui critérios de aceitação definidos;
- Está suficientemente detalhada para orientar o desenvolvimento;
- Possui dependências identificadas;
- Está priorizada no Product Backlog.

### 6.2. Definition of Done (DoD)

Uma funcionalidade pode ser considerada concluída quando:

- O desenvolvimento da funcionalidade foi realizado;
- A implementação está integrada ao sistema;
- A conexão com o banco de dados MySQL hospedado na Aiven está funcionando quando necessária;
- Os critérios de aceitação foram atendidos;
- Foram realizadas as verificações necessárias;
- Não existem erros conhecidos que impeçam o funcionamento da funcionalidade;
- A documentação correspondente foi atualizada quando necessário.

---

## 🔗 7. Matriz de Rastreabilidade

A matriz de rastreabilidade permite relacionar os elementos da EAP às Histórias de Usuário correspondentes, mantendo a ligação entre o planejamento inicial e o desenvolvimento ágil.

| EAP | Descrição | História de Usuário |
|---|---|---|
| 2.1 | Gerenciamento de movimentações financeiras | US-001 |
| 2.2 | Visualização das informações financeiras | US-002 |
| 2.3 | Notificações e alertas | US-003 |
| 3.1 | Metas e acompanhamento financeiro | US-004 |

**Evolução do escopo:** A US-005, relacionada aos gráficos financeiros, e a US-006, referente à alteração de senha no primeiro acesso, foram organizadas no Product Backlog conforme as funcionalidades do sistema. A US-007, referente à redefinição de senha, foi acrescentada durante a transição para Scrum, representando uma evolução do escopo inicial.

---

## 🛠️ 8. Arquitetura e Tecnologias Utilizadas

O sistema foi desenvolvido utilizando Python e Streamlit, com banco de dados MySQL hospedado na plataforma Aiven. Essa configuração permite que as informações sejam armazenadas em um banco de dados externo, acessível pela aplicação por meio de uma conexão remota.

### 8.1. Tecnologias

| Tecnologia | Utilização |
|---|---|
| Python | Linguagem de programação |
| Streamlit | Desenvolvimento da interface web |
| MySQL | Sistema gerenciador de banco de dados relacional |
| Aiven | Plataforma de hospedagem do banco de dados MySQL na nuvem |
| Pandas | Manipulação e análise de dados |
| Plotly | Criação de gráficos |
| mysql-connector-python | Conexão entre Python e MySQL |
| hashlib | Geração de hash para senhas |

### 8.2. Estrutura do Banco de Dados

A transição técnica também envolveu a migração do banco de dados SQLite para MySQL, com a hospedagem da nova estrutura na plataforma Aiven.

Foram utilizadas, entre outras, as seguintes tabelas:

**Tabela: Usuarios**

| Campo | Descrição |
|---|---|
| id | Identificador do usuário |
| email | E-mail cadastrado |
| senha_hash | Hash da senha |
| primeiro_acesso | Indica se o usuário precisa alterar a senha no primeiro acesso |

**Tabela: Transacoes**

| Campo | Descrição |
|---|---|
| id | Identificador da transação |
| usuario_id | Identificador do usuário relacionado |
| valor | Valor da movimentação |
| tipo | Tipo da movimentação |
| data | Data da movimentação |
| descricao | Descrição da movimentação |
| categoria | Categoria financeira |

A tabela `Transacoes` possui uma chave estrangeira relacionada à tabela `Usuarios`, utilizando o relacionamento com exclusão em cascata (`ON DELETE CASCADE`).

---

## 🔐 9. Segurança e Gerenciamento de Senhas

O sistema utiliza hash SHA-256 por meio da biblioteca `hashlib` para armazenar as senhas, evitando que sejam gravadas diretamente em texto puro no banco de dados.

É importante destacar que SHA-256 é uma função de hash, e não uma criptografia reversível.

Para aplicações em produção, recomenda-se utilizar algoritmos específicos para armazenamento seguro de senhas, como Argon2 ou bcrypt, além de implementar mecanismos adicionais de verificação de identidade e recuperação de acesso.

As credenciais de conexão com o banco de dados são armazenadas utilizando o recurso `st.secrets` do Streamlit, evitando deixar informações sensíveis diretamente no código-fonte.

Exemplo de configuração:

```toml
[mysql]
host = "HOST_FORNECIDO_PELA_AIVEN"
port = 26250
user = "avnadmin"
password = "SUA_SENHA"
database = "defaultdb"
```

**Importante:** Os valores acima são um exemplo de configuração. O endereço do host, a porta, o usuário, a senha e o nome do banco devem corresponder às credenciais disponibilizadas na sua instância MySQL da Aiven. A senha real não deve ser publicada no GitHub.

---

## ▶️ 10. Como Executar o Projeto

### 10.1. Pré-requisitos

Antes de executar o projeto, é necessário possuir:

- Python instalado;
- Acesso à instância MySQL hospedada na Aiven;
- Credenciais de conexão disponibilizadas pela Aiven;
- Arquivo de configuração das credenciais do MySQL no Streamlit;
- Dependências do projeto instaladas.

**Observação:** Não é necessário instalar o MySQL localmente, pois o banco de dados utilizado pelo sistema está hospedado na nuvem pela Aiven.

### 10.2. Instalação das dependências

No terminal, execute:

```bash
pip install streamlit mysql-connector-python pandas plotly
```

### 10.3. Configuração da conexão com a Aiven

Crie o arquivo `secrets.toml` dentro da pasta `.streamlit`, na estrutura do projeto.

Exemplo:

```text
FAMT_Control/
│
├── .streamlit/
│   └── secrets.toml
│
├── famt-control-app-com-logo-transicao.py
└── ...
```

No arquivo `secrets.toml`, configure as informações de conexão fornecidas pela Aiven:

```toml
[mysql]
host = "HOST_FORNECIDO_PELA_AIVEN"
port = 26250
user = "avnadmin"
password = "SUA_SENHA"
database = "defaultdb"
```

As informações devem ser preenchidas conforme os dados da instância MySQL criada na Aiven.

O arquivo `secrets.toml` deve ser mantido fora do repositório público para proteger as credenciais de acesso ao banco de dados.

### 10.4. Executar a aplicação

Na pasta onde está localizado o arquivo principal do projeto, execute:

```bash
python -m streamlit run famt-control-app-com-logo-transicao.py
```

Após a execução, a aplicação poderá ser acessada pelo navegador no endereço:

```text
http://localhost:8501
```

---

## ✅ 11. Qualidade e Validação

A qualidade do sistema é acompanhada por meio dos critérios de aceitação definidos nas Histórias de Usuário e das verificações realizadas durante o desenvolvimento.

A utilização do BDD auxilia na descrição do comportamento esperado das funcionalidades, permitindo relacionar os requisitos às validações do sistema.

As verificações devem considerar:

- Cadastro e autenticação de usuários;
- Registro e gerenciamento de receitas e despesas;
- Atualização das informações do dashboard;
- Exibição de gráficos e metas;
- Funcionamento dos alertas;
- Alteração de senha no primeiro acesso;
- Redefinição de senha;
- Persistência e integridade das informações no MySQL hospedado na Aiven;
- Conexão entre a aplicação e o banco de dados remoto.

A existência de uma suíte automatizada de testes deve ser documentada somente quando os respectivos testes estiverem implementados e disponíveis no projeto.

---

## 🎯 12. Considerações Finais

A transição do FAMT Control da metodologia Waterfall para Scrum representou uma evolução na organização e no gerenciamento do projeto.

O planejamento inicial, estruturado por meio de documentos tradicionais de gerenciamento, serviu como base para a construção do Product Backlog e a organização das funcionalidades em Histórias de Usuário e tarefas técnicas.

Além da adaptação metodológica, o projeto passou por uma evolução técnica com a migração do banco de dados SQLite para MySQL, sua hospedagem na nuvem por meio da plataforma Aiven e a inclusão da funcionalidade de redefinição de senha.

Dessa forma, o projeto demonstra a aplicação prática dos conceitos de gerenciamento de projetos, desenvolvimento ágil, organização de requisitos, evolução de software e utilização de serviços de banco de dados em nuvem.

---

## 📄 13. Licença e Direitos Autorais

Este projeto foi desenvolvido pela **Squad FAMT** para fins acadêmicos, como parte das atividades do curso de Engenharia de Software da Universidade de Mogi das Cruzes (UMC).

© 2026 Squad FAMT. Todos os direitos reservados.

---

<p align="center">
  💜 <strong>FAMT CONTROL</strong><br>
  <em>Seu dinheiro sob controle.</em><br><br>
  Desenvolvido com dedicação pela Squad FAMT.
</p>
