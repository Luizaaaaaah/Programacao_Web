# Aula 08 — Atividade com projetos back-end

**Professor:** Prof. Me. Deivison S. Takatu  
**Disciplina:** Programação Web

## Visão geral

A aula retomou HTTP, métodos REST e JSON e avançou para uma API de notas criada com Express.js. A prática envolve operações CRUD, armazenamento em arquivo JSON, integração com front-end React, deploy e documentação da API no Postman.

## Conteúdo estudado

### Organização do back-end

A apresentação retomou MVC e arquitetura em camadas, separando regras de negócio, rotas e acesso aos dados. A componentização em módulos, serviços e middlewares favorece reutilização e manutenção.

### HTTP, REST e JSON

- **GET:** consulta recursos.
- **POST:** cria recursos.
- **PUT:** substitui os dados de um recurso.
- **PATCH:** altera parcialmente os dados.
- **DELETE:** remove um recurso.

JSON é o formato usado para trocar dados entre a API e o front-end, por meio de objetos e arrays.

### Hospedagem com Render

O Render foi apresentado como plataforma de hospedagem de serviços, com integração ao GitHub. O fluxo prático é enviar o código ao repositório, criar um Web Service, conectar a origem e configurar o comando de inicialização.

### API de notas com Express

A aplicação de exemplo utiliza server.js para configurar o servidor e data.json como arquivo de armazenamento. O módulo fs lê e grava o conteúdo; o middleware de parsing permite receber JSON no corpo das requisições.

As rotas apresentadas são:

| Método | Endpoint | Operação |
|---|---|---|
| GET | /api/notes | Listar notas |
| POST | /api/notes | Criar nota |
| PUT | /api/notes/:id | Atualizar nota |
| DELETE | /api/notes/:id | Excluir nota |

### Integração front-end/back-end

A aplicação React deve listar, criar, editar e remover notas consumindo a API. Depois de publicar o back-end no Render, o front-end deve utilizar a URL pública correspondente em vez do endereço local.

### Postman e documentação

Postman permite enviar requisições, inspecionar respostas e documentar endpoints. A documentação de uma API deve informar métodos, parâmetros, formatos de entrada e saída e códigos de resposta.

## Atividades propostas

1. Publicar a API Express de notas no Render.
2. Construir o front-end React consumindo as rotas CRUD.
3. Documentar código, aplicação, repositórios e deploy.
4. Criar uma coleção Postman com as quatro operações CRUD, parâmetros e descrições dos códigos de resposta.
5. Incluir prints e link da coleção do Postman no relatório.

Os slides também propõem reflexão sobre segurança, adequação do arquivo JSON em produção, desempenho com grande volume de registros e organização do código em módulos.

## Ferramentas e conceitos

Express.js, Node.js, JSON, fs, HTTP, CRUD, Render, React, Vercel e Postman.

## Síntese

A aula transformou conceitos de API em uma aplicação completa: o servidor expõe operações CRUD, o front-end consome essas operações e o Postman registra e testa o contrato da API.

**Próximo:** [Atividade 08](../atividades/aula-08/README.md) | [Índice das aulas](README.md)