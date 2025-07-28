# Projeto Node - API de Usuários

Este projeto é uma API REST desenvolvida com Node.js, Express e Prisma ORM, utilizando MongoDB como banco de dados. Ela permite criar, listar, atualizar e deletar usuários.

## Estrutura do Projeto

- `server.js`: Código principal da API.
- `prisma/schema.prisma`: Definição do modelo de dados e configuração do Prisma.
- `generated/prisma/`: Código gerado pelo Prisma Client.
- `.env`: Variáveis de ambiente (ex: conexão com banco de dados).
- `package.json`: Dependências e scripts do projeto.

## Instalação

1. Clone o repositório.
2. Instale as dependências:
   ```sh
   npm install
   ```
3. Configure o arquivo `.env` com a variável `DATABASE_URL` para o MongoDB.

## Uso

- Inicie o servidor:
  ```sh
  node server.js
  ```
- A API estará disponível em `http://localhost:3000`.

## Endpoints

- `POST /usuarios`: Cria um novo usuário.
- `GET /usuarios`: Lista usuários (pode filtrar por nome, idade, email).
- `PUT /usuarios/:id`: Atualiza um usuário pelo ID.
- `DELETE /usuarios/:id`: Deleta um usuário pelo ID.

## Modelo de Usuário

- `id`: String (gerado automaticamente)
- `name`: String
- `email`: String (único)
- `age`: String

## Dependências

- express
- cors
- axios
- @prisma/client
- prisma

## Observações

- O Prisma está configurado para gerar o client em `generated/prisma`.
- O banco de dados utilizado é MongoDB.