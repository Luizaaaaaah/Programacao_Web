# Atividade 05 — Aplicação React com cinco funcionalidades

**Disciplina:** Programação Web  
**Professor:** Prof. Me. Deivison S. Takatu  
**Curso:** Análise e Desenvolvimento de Sistemas — Fatec Itapetininga  
**Projeto:** React App — Funcionalidades  
**Repositório do código:** [exercicio_react](https://github.com/Luizaaaaaah/exercicio_react)

## 1. Objetivo

Desenvolver uma aplicação web utilizando React e reunir cinco funcionalidades em uma mesma interface: lista de tarefas, contador de cliques, jogo da velha, calculadora e buscador de CEP. A atividade envolve também organização do código, estilização, versionamento no GitHub, publicação na Vercel e registro das evidências.

## 2. Requisitos propostos na aula

- Criar uma aplicação React com cabeçalho e navegação entre as funcionalidades.
- Implementar To-Do List, contador de cliques, jogo da velha, calculadora e buscador de CEP.
- Aplicar uma identidade visual e adaptar a interface a diferentes tamanhos de tela.
- Registrar o código no GitHub.
- Publicar o projeto na Vercel.
- Documentar as etapas, escolhas de interface, capturas de tela e links.

## 3. Projeto desenvolvido

O projeto está disponível no repositório [Luizaaaaaah/exercicio_react](https://github.com/Luizaaaaaah/exercicio_react), na branch **main**.

A aplicação apresenta um cabeçalho identificado como **React App**, com botões para alternar entre uma tela inicial e as cinco funcionalidades. A tela inicial reúne cartões de apresentação, cada um com um botão para acessar o recurso correspondente.

A navegação entre as telas é controlada por um estado React chamado **pagina**, atualizado por **setPagina**. Assim, o conteúdo é alternado sem precisar carregar uma nova página no navegador.

### 3.1. To-Do List

A lista de tarefas permite digitar uma atividade, adicioná-la, marcar ou desmarcar sua conclusão e removê-la.

No código, as tarefas são armazenadas em um estado chamado **tarefas**. Cada registro possui identificador, texto e um indicador de conclusão. Uma entrada vazia é rejeitada; ao selecionar o texto da tarefa, sua conclusão é alternada.

**Observação:** no código consultado, as tarefas ficam no estado da aplicação. Não foi implementado armazenamento em banco de dados ou localStorage; por isso, não se deve afirmar que permanecem após recarregar a página.

### 3.2. Contador de cliques

O contador começa em zero e mostra a quantidade de cliques. O botão **Clique aqui** incrementa o valor, enquanto **Zerar** o retorna ao estado inicial.

A funcionalidade demonstra a utilização de **useState** e a atualização automática da interface quando o estado muda.

### 3.3. Jogo da velha

O jogo apresenta um tabuleiro de **3 × 3**, no qual os jogadores **X** e **O** fazem jogadas alternadas.

A função de verificação confere as combinações horizontais, verticais e diagonais. A interface informa o vencedor ou o empate e disponibiliza o botão **Reiniciar Jogo**. O código impede jogar em uma posição ocupada ou continuar depois que há um vencedor.

### 3.4. Calculadora

A calculadora permite informar dois números e escolher entre **adição, subtração, multiplicação e divisão**.

Os valores são convertidos em números antes do cálculo. Quando algum valor é inválido, aparece uma mensagem de orientação. A divisão por zero também é tratada com mensagem específica.

### 3.5. Buscador de CEP

O buscador recebe um CEP, remove os caracteres não numéricos e verifica se foram informados **oito dígitos**.

A consulta utiliza a API pública [ViaCEP](https://viacep.com.br/), com uma requisição **fetch** ao endereço correspondente. Quando encontrado, o resultado apresenta CEP, logradouro, bairro, cidade e estado. O código também contém tratamentos para CEP inválido, CEP não encontrado e falha na requisição.

## 4. Tecnologias e organização do código

| Tecnologia ou recurso | Aplicação no projeto |
|---|---|
| React | Construção da interface e renderização condicional |
| JavaScript e JSX | Lógica, eventos e estrutura dos componentes |
| useState | Controle das páginas, tarefas, contador, jogo, calculadora e CEP |
| HTML e CSS | Estrutura e apresentação visual |
| CSS Media Queries | Ajustes de layout em telas menores |
| fetch e async/await | Requisição ao ViaCEP |
| Node.js e NPM | Ambiente de desenvolvimento e gerenciamento de dependências |
| Git e GitHub | Versionamento e disponibilização do código |

**Arquivos consultados:**

| Arquivo | Função |
|---|---|
| [src/App.js](https://github.com/Luizaaaaaah/exercicio_react/blob/main/src/App.js) | Implementa a navegação e as cinco funcionalidades |
| [src/index.js](https://github.com/Luizaaaaaah/exercicio_react/blob/main/src/index.js) | Monta a aplicação React e carrega os estilos globais |
| [src/index.css](https://github.com/Luizaaaaaah/exercicio_react/blob/main/src/index.css) | Concentra os estilos personalizados e a responsividade |
| [src/App.css](https://github.com/Luizaaaaaah/exercicio_react/blob/main/src/App.css) | Mantém estilos básicos do projeto React |
| [package.json](https://github.com/Luizaaaaaah/exercicio_react/blob/main/package.json) | Define dependências e comandos do projeto |

O projeto utiliza React, React DOM e o conjunto de scripts do **Create React App**. O código observado foi escrito principalmente em um componente chamado **App**, com diferentes seções exibidas conforme a opção selecionada.

## 5. Estilização e experiência do usuário

A identidade visual utiliza cabeçalho e rodapé em cinza-escuro (**#20232a**), fundo geral claro (**#f4f6f8**), cartões brancos, botões arredondados e detalhes em azul-ciano (**#61dafb**).

A escolha de cartões na página inicial facilita o reconhecimento das funcionalidades. A navegação por botões mantém os cinco exercícios dentro de uma mesma aplicação.

A folha **src/index.css** contém regras responsivas para larguras de até **768 px**: o cabeçalho passa a organizar seu conteúdo verticalmente, o menu é centralizado, o formulário de tarefas passa a utilizar coluna e o espaçamento das seções é reduzido.

Essas decisões são identificadas no código-fonte; testes visuais em diferentes dispositivos ainda precisam ser registrados como evidência.

## 6. Como executar localmente

Em um computador com Node.js e NPM instalados:

~~~bash
git clone https://github.com/Luizaaaaaah/exercicio_react.git
cd exercicio_react
npm install
npm start
~~~

O comando **npm start** inicia o servidor de desenvolvimento. Para gerar a versão de produção, o projeto dispõe de **npm run build**. Estes são os comandos configurados no package.json; a execução não foi realizada nesta conferência.

## 7. Publicação e links

| Recurso | Situação |
|---|---|
| Repositório GitHub | [exercicio_react](https://github.com/Luizaaaaaah/exercicio_react) |
| Código principal | [src/App.js](https://github.com/Luizaaaaaah/exercicio_react/blob/main/src/App.js) |
| Estilos da interface | [src/index.css](https://github.com/Luizaaaaaah/exercicio_react/blob/main/src/index.css) |
| Deploy na Vercel | **Pendente de confirmação:** não foi identificada uma URL de produção verificada |
| Teste em navegador | **Pendente de confirmação** |

Não foram atribuídas tags, releases ou endereços de publicação que não tenham sido confirmados no GitHub ou por execução real.

## 8. Evidências a reunir

As capturas reais devem ser armazenadas na pasta [prints](prints/README.md).

| Nome da imagem | Conteúdo esperado |
|---|---|
| 01-menu-inicial.png | Cabeçalho, cartões e menu da aplicação |
| 02-todo-list.png | Tarefa adicionada e exemplo de conclusão |
| 03-contador.png | Contador após alguns cliques |
| 04-jogo-da-velha.png | Tabuleiro e situação de vitória ou empate |
| 05-calculadora.png | Operação executada e resultado |
| 06-buscador-cep.png | CEP consultado e endereço retornado |
| 07-github-commits.png | Histórico real de commits do projeto |
| 08-vercel-deploy.png | Tela do projeto publicado na Vercel |
| 09-site-publicado.png | Aplicação aberta pela URL pública |

As imagens são previstas para a entrega; **não estão sendo apresentadas como anexadas** nesta versão do relatório.

## 9. Verificação da atividade

- [x] Repositório e estrutura do projeto identificados.
- [x] Código das cinco funcionalidades analisado.
- [x] Recursos de React e integração com ViaCEP documentados.
- [x] Estilização e responsividade descritas com base no CSS.
- [x] Referências para os arquivos do projeto adicionadas.
- [ ] Executar a aplicação e testar as funcionalidades no navegador.
- [ ] Confirmar e registrar a URL publicada na Vercel.
- [ ] Inserir capturas reais das cinco funcionalidades, do GitHub e do deploy.

## 10. Conclusão

O exercício reúne, em uma interface React, cinco situações práticas de interação com o usuário: gerenciamento de tarefas, atualização de contador, regras de jogo, operações matemáticas e consulta de uma API externa.

A análise do código permitiu identificar o uso de estados, tratamento de eventos, renderização condicional, validação de dados e CSS responsivo. O projeto oferece uma base para compreender como recursos independentes podem ser apresentados dentro de uma aplicação front-end.

A documentação foi elaborada a partir do código disponível no repositório próprio, sem reaproveitar o texto do relatório de outro estudante. A validação da aplicação publicada e as capturas de tela permanecem como etapas de conclusão.
