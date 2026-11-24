# Aula 08 — Atividade com projetos back-end

**Professor:** Prof. Me. Deivison S. Takatu  
**Disciplina:** Programação Web

## Visão geral

A aula retomou HTTP, métodos REST e JSON e avançou para uma API de notas criada com Express.js. A prática envolve operações CRUD, armazenamento em arquivo JSON, integração com front-end React, deploy e documentação da API no Postman.

## Conteúdo estudado

### Organização do back-end

A apresentação retomou MVC e arquitetura em camadas, separando regras de negócio, rotas e acesso aos dados. A componentização em módulos, serviços e middlewares favorece reutilização e manutenção.

### HTTP, REST e JSON

* **GET:** consulta recursos.
* **POST:** cria recursos.
* **PUT:** substitui os dados de um recurso.
* **PATCH:** altera parcialmente os dados.
* **DELETE:** remove um recurso.

JSON é o formato usado para trocar dados entre a API e o front-end, por meio de objetos e arrays.

### Hospedagem com Render

O Render foi apresentado como plataforma de hospedagem de serviços, com integração ao GitHub. O fluxo prático é enviar o código ao repositório, criar um Web Service, conectar a origem e configurar o comando de inicialização.

### API de notas com Express

A aplicação de exemplo utiliza server.js para configurar o servidor e data.json como arquivo de armazenamento. O módulo fs lê e grava o conteúdo; o middleware de parsing permite receber JSON no corpo das requisições.

As rotas apresentadas são:

|Método|Endpoint|Operação|
|-|-|-|
|GET|/api/notes|Listar notas|
|POST|/api/notes|Criar nota|
|PUT|/api/notes/:id|Atualizar nota|
|DELETE|/api/notes/:id|Excluir nota|

\# Aula 08 — Atividade com Projetos Back-end



\*\*Disciplina:\*\* Programação Web  

\*\*Professor:\*\* Prof. Me. Deivison S. Takatu  

\*\*Curso:\*\* Análise e Desenvolvimento de Sistemas  

\*\*Instituição:\*\* Fatec Itapetininga  

\*\*Ano:\*\* 2026



\---



\## Sumário



