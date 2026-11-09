# Aula 07 — Introdução a frameworks back-end

**Professor:** Prof. Me. Deivison S. Takatu  
**Disciplina:** Programação Web

## Visão geral

A aula apresentou frameworks back-end, arquitetura de software, padrões de projeto e o Express.js. Também foram discutidos APIs, protocolo HTTP, endpoints e o formato JSON utilizado na comunicação entre sistemas.

## Conteúdo estudado

### Frameworks back-end

Frameworks back-end reúnem bibliotecas, ferramentas e convenções para estruturar a lógica do servidor, rotas, APIs e acesso a dados. Podem reduzir configurações repetitivas e facilitar organização, manutenção, segurança e escalabilidade.

Foram citados Express.js (Node.js), Django (Python) e Laravel (PHP). A escolha depende dos requisitos do projeto, complexidade, equipe, desempenho, curva de aprendizado e suporte da comunidade.

### Arquitetura e padrões de projeto

A aula discutiu MVC e arquiteturas em camadas para separar responsabilidades. Os Design Patterns foram agrupados em criacionais (Factory, Singleton, Builder), estruturais (Adapter, Composite, Proxy) e comportamentais (Observer, Strategy, Command).

### Monólitos e microsserviços

Um monólito mantém os módulos em uma aplicação integrada, podendo ser mais simples em projetos menores. Microsserviços dividem o sistema em serviços independentes, permitindo escala separada, mas aumentando a complexidade operacional. A apresentação utilizou um estudo de caso do Amazon Prime Video para reforçar que a arquitetura deve atender às necessidades reais.

### Express.js

Express é um framework minimalista para Node.js que facilita a criação de servidores e APIs. A aula apresentou rotas como app.get(), middlewares e o tratamento de requisições e respostas.

### HTTP, API REST e endpoints

HTTP estabelece a comunicação cliente-servidor. Os métodos principais são GET para leitura, POST para criação, PUT para substituição, PATCH para atualização parcial e DELETE para exclusão. REST organiza recursos identificados por URIs e utiliza métodos HTTP e representações como JSON.

Endpoint é o endereço específico de uma API que expõe um recurso ou ação.

### JSON e CORS

JSON organiza dados em objetos (pares nome/valor) e arrays (listas). CORS trata das permissões de acesso entre origens diferentes, relevante quando o front-end e o back-end estão hospedados em domínios distintos.

## Prática e atividade propostas

A apresentação demonstra uma API básica com Express, incluindo inicialização do servidor e definição de rota.

A atividade solicita:
1. Criar uma API Express com uma rota que consulte data e hora.
2. Publicar o back-end no Render, conectado a um repositório GitHub.
3. Desenvolver um front-end que consuma a API e apresente a data e a hora.
4. Manter front-end e API em repositórios separados.
5. Documentar código, aplicação, painéis do Render e da Vercel e links dos dois repositórios.

## Ferramentas e conceitos

Node.js, Express.js, HTTP, API REST, endpoints, JSON, CORS, MVC, Design Patterns, Render e Vercel.

## Síntese

A aula conectou arquitetura do servidor e comunicação por APIs. Express facilita a construção de rotas e middlewares; HTTP e JSON padronizam a troca de dados entre a interface e o back-end.

**Próximo:** [Atividade 07](../atividades/aula-07/README.md) | [Índice das aulas](README.md)