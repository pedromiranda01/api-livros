# Sistemas Web II — Aulas e Materiais

Repositório da disciplina de **Sistemas Web II (SW-II)**, reunindo aulas, exemplos de código, atividades práticas, exercícios e materiais utilizados durante o ano letivo de 2026.

O conteúdo do repositório acompanha a evolução do desenvolvimento de APIs, começando pelos fundamentos de APIs REST e PHP, passando pela construção de APIs com Python e FastAPI, persistência com MySQL e SQLAlchemy, e chegando a testes, integração com frontend e conceitos de arquitetura de software.

---

## 📚 Conteúdo da disciplina

### 1º Bimestre — APIs REST com PHP

Neste bimestre são apresentados os fundamentos necessários para compreender o funcionamento de APIs e a comunicação entre sistemas.

Principais assuntos:

- Fundamentos de desenvolvimento Web;
- APIs e APIs REST;
- Métodos HTTP;
- Requisições e respostas;
- Variáveis e operadores em PHP;
- Formulários e recebimento de dados;
- Manipulação de dados em PHP;
- JSON (JavaScript Object Notation);
- Criação de APIs utilizando PHP puro;
- Endpoints;
- Parâmetros em requisições;
- Exemplos práticos de operações GET e manipulação de dados.

**Materiais:** [`aulas/1 BIMESTRE/api_exemplo`](aulas/1%20BIMESTRE/api_exemplo/)

---

### 2º Bimestre — FastAPI e CRUD em Python

O segundo bimestre inicia a construção de APIs utilizando Python e o framework FastAPI.

Principais assuntos:

- Introdução ao Python para desenvolvimento de APIs;
- Criação de ambientes virtuais (`venv`);
- Instalação e gerenciamento de dependências;
- FastAPI;
- Rotas e endpoints;
- Método GET;
- Método POST;
- Método PUT;
- Método DELETE;
- Pydantic;
- Validação de dados;
- CRUD em memória;
- Swagger UI e documentação automática;
- Introdução à persistência de dados;
- MySQL;
- SQLAlchemy;
- ORM (Object-Relational Mapping);
- Conexão entre FastAPI e banco de dados.

**Materiais:** [`aulas/2 BIMESTRE`](aulas/2%20BIMESTRE/)

---

### 3º Bimestre — API com MySQL, CRUD, Frontend e Testes

No terceiro bimestre os conhecimentos anteriores são aprofundados, trabalhando com APIs conectadas a banco de dados real e práticas de desenvolvimento mais próximas de um projeto completo.

Principais assuntos:

- Revisão de APIs REST e FastAPI;
- Python aplicado ao desenvolvimento Web;
- FastAPI com MySQL;
- SQLAlchemy;
- Modelos ORM;
- Schemas com Pydantic;
- CRUD completo;
- GET por ID;
- POST;
- PUT;
- DELETE;
- Commit e persistência das alterações;
- CORS;
- Integração com frontend;
- Testes unitários;
- `unittest.mock`;
- `MagicMock`;
- `dependency_overrides`;
- Pytest;
- Arquitetura de software em camadas;
- Organização e documentação de projetos.

**Materiais:** [`aulas/3 BIMESTRE`](aulas/3%20BIMESTRE/)

---

## 🗂️ Estrutura do repositório

```text
SW-II_2026/
│
├── README.md
├── Bases SW-II.pdf
│
└── aulas/
    │
    ├── 1 BIMESTRE/
    │   └── api_exemplo/
    │       ├── aulas em PDF
    │       ├── atividades
    │       ├── API REST em PHP
    │       └── exemplos/
    │
    ├── 2 BIMESTRE/
    │   ├── Aula 01 - API com Python
    │   ├── Aula 02 - Dependências, Validação e CRUD
    │   ├── Aula 03 - Atividade Prática
    │   └── Aula 04 - MySQL e SQLAlchemy
    │
    └── 3 BIMESTRE/
        ├── revisão FastAPI
        ├── exercícios práticos
        ├── integração com frontend
        ├── CRUD com MySQL
        ├── testes unitários
        ├── guias de Pytest
        ├── arquitetura em camadas
        └── notas técnicas
```

---

## 🛠️ Tecnologias utilizadas

### Backend

- **Python**
- **FastAPI**
- **Pydantic**
- **SQLAlchemy**
- **PyMySQL**

### Banco de dados

- **MySQL**
- **phpMyAdmin** para administração do banco durante as atividades

### Desenvolvimento e testes

- **Visual Studio Code**
- **Swagger / OpenAPI**
- **Pytest**
- **unittest.mock**
- **Git e GitHub**

### Frontend

- **HTML**
- **CSS**
- **JavaScript**

---

## 🚀 Preparação do ambiente Python

Para executar os exemplos das aulas que utilizam FastAPI, recomenda-se utilizar Python 3.11 ou superior.

### 1. Criar o ambiente virtual

