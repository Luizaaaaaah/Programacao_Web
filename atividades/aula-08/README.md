# Atividade 08 — API de notas com CRUD e front-end React

**Disciplina:** Programação Web  
**Professor:** Prof. Me. Deivison S. Takatu

## 1. Objetivo

Construir uma API REST de notas com Express.js, armazenar os dados em JSON, desenvolver uma interface React que consuma as rotas e publicar o back-end no Render e o front-end na Vercel. A atividade também pede uma coleção Postman para documentar as operações CRUD.

## 2. O que foi solicitado

- Back-end Express com leitura, criação, edição e exclusão de notas.
- Armazenamento de registros em data.json.
- Front-end React integrado à API.
- Deploy do back-end no Render e da interface na Vercel.
- Relatório com prints do código, aplicação, links dos repositórios e URLs publicadas.
- Coleção Postman com as quatro operações CRUD, parâmetros e códigos de resposta.

## 3. Projetos encontrados

| Parte | Repositório | Conteúdo identificado |
|---|---|---|
| API | [exercicio_express1](https://github.com/Luizaaaaaah/exercicio_express1) | server.js, data.json e package.json |
| Front-end | [exercicio_react1](https://github.com/Luizaaaaaah/exercicio_react1) | Aplicação React com listagem, criação, edição e exclusão de notas |

### Back-end

O arquivo server.js define as rotas:

| Método | Endpoint | Operação |
|---|---|---|
| GET | /api/notes | Listar notas |
| POST | /api/notes | Criar nota |
| PUT | /api/notes/:id | Editar nota |
| DELETE | /api/notes/:id | Excluir nota |

O arquivo data.json foi localizado. O servidor utiliza Express, body-parser e fs para receber JSON, ler e salvar os registros.

**Ponto de atenção:** a árvore do repositório mostra node_modules versionado e não foi encontrado um .gitignore na raiz. O recomendado é retirar a pasta do Git e ignorá-la; as dependências devem ser restauráveis pelo package.json/package-lock.json.

### Front-end

O arquivo src/App.jsx foi conferido. A interface apresenta notas em cards e implementa busca da lista, modal para criar/editar, validação de título e conteúdo, confirmação de exclusão e atualização da lista após as requisições.

O endereço configurado no código é http://localhost:3000/api/notes. Isso demonstra integração no ambiente local, mas ainda precisa ser substituído pela URL pública do Render para o deploy.

## 4. Deploy e testes

| Entrega | Link / situação |
|---|---|
| API GitHub | [exercicio_express1](https://github.com/Luizaaaaaah/exercicio_express1) |
| Front-end GitHub | [exercicio_react1](https://github.com/Luizaaaaaah/exercicio_react1) |
| Endpoint local configurado | http://localhost:3000/api/notes |
| URL pública Render | Não localizada |
| URL pública Vercel | Não localizada |
| Coleção Postman | Não localizada |

Antes de considerar a integração pronta, testar os quatro métodos com a API publicada e configurar o front-end para usar o endereço público. O arquivo local JSON também deve ser avaliado para persistência e concorrência no ambiente de produção.

## 5. Evidências a anexar

| Arquivo sugerido | O que deve mostrar |
|---|---|
| 01-estrutura-api.png | server.js, data.json e package.json |
| 02-listar-notas-get.png | Requisição GET e resposta |
| 03-criar-nota-post.png | Requisição POST e nota criada |
| 04-editar-nota-put.png | Requisição PUT e resposta atualizada |
| 05-excluir-nota-delete.png | Requisição DELETE |
| 06-interface-react.png | Lista de notas no front-end |
| 07-modal-criar-editar.png | Formulário e validação |
| 08-render-deploy.png | Serviço de back-end publicado |
| 09-vercel-deploy.png | Front-end publicado |
| 10-postman-collection.png | Coleção com os quatro endpoints |

As capturas devem ser colocadas em [prints/](prints/README.md).

## 6. Questões de reflexão indicadas nos slides

- Quais riscos de segurança existem e como poderiam ser mitigados?
- O arquivo JSON é adequado para produção? Quais são os limites e benefícios?
- Que dificuldades surgiriam com 10.000 registros?
- Como dividir o código em módulos, rotas e serviços para facilitar manutenção?

## 7. Situação desta documentação

- [x] Repositório da API localizado e código CRUD conferido.
- [x] Arquivo de dados JSON localizado.
- [x] Repositório React localizado e operações CRUD identificadas no código.
- [ ] Substituir localhost pela URL de produção do Render.
- [ ] Confirmar deploy do Render e da Vercel.
- [ ] Criar e compartilhar a coleção Postman.
- [ ] Documentar testes e anexar capturas.