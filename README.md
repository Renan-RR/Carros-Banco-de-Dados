# 🚗 Banco de Dados - Projeto de Carros

Este repositório contém um projeto de banco de dados em **MySQL**, desenvolvido com fins educacionais. Ele simula um sistema de gerenciamento de **clientes**, **marcas de automóveis** e um **inventário de modelos de carros**, permitindo praticar os principais comandos de criação, inserção e relacionamentos entre tabelas.

---

## 🗃️ Estrutura do Banco

O banco de dados se chama `carros` e possui três tabelas interligadas.

### 🔧 Tabelas criadas

#### 🏷️ `Marcas`
Armazena os fabricantes dos veículos.

- `ID` (PK)
- `Nome_Marca`
- `Origem`

#### 🚘 `Inventario`
Contém os modelos disponíveis, com informações técnicas e relação com a marca.

- `ID` (PK)
- `Modelo`
- `Ano`
- `Transmissão`
- `Motor`
- `Combustível`
- `Marcas_ID` (FK → Marcas.ID)

#### 👤 `Clientes`
Armazena informações básicas dos clientes cadastrados.

- `ID` (PK)
- `Nome`
- `Sobrenome`
- `Endereço`

---

## 🔗 Relacionamentos

- A tabela `Inventario` possui uma **chave estrangeira** (`Marcas_ID`) que referencia a tabela `Marcas`, criando um relacionamento de **1:N** (uma marca → vários modelos).

---

## 📦 Scripts incluídos

| Arquivo                | Descrição                                  |
|------------------------|--------------------------------------------|
| `criar_tabelas.sql`    | Script para criar as tabelas e relações    |
| `inserir_dados.sql`    | Inserção de registros nas três tabelas     |
| `README.md`            | Descrição do projeto                       |

---

## ✅ Comandos praticados

- `CREATE TABLE` com `PRIMARY KEY` e `FOREIGN KEY`
- `INSERT INTO` com múltiplas linhas
- Uso de **tipos de dados apropriados** (VARCHAR, INT)
- Organização relacional entre tabelas

---

## 💡 Observações

- Evite o erro `Error Code: 1136. Column count doesn't match value count at row...` certificando-se de que o número de colunas e de valores em `INSERT INTO` sejam iguais.
- Sempre utilize `FOREIGN KEY` para garantir a integridade dos dados entre tabelas relacionadas.

---

## 🎯 Objetivo

Este projeto foi criado com o objetivo de **consolidar conhecimentos em SQL** e servir como **portfólio de estudos em banco de dados relacional**.
