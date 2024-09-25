# Gerenciamento de Tarefas API

Este projeto é uma API RESTful desenvolvida com NestJS para gerenciar tarefas, projetos, usuários e atribuições de tarefas. A API inclui autenticação com JWT, validação de dados e está documentada com Swagger.

## Funcionalidades

- **CRUD de Usuários**: Gerenciamento de usuários, incluindo criação, leitura, atualização e exclusão.
- **CRUD de Projetos**: Gerenciamento de projetos com suporte a múltiplas tarefas.
- **CRUD de Tarefas**: Gerenciamento de tarefas associadas a projetos.
- **CRUD de Atribuições**: Gerenciamento das atribuições de tarefas a usuários.
- **Autenticação JWT**: Sistema de autenticação e proteção de rotas.
- **Documentação com Swagger**: Interface interativa para testar a API.

## Tecnologias Utilizadas

- **Node.js**
- **NestJS**
- **TypeORM** - ORM para interação com o banco de dados.
- **MySQL** - Banco de dados relacional.
- **Swagger** - Documentação da API.
- **JWT** - Autenticação baseada em tokens.

## Instalação

### Pré-requisitos

- Node.js instalado (versão 12+)
- MySQL instalado e rodando

### Passos

1. Instale as dependências:

   ```bash
   npm install
   ```

2. Configure o banco de dados:

   - Crie um banco de dados MySQL chamado `gerenciamento_tarefas`.
   - Configure as credenciais do banco de dados no arquivo `src/app.module.ts` ou em um arquivo `.env`.

3. Execute as migrações para criar as tabelas no banco de dados:

   ```bash
   npm run typeorm migration:run
   ```

4. Execute o servidor de desenvolvimento:

   ```bash
   npm run start
   ```

   A API estará disponível em `http://localhost:3000`.

## Documentação da API

Após iniciar o servidor, você pode acessar a documentação da API no Swagger em `http://localhost:3000/api`.

## Endpoints Principais

- **Autenticação**:
  - `POST /autenticacao/login`: Autenticação de usuário e geração de token JWT.

- **Usuários**:
  - `GET /usuarios`: Listar todos os usuários.
  - `POST /usuarios`: Criar um novo usuário.
  - `PUT /usuarios/:id`: Atualizar um usuário.
  - `DELETE /usuarios/:id`: Deletar um usuário.

- **Projetos**:
  - `GET /projetos`: Listar todos os projetos.
  - `POST /projetos`: Criar um novo projeto.
  - `PUT /projetos/:id`: Atualizar um projeto.
  - `DELETE /projetos/:id`: Deletar um projeto.

- **Tarefas**:
  - `GET /tarefas`: Listar todas as tarefas.
  - `POST /tarefas`: Criar uma nova tarefa.
  - `PUT /tarefas/:id`: Atualizar uma tarefa.
  - `DELETE /tarefas/:id`: Deletar uma tarefa.

- **Atribuições**:
  - `GET /atribuicoes`: Listar todas as atribuições.
  - `POST /atribuicoes`: Criar uma nova atribuição.
  - `PUT /atribuicoes/:id`: Atualizar uma atribuição.
  - `DELETE /atribuicoes/:id`: Deletar uma atribuição.

## Testes

Você pode testar a API usando ferramentas como Postman, Insomnia ou diretamente pelo Swagger.
