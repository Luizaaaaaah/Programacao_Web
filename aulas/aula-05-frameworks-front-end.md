# Aula 05 — Introdução a frameworks front-end

**Professor:** Prof. Me. Deivison S. Takatu  
**Disciplina:** Programação Web

## Visão geral

A aula introduziu ferramentas modernas para desenvolver interfaces web. O foco foi entender o papel de frameworks e bibliotecas, comparar essas abordagens e conhecer React, seus conceitos centrais e a preparação do ambiente com Node.js.

## Conteúdo estudado

### Frameworks front-end

Um framework oferece estrutura, convenções e ferramentas para acelerar o desenvolvimento de interfaces. A organização por componentes, o gerenciamento de estado e a reutilização de código ajudam a reduzir repetição e facilitar a manutenção em aplicações maiores.

### Framework x biblioteca

No framework, a ferramenta controla boa parte do fluxo da aplicação (inversão de controle). Em uma biblioteca, o desenvolvedor chama os recursos quando precisa. A apresentação usa Angular e Vue como exemplos de frameworks e React e jQuery como bibliotecas, ressaltando que React é tecnicamente uma biblioteca, embora seja frequentemente chamado de framework.

### Benefícios e características

Foram abordadas produtividade, componentização, programação reativa, ferramentas de build, rotas, integração com APIs, documentação, comunidade, acessibilidade e suporte a testes.

### React

React é uma biblioteca JavaScript para construir interfaces com componentes reutilizáveis. A aula apresentou JSX, no qual expressões JavaScript são inseridas entre chaves; Hooks, incluindo useState e useEffect; gerenciamento de estado com Context API ou Redux; e DOM/Virtual DOM.

- **useState:** armazena e atualiza o estado de um componente.
- **useEffect:** executa efeitos colaterais, como chamadas de API.
- **JSX:** permite descrever a interface com sintaxe semelhante a HTML no JavaScript.
- **Virtual DOM:** representação utilizada pelo React para calcular mudanças na interface antes de atualizar o DOM real.

### Node.js e NPM

Node.js permite executar JavaScript fora do navegador. NPM gerencia pacotes e dependências. O package.json registra metadados, scripts e dependências do projeto.

### Criação do projeto React

A apresentação demonstra o uso do Create React App:

~~~bash
npx create-react-app meu-projeto-react
cd meu-projeto-react
code .
npm start
~~~

Também foram identificados os diretórios public, src e node_modules, além dos arquivos de entrada, componente principal, estilos e .gitignore.

## Atividade proposta

1. Criar um projeto React com um cabeçalho que permita acessar cinco funcionalidades: To-Do List, contador de cliques, jogo da velha, calculadora e buscador de CEP.
2. Utilizar Git para registrar o projeto no GitHub e publicar o site na Vercel.
3. Documentar os elementos implementados e justificar a escolha da estilização.
4. Incluir etapas, prints, link do repositório e endereço do site publicado.

## Ferramentas e conceitos

React, Angular, Vue, JSX, Hooks, useState, useEffect, DOM, Virtual DOM, Node.js, NPM, GitHub e Vercel.

## Síntese

Frameworks e bibliotecas oferecem estruturas e recursos para tornar o front-end mais reutilizável e organizado. React foi utilizado como referência prática, conectando componentes, estado, Node.js e publicação do projeto.

**Próximo:** [Atividade 05](../atividades/aula-05/README.md) | [Índice das aulas](README.md)