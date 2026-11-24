---
author: Resumo didático
date: 08/09/2026
title: Aula 06 --- Atividade com Projetos Front-end
---

# ❄️ Aula 06 --- Atividade com Projetos Front-end

> **Tema:** criação, estrutura, importação, alteração e publicação de
> projetos Front-end usando **React, Angular e Vue**.

📚 **Material-base:** Aula 06 --- *Atividade com Projetos Front-end*,
Prof. Me. Deivison S. Takatu.\
A aula apresenta Node.js/NPM, criação de projetos React, Angular e Vue,
estrutura de pastas, importação de templates e uma atividade prática
envolvendo GitHub e Vercel.

------------------------------------------------------------------------

## 🧭 Sumário

1.  [Objetivos da aula](#-objetivos-da-aula)
2.  [Node.js](#-nodejs)
3.  [NPM](#-npm-node-package-manager)
4.  [React](#-react)
5.  [Angular](#-angular)
6.  [Vue](#-vue)
7.  [Comparação rápida](#-comparação-rápida)
8.  [Importação de projetos](#-importação-de-projetos)
9.  [Atividade proposta pelo
    professor](#-atividade-proposta-pelo-professor)
10. [Projeto prático desenvolvido ---
    HoennDex](#-projeto-prático-desenvolvido--hoenndex)
11. [Conceitos Vue utilizados no
    projeto](#-conceitos-vue-utilizados-no-projeto)
12. [Checklist da aula](#-checklist-da-aula)
13. [Resumo final](#-resumo-final)
14. [Referências](#-referências)

------------------------------------------------------------------------

# 🎯 Objetivos da aula

Ao final da aula, a ideia é compreender o fluxo básico para trabalhar
com frameworks Front-end:

``` text
Node.js
   ↓
NPM
   ↓
Framework
   ↓
Criação do projeto
   ↓
Alteração do código
   ↓
Git / GitHub
   ↓
Deploy na Vercel
```

A aula trabalha principalmente:

-   instalação e utilização do **Node.js**;
-   gerenciamento de dependências com **NPM**;
-   criação de projetos com **React**;
-   criação de projetos com **Angular**;
-   criação de projetos com **Vue**;
-   compreensão da estrutura dos projetos;
-   importação de projetos/templated;
-   versionamento com Git e GitHub;
-   publicação dos projetos na Vercel.

------------------------------------------------------------------------

# 🟦 Node.js

## O que é?

**Node.js** é um ambiente de execução JavaScript que permite executar
JavaScript no **backend**, ou seja, no lado do servidor.

Uma das principais vantagens apresentadas na aula é poder utilizar
JavaScript tanto no navegador quanto no servidor.

``` text
                 JavaScript
                /          \
               ↓            ↓
          Navegador       Servidor
          Front-end       Node.js
```

Isso facilita a integração entre Front-end e Back-end.

## Instalação

O material indica:

1.  acessar o site do Node.js;
2.  escolher a versão adequada ao sistema operacional;
3.  baixar o instalador;
4.  executar o instalador;
5.  seguir as etapas de instalação.

### Verificando a instalação

No Prompt de Comando:

``` bash
node --version
```

Se uma versão for exibida, o Node.js está instalado.

------------------------------------------------------------------------

# 📦 NPM --- Node Package Manager

O **NPM** é o gerenciador de pacotes do Node.js e é instalado junto com
ele.

Ele permite:

-   instalar bibliotecas;
-   atualizar pacotes;
-   remover pacotes;
-   gerenciar dependências;
-   criar e compartilhar módulos;
-   automatizar a configuração das dependências do projeto.

## `package.json`

O arquivo:

``` text
package.json
```

registra informações importantes do projeto, incluindo suas dependências
e scripts.

Um projeto pode utilizar:

``` bash
npm install
```

para instalar as dependências registradas.

### Ideia principal

Em vez de cada desenvolvedor baixar manualmente todas as bibliotecas, o
projeto registra suas dependências e o NPM pode instalá-las
automaticamente.

------------------------------------------------------------------------

# ⚛️ React

## O que é?

React é uma biblioteca para desenvolvimento de interfaces.

O material destaca:

-   **Flexibilidade:** não impõe uma estrutura rígida;
-   **Grande ecossistema:** Redux, React Router, Next.js etc.;
-   **Componentização:** reutilização de código;
-   **Virtual DOM:** otimização da atualização da interface;
-   **Comunidade ativa:** grande quantidade de materiais e soluções.

## Requisitos destacados

-   Node.js instalado;
-   conhecimento em JSX;
-   conhecimento em Hooks, como `useState` e `useEffect`.

## Criação de projeto

O material apresenta:

``` bash
npx create-react-app meu-projeto-react
```

Depois:

``` bash
cd meu-projeto-react
```

Abrir no VS Code:

``` bash
code .
```

Executar:

``` bash
npm start
```

## Estrutura apresentada

``` text
meu-projeto-react/
│
├── node_modules/
├── public/
├── src/
├── .gitignore
├── package.json
└── package-lock.json
```

### `node_modules`

Contém os pacotes instalados e suas dependências.

### `public`

Contém arquivos públicos/estáticos, como HTML, JSON e imagens.

### `src`

Contém os arquivos principais do código React.

### `.gitignore`

Define arquivos e diretórios que devem ser ignorados pelo Git.

### `package.json`

Registra dependências, scripts e informações do projeto.

### `package-lock.json`

Registra informações detalhadas das dependências instaladas.

## Arquivos principais

``` text
index.js
```

É o ponto de entrada que renderiza a aplicação no DOM.

``` text
App.js
```

É o componente raiz.

``` text
App.css
```

Contém estilos associados ao componente App.

``` text
index.css
```

Contém estilos globais.

------------------------------------------------------------------------

# 🅰️ Angular

## O que é?

Angular é apresentado como um **framework completo** para
desenvolvimento de aplicações.

O material destaca:

-   roteamento;
-   HTTP Client;
-   injeção de dependências;
-   TypeScript;
-   arquitetura MVC;
-   CLI;
-   componentes;
-   serviços;
-   Data Binding;
-   performance.

## Requisitos destacados

-   Node.js instalado;
-   conhecimentos relacionados à programação orientada a objetos (POO).

## Conceitos fundamentais

### Componentes

Estruturam a aplicação combinando lógica, HTML e estilos.

### Módulos

Organizam a aplicação em blocos funcionais.

### Serviços

Permitem criar lógica reutilizável.

### Data Binding

O material apresenta recursos como:

``` text
{{ }}
```

e:

``` text
[(ngModel)]
```

### Injeção de Dependência

Permite disponibilizar dependências para os componentes e serviços.

### Roteamento

Permite organizar a navegação entre diferentes views.

------------------------------------------------------------------------

# 🛠️ Angular CLI

A CLI é uma ferramenta de linha de comando utilizada para criar,
gerenciar e construir aplicações Angular.

## Instalação

``` bash
npm install -g @angular/cli
```

## Criar projeto

``` bash
ng new meu-app-angular
```

## Entrar na pasta

``` bash
cd meu-app-angular
```

## Abrir no VS Code

``` bash
code .
```

## Executar

``` bash
ng serve
```

------------------------------------------------------------------------

# 📁 Estrutura Angular

Uma estrutura apresentada na aula inclui:

``` text
meu-app-angular/
│
├── node_modules/
├── public/
├── src/
├── .angular/
├── .vscode/
├── app/
├── index.html
├── main.ts
├── main.server.ts
├── server.ts
├── styles.css
├── angular.json
├── package.json
├── package-lock.json
├── tsconfig.json
├── tsconfig.app.json
└── tsconfig.spec.json
```

### Diretórios importantes

**`node_modules/`**\
Dependências do projeto.

**`public/`**\
Arquivos estáticos públicos.

**`src/`**\
Código-fonte da aplicação.

**`.angular/`**\
Cache e configurações temporárias geradas pelo Angular CLI.

**`.vscode/`**\
Configurações específicas do VS Code.

**`app/`**\
Componentes, módulos, serviços e demais partes principais da aplicação.

## Arquivos importantes

**`index.html`**\
Ponto de entrada HTML.

**`main.ts`**\
Inicialização da aplicação.

**`styles.css`**\
Estilos globais.

**`angular.json`**\
Configurações principais de build, testes e estilos.

**Arquivos `tsconfig`**\
Configurações do TypeScript.

------------------------------------------------------------------------

# 💚 Vue

## O que é?

Vue é um framework progressivo para desenvolvimento de interfaces.

O material destaca:

-   adoção progressiva;
-   reatividade eficiente;
-   Single-File Components;
-   curva de aprendizado suave;
-   performance otimizada.

## Requisitos destacados

-   Node.js instalado;
-   conhecimento em JavaScript/TypeScript;
-   conceitos de programação reativa;
-   conceitos de desenvolvimento baseado em componentes.

------------------------------------------------------------------------

# 🧩 Single-File Components --- SFC

Uma característica importante do Vue é o **Single-File Component**.

Um componente pode reunir:

``` text
┌────────────────────────────┐
│       Componente Vue       │
├────────────────────────────┤
│ <template>                 │
│ HTML / estrutura           │
├────────────────────────────┤
│ <script>                   │
│ JavaScript / TypeScript    │
├────────────────────────────┤
│ <style>                    │
│ CSS / estilos              │
└────────────────────────────┘
```

Normalmente isso fica em um arquivo:

``` text
Componente.vue
```

------------------------------------------------------------------------

# 🚀 Criando um projeto Vue

O material apresenta:

``` bash
npm create vue@latest
```

Depois:

``` bash
cd meu-projeto-vue
```

Instalar dependências:

``` bash
npm install
```

Abrir no VS Code:

``` bash
code .
```

Executar o servidor:

``` bash
npm run dev
```

O Vite disponibiliza a aplicação em um endereço local, normalmente
semelhante a:

``` text
http://localhost:5173/
```

------------------------------------------------------------------------

# 📂 Estrutura Vue

A estrutura apresentada no material pode ser resumida assim:

``` text
meu-projeto-vue/
│
├── node_modules/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   ├── App.vue
│   └── main.js / main.ts
│
├── .vscode/
├── .gitignore
├── package.json
├── package-lock.json
└── vite.config.js
```

## `node_modules`

Contém as dependências instaladas.

## `public`

Contém arquivos estáticos que não passam pelo processamento principal do
Vite.

## `src`

É o diretório principal do código-fonte.

------------------------------------------------------------------------

# 🖼️ `assets`

A pasta:

``` text
src/assets/
```

pode conter:

-   imagens;
-   fontes;
-   CSS global;
-   outros arquivos processados pelo Vite.

------------------------------------------------------------------------

# 🧱 `components`

A pasta:

``` text
src/components/
```

é utilizada para componentes Vue reutilizáveis.

Exemplos:

``` text
components/
├── Header.vue
├── Button.vue
├── Card.vue
└── Menu.vue
```

A ideia é evitar colocar toda a aplicação em um único arquivo.

------------------------------------------------------------------------

# ⭐ `App.vue`

O:

``` text
App.vue
```

é o **componente raiz da aplicação**.

Ele define a estrutura inicial e pode importar outros componentes.

Exemplo conceitual:

``` vue
<script setup lang="ts">
import Header from './components/Header.vue'
</script>

<template>
  <Header />
</template>
```

------------------------------------------------------------------------

# 🟢 `main.js` / `main.ts`

É o ponto de entrada do Vue.

Ele monta a aplicação no DOM e pode configurar recursos globais.

------------------------------------------------------------------------

# 🌐 `index.html`

É o HTML principal da SPA.

O Vue é injetado na página através de uma estrutura semelhante a:

``` html
<div id="app"></div>
```

------------------------------------------------------------------------

# ⚡ Vue + Vite

No projeto criado pelo comando:

``` bash
npm create vue@latest
```

o Vite participa do ambiente de desenvolvimento e build.

O arquivo:

``` text
vite.config.js
```

contém configurações relacionadas ao Vite.

------------------------------------------------------------------------

# ⚖️ Comparação rápida

  Tecnologia   Característica destacada
  ------------ --------------------------------------
  ⚛️ React     Biblioteca flexível e componentizada
  🅰️ Angular   Framework completo
  💚 Vue       Framework progressivo e acessível

### Em comum

Os três podem ser utilizados para desenvolver interfaces modernas
baseadas em componentes.

### Diferença de abordagem

``` text
React
  → mais flexível

Angular
  → estrutura mais completa/opinativa

Vue
  → progressivo e com sintaxe acessível
```

------------------------------------------------------------------------

# 📦 Importação de projetos

A aula também apresenta a ideia de utilizar projetos existentes como
ponto de partida.

Isso é útil porque nem sempre é necessário começar uma aplicação do
zero.

A comunidade open source disponibiliza projetos e templates que podem
ser estudados e personalizados.

## Ferramentas citadas

### GitHub

Pode ser utilizado para pesquisar projetos e repositórios.

Com Git, um repositório pode ser clonado usando:

``` bash
git clone <url>
```

### Vercel

Pode ser utilizada para encontrar templates e posteriormente publicar
aplicações.

### CodeSandbox

Pode ser utilizada para pesquisar templates e experimentar projetos.

------------------------------------------------------------------------

# 🔄 Fluxo de importação

Um fluxo possível é:

``` text
Template / Projeto existente
          ↓
       Importar
          ↓
      Analisar
          ↓
       Alterar
          ↓
       Testar
          ↓
       Git commit
          ↓
        GitHub
          ↓
        Vercel
```

O objetivo não é simplesmente copiar um projeto, mas **entender,
modificar e personalizar** o código.

------------------------------------------------------------------------

# 📝 Atividade proposta pelo professor

A atividade possui quatro etapas principais.

## 1️⃣ Criar três projetos

Criar projetos utilizando:

``` text
React
Angular
Vue
```

Depois:

-   realizar alterações iniciais;
-   utilizar Git;
-   criar um commit;
-   enviar cada projeto para um repositório diferente no GitHub.

Resultado:

``` text
GitHub
├── projeto-react
├── projeto-angular
└── projeto-vue
```

------------------------------------------------------------------------

## 2️⃣ Importar um template

Pesquisar um template desenvolvido com um dos frameworks estudados.

Depois:

1.  importar o projeto;
2.  entender sua estrutura;
3.  realizar alterações;
4.  personalizar;
5.  versionar;
6.  enviar para um quarto repositório.

Resultado:

``` text
GitHub
├── React
├── Angular
├── Vue
└── Template alterado
```

------------------------------------------------------------------------

## 3️⃣ Deploy

Com os quatro projetos prontos, realizar o deploy na **Vercel**.

``` text
Projeto local
     ↓
   GitHub
     ↓
  Vercel
     ↓
Projeto publicado
```

------------------------------------------------------------------------

## 4️⃣ Documentação

Documentar toda a atividade em um único arquivo.

A documentação deve incluir:

-   descrição das etapas;
-   prints das telas;
-   links dos repositórios no GitHub;
-   links dos projetos publicados na Vercel.

------------------------------------------------------------------------

# 🎮 Projeto prático desenvolvido --- HoennDex

Durante a atividade prática, foi iniciado um projeto Vue com o tema:

> **Pokédex da terceira geração de Pokémon.**

Nome escolhido:

# 💚 HoennDex

A proposta é criar uma espécie de Pokédex digital dedicada à região de
**Hoenn**.

## Objetivos do projeto

A aplicação foi planejada para apresentar:

-   imagens dos Pokémon;
-   informações;
-   número da Pokédex;
-   tipos;
-   atributos;
-   pesquisa;
-   filtros;
-   cards;
-   informações sobre Hoenn;
-   interface responsiva.

------------------------------------------------------------------------

# 🧱 Primeiro `App.vue`

O projeto Vue criado inicialmente apresentava os componentes padrão do
template.

O `App.vue` original continha componentes de exemplo, como:

``` vue
<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>
```

Esses componentes foram substituídos para iniciar a construção da
HoennDex.

------------------------------------------------------------------------

# 🐉 Estrutura inicial da HoennDex

A primeira versão foi organizada em:

``` text
┌──────────────────────────────────────┐
│              HOENNDex                │
│       Pokédex da Região de Hoenn     │
├──────────────────────────────────────┤
│                                      │
│        A região de Hoenn             │
│                                      │
│             Rayquaza                 │
│                                      │
│        [Explorar Pokédex]            │
│                                      │
├──────────────────────────────────────┤
│               POKÉDEX                │
│                                      │
│   🔎 Pesquisa       Tipo             │
│                                      │
│   ┌──────┐ ┌──────┐ ┌──────┐        │
│   │      │ │      │ │      │        │
│   │ 🌱   │ │ 🔥   │ │ 💧   │        │
│   └──────┘ └──────┘ └──────┘        │
│                                      │
├──────────────────────────────────────┤
│          SOBRE A REGIÃO              │
└──────────────────────────────────────┘
```

------------------------------------------------------------------------

# 🔎 Busca de Pokémon

Foi utilizado o recurso reativo do Vue:

``` ts
const search = ref('')
```

No template:

``` html
<input
  v-model="search"
  type="text"
  placeholder="Pesquisar Pokémon..."
>
```

O:

``` text
v-model
```

faz a ligação entre o campo de entrada e a variável reativa.

------------------------------------------------------------------------

# 🧠 `computed()`

Para filtrar a lista:

``` ts
const filteredPokemons = computed(() => {
  return pokemons.filter((pokemon) => {
    return pokemon.name
      .toLowerCase()
      .includes(search.value.toLowerCase())
  })
})
```

A ideia é:

``` text
Usuário digita
      ↓
search muda
      ↓
computed recalcula
      ↓
lista filtrada
      ↓
interface atualizada
```

------------------------------------------------------------------------

# 🔁 `v-for`

Para gerar os cards automaticamente:

``` html
<article
  v-for="pokemon in filteredPokemons"
  :key="pokemon.id"
>
```

Em vez de criar cada card manualmente, o Vue percorre os dados e gera os
elementos.

``` text
Array de Pokémon
       ↓
     v-for
       ↓
┌──────────┐
│  Card 1  │
├──────────┤
│  Card 2  │
├──────────┤
│  Card 3  │
└──────────┘
```

------------------------------------------------------------------------

# 🏷️ Tipos

O card utiliza outro `v-for` para os tipos:

``` html
<span
  v-for="type in pokemon.types"
  :key="type"
>
  {{ type }}
</span>
```

Assim um Pokémon com dois tipos pode apresentar, por exemplo:

``` text
┌─────────────┐
│   Blaziken  │
├─────────────┤
│ Fogo | Lutador │
└─────────────┘
```

------------------------------------------------------------------------

# 🖼️ Imagens

As imagens dos Pokémon foram configuradas através de URLs nos dados:

``` ts
image: 'URL_DA_IMAGEM'
```

E exibidas com:

``` html
<img
  :src="pokemon.image"
  :alt="pokemon.name"
>
```

O `:` antes de `src` indica um **binding** de atributo no Vue.

------------------------------------------------------------------------

# 📊 Dados dos Pokémon

Foi criada uma estrutura TypeScript:

``` ts
interface Pokemon {
  id: number
  name: string
  image: string
  types: string[]
  hp: number
  attack: number
  defense: number
}
```

Isso define o formato esperado para cada Pokémon.

Exemplo:

``` ts
{
  id: 252,
  name: 'Treecko',
  image: '...',
  types: ['Grama'],
  hp: 40,
  attack: 45,
  defense: 35
}
```

------------------------------------------------------------------------

# 🎨 Interface

A interface da HoennDex foi construída com CSS utilizando:

-   layout flexível;
-   CSS Grid;
-   cards;
-   sombras;
-   bordas arredondadas;
-   animações;
-   hover;
-   responsividade;
-   header fixo;
-   seção hero;
-   footer.

------------------------------------------------------------------------

# 📱 Responsividade

Foi utilizada uma media query:

``` css
@media (max-width: 800px) {
  ...
}
```

A ideia é adaptar o layout para telas menores.

### Desktop

``` text
┌─────────────────────────────────────────────┐
│ Header                                      │
├─────────────────────────────────────────────┤
│ Texto                 Pokémon               │
│                                             │
├─────────────────────────────────────────────┤
│ Card │ Card │ Card │ Card                   │
└─────────────────────────────────────────────┘
```

### Celular

``` text
┌──────────────────┐
│      Header      │
├──────────────────┤
│      Texto       │
│                  │
│     Pokémon      │
├──────────────────┤
│      Card        │
├──────────────────┤
│      Card        │
├──────────────────┤
│      Card        │
└──────────────────┘
```

------------------------------------------------------------------------

# 🛠️ Correção realizada no projeto

Após executar a aplicação, foi identificado que a página estava ocupando
somente uma parte da largura da tela.

Isso ocorreu por causa dos estilos padrão do projeto Vue.

O arquivo:

``` text
src/assets/main.css
```

foi ajustado para remover a limitação de largura do `#app`.

CSS utilizado:

``` css
* {
  box-sizing: border-box;
}

html {
  margin: 0;
  padding: 0;
  scroll-behavior: smooth;
}

body {
  margin: 0;
  padding: 0;
  min-width: 320px;
}

#app {
  width: 100%;
  max-width: none;
  margin: 0;
  padding: 0;
}
```

### Por que isso resolveu?

O template inicial podia aplicar uma largura máxima ao:

``` css
#app
```

Com:

``` css
max-width: none;
```

e:

``` css
width: 100%;
```

a aplicação passa a utilizar toda a largura disponível.

------------------------------------------------------------------------

# 🧩 Próxima evolução da HoennDex

O projeto pode evoluir para uma estrutura mais organizada:

``` text
src/
│
├── assets/
│
├── components/
│   ├── Header.vue
│   ├── Hero.vue
│   ├── SearchBar.vue
│   ├── PokemonCard.vue
│   ├── PokemonGrid.vue
│   └── AboutHoenn.vue
│
├── data/
│   └── pokemons.ts
│
├── App.vue
│
└── main.ts
```

Isso demonstra de forma mais clara a **componentização** do Vue.

------------------------------------------------------------------------

# 🧠 Conceitos Vue utilizados

  Conceito           Utilização no projeto
  ------------------ ---------------------------------
  `ref()`            Armazenar busca e filtro
  `computed()`       Criar lista filtrada
  `v-model`          Capturar pesquisa
  `v-for`            Gerar cards
  `:key`             Identificar elementos da lista
  `:src`             Vincular URL das imagens
  `{{ }}`            Exibir dados
  Componentes        Organização da aplicação
  `<script setup>`   Código TypeScript do componente
  `<template>`       Estrutura HTML
  `<style>`          Estilização
  CSS Grid           Grade de Pokémon
  Media Query        Responsividade

------------------------------------------------------------------------

# 🔄 Fluxo da aplicação Vue

``` text
              ┌──────────────┐
              │    App.vue   │
              └──────┬───────┘
                     │
          ┌──────────┼──────────┐
          ↓          ↓          ↓
       Header       Hero     Pokédex
                               │
                         ┌─────┴─────┐
                         ↓           ↓
                      Busca       Filtro
                         │           │
                         └─────┬─────┘
                               ↓
                         computed()
                               ↓
                           v-for
                               ↓
                       Pokemon Cards
```

------------------------------------------------------------------------

# 💻 Comandos essenciais da aula

## Node.js

Verificar versão:

``` bash
node --version
```

## NPM

Instalar dependências:

``` bash
npm install
```

## React

Criar:

``` bash
npx create-react-app meu-projeto-react
```

Executar:

``` bash
npm start
```

## Angular

Instalar CLI:

``` bash
npm install -g @angular/cli
```

Criar:

``` bash
ng new meu-app-angular
```

Executar:

``` bash
ng serve
```

## Vue

Criar:

``` bash
npm create vue@latest
```

Instalar:

``` bash
npm install
```

Executar:

``` bash
npm run dev
```

## Git

Clonar projeto:

``` bash
git clone <url>
```

------------------------------------------------------------------------

# 🧪 Checklist da aula

### Node.js / NPM

-   [x] Entender o Node.js
-   [x] Entender o NPM
-   [x] Conhecer `package.json`
-   [x] Conhecer `node_modules`

### React

-   [x] Conhecer a proposta
-   [x] Criar projeto
-   [x] Conhecer estrutura básica

### Angular

-   [x] Conhecer a proposta
-   [x] Conhecer Angular CLI
-   [x] Criar projeto
-   [x] Conhecer estrutura básica

### Vue

-   [x] Conhecer a proposta
-   [x] Criar projeto
-   [x] Conhecer SFC
-   [x] Conhecer `App.vue`
-   [x] Conhecer `components`
-   [x] Executar com Vite
-   [x] Criar aplicação prática

### Projeto HoennDex

-   [x] Criar interface
-   [x] Adicionar Pokémon
-   [x] Adicionar imagens
-   [x] Criar cards
-   [x] Criar busca
-   [x] Criar filtro
-   [x] Criar seção sobre Hoenn
-   [x] Tornar layout responsivo
-   [x] Corrigir largura do `#app`

### Atividade acadêmica

-   [ ] Criar projeto React
-   [ ] Criar projeto Angular
-   [ ] Criar projeto Vue
-   [ ] Criar/importar template
-   [ ] Versionar projetos com Git
-   [ ] Criar quatro repositórios
-   [ ] Fazer deploy dos quatro projetos
-   [ ] Documentar com prints e links

------------------------------------------------------------------------

# 🧊 Resumo final

## O que é Node.js?

Ambiente de execução JavaScript que permite executar JavaScript fora do
navegador, inclusive no servidor.

## O que é NPM?

Gerenciador de pacotes utilizado para instalar e administrar
dependências.

## O que é React?

Biblioteca para construção de interfaces, destacada pela flexibilidade e
componentização.

## O que é Angular?

Framework completo que fornece diversos recursos para construção de
aplicações.

## O que é Vue?

Framework progressivo que trabalha com reatividade e componentes.

## O que é um componente?

Uma parte reutilizável da interface.

``` text
Aplicação
   ↓
Componentes
   ↓
Interface organizada
```

## O que é reatividade?

É a capacidade da interface de acompanhar alterações nos dados e
atualizar a visualização.

Na HoennDex:

``` text
Usuário digita
      ↓
v-model
      ↓
ref()
      ↓
computed()
      ↓
lista atualizada
```

## O que é `v-for`?

Uma diretiva Vue utilizada para renderizar uma estrutura repetidamente a
partir de uma lista.

## O que é `v-model`?

Uma diretiva que cria uma ligação entre o valor de um elemento de
formulário e um dado reativo.

## O que é `computed()`?

Uma forma de criar valores derivados de outros dados reativos.

------------------------------------------------------------------------

# 📚 Referências da aula

-   Material da aula: **Aula 06 --- Atividade com Projetos Front-end**,
    Prof. Me. Deivison S. Takatu.
-   Node.js --- material indicado na aula.
-   React --- documentação indicada na aula.
-   Angular --- documentação indicada na aula.
-   Vue --- documentação indicada na aula.
-   GitHub --- ferramenta indicada para pesquisa e versionamento.
-   Vercel --- plataforma indicada para templates e deploy.
-   CodeSandbox --- ferramenta indicada para pesquisa de templates.

------------------------------------------------------------------------

# ❄️ Conclusão

A aula apresentou o ecossistema necessário para sair de uma página
Front-end simples e começar a trabalhar com **frameworks e ferramentas
modernas**.

O fluxo mais importante para guardar é:

``` text
                NODE.JS
                   ↓
                 NPM
                   ↓
       ┌───────────┼───────────┐
       ↓           ↓           ↓
     React      Angular       Vue
       │           │           │
       └───────────┼───────────┘
                   ↓
              Projeto Web
                   ↓
                 Git
                   ↓
                GitHub
                   ↓
                Vercel
                   ↓
             🌐 Aplicação
```

> **Ideia central:** aprender um framework não significa apenas conhecer
> sua sintaxe. É necessário entender também a estrutura do projeto,
> gerenciamento de dependências, componentes, versionamento e publicação
> da aplicação.
