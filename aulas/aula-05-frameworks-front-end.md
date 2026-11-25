# Aula 05 — Introdução a Frameworks Front-end

**Disciplina:** Programação Web  
**Professor:** Prof. Me. Deivison S. Takatu  
**Curso:** Análise e Desenvolvimento de Sistemas  
**Instituição:** Fatec Itapetininga  
**Ano:** 2026

---

## Sumário

1. [Introdução aos frameworks front-end](#1-introdução-aos-frameworks-front-end)
2. [Diferenças entre framework e biblioteca](#2-diferenças-entre-framework-e-biblioteca)
3. [Vantagens dos frameworks](#3-vantagens-dos-frameworks)
4. [React, Angular e Vue.js](#4-react-angular-e-vuejs)
5. [Características dos frameworks front-end](#5-características-dos-frameworks-front-end)
6. [Comparação entre tecnologias](#6-comparação-entre-tecnologias)
7. [Introdução ao React](#7-introdução-ao-react)
8. [Conceitos fundamentais do React](#8-conceitos-fundamentais-do-react)
9. [DOM e Virtual DOM](#9-dom-e-virtual-dom)
10. [Node.js e NPM](#10-nodejs-e-npm)
11. [Criando um projeto React](#11-criando-um-projeto-react)
12. [Estrutura de um projeto React](#12-estrutura-de-um-projeto-react)
13. [Publicação no GitHub](#13-publicação-no-github)
14. [Atividade proposta](#14-atividade-proposta)
15. [Conclusão](#15-conclusão)
16. [Referências](#16-referências)

---

## 1. Introdução aos frameworks front-end

Um **framework front-end** é um conjunto de ferramentas, bibliotecas e convenções que fornece uma estrutura para desenvolver interfaces web.

Seu objetivo é padronizar o desenvolvimento, facilitar a organização do código e agilizar a construção de aplicações.

### Desenvolvimento com Vanilla JavaScript

O Vanilla JavaScript corresponde à utilização do JavaScript puro, sem frameworks ou bibliotecas adicionais.

Nesse modelo, o desenvolvedor é responsável por implementar manualmente diversos comportamentos da aplicação.

### Desenvolvimento com frameworks

A utilização de frameworks e bibliotecas modernas permite:

- Criar componentes reutilizáveis;
- Organizar melhor o código;
- Gerenciar o estado da aplicação;
- Atualizar interfaces de maneira eficiente;
- Facilitar a manutenção dos projetos.

## 2. Diferenças entre framework e biblioteca

Embora os dois conceitos estejam relacionados, frameworks e bibliotecas possuem características diferentes.

| Framework | Biblioteca |
|---|---|
| Define uma estrutura para a aplicação. | Disponibiliza funções e recursos reutilizáveis. |
| Controla parte do fluxo de execução. | O desenvolvedor controla quando utilizar seus recursos. |
| Estabelece convenções de desenvolvimento. | Oferece maior liberdade de integração. |
| Exemplos: Angular e Vue.js. | Exemplos: React e jQuery. |

### Exemplo apresentado na aula

Com uma biblioteca, o desenvolvedor chama os recursos necessários para executar determinadas operações.

Já um framework estabelece uma estrutura de funcionamento e controla parte do ciclo da aplicação.

Essa diferença está relacionada ao conceito de **inversão de controle**.

## 3. Vantagens dos frameworks

Os frameworks front-end oferecem recursos que facilitam o desenvolvimento e a manutenção de aplicações.

### Produtividade

Fornecem soluções e ferramentas para tarefas comuns, reduzindo a necessidade de desenvolver tudo do início.

### Organização do código

Favorecem a utilização de componentes e padrões de desenvolvimento.

### Manutenção

Recursos internos de atualização de interface ajudam a controlar as mudanças na aplicação.

### Comunidade

As tecnologias populares possuem documentação, tutoriais, plugins e comunidades de desenvolvedores.

Essas características contribuem para a criação de aplicações organizadas e escaláveis.

## 4. React, Angular e Vue.js

Durante a aula, foram apresentadas três tecnologias utilizadas no desenvolvimento front-end.

### React

Biblioteca JavaScript desenvolvida pelo Facebook, utilizada para construir interfaces por meio de componentes reutilizáveis.

Apesar de ser frequentemente chamada de framework, o material destaca que o React é tecnicamente uma **biblioteca**.

### Angular

Framework desenvolvido pelo Google, com recursos para a construção de aplicações web, incluindo aplicações de página única.

### Vue.js

Framework progressivo que pode ser adotado gradualmente conforme as necessidades da aplicação.

### Comparação

| Tecnologia | Classificação apresentada | Característica |
|---|---|---|
| React | Biblioteca | Construção de interfaces baseadas em componentes. |
| Angular | Framework | Estrutura abrangente para aplicações web. |
| Vue.js | Framework progressivo | Adaptação gradual e construção de interfaces. |

O professor também apresentou o Google Trends como ferramenta de consulta e comparação de tendências.

**Ferramenta:** https://trends.google.com.br/

## 5. Características dos frameworks front-end

### Estrutura organizada

Frameworks front-end ajudam a organizar os arquivos e os elementos que compõem uma aplicação.

### Componentização

Os componentes são partes independentes e reutilizáveis de uma interface.

Eles podem reunir apresentação e lógica, facilitando a manutenção do projeto.

### Programação reativa

Permite atualizar a interface conforme ocorrem mudanças no estado da aplicação, reduzindo a necessidade de manipular manualmente os elementos do DOM.

### Ferramentas de build e bundling

São utilizadas para processar e organizar os arquivos da aplicação, incluindo tarefas como:

- Minificação;
- Transpilação;
- Agrupamento de arquivos.

### Sistema de rotas

Permite organizar a navegação entre as diferentes telas ou seções de uma aplicação.

Esse recurso é importante nas **Single Page Applications (SPAs)**.

### Integração com APIs

Facilita a comunicação com serviços externos e a utilização de dados nas interfaces.

### Documentação e comunidade

As tecnologias populares oferecem recursos de aprendizado e suporte para desenvolvedores.

### Design e acessibilidade

Os frameworks podem auxiliar na aplicação de padrões visuais e práticas de acessibilidade.

### Suporte a testes

Ferramentas de testes unitários e de integração ajudam a verificar o funcionamento das aplicações.

## 6. Comparação entre tecnologias

A escolha de uma tecnologia front-end deve considerar as necessidades do projeto.

Entre os fatores apresentados estão:

- Complexidade da aplicação;
- Curva de aprendizado;
- Desempenho;
- Escalabilidade;
- Facilidade de manutenção;
- Experiência do usuário;
- Suporte da comunidade.

Durante a aula, foi apresentada a plataforma StackShare para comparação de tecnologias.

**Ferramenta:** https://stackshare.io/stackups

## 7. Introdução ao React

O **React** é uma biblioteca JavaScript utilizada na criação de interfaces de usuário dinâmicas e interativas.

Segundo o material apresentado, foi desenvolvido pelo Facebook em 2013.

### Principais características

- Construção de interfaces por componentes;
- Reutilização de código;
- Atualizações eficientes da interface;
- Organização da aplicação;
- Utilização do Virtual DOM.

Para trabalhar com React, é importante conhecer os fundamentos de HTML e JavaScript.

## 8. Conceitos fundamentais do React

### JSX

O **JSX** permite escrever uma sintaxe semelhante ao HTML dentro do código JavaScript.

O material destaca algumas diferenças entre JSX e HTML:

- Expressões JavaScript podem ser inseridas entre chaves `{}`;
- Alguns atributos utilizam a convenção camelCase;
- `className` é utilizado no lugar de `class`;
- Elementos precisam ser corretamente fechados.

### Hooks

Hooks são recursos utilizados em componentes funcionais do React.

**useState**

Permite criar e atualizar estados dentro de um componente.

**useEffect**

Permite lidar com efeitos, como a comunicação com APIs.

### Gerenciamento de estado

O estado representa informações que podem mudar durante a utilização da aplicação.

Foram apresentadas duas alternativas de gerenciamento:

- **Context API:** recurso para compartilhar informações entre componentes;
- **Redux:** biblioteca utilizada para gerenciamento de estados, especialmente em aplicações mais complexas.

## 9. DOM e Virtual DOM

### DOM — Document Object Model

O DOM é uma representação em árvore dos elementos de uma página web.

Por meio dele, o JavaScript consegue acessar e modificar o conteúdo e a estrutura de uma página.

### Virtual DOM

O **Virtual DOM** é uma representação utilizada pelo React para acompanhar mudanças na interface.

Quando o estado de um componente muda, o React compara as representações e identifica quais atualizações precisam ser aplicadas ao DOM.

Essa abordagem auxilia na atualização eficiente das interfaces.

## 10. Node.js e NPM

### Node.js

O **Node.js** é um ambiente de execução que permite executar JavaScript fora do navegador, incluindo aplicações no servidor.

Sua utilização permite trabalhar com JavaScript tanto no front-end quanto no back-end.

**Site oficial:** https://nodejs.org/en/download

### Instalação

O procedimento apresentado pelo professor foi:

1. Acessar o site oficial;
2. Selecionar a versão para o sistema operacional;
3. Executar o instalador;
4. Concluir a instalação;
5. Verificar a versão instalada.

Comando de verificação:

`node --version`

### NPM — Node Package Manager

O **NPM** é o gerenciador de pacotes utilizado no ambiente Node.js.

Ele permite instalar, atualizar e gerenciar bibliotecas e dependências.

### Arquivo package.json

O arquivo `package.json` registra informações do projeto, suas dependências e scripts.

### Instalando dependências

O comando apresentado na aula foi:

`npm install`

Ele permite instalar as dependências definidas no projeto.

## 11. Criando um projeto React

Durante a aula, o professor demonstrou a criação de um projeto React utilizando o **Create React App**.

### Passo 1 — Criar o projeto

`npx create-react-app meu-projeto-react`

O comando cria uma estrutura inicial para desenvolvimento com React.

O material apresenta recursos como Webpack, Babel, servidor de desenvolvimento e scripts de build e teste.

### Passo 2 — Acessar a pasta

`cd meu-projeto-react`

### Passo 3 — Abrir no Visual Studio Code

`code .`

### Passo 4 — Iniciar o servidor local

`npm start`

Esse comando inicia o ambiente de desenvolvimento para visualizar a aplicação no navegador.

Os comandos foram registrados conforme o procedimento apresentado nos slides da Aula 05.

## 12. Estrutura de um projeto React

O professor apresentou os principais arquivos e diretórios criados no projeto.

### Diretórios

| Diretório | Finalidade |
|---|---|
| node_modules | Armazena os pacotes e dependências instalados. |
| public | Contém arquivos públicos, como HTML e imagens. |
| src | Contém os arquivos utilizados no desenvolvimento da aplicação React. |

### Arquivos de configuração

**package.json:** informações, scripts e dependências do projeto.

**package-lock.json:** registra informações sobre as versões das dependências instaladas.

**.gitignore:** define quais arquivos e diretórios devem ser ignorados pelo Git.

### Arquivos da aplicação

| Arquivo | Finalidade |
|---|---|
| index.js | Ponto de entrada utilizado para renderizar a aplicação React. |
| App.js | Componente principal da aplicação. |
| App.css | Estilos associados ao componente App. |
| index.css | Estilos globais da aplicação. |

Essa estrutura corresponde ao exemplo de projeto apresentado durante a aula.

## 13. Publicação no GitHub

Após criar o projeto, o professor apresentou a publicação dos arquivos em um repositório no GitHub.

### Etapas apresentadas

1. Abrir o projeto no Visual Studio Code;
2. Acessar a aba de controle de código-fonte;
3. Realizar o commit das alterações;
4. Selecionar a opção de publicar a branch;
5. Autenticar-se no GitHub;
6. Definir a visibilidade do repositório;
7. Confirmar a publicação;
8. Verificar os arquivos no GitHub.

O uso do GitHub permite registrar o histórico e disponibilizar o código do projeto.

## 14. Atividade proposta

A atividade prática da Aula 05 consiste em criar um projeto React com cinco funcionalidades.

### Etapa 1 — Desenvolvimento do projeto

Criar uma aplicação React contendo um **cabeçalho que liste as seguintes funcionalidades**:

1. **To-Do List:** lista de tarefas;
2. **Contador de Cliques:** registro da quantidade de cliques;
3. **Jogo da Velha:** jogo interativo;
4. **Calculadora:** realização de operações matemáticas;
5. **Buscador de CEP:** consulta de informações a partir de um CEP.

### Etapa 2 — Versionamento e deploy

Após o desenvolvimento:

1. Utilizar o Git para registrar as alterações;
2. Realizar o commit no GitHub;
3. Conectar o repositório à Vercel;
4. Fazer o deploy;
5. Disponibilizar a aplicação online.

### Etapa 3 — Documentação

Documentar os elementos desenvolvidos no projeto, incluindo as escolhas de estilização.

### Etapa 4 — Entrega

Organizar um documento contendo:

- Descrição das etapas realizadas;
- Explicação das funcionalidades;
- Justificativa da estilização;
- Prints das telas;
- Link do repositório no GitHub;
- Link do site publicado na Vercel.

O documento deverá ser submetido conforme as orientações do professor.

## 15. Conclusão

A Aula 05 apresentou os fundamentos dos frameworks front-end e suas principais características.

Foram estudadas as diferenças entre frameworks e bibliotecas, além de uma introdução às tecnologias React, Angular e Vue.js.

A aula também abordou componentes, JSX, Hooks, DOM, Virtual DOM, Node.js, NPM e a estrutura inicial de um projeto React.

A atividade prática propôs aplicar esses conhecimentos no desenvolvimento de uma interface com cinco funcionalidades, versionamento no GitHub e publicação na Vercel.

## 16. Referências

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

**Observação:** Os slides também citam Banks e Porcello (2017), Aggarwal et al. (2018) e Rahat et al. (2023), mas não apresentam os dados bibliográficos completos dessas obras.

---

**Complemento — Navegação do repositório**

- [Documentação da Atividade 05](../atividades/aula-05/README.md)
- [Índice das aulas](README.md)
- [Página principal do repositório](../README.md)