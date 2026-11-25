\# Aula 07 — Introdução aos Frameworks Back-end



\*\*Disciplina:\*\* Programação Web  

\*\*Professor:\*\* Prof. Me. Deivison S. Takatu  

\*\*Curso:\*\* Análise e Desenvolvimento de Sistemas  

\*\*Instituição:\*\* Fatec Itapetininga  

\*\*Ano:\*\* 2026



\---



\## Sumário



1\. \[Introdução aos frameworks back-end](#1-introdução-aos-frameworks-back-end)

2\. \[Características dos frameworks back-end](#2-características-dos-frameworks-back-end)

3\. \[Exemplos de frameworks](#3-exemplos-de-frameworks)

4\. \[Arquitetura de software](#4-arquitetura-de-software)

5\. \[Design Patterns](#5-design-patterns)

6\. \[Monolitos e microsserviços](#6-monolitos-e-microsserviços)

7\. \[Introdução ao Express.js](#7-introdução-ao-expressjs)

8\. \[Funcionamento das requisições](#8-funcionamento-das-requisições)

9\. \[Protocolo e métodos HTTP](#9-protocolo-e-métodos-http)

10\. \[APIs REST e endpoints](#10-apis-rest-e-endpoints)

11\. \[Servidor back-end, Web Services e JSON](#11-servidor-back-end-web-services-e-json)

12\. \[Criando uma API com Express](#12-criando-uma-api-com-express)

13\. \[Deploy no Render](#13-deploy-no-render)

14\. \[Atividade proposta](#14-atividade-proposta)

15\. \[Conclusão](#15-conclusão)

16\. \[Referências](#16-referências)



\---



\## 1. Introdução aos frameworks back-end



Um \*\*framework back-end\*\* é um conjunto de ferramentas, bibliotecas e convenções utilizado para organizar o desenvolvimento da lógica executada no servidor.



Esses frameworks auxiliam na criação de APIs, integração com bancos de dados e implementação das funcionalidades internas de uma aplicação.



\### Desenvolvimento sem framework



Quando uma aplicação é desenvolvida sem um framework, o programador precisa implementar manualmente diversas estruturas e configurações.



Isso pode resultar em:



\- Repetição de código;

\- Maior dificuldade de manutenção;

\- Configurações mais complexas;

\- Maior esforço para implementar recursos comuns.



\### Desenvolvimento com framework



Os frameworks oferecem recursos que facilitam:



\- Organização de rotas;

\- Separação de responsabilidades;

\- Integração com bancos de dados;

\- Autenticação e validação;

\- Manutenção e escalabilidade.



\## 2. Características dos frameworks back-end



\### Estrutura de código organizada



Os frameworks podem utilizar padrões como \*\*MVC (Model-View-Controller)\*\* e arquitetura em camadas.



Esses padrões ajudam a separar as regras de negócio, o acesso aos dados e o tratamento das requisições.



\### Modularização



Permite organizar o sistema em módulos e serviços reutilizáveis.



\### Programação assíncrona



Possibilita executar operações de entrada e saída, como consultas a bancos de dados e chamadas a APIs, sem bloquear desnecessariamente a execução de outras tarefas.



\### Segurança



Frameworks podem ser combinados com recursos de autenticação, validação de dados, registro de eventos e proteção das aplicações.



\### Rotas e APIs



Facilitam a definição de caminhos utilizados para acessar funcionalidades e recursos do servidor.



\## 3. Exemplos de frameworks



Durante a aula, foram apresentados três exemplos de frameworks back-end.



| Framework | Linguagem | Características |

|---|---|---|

| Express.js | JavaScript / Node.js | Minimalista, flexível e extensível por middlewares. |

| Django | Python | Framework completo, com ORM, autenticação e administração. |

| Laravel | PHP | Possui roteamento, ORM Eloquent e ferramenta Artisan. |



\### Escolha do framework



A escolha deve considerar:



\- Necessidades do projeto;

\- Complexidade;

\- Curva de aprendizado;

\- Desempenho;

\- Escalabilidade;

\- Facilidade de manutenção;

\- Suporte da comunidade.



O material apresentou a ferramenta StackShare como recurso para comparar tecnologias.



\*\*Ferramenta:\*\* https://stackshare.io/stackups



\## 4. Arquitetura de software



A \*\*arquitetura de software\*\* define como os componentes de um sistema são organizados e como se relacionam.



Ela influencia o desempenho, a manutenção, a escalabilidade e a capacidade de evolução da aplicação.



\### Fatores importantes



\- Requisitos do projeto;

\- Complexidade do sistema;

\- Tamanho da equipe;

\- Necessidades de manutenção;

\- Objetivos do negócio;

\- Tecnologias disponíveis.



O planejamento da arquitetura ajuda a reduzir o retrabalho e permite adaptar a aplicação a novas necessidades.



\## 5. Design Patterns



Os \*\*Design Patterns\*\*, ou padrões de projeto, são soluções reutilizáveis para problemas recorrentes no desenvolvimento de software.



O professor apresentou três categorias principais.



\### Padrões criacionais



Relacionados à criação de objetos e à organização desse processo.



Exemplos:



\- Factory;

\- Singleton;

\- Builder.



\### Padrões estruturais



Relacionados à organização e à composição de classes e objetos.



Exemplos:



\- Adapter;

\- Composite;

\- Proxy.



\### Padrões comportamentais



Relacionados à comunicação e à distribuição de responsabilidades entre objetos.



Exemplos:



\- Observer;

\- Strategy;

\- Command.



\*\*Referência apresentada:\*\* https://refactoring.guru/design-patterns/catalog



\## 6. Monolitos e microsserviços



A aula apresentou duas possibilidades de organização de uma aplicação.



\### Arquitetura monolítica



O \*\*monolito\*\* reúne os principais módulos de um sistema em uma única aplicação.



Entre suas características estão a estrutura integrada e a possibilidade de simplificar o desenvolvimento de projetos menores.



\### Arquitetura de microsserviços



Os \*\*microsserviços\*\* dividem o sistema em serviços independentes.



Cada serviço pode ser desenvolvido e atualizado separadamente, mas essa abordagem também aumenta a complexidade de comunicação e operação.



\### Comparação



| Monolito | Microsserviços |

|---|---|

| Aplicação integrada. | Aplicação dividida em serviços. |

| Pode simplificar projetos menores. | Permite maior independência entre serviços. |

| Possui uma estrutura centralizada. | Exige gerenciamento da comunicação entre serviços. |

| O crescimento pode exigir ajustes na arquitetura. | Pode facilitar a escalabilidade de serviços específicos. |



\### Estudo de caso — Amazon Prime Video



O professor apresentou um caso relacionado à arquitetura de um serviço do Amazon Prime Video.



Segundo o exemplo dos slides, em 2023 houve uma alteração arquitetural que substituiu uma solução distribuída por uma abordagem mais integrada, resultando em redução significativa dos custos.



O caso foi utilizado para demonstrar que a escolha da arquitetura deve considerar as necessidades do projeto, e não apenas a popularidade de uma tecnologia.



\## 7. Introdução ao Express.js



O \*\*Express.js\*\* é um framework para Node.js utilizado na criação de servidores web e APIs.



Ele oferece uma estrutura minimalista e flexível para o desenvolvimento back-end.



\### Características



\*\*Simplicidade:\*\* reduz a quantidade de código necessária para configurar um servidor.



\*\*Roteamento:\*\* facilita a criação de caminhos e funcionalidades da aplicação.



\*\*Middlewares:\*\* permite utilizar funções intermediárias para processar requisições e respostas.



\*\*Flexibilidade:\*\* pode ser integrado a outras bibliotecas conforme as necessidades do projeto.



\### Exemplo de servidor Express



O professor apresentou um exemplo no qual o servidor responde à rota inicial com a mensagem "Olá, mundo!".



```javascript

const express = require('express');



const app = express();



app.get('/', (req, res) => {

&#x20;   res.send('Olá, mundo!');

});



app.listen(3000, () => {

&#x20;   console.log('Servidor rodando em http://localhost:3000');

});

```



Nesse exemplo:



\- `express()` cria a aplicação;

\- `app.get()` define uma rota que utiliza o método GET;

\- `res.send()` envia uma resposta;

\- `app.listen()` inicia o servidor.



A aplicação pode ser acessada localmente em `http://localhost:3000`.



\### Quando utilizar Express.js



O material destaca sua utilização em:



\- APIs REST;

\- Aplicações web;

\- Integração com bancos de dados;

\- Serviços back-end;

\- Prototipação de aplicações.



Também foram discutidas alternativas para necessidades específicas, como comunicação em tempo real e processamento intensivo.



\## 8. Funcionamento das requisições



Uma aplicação web normalmente utiliza uma comunicação entre o front-end e o servidor.



\### Etapas apresentadas



1\. O usuário interage com a interface.

2\. O navegador envia uma requisição HTTP.

3\. O servidor Express identifica a rota solicitada.

4\. A lógica da aplicação é executada.

5\. O servidor pode consultar um banco de dados ou serviço externo.

6\. A resposta é enviada ao cliente, frequentemente em JSON.

7\. O front-end utiliza a resposta para atualizar a interface.



Esse processo permite separar a apresentação dos dados e a lógica de processamento.



\## 9. Protocolo e métodos HTTP



O \*\*HTTP (Hypertext Transfer Protocol)\*\* é o protocolo utilizado para comunicação entre clientes e servidores na web.



\### Características



\- Modelo cliente-servidor;

\- Comunicação baseada em requisições e respostas;

\- Protocolo sem estado (\*stateless\*).



\### Métodos HTTP



| Método | Finalidade |

|---|---|

| GET | Consultar informações de um recurso. |

| POST | Enviar dados, geralmente para criar um recurso. |

| PUT | Substituir a representação de um recurso. |

| PATCH | Atualizar parcialmente um recurso. |

| DELETE | Solicitar a remoção de um recurso. |



\### Conceitos apresentados



\*\*GET:\*\* utilizado para consultar dados, sem solicitar alterações no recurso.



\*\*POST:\*\* normalmente utilizado para criação de recursos.



\*\*PUT:\*\* utilizado para substituição de informações.



\*\*PATCH:\*\* utilizado para atualizações parciais.



\*\*DELETE:\*\* utilizado para remoção de recursos.



\## 10. APIs REST e endpoints



\### API



Uma \*\*API (Application Programming Interface)\*\* é uma interface que estabelece como diferentes sistemas e componentes podem se comunicar.



Ela permite disponibilizar dados e funcionalidades para outras aplicações.



\### REST



O \*\*REST (Representational State Transfer)\*\* é um estilo arquitetural utilizado no desenvolvimento de sistemas distribuídos.



Entre seus princípios apresentados estão:



\- Comunicação cliente-servidor;

\- Comunicação sem estado;

\- Utilização dos métodos HTTP;

\- Identificação de recursos por URLs ou URIs;

\- Representação de informações em formatos como JSON.



\### Endpoints



Um \*\*endpoint\*\* é um endereço utilizado para acessar determinado recurso ou funcionalidade disponibilizada por uma API.



Exemplo ilustrativo:



`https://api.exemplo.com/usuarios`



Diferentes métodos HTTP podem ser utilizados nesse endereço.



\- `GET`: consultar usuários;

\- `POST`: cadastrar usuários.



O professor também apresentou como referência um repositório de APIs de consulta de CEP:



https://github.com/awesomeapibrasil/awesomeapi-cep



\## 11. Servidor back-end, Web Services e JSON



\### Servidor back-end



O servidor back-end recebe e processa requisições enviadas pelos clientes.



Entre suas funções estão:



\- Executar regras de negócio;

\- Consultar e armazenar dados;

\- Disponibilizar APIs;

\- Processar requisições;

\- Retornar respostas.



\### Web Services



Os \*\*Web Services\*\* permitem a comunicação entre diferentes sistemas por meio de padrões e protocolos utilizados na web.



Essa comunicação possibilita a integração de aplicações desenvolvidas em diferentes linguagens e tecnologias.



\### JSON



O \*\*JSON (JavaScript Object Notation)\*\* é um formato leve para representação e troca de dados.



Suas estruturas principais incluem objetos e arrays.



\### Exemplo de JSON



```json

{

&#x20; "nome": "Exemplo",

&#x20; "status": "ativo",

&#x20; "funcionalidades": \["consulta", "cadastro"]

}

```



\*\*Complemento:\*\* o exemplo acima é apenas ilustrativo e não corresponde a dados de uma aplicação desenvolvida durante a atividade.



\## 12. Criando uma API com Express



A aula apresentou a criação de uma API utilizando Node.js, Express e CORS.



\### Etapa 1 — Inicializar o projeto



Criar uma pasta para o projeto e abri-la no Visual Studio Code.



\### Etapa 2 — Instalar o Express



Comando apresentado:



```bash

npm install express

```



\### Etapa 3 — Instalar o CORS



Comando apresentado no slide:



```bash

npm install cors express

```



O \*\*CORS (Cross-Origin Resource Sharing)\*\* controla quais origens podem acessar respostas de uma aplicação em situações de comunicação entre diferentes domínios.



\### Etapa 4 — Criar o arquivo da API



O professor utilizou um arquivo chamado `api.js`.



O exemplo apresentado no slide utiliza:



\- Express para criar o servidor;

\- CORS para permitir a comunicação com o front-end;

\- Uma rota GET;

\- Um objeto JSON contendo a data e uma mensagem de status;

\- Uma porta configurável para a hospedagem no Render.



O slide utiliza a expressão:



```javascript

new Date().toLocaleString('pt-BR')

```



Ela gera uma representação da data e hora no formato brasileiro.



Também foi apresentada a configuração da porta por meio de `process.env.PORT`, permitindo que o ambiente de hospedagem defina a porta do servidor.



\### Etapa 5 — Executar a API



Comando apresentado:



```bash

node api.js

```



\*\*Complemento:\*\* o código exibido no slide utiliza a sintaxe `import`. Para executá-lo dessa forma no Node.js, é necessário utilizar uma configuração compatível com módulos ES, como definir `"type": "module"` no `package.json`.



\## 13. Deploy no Render



O \*\*Render\*\* é uma plataforma de hospedagem em nuvem que permite publicar aplicações back-end e APIs.



\### Características apresentadas



\- Integração com repositórios Git;

\- Publicação de aplicações Node.js;

\- Deploy automatizado;

\- Configuração pela interface da plataforma;

\- Recursos de monitoramento;

\- Hospedagem de serviços web.



\*\*Site:\*\* https://render.com/



\### Etapas apresentadas na aula



1\. Publicar o projeto em um repositório no GitHub.

2\. Acessar o painel do Render.

3\. Criar um novo serviço do tipo \*\*Web Service\*\*.

4\. Conectar o repositório do GitHub.

5\. Configurar os comandos necessários para iniciar a aplicação.

6\. Realizar o deploy.

7\. Verificar o endereço disponibilizado pelo Render.



\*\*Painel:\*\* https://dashboard.render.com/



O material apresenta `node api.js` como comando para iniciar a API.



Após a publicação, a aplicação pode receber um endereço semelhante a:



`https://seu-projeto.onrender.com`



Esse endereço é apenas ilustrativo e não representa um deploy confirmado.



\## 14. Atividade proposta



A atividade da Aula 07 consiste em desenvolver uma \*\*API com Express.js\*\* e uma aplicação front-end que consuma os dados disponibilizados.



\### Etapa 1 — Criar a API



Desenvolver uma API com Express contendo uma rota para consultar a \*\*data e hora\*\*.



A API deverá retornar essas informações para a aplicação cliente.



\### Etapa 2 — Publicar a API no Render



Publicar o projeto back-end em um repositório no GitHub.



Em seguida:



1\. Conectar o repositório ao Render;

2\. Configurar o serviço;

3\. Realizar o deploy;

4\. Verificar se a API está acessível online.



\### Etapa 3 — Desenvolver o front-end



Criar uma aplicação front-end que consuma a API desenvolvida.



A interface deverá apresentar na tela a data e a hora recebidas do servidor.



\### Etapa 4 — Separar os repositórios



Utilizar \*\*repositórios diferentes\*\* para o back-end e o front-end.



Essa separação permite organizar os códigos e documentar individualmente as aplicações.



\### Etapa 5 — Documentação



Organizar um documento contendo:



\- Descrição da API;

\- Explicação da aplicação front-end;

\- Prints do código;

\- Prints da aplicação em funcionamento;

\- Capturas do painel do Render;

\- Capturas do painel da Vercel;

\- Links dos repositórios no GitHub;

\- Evidências da publicação das aplicações.



O documento deverá ser salvo no GitHub, conforme solicitado pelo professor.



\*\*Observação:\*\* a documentação da atividade prática deverá apresentar somente os resultados e as publicações realmente realizados.



\## 15. Conclusão



A Aula 07 apresentou os principais conceitos relacionados ao desenvolvimento back-end e à construção de APIs.



Foram estudados frameworks, arquitetura de software, padrões de projeto, monolitos, microsserviços e o funcionamento das requisições HTTP.



O conteúdo também introduziu o Express.js, a criação de endpoints REST e a utilização do JSON para comunicação entre sistemas.



A atividade prática propôs o desenvolvimento de uma API de data e hora, sua publicação no Render e a construção de uma aplicação front-end para consumir as informações.



\## 16. Referências



DINIZ, Luciana Mara Freitas et al. Aprendizado baseado em projetos em IHC (presencial e remoto): prototipação segundo as heurísticas de Nielsen. In: \*\*SIMPÓSIO BRASILEIRO DE FATORES HUMANOS EM SISTEMAS COMPUTACIONAIS (IHC)\*\*, 2020. Anais \[...]. SBC, 2020. p. 13-18.



FERREIRA, Arthur Gonçalves. \*\*Interface de programação de aplicações (API) e web services\*\*. São Paulo: Platos Soluções Educacionais, 2021.



FREEMAN, E.; ROBSON, E. \*\*Modern Web Development: building and deploying with modern tools\*\*. 1. ed. Sebastopol: O'Reilly Media, 2022.



GONÇALVES, Rodrigo Franco et al. Uma proposta de processo de produção de aplicações Web. \*\*Production\*\*, v. 15, p. 376-389, 2005.



LUCASSEN, Garm et al. The use and effectiveness of user stories in practice. In: \*\*REQUIREMENTS ENGINEERING: FOUNDATION FOR SOFTWARE QUALITY (REFSQ)\*\*, 22., 2016, Gothenburg. Proceedings \[...]. Springer International Publishing, 2016. p. 205-222.



MILETTO, Evandro Manara; DE CASTRO BERTAGNOLLI, Silvia. \*\*Desenvolvimento de Software II: introdução ao desenvolvimento web com HTML, CSS, JavaScript e PHP\*\*. \[S. l.]: Bookman, 2014.



NEWMAN, S. \*\*Building Microservices: designing fine-grained systems\*\*. 2. ed. Sebastopol: O'Reilly Media, 2021.



NGUYEN, Hong-Thu Thi. Website Builder as an Assistive Technology Tool for Reflection, Collaboration and Skills Development in Learning ESP. \*\*Journal of Learning for Development\*\*, v. 11, n. 1, p. 138-150, 2024.



OLIVEIRA, Cláudio Luís Vieira. \*\*Node.js: programe de forma rápida e prática\*\*. São Paulo: Expressa, 2021.



RANJAN, Alok; SINHA, Abhilasha; BATTEWAD, Ranjit. \*\*JavaScript for Modern Web Development\*\*. \[S. l.]: BPB Publications, 2020.



SALINAS, C. et al. Agile, Web Engineering and Capability Maturity Model Integration: a systematic literature review. \*\*Information and Software Technology\*\*, v. 71, p. 92-107, 2016. DOI: 10.1016/j.infsof.2015.11.002.



WILDT, Daniel et al. \*\*Extreme Programming: práticas para o dia a dia no desenvolvimento ágil de software\*\*. São Paulo: Casa do Código, 2015.



ZABOT, Diego. \*\*Aplicativos com Bootstrap e Angular: como desenvolver apps responsivos\*\*. São Paulo: Érica, 2020.



\*\*Observação:\*\* os slides também mencionam Fielding (2000) e Rockford (2008), mas não apresentam seus dados bibliográficos completos.



\---



\*\*Complemento — Navegação do repositório\*\*



\- \[Documentação da Atividade 07](../atividades/aula-07/README.md)

\- \[Índice das aulas](README.md)

\- \[Página principal do repositório](../README.md)

