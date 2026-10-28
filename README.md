# 🍹 API Python com Flask & SQLAlchemy

Esta é uma API RESTful simples desenvolvida em Python utilizando o framework **Flask** e o **Flask-SQLAlchemy** para persistência de dados em um banco de dados **SQLite**. O projeto permite gerenciar uma lista de bebidas (drinks), realizando operações básicas de leitura, criação e exclusão.

O projeto foi desenvolvido como parte de um estudo prático de desenvolvimento de APIs e manipulação de banco de dados relacional.

## 🚀 Tecnologias Utilizadas

* **Python 3.13+**
* **Flask** (Framework Web)
* **Flask-SQLAlchemy** (ORM para integração com Banco de Dados)
* **SQLite** (Banco de dados relacional local)

## 📌 Rotas da API

A API possui os seguintes endpoints configurados:

| Método | Rota | Descrição |
| :--- | :--- | :--- |
| **GET** | `/` | Retorna uma mensagem simples de boas-vindas. |
| **GET** | `/drinks` | Retorna a lista completa de todos os drinks cadastrados no banco. |
| **GET** | `/drinks/<id>` | Retorna os detalhes de um drink específico com base no ID enviado. |
| **POST** | `/drinks` | Cadastra um novo drink enviando um JSON com `name` e `description`. |
| **DELETE** | `/drink/<id>` | Remove um drink do banco de dados com base no ID enviado. |

---

## 💻 Como Executar o Projeto Localmente

### 1. Clonar o repositório
```bash
git clone https://github.com
cd API-Python
```

### 2. Criar e ativar o ambiente virtual (venv)
No macOS/Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Instalar as dependências
*(Gere o arquivo `requirements.txt` no projeto principal para que este comando funcione)*
```bash
pip install -r requirements.txt
```

### 4. Criar o Banco de Dados (Via Flask Shell)
Abra o console interativo do Flask para gerar as tabelas do SQLite:
```bash
flask --app application.py shell
```
Dentro do terminal interativo (`>>>`), execute:
```python
from application import db
db.create_all()
exit()
```

### 5. Rodar o Servidor de Desenvolvimento
Inicie o Flask especificando a porta livre no Mac:
```bash
flask --app application.py --debug run --port 8080
```
O servidor estará rodando em: `http://127.0.0.1:8080`

---
🔒 *Nota: Os arquivos de banco de dados (`data.db`) e a pasta do ambiente virtual (`venv`) foram intencionalmente adicionados ao `.gitignore` para manter as credenciais e dados de teste locais seguros.*
