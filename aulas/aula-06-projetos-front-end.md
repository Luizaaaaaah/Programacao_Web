# Aula 06 — Atividade com Projetos Front-end

**Disciplina:** Programação Web  
**Professor:** Prof. Me. Deivison S. Takatu  
**Curso:** Análise e Desenvolvimento de Sistemas  
**Instituição:** Fatec Itapetininga  
**Ano:** 2026

---

## Sumário

1. [Introdução](#1-introdução)
2. [Instalação do Node.js](#2-instalação-do-nodejs)
3. [Node Package Manager (NPM)](#3-node-package-manager-npm)
4. [Criando um projeto React](#4-criando-um-projeto-react)
5. [Estrutura de um projeto React](#5-estrutura-de-um-projeto-react)
6. [Criando um projeto Angular](#6-criando-um-projeto-angular)
7. [Conceitos fundamentais do Angular](#7-conceitos-fundamentais-do-angular)
8. [Estrutura de um projeto Angular](#8-estrutura-de-um-projeto-angular)
9. [Criando um projeto Vue](#9-criando-um-projeto-vue)
10. [Estrutura de um projeto Vue](#10-estrutura-de-um-projeto-vue)
11. [Importação de projetos e templates](#11-importação-de-projetos-e-templates)
12. [Atividade proposta](#12-atividade-proposta)
13. [Conclusão](#13-conclusão)
14. [Referências](#14-referências)

---

## 1. Introdução

A Aula 06 foi dedicada à criação e configuração de projetos utilizando três tecnologias de desenvolvimento front-end: **React, Angular e Vue.js**.

O objetivo foi compreender os requisitos, os comandos de inicialização e as principais estruturas de arquivos utilizadas por cada tecnologia.

Também foi apresentada a possibilidade de importar projetos e templates existentes para personalizá-los, utilizando ferramentas como GitHub, Vercel e CodeSandbox.

## 2. Instalação do Node.js

O **Node.js** é um ambiente de execução que permite utilizar JavaScript fora do navegador, inclusive no desenvolvimento de aplicações back-end.

Com ele, é possível utilizar JavaScript tanto no cliente quanto no servidor, favorecendo a integração entre as diferentes partes de uma aplicação web.

### Procedimento apresentado

1. Acessar o site oficial do Node.js.
2. Selecionar a versão correspondente ao sistema operacional.
3. Baixar e executar o instalador.
4. Seguir as instruções até concluir a instalação.
5. Abrir o Prompt de Comando para verificar a instalação.

**Site oficial:** https://nodejs.org/en/download

### Verificação

```bash
node --version
```

Quando a instalação está correta, o comando informa a versão instalada.

## 3. Node Package Manager (NPM)

O **NPM (Node Package Manager)** é o gerenciador de pacotes utilizado com o Node.js.

Ele permite:

- Instalar bibliotecas e frameworks;
- Atualizar dependências;
- Remover pacotes;
- Gerenciar módulos;
- Compartilhar pacotes;
- Automatizar o gerenciamento das dependências do projeto.

### package.json

O arquivo `package.json` contém informações sobre o projeto, suas dependências e os scripts disponíveis.

### Instalando dependências

```bash
npm install
```

O comando instala os pacotes necessários de acordo com as dependências definidas no projeto.

O uso do NPM facilita a configuração do ambiente e a colaboração entre desenvolvedores.

## 4. Criando um projeto React

O **React** é uma biblioteca JavaScript utilizada na criação de interfaces de usuário.

### Requisitos apresentados

- Node.js instalado;
- Conhecimento em JSX;
- Conhecimento em Hooks, como `useState` e `useEffect`.

### Destaques do React

**Flexibilidade:** permite diferentes formas de organização e integração.

**Ecossistema:** possui ferramentas e bibliotecas complementares, como Redux, React Router e Next.js.

**Componentização:** facilita a reutilização dos elementos da interface.

**Virtual DOM:** auxilia na atualização eficiente dos componentes.

**Comunidade ativa:** disponibiliza documentação, tutoriais e soluções compartilhadas.

### Procedimento de criação

**Passo 1 — Criar o projeto**

```bash
npx create-react-app meu-projeto-react
```

**Passo 2 — Entrar na pasta**

```bash
cd meu-projeto-react
```

**Passo 3 — Abrir no Visual Studio Code**

```bash
code .
```

**Passo 4 — Iniciar o servidor de desenvolvimento**

```bash
npm start
```

Esses comandos correspondem ao procedimento demonstrado nos slides da aula.

### Documentação apresentada

- JSX: https://react.dev/learn/writing-markup-with-jsx
- Hooks: https://react.dev/reference/react/hooks

## 5. Estrutura de um projeto React

Durante a aula, o professor apresentou os principais diretórios e arquivos utilizados em um projeto criado com React.

### Diretórios

| Diretório | Finalidade |
|---|---|
| `node_modules` | Armazena as bibliotecas e dependências instaladas. |
| `public` | Contém arquivos públicos, como HTML, JSON e imagens. |
| `src` | Armazena os arquivos da aplicação React. |

### Arquivos de configuração

- **.gitignore:** identifica arquivos e diretórios que não devem ser enviados ao Git.
- **package.json:** registra informações, dependências e scripts.
- **package-lock.json:** registra informações sobre as dependências instaladas.

### Arquivos principais

| Arquivo | Finalidade |
|---|---|
| `index.js` | Ponto de entrada responsável pela renderização da aplicação. |
| `App.js` | Componente principal da interface. |
| `App.css` | Estilos associados ao componente App. |
| `index.css` | Estilos globais da aplicação. |

Essa estrutura corresponde ao exemplo apresentado pelo professor.

## 6. Criando um projeto Angular

O **Angular** é um framework utilizado para desenvolver aplicações web.

### Requisitos apresentados

- Node.js instalado;
- Conhecimento de programação orientada a objetos.

### Principais características

**Framework completo:** oferece soluções para roteamento, requisições HTTP e injeção de dependências.

**TypeScript:** utiliza recursos de tipagem para organizar o desenvolvimento.

**Arquitetura:** permite separar responsabilidades em componentes e serviços.

**Angular CLI:** ferramenta de linha de comando que facilita a criação e manutenção dos projetos.

**Change Detection:** mecanismo utilizado para acompanhar alterações e atualizar a interface.

### Procedimento de criação

**Passo 1 — Instalar o Angular CLI**

```bash
npm install -g @angular/cli
```

**Passo 2 — Criar o projeto**

```bash
ng new meu-app-angular
```

**Passo 3 — Entrar na pasta**

```bash
cd meu-app-angular
```

**Passo 4 — Abrir no Visual Studio Code**

```bash
code .
```

**Passo 5 — Iniciar o servidor de desenvolvimento**

```bash
ng serve
```

### Documentação apresentada

https://angular.dev/cli/generate/class

## 7. Conceitos fundamentais do Angular

O professor apresentou alguns recursos utilizados na organização das aplicações Angular.

### Componentes

Os componentes definem partes da interface e podem reunir HTML, CSS e TypeScript.

O material apresenta o decorador `@Component` para sua definição.

### Módulos

O material apresenta `@NgModule` como um recurso de organização da aplicação em blocos funcionais.

### Serviços

Os serviços permitem reutilizar funcionalidades e organizar a lógica da aplicação.

O decorador `@Injectable` foi apresentado nesse contexto.

### Data Binding

O Data Binding estabelece a comunicação entre os dados e a interface.

Exemplos apresentados:

- `[(ngModel)]`: associação bidirecional de dados;
- `{{ }}`: interpolação para exibir valores.

### Injeção de dependências

Permite disponibilizar e compartilhar recursos entre partes da aplicação, utilizando uma estrutura de provedores.

### Roteamento

O material apresenta `RouterModule` como recurso utilizado para organizar a navegação entre diferentes visualizações.

## 8. Estrutura de um projeto Angular

### Diretórios principais

| Diretório | Finalidade |
|---|---|
| `node_modules` | Pacotes e dependências instalados. |
| `public` | Arquivos estáticos acessíveis publicamente. |
| `src` | Código-fonte principal da aplicação. |
| `.angular` | Cache e arquivos temporários gerados pelo Angular CLI. |
| `.vscode` | Configurações do Visual Studio Code. |
| `app` | Componentes, serviços e outros arquivos da aplicação. |

### Arquivos de configuração

**.gitignore:** identifica os arquivos e diretórios ignorados pelo Git.

**package.json e package-lock.json:** registram informações sobre dependências e scripts.

**.editorconfig:** estabelece regras de formatação.

**README.md:** documenta informações do projeto.

**angular.json:** contém configurações relacionadas ao Angular, como build, testes e estilos.

**tsconfig.json:** define configurações gerais do TypeScript.

**tsconfig.app.json:** define configurações específicas da aplicação.

**tsconfig.spec.json:** define configurações relacionadas aos testes.

### Arquivos da aplicação

| Arquivo | Finalidade apresentada |
|---|---|
| `index.html` | Documento HTML que contém o elemento utilizado para montar a aplicação. |
| `main.ts` | Inicialização da aplicação Angular. |
| `main.server.ts` | Inicialização associada à renderização no servidor. |
| `server.ts` | Configuração relacionada à execução no servidor. |
| `styles.css` | Estilos globais da aplicação. |

**Observação:** a estrutura efetiva pode variar conforme a versão do Angular e as opções selecionadas ao criar o projeto. A tabela registra os arquivos abordados nos slides.

## 9. Criando um projeto Vue

O **Vue.js** é um framework progressivo utilizado no desenvolvimento de interfaces web.

### Requisitos apresentados

- Node.js instalado;
- Conhecimento em JavaScript ou TypeScript;
- Noções de programação reativa;
- Conhecimento de componentes.

### Principais características

**Progressivo:** permite adoção gradual.

**Reatividade:** atualiza a interface conforme mudanças nos dados.

**Single-File Components (SFC):** permitem reunir estrutura, lógica e estilos em arquivos `.vue`.

**Aprendizado:** apresenta uma sintaxe acessível para diferentes níveis de experiência.

### Procedimento de criação

**Passo 1 — Criar o projeto**

```bash
npm create vue@latest
```

**Passo 2 — Entrar na pasta do projeto**

```bash
cd meu-projeto-vue
```

**Passo 3 — Instalar as dependências**

```bash
npm install
```

**Passo 4 — Abrir no Visual Studio Code**

```bash
code .
```

**Passo 5 — Iniciar o servidor de desenvolvimento**

```bash
npm run dev
```

O nome da pasta utilizado no segundo passo corresponde ao exemplo do professor e deve ser ajustado ao nome escolhido durante a criação do projeto.

### Documentação apresentada

https://vuejs.org/guide/introduction.html

## 10. Estrutura de um projeto Vue

### Diretórios

| Diretório | Finalidade |
|---|---|
| `node_modules` | Armazena as dependências instaladas. |
| `public` | Arquivos estáticos disponibilizados sem processamento pelo Vite. |
| `src` | Código-fonte principal da aplicação. |
| `.vscode` | Configurações do editor. |
| `assets` | Imagens, fontes e arquivos de estilo. |
| `components` | Componentes Vue reutilizáveis. |

### Arquivos de configuração

**.gitignore:** define os arquivos ignorados pelo Git.

**package.json:** contém informações, scripts e dependências.

**package-lock.json:** registra as dependências instaladas.

**vite.config.js:** reúne configurações do Vite, incluindo build e plugins.

### Arquivos principais

| Arquivo | Finalidade |
|---|---|
| `App.vue` | Componente principal da aplicação. |
| `main.js` | Ponto de entrada do Vue, utilizado para montar a aplicação. |
| `index.html` | Arquivo HTML que contém o elemento onde a aplicação é montada. |

No exemplo apresentado, o `index.html` contém o elemento `#app`, utilizado para montar a interface Vue.

## 11. Importação de projetos e templates

A aula também abordou a utilização de projetos existentes como ponto de partida para novas aplicações.

A comunidade de código aberto disponibiliza exemplos que podem ser estudados, adaptados e personalizados.

### Ferramentas apresentadas

**GitHub**

Permite pesquisar repositórios e encontrar projetos criados com diferentes tecnologias.

**Vercel**

Disponibiliza templates que podem servir como base para novas aplicações.

**CodeSandbox**

Oferece ferramentas para pesquisar e experimentar projetos e templates.

### Importação por Git

O material apresenta o comando:

```bash
git clone <url>
```

Ele permite criar uma cópia local de um repositório remoto.

### Cuidados com a utilização de templates

**Complemento:** ao importar um projeto, é importante verificar suas dependências, instruções de uso e licença antes de realizar alterações ou reutilizar o código.

### Ferramentas

- GitHub: https://github.com/
- Vercel: https://vercel.com/
- CodeSandbox: https://codesandbox.io/

## 12. Atividade proposta

A atividade prática da Aula 06 exige a criação e publicação de **quatro projetos front-end**.

### Etapa 1 — Criar três projetos

Desenvolver três projetos iniciais utilizando as tecnologias estudadas:

1. React;
2. Angular;
3. Vue.js.

Para cada projeto, realizar alterações iniciais no código e utilizar o Git para registrar as modificações.

Os três projetos deverão ser publicados em **repositórios diferentes no GitHub**.

### Etapa 2 — Importar e personalizar um template

Pesquisar um template desenvolvido com uma das tecnologias estudadas.

Em seguida:

1. Selecionar o template;
2. Importar o projeto;
3. Personalizar seu conteúdo;
4. Registrar as alterações com Git;
5. Publicar em um quarto repositório no GitHub.

### Etapa 3 — Publicar os quatro projetos

Realizar o deploy dos quatro projetos na Vercel:

| Projeto | Plataforma de deploy |
|---|---|
| React | Vercel |
| Angular | Vercel |
| Vue.js | Vercel |
| Template personalizado | Vercel |

### Etapa 4 — Documentar a atividade

Organizar toda a atividade em **um único arquivo de documentação**.

O documento deverá incluir:

- Descrição das etapas realizadas;
- Explicação das alterações;
- Prints das telas;
- Links dos quatro repositórios no GitHub;
- Links dos quatro projetos publicados na Vercel.

A documentação deverá registrar as atividades efetivamente desenvolvidas e os resultados obtidos.

## 13. Conclusão

A Aula 06 apresentou os procedimentos para criar e configurar aplicações utilizando React, Angular e Vue.js.

Foram estudados os requisitos, comandos de inicialização, estruturas de diretórios e principais arquivos de cada tecnologia.

Também foi apresentada a importação de projetos e templates como alternativa para acelerar o desenvolvimento.

A atividade prática reforçou a importância do versionamento com Git, da organização dos repositórios no GitHub, da publicação na Vercel e da documentação das etapas de desenvolvimento.

## 14. Referências

DINIZ, Luciana Mara Freitas et al. Aprendizado baseado em projetos em IHC (presencial e remoto): prototipação segundo as heurísticas de Nielsen. In: **SIMPÓSIO BRASILEIRO DE FATORES HUMANOS EM SISTEMAS COMPUTACIONAIS (IHC)**, 2020. Anais [...]. SBC, 2020. p. 13-18.

FERREIRA, Arthur Gonçalves. **Interface de programação de aplicações (API) e web services**. São Paulo: Platos Soluções Educacionais, 2021.

GONÇALVES, Rodrigo Franco et al. Uma proposta de processo de produção de aplicações Web. **Production**, v. 15, p. 376-389, 2005.

LUCASSEN, Garm et al. The use and effectiveness of user stories in practice. In: **REQUIREMENTS ENGINEERING: FOUNDATION FOR SOFTWARE QUALITY (REFSQ)**, 22., 2016, Gothenburg. Proceedings [...]. Springer International Publishing, 2016. p. 205-222.

MACDONALD, Matthew. **WordPress: the missing manual**. 3. ed. Sebastopol: O'Reilly Media, 2020.

MESSENLEHNER, Brian; COLEMAN, Jason. **Building Web Apps with WordPress: WordPress as an Application Framework**. 2. ed. Sebastopol: O'Reilly Media, 2019.

MILETTO, Evandro Manara; DE CASTRO BERTAGNOLLI, Silvia. **Desenvolvimento de Software II: introdução ao desenvolvimento web com HTML, CSS, JavaScript e PHP**. [S. l.]: Bookman, 2014.

NGUYEN, Hong-Thu Thi. Website Builder as an Assistive Technology Tool for Reflection, Collaboration and Skills Development in Learning ESP. **Journal of Learning for Development**, v. 11, n. 1, p. 138-150, 2024.

OLIVEIRA, Cláudio Luís Vieira. **Node.js: programe de forma rápida e prática**. São Paulo: Expressa, 2021.

PANTHEON. **WebOps Platform for Drupal & WordPress Hosting**. Disponível em: https://pantheon.io/.

RANJAN, Alok; SINHA, Abhilasha; BATTEWAD, Ranjit. **JavaScript for Modern Web Development**. [S. l.]: BPB Publications, 2020.

SALINAS, C. et al. Agile, Web Engineering and Capability Maturity Model Integration: a systematic literature review. **Information and Software Technology**, v. 71, p. 92-107, 2016. DOI: 10.1016/j.infsof.2015.11.002.

W3TECHS. **Usage statistics and market share of content management systems**. Disponível em: https://w3techs.com/.

WILDT, Daniel et al. **Extreme Programming: práticas para o dia a dia no desenvolvimento ágil de software**. São Paulo: Casa do Código, 2015.

WORDPRESS. **WordPress — crie um site ou blog gratuitamente**. Disponível em: https://wordpress.org/.

ZABOT, Diego. **Aplicativos com Bootstrap e Angular: como desenvolver apps responsivos**. São Paulo: Érica, 2020.

---

**Complemento — Navegação do repositório**

- [Documentação da Atividade 06](../atividades/aula-06/README.md)
- [Índice das aulas](README.md)
- [Página principal do repositório](../README.md)