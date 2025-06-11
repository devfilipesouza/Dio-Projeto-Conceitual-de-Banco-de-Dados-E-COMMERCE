# Modelagem de Banco de Dados para E-commerce (Desafio DIO)

![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)
![Tecnologia](https://img.shields.io/badge/Tecnologia-SQL-blue)
![Ferramenta](https://img.shields.io/badge/Ferramenta-MySQL%20Workbench-orange)

Projeto de modelagem de banco de dados desenvolvido como parte do desafio "Construa um Projeto Lógico de Banco de Dados do Zero" da [Digital Innovation One (DIO)](https://www.dio.me/).

---

## 📋 Índice

- [Sobre o Projeto](#-sobre-o-projeto)
- [O Esquema Conceitual](#-o-esquema-conceitual)
- [O Esquema Lógico (SQL)](#-o-esquema-lógico-sql)
- [Entidades Modeladas](#-entidades-modeladas)
- [Como Utilizar](#-como-utilizar)
- [Ferramentas e Tecnologias](#️-ferramentas-e-tecnologias)
- [Contato](#-contato)

---

## 🧐 Sobre o Projeto

O objetivo deste desafio foi criar um esquema de banco de dados completo para um **sistema de e-commerce**, partindo do zero. O processo envolveu a criação do **modelo conceitual**, que define as entidades, seus atributos e os relacionamentos, seguido pela construção do **modelo lógico** com o script SQL para a criação das tabelas.

Este projeto visa demonstrar as habilidades em modelagem de dados relacionais, normalização e a tradução de requisitos de negócio em uma estrutura de banco de dados funcional e coesa.

---

## 🎨 O Esquema Conceitual

O modelo entidade-relacionamento (MER) foi desenhado para representar visualmente a estrutura do banco de dados. O esquema abaixo é a versão final e refinada do modelo.

![Esquema E-COMMERCE Refinado](https://raw.githubusercontent.com/devfilipesouza/Dio-Projeto-Conceitual-de-Banco-de-Dados-E-COMMERCE/main/E-COMMERCE_refinado.png)

---

## 💻 O Esquema Lógico (SQL)

A partir do modelo conceitual, foi gerado um script SQL (`dio-ecommerce.sql`) contendo as instruções `CREATE TABLE` para todas as entidades, incluindo a definição de chaves primárias (PK), chaves estrangeiras (FK) e as restrições necessárias para garantir a integridade dos dados.

**Exemplo de uma das queries do script:**
```sql
-- Tabela Cliente
CREATE TABLE clients(
    idClient INT AUTO_INCREMENT PRIMARY KEY,
    Fname VARCHAR(15),
    Minit CHAR(3),
    Lname VARCHAR(20),
    CPF CHAR(11) NOT NULL,
    Address VARCHAR(255),
    CONSTRAINT unique_cpf_client UNIQUE (CPF)
);
```

---

## 📦 Entidades Modeladas

As principais entidades que compõem este sistema de e-commerce são:

- **Clients** (Clientes)
- **Product** (Produtos)
- **Orders** (Pedidos)
- **Supplier** (Fornecedores)
- **Seller** (Vendedores Terceiros)
- **ProductStorage** (Estoque)
- **Payments** (Formas de Pagamento)
- E as tabelas de relacionamento para estruturas N:M (muitos para muitos).

---

## 🚀 Como Utilizar

Para visualizar ou recriar este banco de dados em seu ambiente local, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/devfilipesouza/Dio-Projeto-Conceitual-de-Banco-de-Dados-E-COMMERCE.git](https://github.com/devfilipesouza/Dio-Projeto-Conceitual-de-Banco-de-Dados-E-COMMERCE.git)
    ```
2.  **Abra os arquivos de imagem** (`.png`) para visualizar o modelo conceitual em qualquer visualizador de imagens.

3.  **Execute o script SQL:**
    - Abra o arquivo `dio-ecommerce.sql` em um cliente de banco de dados que suporte MySQL (como MySQL Workbench, DBeaver, etc.).
    - Execute o script para criar todas as tabelas e relacionamentos em seu banco de dados.

---

## 🛠️ Ferramentas e Tecnologias

- **MySQL Workbench:** Utilizado para a modelagem do diagrama ER e para a geração do script SQL.
- **SQL:** Linguagem de definição de dados (DDL) para a criação do esquema lógico.
- **Git & GitHub:** Para controle de versão e compartilhamento do projeto.

---

## 📬 Contato

**Filipe Souza**
- **GitHub:** [devfilipesouza](https://github.com/devfilipesouza)