1\. \[Introdução](#1-introdução)

2\. \[Fundamentos de frameworks back-end](#2-fundamentos-de-frameworks-back-end)

3\. \[Protocolo e métodos HTTP](#3-protocolo-e-métodos-http)

4\. \[JSON e troca de dados](#4-json-e-troca-de-dados)

5\. \[Hospedagem de APIs com Render](#5-hospedagem-de-apis-com-render)

6\. \[Evolução do projeto Express.js](#6-evolução-do-projeto-expressjs)

7\. \[Conceito de CRUD](#7-conceito-de-crud)

8\. \[Estrutura da API de notas](#8-estrutura-da-api-de-notas)

9\. \[Rotas CRUD da aplicação](#9-rotas-crud-da-aplicação)

10\. \[Implementação com Express.js](#10-implementação-com-expressjs)

11\. \[Armazenamento em arquivo JSON](#11-armazenamento-em-arquivo-json)

12\. \[Integração entre back-end e React](#12-integração-entre-back-end-e-react)

13\. \[Deploy do back-end e front-end](#13-deploy-do-back-end-e-front-end)

14\. \[Documentação de APIs com Postman](#14-documentação-de-apis-com-postman)

15\. \[Atividade proposta](#15-atividade-proposta)

16\. \[Questões para reflexão](#16-questões-para-reflexão)

17\. \[Conclusão](#17-conclusão)

18\. \[Referências](#18-referências)



\---



\## 1. Introdução



A Aula 08 apresentou a continuidade do desenvolvimento de aplicações back-end utilizando \*\*Node.js e Express.js\*\*.



O projeto trabalhado na aula anterior, que apresentava informações de data e hora, foi utilizado como ponto de partida para a implementação de novas funcionalidades.



Nesta aula, a proposta foi desenvolver uma aplicação de gerenciamento de notas, permitindo ao usuário:



\- Criar notas;

\- Visualizar notas existentes;

\- Editar informações;

\- Excluir notas.



Essas funcionalidades representam as quatro operações do \*\*CRUD\*\*.



O projeto também envolve a integração de uma API Express.js com uma interface React, publicação das aplicações e documentação das requisições utilizando Postman.



\## 2. Fundamentos de frameworks back-end



Os frameworks back-end auxiliam no desenvolvimento de sistemas responsáveis por receber requisições, executar regras de negócio e disponibilizar dados.



\### Organização do código



Frameworks podem utilizar padrões arquiteturais, como:



\- MVC (Model-View-Controller);

\- Arquitetura em camadas;

\- Organização por módulos e serviços.



Essas abordagens ajudam a separar responsabilidades e facilitar a manutenção do software.



\### Componentização



A divisão da aplicação em módulos permite organizar suas funcionalidades.



Os slides também apresentam middlewares e microsserviços como exemplos de recursos relacionados à modularização de sistemas.



\## 3. Protocolo e métodos HTTP



O \*\*HTTP (Hypertext Transfer Protocol)\*\* é o protocolo utilizado para estabelecer a comunicação entre clientes e servidores na web.



\### Características



\*\*Cliente-servidor:\*\* o cliente envia uma requisição e o servidor processa e retorna uma resposta.



\*\*Stateless:\*\* cada requisição é independente das anteriores.



\*\*Mensagens:\*\* a comunicação utiliza requisições e respostas com informações estruturadas.



\### Métodos HTTP



| Método | Finalidade |

|---|---|

| GET | Recuperar informações. |

| POST | Criar novos recursos. |

| PUT | Substituir informações de um recurso. |

| PATCH | Atualizar parcialmente um recurso. |

| DELETE | Remover um recurso. |



Esses métodos serão utilizados na construção da API de gerenciamento de notas.



\## 4. JSON e troca de dados



O \*\*JSON (JavaScript Object Notation)\*\* é um formato leve utilizado na representação e troca de dados.



Suas principais estruturas são:



\- Objetos, que armazenam pares de chave e valor;

\- Arrays, que armazenam listas ordenadas de valores.



\### Exemplo de JSON



```json

{

&#x20; "id": "1",

&#x20; "titulo": "Lembretes",

&#x20; "texto": "Comprar leite e pão",

&#x20; "criadoEm": "2025-04-29T10:00:00Z"

}

```



O exemplo segue a estrutura de uma nota apresentada nos slides do professor.



Nesse projeto, o JSON é utilizado tanto nas respostas da API quanto no armazenamento das notas em um arquivo.



\## 5. Hospedagem de APIs com Render



O \*\*Render\*\* é uma plataforma de hospedagem em nuvem utilizada para publicar serviços web e APIs.



\### Características apresentadas



\- Suporte a Node.js e outras linguagens;

\- Integração com repositórios Git;

\- Publicação de serviços web;

\- Deploy automatizado;

\- Configuração por meio de painel visual;

\- Recursos de monitoramento.



\*\*Site:\*\* https://render.com/



\### Publicação de uma aplicação Express



O procedimento apresentado foi:



1\. Enviar o projeto para um repositório no GitHub;

2\. Criar uma conta no Render;

3\. Selecionar um novo serviço do tipo \*\*Web Service\*\*;

4\. Conectar o repositório;

5\. Configurar o comando de inicialização;

6\. Executar o deploy;

7\. Verificar o endereço disponibilizado para a API.



\*\*Painel:\*\* https://dashboard.render.com/



O material apresenta `node api.js` como exemplo de comando de inicialização utilizado na aula anterior.



\## 6. Evolução do projeto Express.js



O professor propôs evoluir a aplicação desenvolvida na Aula 07.



Anteriormente, o projeto tinha como objetivo disponibilizar informações de data e hora.



Na Aula 08, a proposta passou a ser o desenvolvimento de uma aplicação que permite gerenciar notas.



\### Funcionalidades



\- Armazenar notas;

\- Visualizar registros;

\- Atualizar conteúdos;

\- Excluir informações.



Para isso, foi apresentado o uso de uma API REST desenvolvida com Express.js e um arquivo JSON utilizado como armazenamento.



\## 7. Conceito de CRUD



O \*\*CRUD\*\* representa as quatro operações fundamentais de manipulação de dados.



| Operação | Significado | Método HTTP utilizado |

|---|---|---|

| Create | Criar um registro. | POST |

| Read | Consultar registros. | GET |

| Update | Atualizar um registro. | PUT |

| Delete | Excluir um registro. | DELETE |



\### Aplicação no projeto de notas



\*\*Create:\*\* o usuário cria uma nova nota.



\*\*Read:\*\* o sistema apresenta as notas armazenadas.



\*\*Update:\*\* o usuário modifica o título ou o conteúdo de uma nota.



\*\*Delete:\*\* o usuário remove uma nota existente.



Essas operações serão acessadas por meio das rotas disponibilizadas pela API.



\## 8. Estrutura da API de notas



O projeto utiliza o Express.js para criar um servidor responsável pelo gerenciamento das notas.



\### Arquivos principais



| Arquivo | Finalidade |

|---|---|

| `server.js` | Configuração do servidor, rotas e operações da API. |

| `data.json` | Armazenamento das notas. |

| `package.json` | Informações, scripts e dependências do projeto. |



\### Organização apresentada



O arquivo `server.js` recebe as requisições HTTP e executa as operações necessárias.



O arquivo `data.json` mantém os registros utilizados pela aplicação.



Esse modelo foi apresentado como uma estratégia simples de armazenamento para o exercício.



\## 9. Rotas CRUD da aplicação



O professor apresentou quatro rotas principais para o gerenciamento das notas.



| Método | Endpoint | Finalidade |

|---|---|---|

| GET | `/api/notes` | Listar todas as notas. |

| POST | `/api/notes` | Criar uma nova nota. |

| PUT | `/api/notes/:id` | Atualizar uma nota pelo identificador. |

| DELETE | `/api/notes/:id` | Excluir uma nota pelo identificador. |



\### GET — Listar notas



Consulta os registros disponíveis no arquivo JSON e retorna a lista de notas.



\### POST — Criar nota



Adiciona uma nova nota ao conjunto de registros.



O slide descreve os campos `titulo` e `texto` e apresenta a geração de um identificador por meio de:



```javascript

Date.now().toString()

```



\### PUT — Atualizar nota



Localiza uma nota utilizando seu identificador e modifica os campos informados.



\### DELETE — Excluir nota



Remove a nota identificada pelo parâmetro `id`.



\*\*Observação sobre o material:\*\* a descrição das rotas no slide 14 menciona o registro da data de criação e uma resposta HTTP `204` para a exclusão. Entretanto, os exemplos de código dos slides seguintes não implementam integralmente esses comportamentos: a criação não adiciona o campo `criadoEm`, e a exclusão retorna uma mensagem JSON. Por isso, esses resultados devem ser verificados na implementação prática, sem presumir que já estejam funcionando dessa maneira.



\## 10. Implementação com Express.js



A aula apresentou o desenvolvimento de uma API REST para gerenciar notas.



\### Passo 1 — Criar o projeto



Criar uma pasta chamada `projeto-notas` e abri-la no Visual Studio Code.



\### Passo 2 — Instalar o Express



```bash

npm install express

```



\### Passo 3 — Instalar o Body-Parser



```bash

npm install body-parser

```



O Body-Parser é utilizado para processar dados recebidos no corpo de requisições HTTP.



\### Passo 4 — Criar o servidor



Criar um arquivo chamado `server.js`.



O professor apresentou os seguintes recursos:



\- Express para configurar a aplicação;

\- Body-Parser para processar JSON;

\- Módulo `fs` para leitura e escrita do arquivo;

\- Rotas HTTP para as operações CRUD.



\### Configuração inicial apresentada



```javascript

const express = require('express');

const bodyParser = require('body-parser');

const fs = require('fs');



const app = express();

const PORT = 3000;

const FILE = 'data.json';



app.use(bodyParser.json());

```



\### Configuração de CORS



O exemplo dos slides apresenta a liberação de acesso externo utilizando um middleware:



```javascript

app.use((req, res, next) => {

&#x20; res.header('Access-Control-Allow-Origin', '\*');

&#x20; next();

});

```



\*\*Complemento:\*\* permitir todas as origens com `\*` foi a configuração demonstrada no exercício. Em aplicações de produção, é importante avaliar quais origens precisam ter acesso à API.



\### Leitura das notas



O exemplo utiliza o módulo `fs` para ler as informações armazenadas.



```javascript

function readNotes() {

&#x20;   try {

&#x20;       const data = fs.readFileSync(FILE);

&#x20;       return JSON.parse(data);

&#x20;   } catch {

&#x20;       return \[];

&#x20;   }

}

```



\### Gravação das notas



A função apresentada salva o conjunto de registros no arquivo JSON.



```javascript

function saveNotes(notes) {

&#x20;   fs.writeFileSync(FILE, JSON.stringify(notes, null, 2));

}

```



\### Implementação das operações



\*\*GET\*\*



A rota lê e retorna as notas armazenadas.



```javascript

app.get('/api/notes', (req, res) => {

&#x20;   const notes = readNotes();

&#x20;   res.json(notes);

});

```



\*\*POST\*\*



A rota cria uma nota com identificador, título e texto, adicionando o registro ao arquivo.



\*\*PUT\*\*



A rota localiza uma nota pelo identificador e altera seu título e texto.



O exemplo apresenta uma resposta HTTP `404` quando o registro não é encontrado.



\*\*DELETE\*\*



A rota filtra os registros para remover a nota correspondente ao identificador informado.



Após a remoção, o arquivo JSON é atualizado.



\### Passo 5 — Executar o servidor



```bash

node server.js

```



O exemplo do professor utiliza a porta `3000`, permitindo acessar o servidor localmente.



\## 11. Armazenamento em arquivo JSON



Após criar o servidor, o professor orientou a criação do arquivo `data.json`.



\### Exemplo apresentado na aula



```json

\[

&#x20; {

&#x20;   "id": "1",

&#x20;   "titulo": "Lembretes",

&#x20;   "texto": "Comprar leite e pão",

&#x20;   "criadoEm": "2025-04-29T10:00:00Z"

&#x20; },

&#x20; {

&#x20;   "id": "2",

&#x20;   "titulo": "Tarefas do trabalho",

&#x20;   "texto": "Enviar relatório até sexta-feira",

&#x20;   "criadoEm": "2025-04-29T10:00:00Z"

&#x20; }

]

```



O arquivo contém uma lista de objetos, cada um representando uma nota.



\### Campos apresentados



| Campo | Finalidade |

|---|---|

| `id` | Identificar a nota. |

| `titulo` | Armazenar o título. |

| `texto` | Armazenar o conteúdo. |

| `criadoEm` | Registrar a data de criação. |



\### Complemento — Limitações do armazenamento em arquivo



Embora seja uma alternativa simples para exercícios e protótipos, o armazenamento em arquivo JSON pode apresentar limitações relacionadas a acessos simultâneos, desempenho, integridade e persistência dos dados.



Esses aspectos estão relacionados às questões para reflexão propostas pelo professor.



\## 12. Integração entre back-end e React



Depois de desenvolver a API, a aula propôs criar uma interface React para consumir suas rotas.



\### Funcionalidades da interface



\- Listar as notas disponíveis;

\- Criar novas notas;

\- Editar notas existentes;

\- Excluir registros.



\### Comunicação com a API



O front-end envia requisições HTTP para os endpoints do servidor Express.



Durante o desenvolvimento local, o endereço apresentado foi:



`http://localhost:3000/api/notes`



Após publicar a API no Render, o endereço local deverá ser substituído pelo endpoint disponibilizado pela plataforma.



\### Fluxo de funcionamento



1\. O usuário acessa a interface React.

2\. A interface realiza uma requisição HTTP.

3\. A API Express identifica a operação solicitada.

4\. O servidor consulta ou modifica os registros armazenados.

5\. A API envia uma resposta.

6\. O React atualiza as informações exibidas na tela.



Essa integração permite separar a interface do usuário da lógica de gerenciamento dos dados.



\## 13. Deploy do back-end e front-end



A aula apresentou a publicação dos dois componentes da aplicação.



\### Back-end — Render



O projeto Express deverá ser:



1\. Enviado para o GitHub;

2\. Conectado à plataforma Render;

3\. Configurado para execução;

4\. Publicado como serviço web.



Após a publicação, deverá ser verificado se os endpoints estão acessíveis.



\### Front-end — Vercel



O projeto React deverá ser:



1\. Enviado para o GitHub;

2\. Configurado para consumir a API publicada;

3\. Conectado à Vercel;

4\. Publicado para acesso online.



\*\*Site da Vercel:\*\* https://vercel.com/



\### Resultado esperado



A aplicação front-end deverá conseguir consultar, cadastrar, editar e excluir notas por meio da API publicada.



\*\*Complemento:\*\* quando os dados são armazenados em um arquivo local do servidor, é necessário verificar as características de persistência do ambiente de hospedagem. Um deploy bem-sucedido, por si só, não garante que as notas permanecerão armazenadas após reinicializações.



\## 14. Documentação de APIs com Postman



O \*\*Postman\*\* é uma ferramenta utilizada para criar, executar, testar e documentar requisições HTTP.



Ele facilita o desenvolvimento e a verificação do funcionamento de APIs.



\*\*Site oficial:\*\* https://www.postman.com/



\### Funcionalidades apresentadas



\- Envio de requisições HTTP;

\- Visualização de respostas;

\- Organização de endpoints;

\- Criação de coleções;

\- Utilização de variáveis de ambiente;

\- Testes automatizados;

\- Compartilhamento de documentação.



\### Coleções de requisições



Uma coleção permite reunir diferentes requisições relacionadas a uma API.



No projeto de notas, a coleção deverá documentar as quatro operações CRUD.



| Requisição | Método | Endpoint |

|---|---|---|

| Listar notas | GET | `/api/notes` |

| Criar nota | POST | `/api/notes` |

| Atualizar nota | PUT | `/api/notes/:id` |

| Excluir nota | DELETE | `/api/notes/:id` |



\### Informações de uma documentação de API



A aula destacou a importância de registrar:



\- Endpoints disponíveis;

\- Métodos HTTP;

\- Parâmetros exigidos;

\- Formatos das respostas;

\- Exemplos de requisições;

\- Códigos de resposta.



\### Recursos adicionais apresentados



O professor também apresentou recursos como:



\- Mock Servers;

\- Monitoramento;

\- GraphQL;

\- WebSockets;

\- OAuth 2.0;

\- Newman para execução automatizada de coleções.



\## 15. Atividade proposta



A atividade prática da Aula 08 envolve a criação de uma aplicação de notas com operações CRUD, integração entre front-end e back-end e documentação da API.



\### Etapa 1 — Desenvolver o back-end



Criar uma aplicação com Express.js contendo as quatro rotas CRUD.



As notas deverão ser armazenadas em um arquivo JSON.



\### Etapa 2 — Publicar a API



Publicar o back-end na plataforma Render, garantindo que a API esteja acessível online.



\### Etapa 3 — Desenvolver o front-end



Criar uma interface que consuma a API e permita:



1\. Cadastrar notas;

2\. Visualizar as notas existentes;

3\. Editar informações;

4\. Excluir notas.



\### Etapa 4 — Publicar a interface



Publicar a aplicação front-end na Vercel e configurar sua integração com o back-end hospedado no Render.



\### Etapa 5 — Documentar o projeto



Organizar um documento contendo:



\- Prints do código;

\- Prints da aplicação em funcionamento;

\- Link do repositório no GitHub;

\- Link do deploy realizado na Vercel.



\### Etapa 6 — Criar uma coleção no Postman



Criar uma coleção documentando as quatro operações CRUD da API.



\### Etapa 7 — Configurar as requisições



Para cada operação, definir:



\- Método HTTP;

\- Endpoint;

\- Parâmetros;

\- Dados enviados, quando necessários;

\- Descrição dos códigos de resposta.



\### Etapa 8 — Entregar a documentação



Organizar os registros da atividade em um documento contendo:



\- Evidências da implementação;

\- Prints da aplicação;

\- Informações das rotas;

\- Link da coleção do Postman.



O documento deverá ser enviado ao repositório da disciplina no GitHub.



\### Repositórios de exemplo apresentados pelo professor



\- \[Exemplo de back-end](https://github.com/deivisontakatu/exemplo-api-backend)

\- \[Exemplo de front-end](https://github.com/deivisontakatu/exemplo-api-frontend)



\*\*Observação:\*\* esses são repositórios de referência apresentados no material, e não links da entrega da atividade.



\## 16. Questões para reflexão



Além da implementação prática, o professor apresentou quatro questões sobre segurança, armazenamento e organização do projeto.



\### Questão 1 — Segurança



Quais são os riscos de segurança desse projeto e como poderiam ser eliminados ou mitigados?



\### Questão 2 — Armazenamento em JSON



Usar um arquivo JSON (`data.json`) para armazenar notas é uma boa prática em produção? Quais são as vantagens e desvantagens dessa abordagem?



\### Questão 3 — Escalabilidade



Quais limitações um servidor baseado em arquivo JSON teria se o número de notas crescesse para 10.000 registros?



\### Questão 4 — Organização do código



O código atual está todo em `server.js`. Por que isso é problemático e como você melhoraria a organização da lógica?



\*\*Observação:\*\* as perguntas foram mantidas conforme a proposta da aula. As respostas e análises da atividade deverão ser registradas na documentação prática.



\## 17. Conclusão



A Aula 08 permitiu aprofundar os conhecimentos sobre desenvolvimento back-end utilizando Express.js.



Foram apresentados os métodos HTTP, o formato JSON e a implementação das operações CRUD em uma API de gerenciamento de notas.



A aula também abordou o armazenamento de dados em arquivo, a integração com uma interface React e a publicação das aplicações utilizando Render e Vercel.



Por fim, foram apresentados os recursos do Postman para testar e documentar os endpoints, além de questões importantes sobre segurança, desempenho e organização do código.



\## 18. Referências



DINIZ, Luciana Mara Freitas et al. Aprendizado baseado em projetos em IHC (presencial e remoto): prototipação segundo as heurísticas de Nielsen. In: \*\*SIMPÓSIO BRASILEIRO DE FATORES HUMANOS EM SISTEMAS COMPUTACIONAIS (IHC)\*\*, 2020. Anais \[...]. SBC, 2020. p. 13-18.



FERREIRA, Arthur Gonçalves. \*\*Interface de programação de aplicações (API) e web services\*\*. São Paulo: Platos Soluções Educacionais, 2021.



GONÇALVES, Rodrigo Franco et al. Uma proposta de processo de produção de aplicações Web. \*\*Production\*\*, v. 15, p. 376-389, 2005.



LUCASSEN, Garm et al. The use and effectiveness of user stories in practice. In: \*\*REQUIREMENTS ENGINEERING: FOUNDATION FOR SOFTWARE QUALITY (REFSQ)\*\*, 22., 2016, Gothenburg. Proceedings \[...]. Springer International Publishing, 2016. p. 205-222.



MILETTO, Evandro Manara; DE CASTRO BERTAGNOLLI, Silvia. \*\*Desenvolvimento de Software II: introdução ao desenvolvimento web com HTML, CSS, JavaScript e PHP\*\*. \[S. l.]: Bookman, 2014.



NGUYEN, Hong-Thu Thi. Website Builder as an Assistive Technology Tool for Reflection, Collaboration and Skills Development in Learning ESP. \*\*Journal of Learning for Development\*\*, v. 11, n. 1, p. 138-150, 2024.



OLIVEIRA, Cláudio Luís Vieira. \*\*Node.js: programe de forma rápida e prática\*\*. São Paulo: Expressa, 2021.



RANJAN, Alok; SINHA, Abhilasha; BATTEWAD, Ranjit. \*\*JavaScript for Modern Web Development\*\*. \[S. l.]: BPB Publications, 2020.



SALINAS, C. et al. Agile, Web Engineering and Capability Maturity Model Integration: a systematic literature review. \*\*Information and Software Technology\*\*, v. 71, p. 92-107, 2016. DOI: 10.1016/j.infsof.2015.11.002.



WILDT, Daniel et al. \*\*Extreme Programming: práticas para o dia a dia no desenvolvimento ágil de software\*\*. São Paulo: Casa do Código, 2015.



ZABOT, Diego. \*\*Aplicativos com Bootstrap e Angular: como desenvolver apps responsivos\*\*. São Paulo: Érica, 2020.



\---



\*\*Complemento — Navegação do repositório\*\*



\- \[Documentação da Atividade 08](../atividades/aula-08/README.md)

\- \[Índice das aulas](README.md)

\- \[Página principal do repositório](../README.md)

