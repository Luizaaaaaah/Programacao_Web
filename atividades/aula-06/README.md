# Atividade 06 — Projetos front-end em React, Angular e Vue

**Disciplina:** Programação Web  
**Professor:** Prof. Me. Deivison S. Takatu  
**Instituição:** Fatec Itapetininga

## 1. Objetivo e proposta da aula

A atividade propôs criar três projetos independentes utilizando **React**, **Angular** e **Vue**, modificar os projetos iniciais, importar e personalizar um template em um quarto repositório, publicar os quatro projetos na **Vercel** e documentar o processo com links e capturas.

Este relatório aproveita o código existente nos repositórios já desenvolvidos, distinguindo as implementações confirmadas das etapas ainda não comprovadas.

## 2. Repositórios relacionados

| Papel na atividade | Repositório | Situação observada |
|---|---|---|
| Projeto React | [exercicio_react](https://github.com/Luizaaaaaah/exercicio_react) | Aplicação com cinco funcionalidades, também documentada na Aula 05; confirmar seu reaproveitamento nesta aula |
| Projeto Angular | [exercicio_angular](https://github.com/Luizaaaaaah/exercicio_angular) | Código Angular identificado e analisado |
| Projeto Vue básico | [exercicio_vue](https://github.com/Luizaaaaaah/exercicio_vue) | Organizador de Estudos em Vue 3 criado como complementação em 24/11/2026; execução no navegador ainda pendente; deploy Vercel `READY` confirmado |
| Projeto Vue personalizado | [vue-project](https://github.com/Luizaaaaaah/vue-project) | HoennDex desenvolvida em Vue com pesquisa, filtros e design próprio |

**Trabalho em conjunto:** também foi encontrado o repositório [pokedex_vue, do Rafael](https://github.com/RafaelRachidd/pokedex_vue), com código Vue. Esse material pode ser consultado como referência do trabalho compartilhado, sem atribuir a ele automaticamente o papel de quarto projeto ou de template utilizado.

## 3. Projeto Angular — Mini Jogos

**Repositório:** [exercicio_angular](https://github.com/Luizaaaaaah/exercicio_angular)

A aplicação está organizada em um componente Angular com lógica no arquivo [src/app/app.ts](https://github.com/Luizaaaaaah/exercicio_angular/blob/main/src/app/app.ts), estrutura no arquivo [src/app/app.html](https://github.com/Luizaaaaaah/exercicio_angular/blob/main/src/app/app.html) e estilos em [src/app/app.css](https://github.com/Luizaaaaaah/exercicio_angular/blob/main/src/app/app.css).

### 3.1. Funcionalidades

| Funcionalidade | Funcionamento identificado no código |
|---|---|
| Contador | Incrementa, decrementa sem permitir valores negativos e reinicia em zero |
| Dado | Sorteia um número inteiro de 1 a 6 |
| Adivinhe o número | Gera um número de 1 a 50, recebe palpites, informa se o usuário deve tentar um valor maior ou menor e conta tentativas |

O projeto utiliza **TypeScript**, **Angular**, **CommonModule** e **FormsModule**. No template, são usados eventos de clique, interpolação, diretivas condicionais e associação de formulário com **ngModel**.

### 3.2. Estilização

A interface apresenta cartões em fundo claro, números destacados, botões azul-índigo e campos arredondados. As regras de CSS definem um conteúdo centralizado com largura máxima de 500 px e disposição flexível para os botões.

### 3.3. Execução prevista

Após clonar o repositório e instalar as dependências:

~~~bash
npm install
npm start
~~~

O comando de compilação previsto em **package.json** é **npm run build**. Esta conferência analisou o código, mas não executou o aplicativo no navegador.

## 4. Projeto Vue — HoennDex

**Repositório:** [vue-project](https://github.com/Luizaaaaaah/vue-project)

O arquivo [src/App.vue](https://github.com/Luizaaaaaah/vue-project/blob/main/src/App.vue) apresenta uma aplicação temática da região de Hoenn com:

- Cabeçalho e navegação para Início, Pokédex e Sobre Hoenn;
- Destaque visual de apresentação;
- Catálogo com nove Pokémon cadastrados diretamente no código;
- Filtro por nome e por tipo;
- Exibição de imagem, número, tipos e atributos de HP, ataque e defesa;
- Seção informativa sobre a região de Hoenn.

### 4.1. Recursos Vue utilizados

| Recurso | Aplicação |
|---|---|
| Vue 3 | Estrutura e atualização da interface |
| TypeScript | Definição do formato dos dados dos Pokémon |
| script setup | Organização da lógica do componente |
| ref | Estados de pesquisa e de filtro |
| computed | Lista de Pokémon filtrados |
| v-model | Vinculação dos filtros aos campos |
| v-for | Geração dos cartões e tipos |
| Vite | Ambiente de desenvolvimento e build |

As imagens são referenciadas por endereços do repositório público de sprites da PokeAPI; os dados dos nove Pokémon presentes no catálogo estão declarados localmente no componente. **Não foi identificada uma consulta dinâmica à API para carregar os Pokémon.**

### 4.2. Identidade visual e responsividade

A HoennDex utiliza vermelho no cabeçalho e nos detalhes, cartões claros, imagens dos Pokémon e blocos de apresentação. Em larguras de até 800 px, o código CSS altera a disposição do destaque, dos filtros e da seção informativa, além de ocultar a navegação do cabeçalho.

### 4.3. Execução prevista

~~~bash
npm install
npm run dev
~~~

Para compilação de produção, o projeto define **npm run build**. Ainda é necessário registrar uma execução real e o link de publicação.

### 4.4. Projeto Vue básico — Organizador de Estudos

O repositório [exercicio_vue](https://github.com/Luizaaaaaah/exercicio_vue), inicialmente vazio, recebeu em **24/11/2026** uma implementação complementar em Vue 3 e Vite, separada da HoennDex.

A aplicação chamada **Organizador de Estudos** permite cadastrar tarefas acadêmicas, escolher prioridades, marcar atividades concluídas, excluir itens, filtrar a lista e armazenar dados no **localStorage**.

O código utiliza os recursos **ref**, **computed**, **watch**, **v-model** e **v-for**, além de estilos responsivos. Os arquivos principais são [src/App.vue](https://github.com/Luizaaaaaah/exercicio_vue/blob/main/src/App.vue) e [src/style.css](https://github.com/Luizaaaaaah/exercicio_vue/blob/main/src/style.css).

Este projeto foi criado para completar a prática e **não é apresentado como entrega originalmente produzida na data da aula**. Seu deploy foi criado na Vercel e recebeu status `READY`; o funcionamento no navegador ainda precisa ser testado.

## 5. Projeto React

O projeto [exercicio_react](https://github.com/Luizaaaaaah/exercicio_react) utiliza React e contém **To-Do List, contador de cliques, jogo da velha, calculadora e buscador de CEP**.

A implementação completa está descrita no [relatório da Atividade 05](../aula-05/README.md). Como o mesmo repositório foi utilizado nessa atividade anterior, seu vínculo como o primeiro projeto da Aula 06 precisa ser confirmado, sem duplicar artificialmente a autoria ou a entrega.

## 6. Importação e personalização de template

O enunciado pede um quarto repositório derivado de um template pesquisado e personalizado.

A aplicação HoennDex possui estrutura e personalizações identificáveis no código, mas **não foi localizado o endereço do template original, o procedimento de importação nem uma comparação antes/depois**. Portanto, não é possível afirmar que todas as exigências da importação foram comprovadas apenas pelo código final.

O repositório **exercicio_vue** estava vazio na conferência original e recebeu posteriormente uma implementação básica própria, o **Organizador de Estudos**, em 24/11/2026. A HoennDex continua sendo um projeto Vue distinto; a fonte do template importado ainda precisa ser confirmada.

## 7. Publicação e entrega

| Projeto | Código | URL de produção |
|---|---|---|
| React | [exercicio_react](https://github.com/Luizaaaaaah/exercicio_react) | [exercicio-react-ecru.vercel.app](https://exercicio-react-ecru.vercel.app) — `READY` |
| Angular | [exercicio_angular](https://github.com/Luizaaaaaah/exercicio_angular) | [exercicioangular.vercel.app](https://exercicioangular.vercel.app) — `READY` |
| Vue básico | [exercicio_vue](https://github.com/Luizaaaaaah/exercicio_vue) — complementação em 24/11/2026 | [exercicio-vue-fawn.vercel.app](https://exercicio-vue-fawn.vercel.app) — `READY` |
| Vue personalizado | [vue-project](https://github.com/Luizaaaaaah/vue-project) | [vue-project-alpha-peach.vercel.app](https://vue-project-alpha-peach.vercel.app) — `READY` |

Os quatro links foram obtidos diretamente da conta Vercel conectada. Os deploys aparecem com estado `READY`, mas **não foi validado** o funcionamento das interfaces no navegador, o acesso por terceiros nem a origem do template.

## 8. Evidências

Capturas reais a incluir na pasta [prints](prints/README.md):

| Arquivo | Evidência |
|---|---|
| 01-projeto-react.png | Aplicação React |
| 02-projeto-angular.png | Mini Jogos em Angular |
| 03-projeto-vue.png | Projeto Vue de base, quando recuperado |
| 04-template-original.png | Template antes da personalização |
| 05-template-personalizado.png | HoennDex personalizada |
| 06-quatro-repositorios.png | Quatro repositórios utilizados |
| 07-quatro-deploys.png | Quatro endereços Vercel confirmados |

## 9. Situação da atividade

- [x] Código do projeto Angular analisado e documentado.
- [x] Código do projeto HoennDex em Vue analisado e documentado.
- [x] Projeto React da Aula 05 localizado.
- [ ] Confirmar o projeto React correspondente à Aula 06.
- [x] Criar implementação básica em Vue no repositório anteriormente vazio (complementação em 24/11/2026).
- [ ] Identificar o template original e registrar as modificações.
- [ ] Executar e testar os projetos no navegador.
- [x] Identificar e registrar os quatro deploys no painel da Vercel (`READY`).
- [ ] Testar funcionamento e acesso público de cada interface.
- [ ] Adicionar os prints reais.

## 10. Conclusão

A consulta aos projetos existentes demonstrou o uso de diferentes tecnologias para construir interfaces: React para aplicações baseadas em estado, Angular com componentes e formulários, e Vue com reatividade e filtros calculados.

A documentação aproveita os trabalhos já disponíveis. Ela não declara como concluídos os itens cuja execução, importação ou publicação não foi confirmada.
