**💰 FAMT Control — Aplicativo de Controle de Gastos Pessoais**

> **Documentação Oficial do Repositório e Guia de Execução**  
> *Engenharia de Software e Gestão Híbrida de Projetos (Waterfall + Scrum)*  
> **Universidade de Mogi das Cruzes (UMC)** — Semestre 2026/2  
> **Orientador:** Prof. Renato  

👥 Squad FAMT e Atribuições
Integrante |	Matrícula (RA) |	Papel Técnico | 	Atribuições Principais
Franciellen Moreira Santos |	11261403634 |	Gerente de Projetos (PM) |	Coordenação geral, cronograma CPM, documentação TAP/EAP e matriz de comunicação.
Maria Augusta S. Toledo |	11241102057 |	Product Owner (PO) / QA |	Priorização do Backlog, aceite de User Stories, BDD e suíte de testes com Pytest.
André Mitchel Ruiz Santos |	11231102531 |	Tech Lead / Dev Backend & UI |	Arquitetura Python/Streamlit, motor contábil, gráficos Plotly e segurança.
Thamirys Matos da Silva |	11261403155 |	Engenheira de Dados (DBA) | 	Modelagem relacional em 3FN, criação do schema relacional, constraints e índices.

---
📌 Visão Geral do Projeto
O FAMT Control foi concebido para resolver a desorganização financeira e a falta de controle sistemático de receitas e despesas entre estudantes universitários e jovens profissionais. Em vez de planilhas complexas ou anotações informais, o sistema oferece um aplicativo web enxuto, responsivo, seguro e intuitivo.
🌟 Valor Gerado
Centralização Contábil: Registro simplificado de transações com cálculo imediato do saldo consolidado.
Análise Visual Interativa: Gráficos dinâmicos de distribuição de gastos por categoria e histórico de movimentações.
Segurança e LGPD: Proteção de dados através de hashing seguro SHA-256 e validação contábil em tempo real.
---
🏗️ Arquitetura do Sistema
O sistema foi desenvolvido em Python, estruturado em arquitetura modular desacoplada em três camadas:
Interface de Usuário (UI): Streamlit com customização visual e gráficos Plotly.
Camada de Negócio e Regras: Motor contábil em Python, validações de saldo e alerta de saldo devedor.
Camada de Persistência: Banco de dados relacional (SQLite v2 / MySQL).
---
🎯 Funcionalidades e Priorização (Matriz MoSCoW)
🔴 Must Have (Obrigatório / Escopo do MVP)
Cadastro de Receitas e Despesas: Lançamentos com valor, data, descrição e tipo.
Categorização Padronizada: Classificação entre Alimentação, Transporte, Lazer, Saúde, Educação, Moradia e Outros.
Cálculo Automático de Saldo: Atualização dinâmica de receitas, despesas e saldo líquido.
Extrato e Histórico: Visualização de lançamentos com ordenação e busca.
Alerta Contábil por Saldo Devedor: Aviso automático em caso de balanço negativo.
Segurança de Acesso: Criptografia SHA-256 para senhas e conformidade com LGPD.
🟡 Should Have (Desejável)
Painel de Métricas (Dashboard): Cards com indicadores de desempenho financeiro.
Atalhos Rápidos na Home: Ações de lançamento ágil na página principal.
Filtro Avançado de Extrato: Filtragem por intervalo de datas e categoria.
🟢 Could Have (Opcional)
Simulador de Economia Mensal: Cálculo de metas de reserva financeira.
Exportação de Dados: Download do extrato consolidado.
⚪ Won't Have (Fora do Escopo)
Integração direta via Open Finance ou APIs bancárias reais.
Aplicativo móvel nativo (Android/iOS) ou gateway de pagamento.
---
📊 Governança e Metodologia Híbrida
O desenvolvimento do FAMT Control combina o rigor do modelo Waterfall (PMI/PMBOK) na fase de concepção e planejamento com a flexibilidade do Scrum durante a execução.
Fases Waterfall: Termo de Abertura (TAP), EAP/WBS, Dicionário da EAP, Cronograma PDM, Caminho Crítico, Matriz PxI e Matriz RACI.
Execução Scrum: Product Backlog, User Stories (US-001 a US-006), BDD, Definition of Done (DoD) e Definition of Ready (DoR), Kanban e Burndown.
📈 Indicadores Financeiros do Projeto
Orçamento Previsto (BAC): R$ 12.454,50
Linha de Base de Custos: R$ 11.913,00
Reserva de Contingência (Riscos): R$ 541,50
Prazo Total: 21 dias úteis / 4 Sprints semanais
---
📂 Estrutura de Diretórios do Repositório
```
FAMT-Control/
├── app.py                      # Aplicação principal web em Streamlit (UI / Dashboard)
├── famt_db_manager.py          # Gerenciador do Banco de Dados e Conexão (Persistência)
├── famt_db_helper.py           # Funções auxiliares de consulta contábil e filtros
├── famt_control_schema.sql     # Script SQL DDL de criação das tabelas e relacionamentos
├── requirements.txt            # Lista de dependências Python
├── README.md                   # Documentação oficial do projeto
├── docs/                       # Documentações de Engenharia e Gestão do Projeto
│   ├── famt-control-documento-completo-projeto-m1.docx
│   ├── famt-control-relatorio-qualidade-comunicacao-stakeholders.docx
│   └── famt-control-relatorio-transicao-waterfall-scrum.docx
└── tests/                      # Suíte de testes unitários e de integração
    └── test_famt_control.py
```
---        
🛠️ Como Instalar e Executar Localmente
Passo a Passo
Acessar o diretório do projeto:
```bash
   cd FAMT-Control
   ```
Criar e ativar o ambiente virtual (.venv):
```bash
   python -m venv .venv
   source .venv/bin/activate   # No Windows: .venv\Scripts\activate
   ```
Instalar as dependências:
```bash
   pip install -r requirements.txt
   ```
Executar a aplicação Streamlit:
```bash
   streamlit run app.py
   ```
---
**🧪 Qualidade e Testes**

A qualidade do software é validada conforme as diretrizes da norma ISO/IEC 25010 e executada via Pytest:
```bash
pytest -v
```
---
**📄 Licença e Direitos Autorais**

Desenvolvido pela Squad FAMT para a disciplina de Gestão de Projetos de Software do Curso de Engenharia de Software da Universidade de Mogi das Cruzes (UMC).
© 2026 Squad FAMT. Todos os direitos reservados.
