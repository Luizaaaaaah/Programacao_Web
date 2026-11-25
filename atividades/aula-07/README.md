# Atividade 07 — API PurpleMood com Node.js e Express

**Disciplina:** Programação Web  
**Professor:** Prof. Me. Deivison S. Takatu  
**Instituição:** Fatec Itapetininga  
**Projeto:** PurpleMood

## 1. Objetivo e orientação recebida em sala

A Aula 07 abordou os fundamentos de desenvolvimento back-end e apresentou como exemplo uma API de consulta de data e hora com Express.

**Conforme informado pela estudante, durante a aula o professor orientou a turma a experimentar uma proposta diferente.** Por esse motivo, o projeto desenvolvido para esta atividade foi o **PurpleMood**, uma API relacionada ao registro de humor.

Esta documentação descreve o projeto realmente realizado, respeitando a orientação recebida em sala. A API de data e hora do material não está sendo tratada como uma pendência a ser refeita.

## 2. Projeto utilizado

**Código-fonte:** [Luizaaaaaah/exercicio_express](https://github.com/Luizaaaaaah/exercicio_express)  
**Arquivo principal:** [api.js](https://github.com/Luizaaaaaah/exercicio_express/blob/main/api.js)

O PurpleMood utiliza **Node.js**, **Express** e **CORS** para disponibilizar informações sobre registros de humor por meio de rotas HTTP que retornam dados em JSON.

O código começa com três registros de exemplo: Feliz, Tranquilo e Animado. Cada registro contém informações como identificador, humor, emoji, mensagem, intensidade, cor e data.

## 3. Endpoints implementados

| Método | Rota | Finalidade |
|---|---|---|
| GET | / | Identificar a API e informar seu status |
| GET | /humores | Listar os registros de humor |
| GET | /humores/:id | Consultar um humor específico |
| POST | /humores | Cadastrar um novo registro |
| PUT | /humores/:id | Atualizar um registro existente |
| DELETE | /humores/:id | Excluir um registro |
| GET | /estatisticas | Obter quantidade de registros e média de intensidade |
| GET | /frases | Obter frases motivacionais |

O código contém respostas de erro para identificadores não encontrados e para campos obrigatórios ausentes no cadastro.

### 3.1. Cadastro

A rota **POST /humores** recebe os campos relacionados ao humor e cria um registro. O código exige humor, mensagem e intensidade, e estabelece valores padrão para alguns campos.

### 3.2. Atualização e exclusão

O método **PUT** modifica campos de um registro identificado por ID. O método **DELETE** remove o registro correspondente, quando encontrado.

### 3.3. Estatísticas

A rota **GET /estatisticas** calcula a quantidade de registros e a média das intensidades cadastradas.

### 3.4. Frases

A rota **GET /frases** apresenta uma lista de mensagens motivacionais definidas no código.

## 4. Organização técnica

O arquivo **api.js** reúne a inicialização do Express, a configuração de CORS, a lista de dados de exemplo e as rotas.

Os dados são armazenados em um **array em memória**. Isso significa que as alterações não são persistidas em um banco de dados e podem ser perdidas quando o processo é reiniciado. O projeto tem caráter didático.

O código utiliza a porta **3000** definida diretamente no arquivo. Para publicar em serviços que exigem uma porta fornecida pelo ambiente, essa configuração pode precisar de adaptação.

O repositório contém dependências instaladas sob **node_modules**; em uma revisão posterior, recomenda-se usar um arquivo **.gitignore** e retirar essa pasta do versionamento.

## 5. Execução local prevista

Com Node.js e NPM instalados, após obter o código do repositório:

~~~bash
npm install
node api.js
~~~

É possível testar, por exemplo, a rota **http://localhost:3000/humores** usando o navegador ou um cliente HTTP.

Essa sequência descreve como o código pode ser executado. A execução e os resultados não foram reproduzidos nesta conferência.

## 6. Evidências e publicação

### Serviço já publicado no Render

O painel da conta Render confirmou que o repositório **exercicio_express** já estava vinculado a um serviço web gratuito, com branch **main**, em setembro de 2026.

- **URL da API:** [https://exercicio-express-bokp.onrender.com](https://exercicio-express-bokp.onrender.com)
- **Rota de listagem prevista no código:** [https://exercicio-express-bokp.onrender.com/humores](https://exercicio-express-bokp.onrender.com/humores)
- **Painel do serviço:** [Render — exercicio_express](https://dashboard.render.com/web/srv-dakm2lrm8hqs73f2r150)
- **Deploy verificado no painel:** `dep-dakm2mbm8hqs73f2r340`, commit `dc09e4fd`, concluído em **15/09/2026**, status `live` na consulta de 24/11/2026.

**Verificação adicional no navegador:** a estudante acessou as rotas públicas GET `/humores`, `/estatisticas` e `/frases` e enviou três capturas reais mostrando respostas JSON. A consulta foi confirmada visualmente. As operações POST, PUT e DELETE ainda não foram testadas nesta rodada.

| Evidência | Situação |
|---|---|
| Código da API Express | Localizado |
| Rotas de consulta e CRUD | Identificadas no código |
| Rota de estatísticas | Identificada |
| Rota de frases | Identificada |
| Print da execução local | Não anexado |
| Testes HTTP documentados | Respostas GET de `/humores`, `/estatisticas` e `/frases` confirmadas em prints reais; métodos de escrita pendentes |
| URL de deploy no Render | Confirmada no painel: [exercicio-express-bokp.onrender.com](https://exercicio-express-bokp.onrender.com); status do deploy `live` |
| Front-end separado | Não identificado; verificar se integrou a orientação prática desta turma |

Capturas recomendadas para a pasta [prints](prints/README.md):

- **01-codigo-purplemood.png** — rotas e estrutura do projeto;
- **02-lista-humores.png** — resposta real da rota de listagem;
- **03-cadastro-humor.png** — requisição de cadastro e resposta;
- **04-estatisticas.png** — resposta de estatísticas;
- **05-frases.png** — lista de frases;
- **06-deploy-render.png** — serviço publicado, se houver.

As capturas **02**, **04** e **05** foram fornecidas na conversa e preparadas em ZIP para upload. Ainda não foram anexadas ao GitHub. As demais evidências são complementares.

### Testes manuais da API publicada — 25/11/2026

| Endpoint GET | Resultado mostrado no navegador | Situação |
|---|---|---|
| [`/humores`](https://exercicio-express-bokp.onrender.com/humores) | Três registros: **Feliz**, **Tranquilo** e **Animado** | Resposta JSON observada |
| [`/estatisticas`](https://exercicio-express-bokp.onrender.com/estatisticas) | `total: 3`, `mediaIntensidade: 8.7` | Resposta JSON observada |
| [`/frases`](https://exercicio-express-bokp.onrender.com/frases) | Array com seis frases motivacionais | Resposta JSON observada |

Esses registros comprovam o funcionamento das **consultas GET** na sessão da estudante. Não comprovam a criação, alteração ou exclusão de registros na API publicada nem a persistência após reiniciar o serviço.

**Capturas reais recebidas, prontas para upload:** `02-lista-humores.png`, `04-estatisticas.png` e `05-frases.png`. Os arquivos ainda não foram anexados ao GitHub.

## 7. Aprendizados

O desenvolvimento do PurpleMood permitiu aplicar conceitos de API REST, métodos HTTP, rotas parametrizadas, corpo de requisições em JSON e cálculo de dados no servidor.

A atividade mostra que os conhecimentos de Express podem ser aplicados a um tema diferente do exemplo do material, conforme a orientação relatada para a prática em sala.

## 8. Situação da atividade

- [x] Projeto PurpleMood identificado como a implementação utilizada na aula, conforme relato da estudante.
- [x] Código-fonte e funcionalidades analisados.
- [x] Métodos e rotas documentados.
- [x] Obter e organizar três capturas reais dos endpoints GET.
- [ ] Anexar as três imagens à pasta `prints/` no GitHub.
- [x] Confirmar publicação no painel Render (deploy `live` em 15/09/2026).
- [x] Confirmar respostas atuais GET de três rotas públicas com capturas no navegador.
- [ ] Testar requisições de escrita POST, PUT e DELETE, se exigidas para a avaliação.
- [ ] Revisar dependências versionadas caso o repositório seja preparado para produção.

## 9. Conclusão

O PurpleMood é uma API didática construída com Express para consultar e administrar registros de humor. Ela atende à proposta prática alternativa informada pela estudante e permite demonstrar funcionalidades típicas do desenvolvimento back-end.

A documentação descreve o código existente e registra o serviço Render já encontrado na conta. A publicação foi confirmada pelo histórico de deploys, e as três consultas GET foram validadas visualmente. Os testes de escrita e a persistência de dados ainda não foram comprovados.
