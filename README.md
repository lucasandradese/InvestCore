# Sobre o projeto

## 📈 InvestCore

**InvestCore** é uma FULL STACK para gerenciamento de carteira de investimentos focando em ações, permitindo o controle de operações (compra e venda), cálculo de posição atual, dividendos recebidos e rentabilidade do investidor.

**Projeto criado em arquitetura em camadas para modelagem financeira**

---

## Funcionalidades

- 👤 Gestão de usuários
- 📊 Cadastro de ativos (ações)
- 🔁 Registro de operações (BUY / SELL)
- 💰 Controle de dividendos por ativo
- 🧮 Cálculo automático de:
  - Posição atual da carteira
  - Custo médio
  - Lucro / prejuízo realizado
  - Dividendos recebidos
  - Valor patrimonial (mark-to-market)
- 📈 Relatórios financeiros por período

## Layout ER do projeto
<img width="838" height="473" alt="image" src="https://github.com/user-attachments/assets/a396e163-09a5-4ad3-8614-6f5a3fb1968f" />

---

## ⚙️ BackEnd

### Modelagem do Domínio

Principais entidades:

- **User**
- **Stock**
- **Transaction**
- **TransactionType**
- **DividendByStock**
- **DividendReceived**
- **Sector**
- **StockType**
- **EventType**

A relação N:N entre usuários e ativos é resolvida através da entidade **Transaction**, garantindo histórico completo e rastreável.

---

### 🏗️ Arquitetura

- Arquitetura em camadas:
  - Controller
  - Service
  - Repository
- Separação clara entre:
  - Entidades
  - DTOs / Projections
  - Regras de negócio
- Consultas financeiras complexas isoladas no repositório

---

### Tecnologias Utilizadas

- **Java**
- **Spring Boot**
- **Spring Data JPA**
- **Hibernate**
- **PostgreSQL**
- **Docker**
- **Maven**
- **Lombok**
- **JUnit 5**
- **HATEOAS**

---

### Consultas Avançadas Implementadas

- 📌 Posição atual da carteira
- 📌 Custo médio por ativo
- 📌 Lucro / prejuízo realizado
- 📌 Dividendos recebidos (total e por período)
- 📌 Valor patrimonial atual da carteira

As consultas utilizam:
- JPQL
- Native Queries
- Projections (DTOs)

---
```TEXT
📦 Estrutura de Pacotes

com.investcore
 ├── controller
 ├── service
 ├── repository
 ├── domain
 │   ├── entity
 │   ├── enum
 │   └── dto
 ├── config
 └── exception

⚙️ Configuração do Projeto
Pré-requisitos
•	Java 21+
•	Maven
•	PostgreSQL
Banco de dados

Crie o banco:

CREATE DATABASE investcore;
Configure o application.yml ou application.properties:
spring.datasource.url=jdbc:postgresql://localhost:5432/investcore
spring.datasource.username=postgres
spring.datasource.password=postgres

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
________________________________________

▶️ Executando o projeto
mvn clean install
mvn spring-boot:run
A API estará disponível em:
http://localhost:8080
________________________________________

📌 Exemplos de Endpoints (futuros)
GET /api/portfolio/{userId}
GET /api/portfolio/{userId}/profit
GET /api/portfolio/{userId}/dividends
GET /api/stocks
POST /api/transactions
________________________________________

🧪 Testes
•	Testes de serviço focados em regras financeiras
________________________________________
```
## 🖥️ Front End web

- iniciar o front quando completar a estrutura do banckend.


### Motivos para criação do projeto 

🎯 Objetivo do Projeto

- Resolução do problema:
  
  - Gestão dos investimentos em ações em uma única sistema
  - Projetar uma cultura de investimento em ações
  - Prever movimentações (ganho de dividendos, JCP e bonificações) para cada ação na carteira de investimento
  - Aplicar modelagem de dados com base nas movimentações financeira do cliente

- Técnica e Profissional:
  
  - Estudo de pré requisito com base na regra de negócio
  - Demonstrar domínio em JAVA com Spring Boot
  - Demonstrar domínio de consultas Queries mais avançada
  - Aprimorar conhecimento em tecnologia com Docker e AWS
  - Servir como projeto de portfólio profissional
________________________________________

## Autor
**Lucas Andrade**
  - Desenvolvedor Java | Spring Boot | APIs REST
________________________________________

📄 Licença
 Este projeto está sob a licença MIT.

