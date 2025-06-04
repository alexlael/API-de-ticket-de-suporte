# API de Ticket de Suporte

Este repositório contém uma API simples para gerenciamento de tickets de suporte. O projeto foi desenvolvido em Node.js como forma de consolidar conhecimentos e testar a criação de um servidor HTTP sem o uso de frameworks.

A estrutura da aplicação se baseia no [material proposto nesta documentação](https://efficient-sloth-d85.notion.site/API-de-ticket-de-suporte-25654d26e5704936a5da1b3083f03c27), que apresenta o passo a passo para construção de uma API de tickets. A partir dela foram implementados controladores, middlewares, rotas e um banco de dados em arquivo JSON.

## Como executar

1. Instale as dependências (caso existam):
   ```bash
   npm install
   ```
2. Inicie o servidor em modo de desenvolvimento:
   ```bash
   npm run dev
   ```
   O servidor ficará disponível na porta `3333`.

## Funcionalidades

- **Criação de tickets** – `POST /tickets`
- **Listagem de tickets** – `GET /tickets`
- **Atualização de tickets** – `PUT /tickets/:id`
- **Fechamento de tickets** – `PATCH /tickets/:id/close`
- **Remoção de tickets** – `DELETE /tickets/:id`

Os tickets ficam armazenados no arquivo `src/database/db.json`. Cada registro contém informações como equipamento, descrição, usuário e status do ticket.

## Observações

Este projeto não possui testes automatizados nem depende de bibliotecas externas; é um estudo para compreender melhor o funcionamento do Node.js puro, trabalhando diretamente com o módulo `http`, manipulação de arquivos e regex para roteamento.

