

<div align="center">
  <h1>DataOps Mini Lab</h1>
  <p>Pipeline local de ingestão de pedidos com Python, Pandas e DuckDB</p>
</div>

---

## Contexto

Este laboratório propõe a construção de um pipeline de dados simples para ingestão diária de pedidos em CSV, armazenamento em DuckDB e consulta analítica inicial. O objetivo é criar uma base funcional para evoluir com práticas de DataOps como rastreabilidade, rollback, contratos de dados e governança.

---

## Estrutura do Projeto

```
data-ops/
├── data/
│   ├── raw/
│   │   └── orders_2026_03_23.csv
│   └── curated/
├── ingestion/
│   └── load_orders.py
├── warehouse/
│   └── local.duckdb
├── docs/
├── .gitignore
├── README.md
```

---

## Tecnologias Utilizadas

- Python 3.11+
- pandas
- DuckDB
- Git
- VS Code ou editor equivalente

---

## Como Executar

### Prática 1
1. **Crie e ative o ambiente virtual:**
	```bash
	python -m venv .venv
	source .venv/bin/activate  # Linux/Mac
	# .venv\Scripts\activate  # Windows
	python -m pip install --upgrade pip
	```
2. **Instale as dependências:**
	```bash
	pip install pandas duckdb
	```
3. **Execute o pipeline:**
	```bash
	python ingestion/load_orders.py
	```

---

### Prática 2 — Pipeline com Temporal e MongoDB Atlas

1. **Crie e ative o ambiente virtual:**
	```bash
	python -m venv .venv
	source .venv/bin/activate  # Linux/Mac
	# .venv\Scripts\activate  # Windows
	python -m pip install --upgrade pip
	```
2. **Instale as dependências:**
	```bash
	pip install -r requirements.txt
	```
3. **Configure o MongoDB Atlas:**
	- Crie um cluster gratuito no Atlas, adicione seu IP na IP Access List, crie um usuário e copie a connection string.
	- Preencha o arquivo `.env` na raiz do projeto:
	  ```
	  MONGODB_URI=mongodb+srv://SEU_USUARIO:SUA_SENHA@SEU_CLUSTER.mongodb.net/?retryWrites=true&w=majority
	  MONGODB_DATABASE=dataops_lab
	  MONGODB_COLLECTION=orders_raw
	  ```
4. **Suba o servidor Temporal local:**
	```bash
	temporal server start-dev
	```
	- Acesse a UI em http://localhost:8233
5. **Rode o worker em outro terminal:**
	```bash
	python -m app.worker
	```
6. **Dispare o workflow em outro terminal:**
	```bash
	python -m app.run_workflow
	```
7. **Valide a execução:**
	- Veja o resultado no terminal, confira a UI do Temporal e os dados no MongoDB Atlas.

---

Para respostas conceituais da prática 2, veja `docs/pratica2.md`.
	```

---

## Evidências de Execução

### Pratica 1:

### 1. Execução do Script
![Execução do script de ingestão](docs/images/script-rodando.png)

### 2. Commit no Git
![Histórico do Git](docs/images/commit.png)

### 3. Estrutura do Projeto
![Estrutura de pastas e arquivos](docs/images/estrutura.png)

### Prática 2:

### 1. Execução do Workflow
![Execução do workflow](docs/images/workflow-rodando.png)

### 2. Commit no Git
![Histórico do Git](docs/images/commit2.png)
---

## Reflexões Finais

As respostas da reflexão final estão disponíveis em:

- Reflexão Final da Prática 1: [docs/pratica1.md](docs/pratica1.md).
