# Atividade 05 — Aplicação React com cinco funcionalidades

**Disciplina:** Programação Web  
**Professor:** Prof. Me. Deivison S. Takatu

## 1. Objetivo

Desenvolver uma aplicação React com um cabeçalho de navegação e cinco funcionalidades independentes, versionar o código no GitHub e realizar deploy na Vercel.

## 2. O que foi solicitado

- To-Do List.
- Contador de cliques.
- Jogo da velha.
- Calculadora.
- Buscador de CEP.
- Commit do projeto no GitHub e publicação na Vercel.
- Documentação das funcionalidades e da escolha de estilização.
- Prints das telas e links de repositório e site.

## 3. Projeto localizado

**Repositório:** [exercicio_react](https://github.com/Luizaaaaaah/exercicio_react)  
**Visibilidade:** público  
**Branch principal:** main

O código-fonte em src/App.js foi consultado. Foram identificadas as cinco funcionalidades esperadas:

| Funcionalidade | Comportamento identificado |
|---|---|
| To-Do List | Adiciona, conclui e remove tarefas |
| Contador | Incrementa cliques e permite zerar |
| Jogo da velha | Tabuleiro 3x3, alternância X/O e verificação de vencedor |
| Calculadora | Operações de soma, subtração, multiplicação e divisão; verifica divisão por zero |
| Buscador de CEP | Consulta ViaCEP por fetch e apresenta o endereço retornado |

A interface utiliza estado React com useState. A consulta do CEP usa a API pública ViaCEP. O projeto possui arquivos de estilos em App.css e index.css.

## 4. Tecnologias observadas

React, JavaScript, JSX, useState, HTML, CSS, fetch, API ViaCEP, Node.js/NPM, Git e GitHub.

## 5. Links e publicação

| Recurso | Link / situação |
|---|---|
| Código-fonte | [exercicio_react](https://github.com/Luizaaaaaah/exercicio_react) |
| Arquivo principal | [src/App.js](https://github.com/Luizaaaaaah/exercicio_react/blob/main/src/App.js) |
| Estilos | [src/App.css](https://github.com/Luizaaaaaah/exercicio_react/blob/main/src/App.css) |
| Site de produção Vercel | Não localizado; inserir URL após confirmação |
| Documento de execução anterior | Não localizado como arquivo separado |

O README padrão do Create React App ainda é o conteúdo do projeto. Este relatório funciona como documentação acadêmica complementar.

## 6. Evidências a anexar

| Arquivo sugerido | O que deve mostrar |
|---|---|
| 01-menu-inicial.png | Cabeçalho e navegação das cinco opções |
| 02-todo-list.png | Cadastro, conclusão e remoção de tarefa |
| 03-contador.png | Contador e botão de zerar |
| 04-jogo-da-velha.png | Tabuleiro e resultado de uma partida |
| 05-calculadora.png | Operação matemática e resultado |
| 06-buscador-cep.png | CEP pesquisado e endereço retornado |
| 07-github-commits.png | Histórico de commits |
| 08-vercel-deploy.png | Configuração e status do deploy |
| 09-site-publicado.png | Aplicação aberta pelo endereço de produção |

As capturas devem ser colocadas em [prints/](prints/README.md).

## 7. Situação desta documentação

- [x] Repositório público localizado.
- [x] Código das cinco funcionalidades conferido.
- [x] Arquivos principais e estilos identificados.
- [ ] Confirmar a URL Vercel de produção.
- [ ] Anexar capturas e justificar a identidade visual escolhida.
- [ ] Confirmar tag/versão publicada, se aplicável.