```bash
python -m venv .venv
```

### 2. Ativar o ambiente virtual no Windows

```bash
.venv\Scripts\activate
```

### 3. Instalar as dependências

Exemplo:

```bash
pip install fastapi uvicorn sqlalchemy pymysql pydantic-settings python-dotenv
```

Para as aulas de testes:

```bash
pip install pytest
```

---

## ▶️ Executando uma API FastAPI

Depois de entrar na pasta do projeto e ativar o ambiente virtual:

```bash
uvicorn main:app --reload
```

Caso o arquivo principal esteja dentro de uma estrutura como `app/main.py`:

```bash
uvicorn app.main:app --reload
```

A API poderá ser acessada pelo endereço local indicado pelo Uvicorn.

A documentação automática do FastAPI pode ser acessada em:

```text
/docs
```

Também existe a documentação alternativa:

```text
/redoc
```

---

## 🗄️ MySQL

Nas aulas que utilizam persistência real, a API é conectada a um banco de dados MySQL.

O ambiente pode ser preparado utilizando ferramentas como:

- XAMPP;
- MySQL;
- phpMyAdmin;
- DBeaver.

Antes de executar uma API que depende do MySQL, é necessário verificar se o servidor do banco está em execução e se as configurações de conexão estão corretas.

---

## 🔄 Conceito de CRUD

Grande parte das atividades trabalha com o conceito de CRUD:

| Operação | Método HTTP | Função |
|---|---|---|
| Create | `POST` | Criar um registro |
| Read | `GET` | Consultar registros |
| Update | `PUT` | Atualizar um registro |
| Delete | `DELETE` | Excluir um registro |

Exemplo de organização de endpoints:

```text
GET     /produtos
GET     /produtos/{id}
POST    /produtos
PUT     /produtos/{id}
DELETE  /produtos/{id}
```

---

## 🧪 Testes

As aulas do terceiro bimestre também introduzem testes unitários para APIs FastAPI.

Entre os conceitos trabalhados estão:

- Testes de endpoints;
- Pytest;
- `MagicMock`;
- Simulação de sessões do SQLAlchemy;
- `dependency_overrides`;
- Testes de GET;
- Testes de POST;
- Separação entre teste unitário e banco de dados real.

A ideia é permitir que determinadas partes da API sejam testadas sem depender diretamente de uma conexão real com o MySQL.

---

## 🌐 Integração com Frontend

Também são apresentados exemplos de integração entre uma API FastAPI e uma página frontend simples.

O frontend pode realizar requisições HTTP para a API utilizando JavaScript, permitindo:

- Consultar dados;
- Exibir registros;
- Enviar informações;
- Integrar formulários;
- Trabalhar com respostas em JSON.

Para permitir a comunicação entre origens diferentes, é apresentado o conceito de **CORS (Cross-Origin Resource Sharing)**.

---

## 🏗️ Arquitetura de software

O repositório também contém material sobre **arquitetura de software em camadas**, mostrando como organizar melhor uma aplicação.

Uma aplicação pode ser dividida, por exemplo, em:

```text
Frontend
   ↓
API / Rotas
   ↓
Regras de negócio
   ↓
Acesso aos dados
   ↓
Banco de dados
```

Essa organização facilita a manutenção, compreensão e evolução do projeto.

---

## 🎯 Objetivos de aprendizagem

Ao longo das aulas, o objetivo é desenvolver conhecimentos para:

- Compreender o funcionamento de APIs;
- Utilizar corretamente os métodos HTTP;
- Criar endpoints REST;
- Desenvolver APIs com Python e FastAPI;
- Validar dados utilizando Pydantic;
- Implementar operações CRUD;
- Trabalhar com MySQL;
- Utilizar SQLAlchemy como ORM;
- Integrar APIs com páginas frontend;
- Criar testes automatizados;
- Compreender conceitos básicos de arquitetura de software;
- Organizar projetos utilizando boas práticas de desenvolvimento.

---

## 📖 Organização dos materiais

O repositório foi organizado por bimestre para facilitar a consulta das aulas:

**1º Bimestre:** fundamentos, PHP e APIs REST.

**2º Bimestre:** Python, FastAPI, validação e CRUD.

**3º Bimestre:** MySQL, SQLAlchemy, CRUD completo, frontend, testes e arquitetura.

Os arquivos PDF apresentam o conteúdo das aulas, enquanto os arquivos de código e atividades servem como exemplos e exercícios práticos.

---

## 👨‍🏫 Professor

**Anderson Silva Vanin**

Componente Curricular: **Sistemas Web II**

---

## 📌 Observação

Este repositório possui finalidade educacional e reúne materiais desenvolvidos e utilizados durante as aulas de Sistemas Web II em 2026.

Os exemplos devem ser utilizados como apoio ao aprendizado e podem precisar de adaptações de acordo com o ambiente, sistema operacional, versões das bibliotecas e configurações do banco de dados.