# 🧪 Store API — FastAPI com TDD

## 💬 Minha Experiência

Este projeto foi desenvolvido durante o bootcamp BackEnd com Pytho da DIO como meu **primeiro contato com FastAPI e TDD**. Achei o tema bem desafiador no início, especialmente por envolver testes automatizados — algo novo pra mim.

Apesar disso, consegui absorver os conceitos principais de **Test Driven Development** e entendi melhor como construir uma API testável e estruturada. Foi um aprendizado valioso!

---

## 🚀 Sobre o projeto

A **Store API** é uma API educativa construída com FastAPI, MongoDB e Pytest, com foco na prática do TDD. A proposta era entender como estruturar testes unitários e de integração desde o início do desenvolvimento.

### 🛠 Tecnologias e ferramentas
- **FastAPI**
- **MongoDB (Motor)**
- **Pydantic**
- **Pytest**
- **Poetry + Pyenv**

---

## 🧪 TDD: Test Driven Development

O TDD segue um ciclo simples:
1. Escreva um **teste** que falha.
2. Escreva o **código** mínimo para passar no teste.
3. **Refatore** o código mantendo os testes verdes.

### Por que TDD?
- Mais qualidade no código
- Menos chances de bugs
- Força o foco no comportamento esperado
- Evita escrever código desnecessário

---

## 🗂 Funcionalidades da API

A API permite realizar operações básicas com produtos:
- Criar (`POST /products`)
- Listar (`GET /products`)
- Detalhar (`GET /products/{id}`)
- Atualizar (`PUT /products/{id}`)
- Excluir (`DELETE /products/{id}`)

---

## 🔍 Exemplos de Fluxo

### ➕ Criar Produto
```mermaid
sequenceDiagram
Client->>+API: POST /products
API->>API: Valida Body
API->>+DB: Cria Produto
DB->>-API: OK
API->>-Client: 201 Created
