# 💰 FAMT Control — Aplicativo de Controle de Gastos Pessoais

> **Documentação Oficial do Projeto e Guia de Execução**
>
> Projeto desenvolvido para as disciplinas de Engenharia de Software e Gestão Híbrida de Projetos (Waterfall + Scrum).
>
> **Universidade de Mogi das Cruzes (UMC)**  
> **Semestre:** 2026/2  
> **Orientador:** Prof. Renato

---

## 📌 Sobre o Projeto

O **FAMT Control** é um aplicativo web desenvolvido com o objetivo de facilitar a organização e o controle das finanças pessoais, especialmente para estudantes universitários e jovens profissionais.

A proposta é oferecer uma ferramenta simples, intuitiva e acessível, permitindo que os usuários registrem suas receitas e despesas, acompanhem seu saldo financeiro e visualizem suas movimentações por meio de gráficos e indicadores.

Diferentemente de planilhas complexas ou anotações manuais, o sistema centraliza as informações financeiras em uma única plataforma, proporcionando uma visão mais clara da situação financeira do usuário.

### 🌟 Principais benefícios

- **Centralização financeira:** registro e acompanhamento de receitas e despesas em um único ambiente.
- **Controle de saldo:** cálculo automático do saldo disponível.
- **Análise visual:** gráficos interativos para facilitar a compreensão dos gastos.
- **Organização:** categorização das movimentações financeiras.
- **Segurança:** mecanismos de proteção de acesso e tratamento dos dados dos usuários.

---

## 👥 Squad FAMT e Atribuições

| Integrante | Matrícula (RA) | Papel | Principais atribuições |
|---|---|---|---|
| Franciellen Moreira Santos | 11261403634 | Gerente de Projetos (PM) | Coordenação geral, cronograma CPM, documentação TAP/EAP e matriz de comunicação. |
| Maria Augusta S. Toledo | 11241102057 | Product Owner (PO) / QA | Priorização do Backlog, aceite de User Stories, BDD e testes com Pytest. |
| André Mitchel Ruiz Santos | 11231102531 | Tech Lead / Desenvolvedor | Arquitetura Python/Streamlit, regras de negócio, gráficos Plotly e segurança. |
| Thamirys Matos da Silva | 11261403155 | Engenheira de Dados (DBA) | Modelagem relacional em 3FN, estrutura do banco de dados, constraints e índices. |

---

## 🏗️ Arquitetura do Sistema

O FAMT Control foi desenvolvido em **Python**, utilizando uma arquitetura modular organizada em três camadas principais:

| Camada | Tecnologia / Responsabilidade |
|---|---|
| Interface de Usuário (UI) | Streamlit, responsável pela interface e visualização dos dados. |
| Regras de Negócio | Python, responsável pelos cálculos financeiros, validações e regras contábeis. |
| Persistência de Dados | SQLite, responsável pelo armazenamento e gerenciamento das informações. |

A separação dessas responsabilidades facilita a manutenção, a organização e a evolução do sistema.

---

## 🎯 Funcionalidades e Priorização — Matriz MoSCoW

A priorização das funcionalidades foi realizada utilizando a técnica MoSCoW, que organiza os requisitos de acordo com sua importância para o projeto.

### 🔴 Must Have — Obrigatórias

- Cadastro de receitas e despesas, com valor, data, descrição e tipo.
- Categorização de movimentações: Alimentação, Transporte, Lazer, Saúde, Educação, Moradia e Outros.
- Cálculo automático de receitas, despesas e saldo líquido.
- Extrato e histórico de movimentações.
- Alerta automático para situações de saldo negativo.
- Controle de acesso e proteção das informações dos usuários.

### 🟡 Should Have — Desejáveis

- Dashboard com indicadores financeiros.
- Atalhos rápidos para lançamento de movimentações.
- Filtros de extrato por período e categoria.

### 🟢 Could Have — Opcionais

- Simulador de economia mensal.
- Criação e acompanhamento de metas financeiras.
- Exportação de dados e extratos.

### ⚪ Won't Have — Fora do Escopo

- Integração direta com Open Finance ou APIs bancárias reais.
- Aplicativo móvel nativo para Android e iOS.
- Gateway de pagamentos.

---

## 📊 Governança e Metodologia Híbrida

O desenvolvimento do FAMT Control combina duas abordagens de gerenciamento de projetos: **Waterfall (Cascata)** e **Scrum**, buscando unir planejamento estruturado e flexibilidade durante a execução.

### Etapa 1 — Planejamento Waterfall

Foram utilizados instrumentos de gerenciamento baseados nas práticas do PMI/PMBOK:

- Termo de Abertura do Projeto (TAP).
- Estrutura Analítica do Projeto (EAP/WBS).
- Dicionário da EAP.
- Cronograma PDM.
- Análise do Caminho Crítico (CPM).
- Matriz de Probabilidade e Impacto (PxI).
- Matriz RACI.

