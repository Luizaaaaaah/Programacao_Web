# Atividade 08 — CRUD de notas com Express e React

**Disciplina:** Programação Web  
**Professor:** Prof. Me. Deivison S. Takatu  
**Instituição:** Fatec Itapetininga

## 1. Objetivo

Construir uma API REST de notas com Express e armazenamento em JSON; criar um front-end React que utilize os métodos HTTP para listar, cadastrar, editar e excluir notas; registrar uma coleção de requisições no Postman; e publicar back-end e front-end.

## 2. Projetos reaproveitados

| Parte | Repositório | Código principal |
|---|---|---|
| Back-end Express | [exercicio_express1](https://github.com/Luizaaaaaah/exercicio_express1) | [server.js](https://github.com/Luizaaaaaah/exercicio_express1/blob/main/server.js) |
| Front-end React | [exercicio_react1](https://github.com/Luizaaaaaah/exercicio_react1) | [src/App.jsx](https://github.com/Luizaaaaaah/exercicio_react1/blob/main/src/App.jsx) |
| Armazenamento | [data.json](https://github.com/Luizaaaaaah/exercicio_express1/blob/main/data.json) | Arquivo JSON local do servidor |

Ambos os projetos já possuem código desenvolvido; não é necessário recomeçar do zero.

## 3. API REST com Express

O arquivo **server.js** utiliza Express, body-parser e o módulo fs do Node.js. Os registros são lidos do arquivo **data.json** e gravados novamente após operações de escrita.

| Método | Endpoint | Comportamento identificado |
|---|---|---|
| GET | /api/notes | Retorna a lista de notas |
| POST | /api/notes | Adiciona nota a partir de título e texto; responde com a nova nota |
| PUT | /api/notes/:id | Atualiza título e texto da nota indicada |
| DELETE | /api/notes/:id | Remove a nota com o identificador informado |

### Formato dos dados

Os objetos de nota utilizam os campos **id**, **titulo** e **texto**. O arquivo de exemplo possui também **criadoEm** em seus registros iniciais; a rota de cadastro atual não preenche esse campo para novos registros.

### Respostas e tratamento de erros

O código retorna erro **404** quando uma nota solicitada por PUT não é encontrada. Na implementação observada, o cadastro retorna HTTP **200**, e a exclusão retorna uma mensagem de sucesso mesmo se nenhum item corresponder ao ID; essas são características do código atual, não recomendações de comportamento de produção.

### Pontos de atenção antes do deploy

- A porta está fixa em **3000**, em vez de utilizar a variável **PORT** fornecida pelo serviço de hospedagem.
- O CORS é configurado apenas com o cabeçalho **Access-Control-Allow-Origin**. Requisições de edição com JSON feitas por um navegador podem exigir tratamento adequado do preflight **OPTIONS** e dos cabeçalhos e métodos permitidos.
- Não há validação completa das entradas ou autenticação de usuários.
- O armazenamento em **data.json** é local; plataformas com disco efêmero podem perder alterações após reinicializações ou novos deploys.
- O repositório contém **node_modules** versionado, o que deveria ser corrigido com um arquivo de exclusões e remoção dos arquivos rastreados, após revisão.

Esses ajustes são pendências técnicas identificadas no código; não foram aplicados silenciosamente aos repositórios originais.

## 4. Front-end React

O arquivo **src/App.jsx** utiliza **useState** e **useEffect** para carregar notas e controlar o formulário, estados de erro e modal.

As funcionalidades implementadas no código incluem:

- Busca e apresentação de notas em cartões;
- Contador de notas cadastradas;
- Formulário para criação de nota;
- Modal para edição, com preenchimento dos dados selecionados;
- Verificação de título e conteúdo não vazios;
- Exclusão mediante confirmação do usuário;
- Atualização da lista após operações;
- Mensagens para carregamento e falhas de requisição.

A interface utiliza React e Vite, com estilização no arquivo **src/App.css**.

### Integração atual

Na branch **main**, a constante **API_URL** permanece configurada como **http://localhost:3000/api/notes**. Na branch de revisão **preparar-deploy-aula-08**, ela passou a aceitar a variável **VITE_API_URL**, apontada para o endpoint existente no Render em um ambiente de prévia Vercel. A mudança não foi mesclada à main, e o funcionamento conjunto não foi validado.

## 5. Coleção Postman preparada

Foi adicionada uma coleção em formato **Postman Collection v2.1**, com quatro requisições CRUD baseadas nas rotas do servidor:

**[Abrir coleção de notas](postman/notas-crud.postman_collection.json)**

A coleção possui variáveis **baseUrl** (inicialmente http://localhost:3000) e **notaId**, além de exemplos de corpo JSON e verificações básicas de status.

**Como utilizar:**

1. Abra o Postman e escolha **Import**.
2. Selecione o arquivo **notas-crud.postman_collection.json**.
3. Configure **baseUrl** com o endereço local ou com a URL real da API no Render.
4. Execute **Listar notas**, depois **Criar nota**. Esta última requisição armazena o ID retornado em **notaId** para facilitar os testes de edição e exclusão.
5. Execute **Editar nota** e **Excluir nota**, verificando as respostas.

A coleção está **preparada**, mas sua importação e execução real ainda precisam ser realizadas. Os testes não foram marcados como aprovados.

## 6. Execução local prevista

### API

~~~bash
npm install
node server.js
~~~

O servidor utiliza **http://localhost:3000** quando iniciado com a configuração atual.

### Interface

~~~bash
npm install
npm run dev
~~~

O endereço local do front-end será indicado pelo Vite. Antes do teste, a API precisa estar em execução, e o navegador deverá permitir as requisições à origem configurada.

## 7. Questões de reflexão

### 7.1. Que riscos de segurança existem?

A API não implementa autenticação, autorização por usuário nem validações completas de conteúdo. Em um sistema público, isso permitiria acesso ou modificações indevidas. Uma versão para produção exigiria controles de identidade e permissão, validação de entradas, proteção contra abuso e configuração restrita de CORS.

### 7.2. Armazenar em JSON é adequado para produção?

Um único arquivo JSON é simples para exercícios didáticos e protótipos pequenos, mas apresenta riscos de perda de dados, gravações simultâneas e dificuldade de consulta. A permanência dos dados depende do tipo de disco da hospedagem.

### 7.3. E se existissem 10.000 registros?

A leitura e gravação do arquivo inteiro a cada operação aumentariam os custos e poderiam bloquear o processamento de requisições. Um banco de dados com consultas, índices e paginação seria mais adequado.

### 7.4. Como organizar melhor o código?

É possível separar rotas, controladores, serviços e acesso aos dados, além de centralizar validação, tratamento de erros, configuração de ambiente e testes automatizados.

Essas respostas são análise técnica da implementação; não descrevem mudanças já feitas no código.

## 8. Preparação para publicação em branches de revisão

Foram criados dois pull requests **em rascunho**, preservando as branches main originais:

- **[API Express — PR #1](https://github.com/Luizaaaaaah/exercicio_express1/pull/1):** porta configurável para Render, middleware CORS, caminho de dados ajustado, .gitignore e instruções de deploy.
- **[Front-end React — PR #1](https://github.com/Luizaaaaaah/exercicio_react1/pull/1):** variável VITE_API_URL, exemplo de configuração e instruções de deploy Vercel.

As alterações **não foram mescladas à main**. Em 24/11/2026, foi corrigido ainda o seletor CSS inválido em `src/index.css` (`*` ausente), que impedia o build da Vercel.

Uma **prévia na Vercel** foi compilada com status `READY` no commit `f8b21a2`: [abrir preview](https://exercicioreact1-git-preparar-deploy-aula-08-luizaaaaaah.vercel.app). A variável `VITE_API_URL` foi configurada para a prévia da branch de revisão e, depois, para a **produção** da Vercel, apontando para `https://exercicio-express1.onrender.com/api/notes`.

A compilação inicial da prévia não comprovava integração; posteriormente a estudante validou **CRUD de ponta a ponta** nessa prévia, comparando os resultados exibidos no React com as respostas GET do Render. Isso ainda não comprova a publicação da versão definitiva em produção. O acesso ao preview pode estar sujeito à proteção da Vercel.

## 9. Publicação

### Back-end existente no Render

A conta Render possui um serviço gratuito conectado ao repositório **exercicio_express1**, com deploy da branch **main**. A correção do PR #1 já foi integrada à `main` e publicada automaticamente no Render em 24/11/2026, horário de Brasília.

- **URL da API:** [https://exercicio-express1.onrender.com](https://exercicio-express1.onrender.com)
- **Endpoint previsto no código:** [https://exercicio-express1.onrender.com/api/notes](https://exercicio-express1.onrender.com/api/notes)
- **Painel do serviço:** [Render — exercicio_express1](https://dashboard.render.com/web/srv-dap9bgo0cd8s73c7040g)
- **Deploy:** `dep-dap9bh00cd8s73c70510`; commit `5680a121`; concluído em **22/09/2026**; status `live` na consulta de 24/11/2026.

**Importante:** o serviço usa a branch `main` do back-end. A `main` recebeu a correção CORS e a porta configurável, e o Render confirmou o deploy com status `live` em 24/11/2026 às 21h21 (Brasília). Depois disso, o fluxo CRUD foi validado na prévia React e conferido com GET do Render.

### Utilização da API no Postman e React

A coleção Postman contém a variável `baseUrl`, que pode ser configurada como `https://exercicio-express1.onrender.com` para apontar para o Render. Execute as operações de escrita somente em dados de teste: cadastrar, alterar e excluir modifica o arquivo do serviço.

No front-end React, a variável de produção `VITE_API_URL` foi configurada na Vercel com o valor `https://exercicio-express1.onrender.com/api/notes` e o PR #1 foi integrado à `main`.

| Entrega | Situação |
|---|---|
| API no GitHub | [exercicio_express1](https://github.com/Luizaaaaaah/exercicio_express1) |
| Front-end no GitHub | [exercicio_react1](https://github.com/Luizaaaaaah/exercicio_react1) |
| Coleção Postman | Criada neste portfólio; testes ainda não executados |
| URL Render | [exercicio-express1.onrender.com](https://exercicio-express1.onrender.com) — correção do back-end `live`; GET conferido antes, durante e após o CRUD |
| URL Vercel | [Produção React](https://exercicioreact1.vercel.app) — deploy `READY` do commit `18cf156` na `main` (25/11/2026); [prévia validada](https://exercicioreact1-git-preparar-deploy-aula-08-luizaaaaaah.vercel.app) também `READY` |
| Integração React + API Render | **Comprovada na prévia** por criação, listagem, edição e exclusão; front-end `main` publicado em produção (`READY`), mas ainda falta conferir acesso e CRUD diretamente na URL de produção |

A versão principal do front-end foi publicada no Vercel com estado `READY` no deploy `dpl_Fbhm5TvPDmZLpDUn1hSMtZ7rCCds` (commit `18cf1565d35c7caf16f1762379cc61ab7272efc9`). Após a publicação, a proteção SSO da Vercel foi configurada apenas para **prévias** (`preview`), preservando a proteção dos testes e permitindo acesso normal à versão de produção. Ainda é preciso conferir em janela anônima se a URL de produção abre sem login e testar o CRUD nela.

### Conferência inicial no navegador — 24/11/2026 (Brasília)

A estudante abriu os dois endereços da atividade e enviou capturas reais:

- **API Render, GET `/api/notes`:** a resposta JSON apresentou dois objetos com IDs `1` e `2`, incluindo os títulos **Lembretes** e **Tarefas do trabalho**, conteúdos de notas e o campo `criadoEm`. A resposta GET foi confirmada visualmente.
- **Prévia React na Vercel:** a página **Minhas Notas** abriu e apresentou **2 notas**, botão **Nova nota**, botões visuais de editar e excluir e os cartões. A abertura e renderização da interface foram confirmadas visualmente.
- **Atenção:** os títulos e parte dos textos dos cartões exibidos no React **não são iguais** aos objetos JSON capturados na API. Por isso, esses prints **não comprovam que o front-end está sincronizado com essa API específica**. É necessário criar uma nota de teste pela interface e atualizar o GET do Render para conferir se o novo registro aparece lá, antes de afirmar integração ou CRUD funcionando.

As duas capturas estão nesta conversa, **não foram anexadas ainda** à pasta `prints/` no GitHub. A criação, edição e remoção permanecem pendentes.

### Teste de criação — falhou na prévia React

A estudante tentou salvar a nota fictícia com título **“Teste Integracao Aula 08”** e conteúdo **“Verificando a conexao entre React e Express”**. O modal mostrou a mensagem **“Não foi possível salvar a nota.”** A captura comprova a falha da operação, e **não** comprova criação ou sincronização com a API.

**Hipótese técnica fundamentada no código:** na `main` do back-end, o middleware CORS define somente `Access-Control-Allow-Origin: *`. O POST do React utiliza `Content-Type: application/json`, que exige uma requisição preflight `OPTIONS` entre origens diferentes. Sem os cabeçalhos apropriados para métodos e cabeçalhos permitidos, o navegador pode bloquear esse POST. A correção do back-end foi **integrada à branch `main`** em 24/11/2026 (horário de Brasília) por meio do [PR #1](https://github.com/Luizaaaaaah/exercicio_express1/pull/1) (squash commit [`92d3584`](https://github.com/Luizaaaaaah/exercicio_express1/commit/92d35842e3ad108ac3d7ae87bae84bb75cec02f3)). A alteração substitui a configuração manual pelo middleware `cors()` e usa a porta `process.env.PORT || 3000`. **O novo deploy foi confirmado no Render**, com status `live` no serviço `exercicio_express1`, deploy `dep-dc32jc8jo6nc73e71abg` (commit `92d35842e3ad108ac3d7ae87bae84bb75cec02f3`), concluído em **24/11/2026 às 21h21 (horário de Brasília)**. O funcionamento do POST e a URL efetivamente usada pela prévia React ainda precisam de novo teste. É necessário repetir o teste e, se houver falha, inspecionar a aba Rede/Console ou os logs do serviço.

**Outra divergência observada:** os títulos e conteúdos das duas notas visíveis na interface da prévia diferem dos dados da API exibidos diretamente no navegador. Mesmo que o CORS seja corrigido, é preciso confirmar que a variável de ambiente `VITE_API_URL` aponta realmente para o serviço Render desejado.

A imagem da falha ainda está na conversa e não foi anexada ao GitHub.

### Reteste de criação após correção — resultado positivo

Após a integração do PR #1 e a publicação automática da API no Render (deploy `dep-dc32jc8jo6nc73e71abg`, commit `92d3584`, status `live`), a estudante repetiu a criação de uma nota pela interface React. A captura mostra **3 notas** e um novo cartão com título **“Teste de Integração Aula 08”** e conteúdo **“Verificando a conexão entre React e Express”**, sem a mensagem anterior de erro.

**Resultado confirmado:** o fluxo de criação pelo front-end voltou a funcionar no cenário observado, com atualização visual da listagem. A imagem está anexada na conversa e ainda precisa ser enviada à pasta `prints/` do repositório de documentação.

**Sincronização confirmada:** após a criação no React, a estudante atualizou `https://exercicio-express1.onrender.com/api/notes` e o JSON apresentou a **terceira nota**, título **“Teste Integracao Aula 08”**, com o mesmo conteúdo enviado na interface e um novo ID. Isso confirma a comunicação entre a prévia React e **essa API Render** no cenário GET + POST. Os dados iniciais diferiam entre as primeiras capturas; não é possível explicar a divergência anterior apenas com esses testes. A persistência após reinício do serviço não foi avaliada. As evidências estão preparadas para upload.


### Reteste de edição e exclusão — aprovado

**Edição:** a estudante alterou o título da nota de teste para **“Teste Aula 08”**, mantendo o conteúdo de verificação da conexão. O React exibiu três cartões com o título atualizado, e a resposta JSON de `GET /api/notes` no Render também apresentou o mesmo título no terceiro registro. A alteração foi confirmada em ambos os lados.

**Exclusão:** em seguida, a estudante removeu **somente a nota de teste** pela interface. O contador do React voltou de três para **duas notas**, e uma nova consulta `GET /api/notes` no Render retornou apenas os dois registros originais. A exclusão foi confirmada em ambos os lados.

**Conclusão dos testes funcionais:** na versão de **prévia React da Vercel** conectada à API Render corrigida, foram observados cenários positivos de **criar, listar, editar e excluir**. Os testes não demonstram, por si sós, persistência após reinício, validação de entradas inválidas ou publicação da `main` do front-end em produção.

**Evidências:** as **nove capturas reais foram enviadas e confirmadas** em [`atividades/aula-08/prints/`](prints/) na branch `reorganizacao`.


### Deploy de produção do React

O [PR #1 do front-end](https://github.com/Luizaaaaaah/exercicio_react1/pull/1) foi integrado à `main` com o commit [`18cf156`](https://github.com/Luizaaaaaah/exercicio_react1/commit/18cf1565d35c7caf16f1762379cc61ab7272efc9). A variável `VITE_API_URL` foi definida também para o ambiente **Production** na Vercel. O deploy `dpl_Fbhm5TvPDmZLpDUn1hSMtZ7rCCds` passou para **READY** e recebeu o domínio [exercicioreact1.vercel.app](https://exercicioreact1.vercel.app).

**Limites de validação:** o CRUD foi testado na prévia; a nova URL de produção ainda precisa ser aberta pelo usuário e, se possível, em janela anônima. A proteção SSO da Vercel foi alterada para atingir apenas as prévias, não a produção. Ainda falta testar a abertura da URL pública em janela anônima para confirmar o acesso sem autenticação.

## 10. Evidências

Capturas reais **confirmadas no GitHub** em [prints](prints/README.md):

| Arquivo | Evidência observada |
|---|---|
| [02-listar-notas-get.png](prints/02-listar-notas-get.png) | API Render antes da criação: dois registros |
| [03-criar-nota-post.png](prints/03-criar-nota-post.png) | React após criar a terceira nota |
| [04-editar-nota-put.png](prints/04-editar-nota-put.png) | React com título alterado para Teste Aula 08 |
| [05-excluir-nota-delete.png](prints/05-excluir-nota-delete.png) | React após excluir a nota de teste |
| [06-interface-react.png](prints/06-interface-react.png) | Tela inicial do React com duas notas |
| [07-modal-erro-inicial.png](prints/07-modal-erro-inicial.png) | Erro inicial ao tentar salvar uma nota antes da correção |
| [11-api-apos-post.png](prints/11-api-apos-post.png) | JSON do Render após a criação da terceira nota |
| [12-api-apos-put.png](prints/12-api-apos-put.png) | JSON do Render após edição do título |
| [13-api-apos-delete.png](prints/13-api-apos-delete.png) | JSON do Render após exclusão: duas notas |

Imagens adicionais como histórico de commits, painel Render, painel Vercel e execução da coleção Postman poderão ser acrescentadas se exigidas. Não foram tratadas como já anexadas.

### Galeria de evidências dos testes de integração

**Consulta inicial GET — duas notas**

![Consulta inicial GET — duas notas](prints/02-listar-notas-get.png)

**Interface inicial React — duas notas**

![Interface inicial React — duas notas](prints/06-interface-react.png)

**Falha anterior ao ajuste CORS**

![Falha anterior ao ajuste CORS](prints/07-modal-erro-inicial.png)

**Criação da terceira nota no React**

![Criação da terceira nota no React](prints/03-criar-nota-post.png)

**GET da API após criação**

![GET da API após criação](prints/11-api-apos-post.png)

**Edição da nota no React**

![Edição da nota no React](prints/04-editar-nota-put.png)

**GET da API após edição**

![GET da API após edição](prints/12-api-apos-put.png)

**Exclusão da nota no React**

![Exclusão da nota no React](prints/05-excluir-nota-delete.png)

**GET da API após exclusão**

![GET da API após exclusão](prints/13-api-apos-delete.png)

## 11. Situação da atividade

- [x] Código da API e do front-end localizado.
- [x] Quatro operações CRUD identificadas.
- [x] Estrutura dos dados e integração local documentadas.
- [x] Coleção Postman criada e vinculada ao relatório.
- [x] Correção do back-end integrada à `main` por meio do PR #1 em 25/11/2026.
- [x] Confirmar novo deploy da API no Render (`live`, commit `92d3584`).
- [x] Retestar criação de nota pela interface React após o deploy da correção, confirmada visualmente (3 notas).
- [x] Confirmar sincronização da nota criada no React com resposta GET do Render (terceiro registro).
- [x] Testar edição PUT e exclusão DELETE pela interface e verificar novamente por GET no Render.
- [x] Revisar e integrar o PR #1 do front-end React à `main` (squash commit `18cf156`).
- [x] Questões técnicas respondidas.
- [x] Corrigir o back-end e validar a integração do front-end no ambiente de prévia.
- [x] Concluir o deploy de produção do front-end na Vercel.
- [ ] Confirmar que terceiros acessam o site sem login.
- [ ] Importar e executar a coleção Postman.
- [x] Confirmar URL do serviço Render e histórico do deploy (sem validar respostas HTTP).
- [x] Confirmar build `READY` da interface em preview da branch de revisão.
- [x] Conferir abertura da prévia React e resposta GET da API por capturas reais.
- [x] Testar tentativa de criação pelo formulário e documentar a falha real observada.
- [x] Corrigir CORS na API, confirmar deploy `live` e validar criação, edição e exclusão pela prévia React, com conferência no Render.
- [x] Publicar o front-end na `main`/produção com deploy Vercel `READY`.
- [ ] Validar acesso público sem login e testar CRUD na URL de produção.
- [x] Preparar nove capturas reais do fluxo CRUD para upload.
- [x] Anexar as nove capturas reais na pasta `prints/`, conferidas no repositório.

## 12. Conclusão

O projeto permite estudar o fluxo completo de uma aplicação baseada em API: interface React, requisições HTTP, rotas Express e armazenamento JSON.

A API Render foi corrigida e publicada; o CRUD de notas foi validado na **prévia React** com conferência das alterações na API. Nove capturas reais foram anexadas ao portfólio e incluídas neste relatório. A versão aprovada do front-end foi integrada à `main` e gerou um deploy `READY` na Vercel. Ainda é necessário verificar o acesso do professor à URL de produção, retestar o CRUD diretamente nessa URL e, caso solicitado, executar a coleção Postman.
