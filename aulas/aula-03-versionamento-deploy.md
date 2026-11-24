\# Aula 03 — Introdução ao Versionamento e Deploy



\*\*Disciplina:\*\* Programação Web  

\*\*Professor:\*\* Prof. Me. Deivison S. Takatu  

\*\*Curso:\*\* Análise e Desenvolvimento de Sistemas  

\*\*Instituição:\*\* Fatec Itapetininga  

\*\*Ano:\*\* 2026



\---



\## Sumário



1\. \[Versionamento e backup](#1-versionamento-e-backup)

2\. \[Benefícios do versionamento](#2-benefícios-do-versionamento)

3\. \[Versionamento semântico](#3-versionamento-semântico)

4\. \[Tipos de alterações no código](#4-tipos-de-alterações-no-código)

5\. \[Introdução ao Git](#5-introdução-ao-git)

6\. \[Instalação e configuração do Git](#6-instalação-e-configuração-do-git)

7\. \[Repositórios e GitHub](#7-repositórios-e-github)

8\. \[Tags no Git](#8-tags-no-git)

9\. \[Branches e merge](#9-branches-e-merge)

10\. \[Boas práticas com Git](#10-boas-práticas-com-git)

11\. \[Deploy e hospedagem](#11-deploy-e-hospedagem)

12\. \[Vercel](#12-vercel)

13\. \[Atividade proposta](#13-atividade-proposta)

14\. \[Conclusão](#14-conclusão)

15\. \[Referências](#15-referências)



\---



\## 1. Versionamento e backup



O versionamento é o processo de registrar e identificar diferentes versões de arquivos ou softwares ao longo do desenvolvimento.



Ele permite acompanhar alterações, identificar responsáveis e recuperar versões anteriores.



\### Diferenças entre versionamento e backup



| Versionamento | Backup |

|---|---|

| Registra o histórico das alterações. | Armazena uma cópia de determinado momento. |

| Permite identificar quem realizou mudanças. | Não necessariamente registra a autoria. |

| Facilita o trabalho colaborativo. | Tem como objetivo preservar os dados. |

| Permite recuperar alterações específicas. | Geralmente restaura uma cópia completa. |



\### Problemas sem versionamento



A ausência de controle de versões pode provocar:



\- Arquivos duplicados;

\- Perda de código;

\- Conflitos entre desenvolvedores;

\- Dificuldade para recuperar alterações;

\- Falta de histórico das mudanças.



O versionamento contribui para a segurança e organização do desenvolvimento.



\## 2. Benefícios do versionamento



Entre os principais benefícios apresentados estão:



\*\*Trabalho simultâneo:\*\* permite que diferentes desenvolvedores trabalhem em um mesmo projeto.



\*\*Redução do retrabalho:\*\* facilita a identificação de problemas e evita perdas de alterações.



\*\*Auditoria e rastreabilidade:\*\* registra o histórico de modificações, seus responsáveis e justificativas.



\*\*Recuperação de versões:\*\* possibilita retornar a estados anteriores do projeto.



\### Importância no desenvolvimento



O versionamento também contribui para o controle de mudanças, gerenciamento da qualidade, colaboração eficiente, aprimoramento contínuo e integração com outras ferramentas.



\## 3. Versionamento semântico



O \*\*Versionamento Semântico (SemVer)\*\* utiliza uma sequência numérica para identificar as versões de um software.



Seu padrão é:



```text

MAJOR.MINOR.PATCH

```



\### Elementos do SemVer



| Elemento | Finalidade | Exemplo |

|---|---|---|

| MAJOR | Mudanças incompatíveis com versões anteriores. | 2.0.0 |

| MINOR | Novas funcionalidades compatíveis com versões anteriores. | 1.1.0 |

| PATCH | Correções de erros sem mudanças incompatíveis. | 1.0.1 |



\### Exemplo de evolução



\- `1.0.0` — primeira versão estável;

\- `1.1.0` — adição de uma funcionalidade;

\- `1.1.1` — correção de um erro;

\- `2.0.0` — mudança incompatível com versões anteriores.



O material também apresenta versões `0.x.x` como indicativas do desenvolvimento inicial.



\### Vantagens



\- Organização das versões;

\- Facilidade na gestão de dependências;

\- Melhor comunicação das alterações;

\- Previsibilidade na manutenção dos projetos.



\## 4. Tipos de alterações no código



Durante a aula, foram apresentados diferentes tipos de mudanças realizadas durante o desenvolvimento.



| Tipo | Descrição |

|---|---|

| Bug Fix | Correção de erros no código. |

| New Feature | Inclusão de uma nova funcionalidade. |

| Feature Enhancement | Melhoria de funcionalidades existentes. |

| Refactoring | Reorganização do código. |

| Performance | Otimização do desempenho. |

| Security Patch | Correção de vulnerabilidades. |

| Dependency Update | Atualização das dependências utilizadas. |

| Adding Tests | Inclusão de testes automatizados. |



Identificar essas alterações facilita o acompanhamento da evolução do software.



\## 5. Introdução ao Git



O \*\*Git\*\* é um sistema de controle de versões utilizado para registrar alterações em arquivos e acompanhar o histórico de um projeto.



Ele permite:



\- Criar repositórios;

\- Registrar modificações;

\- Recuperar versões anteriores;

\- Criar branches;

\- Trabalhar em equipe;

\- Sincronizar arquivos com repositórios remotos.



O Git pode ser utilizado pelo terminal e integrado a ferramentas de desenvolvimento, como o Visual Studio Code.



\## 6. Instalação e configuração do Git



O professor apresentou o processo de instalação do Git e sua configuração inicial.



\*\*Site oficial:\*\* https://git-scm.com/downloads



\### Verificando a instalação



Após instalar o Git, é possível confirmar a versão pelo Prompt de Comando:



```bash

git --version

```



O terminal deverá mostrar a versão instalada.



\### Configuração do usuário



Caso seja necessário, o nome e o e-mail podem ser configurados pelos comandos:



```bash

git config --global user.name "Nome"

git config --global user.email "email@exemplo.com"

```



Essas informações são utilizadas para identificar a autoria dos commits.



\### Integração com VS Code



No Visual Studio Code, o controle de versões pode ser acessado pela aba \*\*Controle de Código-Fonte\*\*.



Por meio dessa ferramenta, é possível inicializar repositórios, visualizar alterações e registrar commits.



\## 7. Repositórios e GitHub



Um repositório Git armazena os arquivos do projeto e seu histórico de alterações.



\### Criando um repositório



O procedimento apresentado na aula utiliza o VS Code:



1\. Criar uma pasta para o projeto;

2\. Abrir a pasta no VS Code;

3\. Criar um arquivo `index.html`;

4\. Acessar a aba Controle de Código-Fonte;

5\. Inicializar o repositório;

6\. Adicionar uma mensagem e realizar o commit.



\### Publicando no GitHub



Após configurar o repositório local, é possível publicá-lo no GitHub.



O processo apresentado inclui:



1\. Selecionar a opção de publicar a branch;

2\. Autenticar-se no GitHub;

3\. Escolher a visibilidade do repositório;

4\. Confirmar a publicação;

5\. Conferir os arquivos no GitHub.



O GitHub permite armazenar os projetos remotamente e compartilhar o código com outras pessoas.



\## 8. Tags no Git



As \*\*tags\*\* são marcadores utilizados para identificar pontos específicos do histórico de um projeto.



Elas podem representar versões estáveis ou momentos importantes do desenvolvimento.



\### Tipos de tags



\*\*Lightweight:\*\* marcador simples associado a um commit.



\*\*Annotated:\*\* marcador que armazena informações adicionais, como autor, data e mensagem.



\### Comandos apresentados na aula



Listar tags existentes:



```bash

git tag

```



Criar uma tag simples:



```bash

git tag 1.0.0

```



Publicar uma tag no GitHub:



```bash

git push origin 1.0.0

```



O uso das tags facilita a identificação e organização das versões do projeto.



\### Complemento — Tags anotadas



Para documentar melhor as versões do repositório da disciplina, será utilizado o formato de tag anotada:



```bash

git tag -a v1.0.0 -m "v1.0.0 - primeira versão estável"

git push origin v1.0.0

```



Esses comandos são exemplos de utilização e não representam versões já publicadas.



\## 9. Branches e merge



As \*\*branches\*\* são ramificações que permitem desenvolver funcionalidades ou correções sem modificar diretamente a versão principal.



\### Tipos de branches apresentados



| Branch | Finalidade |

|---|---|

| main/master | Manter a versão principal do projeto. |

| develop | Integrar funcionalidades durante o desenvolvimento. |

| feature | Desenvolver funcionalidades específicas. |



\### Merge



O \*\*merge\*\* é o processo de integrar as alterações de uma branch em outra.



\### Conflitos



Conflitos podem ocorrer quando diferentes branches modificam a mesma parte de um arquivo.



Nessas situações, é necessário analisar as mudanças e resolver manualmente as diferenças.



\### Situação-problema apresentada



O professor apresentou o exemplo de uma equipe que precisava implementar uma nova funcionalidade e corrigir um erro crítico.



Para evitar alterações diretas na branch principal, foram utilizadas branches separadas:



\- \*\*Feature:\*\* desenvolvimento da nova funcionalidade;

\- \*\*Hotfix:\*\* correção urgente do erro;

\- \*\*Main:\*\* manutenção da versão estável.



Após os testes, as alterações foram integradas à branch principal.



Essa organização permite desenvolver e corrigir funcionalidades de maneira independente, reduzindo os riscos para a versão em produção.



\## 10. Boas práticas com Git



Entre as boas práticas apresentadas estão:



\- Realizar commits pequenos e frequentes;

\- Escrever mensagens de commit claras;

\- Manter a branch principal estável;

\- Utilizar branches para novas funcionalidades;

\- Atualizar a branch antes de realizar merge;

\- Resolver conflitos cuidadosamente;

\- Executar testes antes de integrar alterações.



Essas práticas contribuem para a qualidade e manutenção dos projetos.



\### Complemento — Padronização dos commits



Para organizar o histórico dos projetos da disciplina, será utilizado o seguinte padrão:



| Prefixo | Utilização |

|---|---|

| docs | Documentação |

| feat | Nova funcionalidade |

| fix | Correção de erro |

| refactor | Reorganização do código |

| chore | Configurações e manutenção |



Exemplo:



```bash

git commit -m "docs: atualiza documentacao da aula 03"

```



\## 11. Deploy e hospedagem



O \*\*deploy\*\* é o processo de disponibilizar uma aplicação em um ambiente de produção, permitindo seu acesso pelos usuários.



O processo pode incluir:



\- Compilação do código;

\- Configuração do ambiente;

\- Testes finais;

\- Publicação da aplicação.



\### Ambientes apresentados



| Ambiente | Finalidade |

|---|---|

| Desenvolvimento | Criação e testes locais do projeto. |

| Staging | Validação antes da publicação definitiva. |

| Produção | Ambiente acessado pelos usuários finais. |



O deploy conecta o desenvolvimento à utilização real da aplicação.



\## 12. Vercel



A \*\*Vercel\*\* é uma plataforma de hospedagem utilizada para publicar sites e aplicações web.



\*\*Site:\*\* https://vercel.com/



\### Principais características



\- Integração com GitHub, GitLab e Bitbucket;

\- Deploy automatizado após alterações enviadas ao repositório;

\- Suporte a frameworks modernos;

\- Possibilidade de retornar a deploys anteriores;

\- Hospedagem de sites estáticos e aplicações modernas;

\- Suporte a funções serverless;

\- Distribuição de conteúdo por CDN;

\- Recursos de desempenho e escalabilidade.



A integração com o Git facilita a publicação e atualização dos projetos.



\## 13. Atividade proposta



A atividade da Aula 03 foi dividida em duas etapas.



\### Etapa 1 — Desenvolvimento, versionamento e deploy



Criar um repositório no GitHub e configurar um projeto simples, como uma página HTML com layout inicial.



Em seguida:



1\. Utilizar o Git para versionar o código;

2\. Criar tags para identificar versões estáveis;

3\. Personalizar o projeto;

4\. Conectar o repositório à Vercel;

5\. Realizar o deploy da aplicação;

6\. Garantir que o site esteja acessível online.



\### Etapa 2 — Documentação



Documentar todo o processo realizado, incluindo:



\- Justificativa das escolhas de design;

\- Personalizações implementadas;

\- Etapas do versionamento;

\- Processo de deploy;

\- Prints das telas;

\- Link do repositório no GitHub;

\- Link do site publicado na Vercel.



Todas as informações deverão ser reunidas em um documento organizado e submetidas como entrega da atividade.



\## 14. Conclusão



A Aula 03 apresentou os fundamentos do versionamento, demonstrando a importância do Git para o controle e a organização de projetos.



Foram estudados o versionamento semântico, as tags, as branches e o processo de merge.



Também foram abordados os ambientes de desenvolvimento e produção, além da utilização da Vercel para hospedagem e deploy de aplicações web.



\## 15. Referências



DINIZ, Luciana Mara Freitas et al. Aprendizado baseado em projetos em IHC (presencial e remoto): prototipação segundo as heurísticas de Nielsen. In: \*\*SIMPÓSIO BRASILEIRO DE FATORES HUMANOS EM SISTEMAS COMPUTACIONAIS (IHC)\*\*, 2020. Anais \[...]. SBC, 2020. p. 13-18.



FERREIRA, Arthur Gonçalves. \*\*Interface de programação de aplicações (API) e web services\*\*. São Paulo: Platos Soluções Educacionais, 2021.



FREEMAN, E.; ROBSON, E. \*\*Modern Web Development: building and deploying with modern tools\*\*. 1. ed. Sebastopol: O'Reilly Media, 2022.



GONÇALVES, Rodrigo Franco et al. Uma proposta de processo de produção de aplicações Web. \*\*Production\*\*, v. 15, p. 376-389, 2005.



HODSON, R. \*\*Continuous Delivery and DevOps: a quickstart guide\*\*. 2. ed. Birmingham: Packt Publishing, 2023.



LUCASSEN, Garm et al. The use and effectiveness of user stories in practice. In: \*\*REQUIREMENTS ENGINEERING: FOUNDATION FOR SOFTWARE QUALITY (REFSQ)\*\*, 22., 2016, Gothenburg. Proceedings \[...]. Springer International Publishing, 2016. p. 205-222.



MILETTO, Evandro Manara; DE CASTRO BERTAGNOLLI, Silvia. \*\*Desenvolvimento de Software II: introdução ao desenvolvimento web com HTML, CSS, JavaScript e PHP\*\*. \[S. l.]: Bookman, 2014.



NEWMAN, S. \*\*Building Microservices: designing fine-grained systems\*\*. 2. ed. Sebastopol: O'Reilly Media, 2021.



OLIVEIRA, Cláudio Luís Vieira. \*\*Node.js: programe de forma rápida e prática\*\*. São Paulo: Expressa, 2021.



RANJAN, Alok; SINHA, Abhilasha; BATTEWAD, Ranjit. \*\*JavaScript for Modern Web Development\*\*. \[S. l.]: BPB Publications, 2020.



SALINAS, C. et al. Agile, Web Engineering and Capability Maturity Model Integration: a systematic literature review. \*\*Information and Software Technology\*\*, v. 71, p. 92-107, 2016. DOI: 10.1016/j.infsof.2015.11.002.



TATE, B.; LOUTH, F. \*\*Version Control with Git: powerful tools and techniques for collaborative software development\*\*. Sebastopol: O'Reilly Media, 2022.



WILDT, Daniel et al. \*\*Extreme Programming: práticas para o dia a dia no desenvolvimento ágil de software\*\*. São Paulo: Casa do Código, 2015.



ZABOT, Diego. \*\*Aplicativos com Bootstrap e Angular: como desenvolver apps responsivos\*\*. São Paulo: Érica, 2020.



\---



\*\*Complemento — Navegação do repositório\*\*



\- \[Documentação da Atividade 03](../atividades/aula-03/README.md)

\- \[Índice das aulas](README.md)

\- \[Página principal do repositório](../README.md)