### Etapa 2 — Execução Scrum

Na execução, foram utilizados os seguintes artefatos e práticas:

- Product Backlog.
- User Stories (US-001 a US-006).
- BDD (Behavior Driven Development).
- Definition of Done (DoD).
- Definition of Ready (DoR).
- Quadro Kanban.
- Gráfico Burndown.

### 📈 Indicadores Financeiros e Prazo do Projeto

| Indicador | Valor |
|---|---:|
| Orçamento Previsto (BAC) | R$ 12.454,50 |
| Linha de Base de Custos | R$ 11.913,00 |
| Reserva de Contingência | R$ 541,50 |
| Prazo total | 21 dias úteis |
| Planejamento de execução | 4 Sprints semanais |

---

## 📂 Estrutura de Diretórios

O repositório está organizado da seguinte maneira:

```text
FAMT-Control/
│
├── app.py
├── famt_db_manager.py
├── famt_db_helper.py
├── famt_control_schema.sql
├── requirements.txt
├── README.md
│
├── docs/
│   ├── famt-control-documento-completo-projeto-m1.docx
│   ├── famt-control-relatorio-qualidade-comunicacao-stakeholders.docx
│   └── famt-control-relatorio-transicao-waterfall-scrum.docx
│
└── tests/
    └── test_famt_control.py
```

### Descrição dos principais arquivos

| Arquivo | Descrição |
|---|---|
| `app.py` | Aplicação principal desenvolvida com Streamlit. |
| `famt_db_manager.py` | Gerenciamento da conexão e operações com o banco de dados. |
| `famt_db_helper.py` | Funções auxiliares para consultas, cálculos e filtros. |
| `famt_control_schema.sql` | Script SQL para criação da estrutura do banco de dados. |
| `requirements.txt` | Dependências necessárias para executar o projeto. |
| `tests/` | Diretório destinado aos testes automatizados. |
| `docs/` | Documentação técnica e gerencial do projeto. |

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Aplicação |
|---|---|
| Python | Linguagem principal de desenvolvimento. |
| Streamlit | Desenvolvimento da interface web. |
| SQLite | Banco de dados relacional. |
| SQL | Criação e gerenciamento da estrutura do banco de dados. |
| Plotly | Criação de gráficos e visualizações interativas. |
| Pytest | Testes automatizados. |
| Git e GitHub | Controle de versão e hospedagem do código. |

---

## 🚀 Como Instalar e Executar Localmente

Siga os passos abaixo para executar o FAMT Control em seu computador.

### 1. Clonar o repositório

```bash
git clone URL_DO_REPOSITORIO
```

### 2. Acessar a pasta do projeto

```bash
cd FAMT-Control
```

### 3. Criar um ambiente virtual

```bash
python -m venv .venv
```

### 4. Ativar o ambiente virtual

**Windows:**

```bash
.venv\Scripts\activate
```

**Linux / macOS:**

```bash
source .venv/bin/activate
```

### 5. Instalar as dependências

```bash
pip install -r requirements.txt
```

### 6. Executar a aplicação

```bash
streamlit run app.py
```

Após a execução, o Streamlit disponibilizará o endereço local para acessar a aplicação pelo navegador, geralmente:

```text
http://localhost:8501
```

---

## 🧪 Qualidade e Testes

A qualidade do FAMT Control é considerada durante o desenvolvimento e a validação das funcionalidades, tendo como referência os critérios da norma **ISO/IEC 25010**, que estabelece características para avaliação da qualidade de produtos de software.

Os testes automatizados são organizados utilizando o framework Pytest.

Para executar a suíte de testes, utilize:

```bash
pytest -v
```

O comando executa os testes e apresenta os resultados detalhados no terminal.

---

## 🔐 Segurança e Proteção de Dados

A segurança é um dos aspectos considerados no desenvolvimento do FAMT Control.

O projeto busca proteger as informações dos usuários por meio de mecanismos de controle de acesso, validação de dados e armazenamento seguro de credenciais.

**Observação técnica:** para o armazenamento de senhas, recomenda-se utilizar algoritmos específicos de hashing, como Argon2 ou bcrypt, em vez de SHA-256 isoladamente.

O tratamento das informações também deve observar os princípios e requisitos aplicáveis da Lei Geral de Proteção de Dados (LGPD).

---

## 📄 Licença e Direitos Autorais

Projeto desenvolvido pela **Squad FAMT** para as disciplinas de Engenharia de Software e Gestão de Projetos de Software do curso de Engenharia de Software da Universidade de Mogi das Cruzes (UMC).

© 2026 Squad FAMT. Todos os direitos reservados.

---

<p align="center">
  💜 <strong>FAMT Control</strong><br>
  <em>Organize suas finanças, conquiste seus sonhos.</em>
</p>
