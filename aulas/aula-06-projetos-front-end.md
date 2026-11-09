# Aula 06 — Atividade com projetos front-end

**Professor:** Prof. Me. Deivison S. Takatu  
**Disciplina:** Programação Web

## Visão geral

A aula teve foco prático na criação e organização de projetos front-end com React, Angular e Vue. Também explicou como localizar projetos-modelo e importar um template para personalizá-lo.

## Conteúdo estudado

### Node.js e NPM

Node.js é o ambiente de execução JavaScript utilizado para ferramentas de desenvolvimento e aplicações no servidor. NPM instala, atualiza e gerencia as dependências; o package.json registra pacotes e scripts. A instalação pode ser verificada com node --version.

### React

A apresentação destacou JSX, Hooks, componentização, flexibilidade e o ecossistema React. O projeto de exemplo pode ser criado com:

~~~bash
npx create-react-app meu-projeto-react
cd meu-projeto-react
npm start
~~~

A estrutura inclui public, src, package.json, package-lock.json e .gitignore. O App.js costuma atuar como componente raiz.

### Angular

Angular foi apresentado como framework completo com TypeScript, CLI, componentes, serviços, módulos, data binding, roteamento e injeção de dependências.

~~~bash
npm install -g @angular/cli
ng new meu-app-angular
cd meu-app-angular
ng serve
~~~

O material descreveu arquivos de configuração como angular.json e arquivos tsconfig, além da estrutura principal dentro de src.

### Vue

Vue é um framework progressivo, com reatividade e Single-File Components (SFC). Um componente .vue pode reunir template, script e estilos.

~~~bash
npm create vue@latest
cd meu-projeto-vue
npm install
npm run dev
~~~

### Importação de projetos-modelo

A aula mostrou que templates disponíveis na comunidade podem acelerar o desenvolvimento. Os slides citaram pesquisa de repositórios no GitHub, templates da Vercel e exemplos do CodeSandbox. O fluxo apresentado envolve localizar o projeto, cloná-lo ou baixar os arquivos, personalizar e versionar a própria cópia.

## Atividade proposta

1. Criar três projetos: um React, um Angular e um Vue. Fazer alterações iniciais e versionar cada um em um repositório GitHub diferente.
2. Pesquisar um template feito com um dos frameworks estudados, importá-lo, realizar alterações e publicar em um quarto repositório.
3. Fazer o deploy dos quatro repositórios na Vercel.
4. Documentar as etapas, prints, links dos quatro repositórios e links dos quatro sites publicados.

## Ferramentas e conceitos

Node.js, NPM, React, Angular CLI, Vue, Vite, Git, GitHub, Vercel e CodeSandbox.

## Síntese

A aula ampliou a prática de criação de projetos para três tecnologias front-end e apresentou a reutilização de templates. A entrega exige separar os projetos em repositórios distintos e publicar cada um, mantendo documentação e evidências.

**Próximo:** [Atividade 06](../atividades/aula-06/README.md) | [Índice das aulas](README.md)