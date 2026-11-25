# Projeto final da disciplina — Itape +

**Disciplina:** Programação Web  
**Curso:** Análise e Desenvolvimento de Sistemas — Fatec Itapetininga  
**Professor:** Prof. Me. Deivison S. Takatu  
**Ano:** 2026  
**Modalidade:** Trabalho em equipe, apresentado e finalizado em sala de aula com o professor, conforme confirmação da integrante da equipe.

## 1. Apresentação

O **Itape +** é uma plataforma web destinada a centralizar a divulgação de **eventos culturais e educacionais de Itapetininga e região**, facilitando a descoberta de atividades pela comunidade.

O projeto permite que organizadores cadastrados submetam eventos. Um administrador avalia as submissões e **aprova ou rejeita** cada evento antes de sua publicação no catálogo público.

Este documento é o **registro do projeto final da disciplina** no portfólio individual da estudante. Não corresponde a uma décima aula, nem copia o código do trabalho coletivo.

## 2. Equipe

Conforme a [release oficial v1.0.0](https://github.com/RafaelRachidd/Itape-plus/releases/tag/v1.0.0), participaram:

- Isabela Machado Oliveira;
- Maria Luiza de Almeida Oliveira;
- Rafael Camargo Rachid;
- Veronica das Dores Bicudo da Silva.

Não foram atribuídas responsabilidades individuais específicas, pois a divisão de tarefas não está detalhada no README consultado.

## 3. Links de acesso

| Recurso | Endereço |
|---|---|
| Código-fonte do projeto | [RafaelRachidd/Itape-plus](https://github.com/RafaelRachidd/Itape-plus) |
| Site publicado (informado no README original) | [itape-plus.vercel.app](https://itape-plus.vercel.app) |
| API publicada (informada no README original) | [itape-plus-api.onrender.com/api/health](https://itape-plus-api.onrender.com/api/health) |
| Versão final entregue | [Release v1.0.0](https://github.com/RafaelRachidd/Itape-plus/releases/tag/v1.0.0) |
| Documentação original | [README do projeto](https://github.com/RafaelRachidd/Itape-plus/blob/main/README.md) |
| Histórico de alterações | [CHANGELOG.md](https://github.com/RafaelRachidd/Itape-plus/blob/main/CHANGELOG.md) |
| Coleção de testes da API | [Postman — itape-plus](https://github.com/RafaelRachidd/Itape-plus/blob/main/docs/itape-plus.postman_collection.json) |
| Configuração do Firebase | [Guia FIREBASE_SETUP.md](https://github.com/RafaelRachidd/Itape-plus/blob/main/docs/FIREBASE_SETUP.md) |

**Observação:** os links do site e da API constam do README oficial do grupo. A publicação foi documentada pelo próprio projeto, mas a disponibilidade dos dois endpoints para visitantes externos ainda não foi confirmada independentemente nesta revisão do portfólio. O plano gratuito do Render pode levar algum tempo para reativar a API após inatividade.

## 4. Tecnologias

| Camada | Tecnologias documentadas |
|---|---|
| Front-end | React, Vite, React Router |
| Back-end | Node.js, Express, API REST |
| Banco de dados | Cloud Firestore — Firebase |
| Autenticação | Firebase Authentication (e-mail e senha, com verificação de e-mail) |
| Segurança e validação | Firebase Admin, `express-validator`, regras do Firestore, CORS e Helmet |
| Publicação informada | Vercel (front-end) e Render (API) |

A organização do repositório original utiliza as pastas `frontend/`, `backend/` e `docs/`, além de `firestore.rules`.

## 5. Funcionalidades documentadas

### Área pública
- Página inicial de apresentação do projeto;
- catálogo de eventos culturais e educacionais, com **busca e filtros**;
- página de detalhes de eventos;
- visualização por **calendário**;
- acesso apenas aos eventos aprovados para divulgação pública.

### Conta e painel do organizador
- Cadastro e login por e-mail e senha usando Firebase Authentication;
- verificação do e-mail cadastrado;
- cadastro, edição e exclusão de eventos próprios;
- visualização do estado da submissão e do motivo de eventual rejeição;
- atualização de dados do perfil público.

### Administração
- Consulta de eventos por status;
- aprovação e rejeição com justificativa;
- registro de quem moderou e quando;
- API protegida por autenticação e perfil de acesso.

As funcionalidades acima estão descritas no README, no CHANGELOG e na release do repositório coletivo; não foram inventadas funcionalidades extras.

## 6. Arquitetura e API

O front-end React interage com uma API REST em Express. A autenticação utiliza tokens do Firebase e os dados dos eventos são armazenados no Firestore. O README original documenta os seguintes grupos de rotas:

| Grupo de rotas | Finalidade |
|---|---|
| `GET /api/health` | Estado da conexão com o banco |
| `GET /api/categorias` | Categorias disponíveis |
| `GET /api/eventos` e `GET /api/eventos/:id` | Catálogo público e detalhes |
| `/api/eu` | Informações do perfil autenticado |
| `/api/painel/eventos` | Gestão de eventos pelo organizador |
| `/api/admin/...` | Moderação de eventos e indicadores administrativos |

O repositório contém `firestore.rules` para restringir o acesso direto ao banco e uma coleção Postman destinada aos testes das rotas. Credenciais, chaves de serviço e arquivos `.env` não devem ser publicados no GitHub.

## 7. Versionamento e entrega

- **v0.1.0 — 10/11/2026:** estrutura inicial do monorepositório e primeira API, conforme o CHANGELOG.
- **v1.0.0 — 23/11/2026:** [release marcada como versão final do Itape +](https://github.com/RafaelRachidd/Itape-plus/releases/tag/v1.0.0), entregue para a disciplina segundo a descrição pública.
- **Registro de alterações 1.1.0 — 24/11/2026:** o CHANGELOG documenta a inclusão de recuperação de senha por e-mail. Essa alteração aparece após a release final e **não deve ser confundida com uma release 1.1.0 publicada**, pois nenhuma foi identificada na consulta.

A release v1.0.0 **declara** que foram aprovados 12 casos de teste e realizadas medições com Lighthouse. O repositório consultado contém a coleção Postman, mas não foram identificados na pasta `docs/` relatórios individuais que permitam confirmar esses 12 resultados ou as medições. Por isso, tais informações são registradas como **declarações da equipe**, não como testes refeitos nesta revisão.

## 8. Registro acadêmico e evidências

A integrante confirmou que o trabalho foi **concluído e apresentado em sala com o professor**. A versão final é identificável por release, histórico de commits, código-fonte e documentação do grupo.

**Comprovações efetivamente localizadas:**
- Repositório GitHub público com `frontend/`, `backend/`, `docs/` e documentação;
- release v1.0.0 publicada, com identificação da equipe e do escopo;
- CHANGELOG com evolução do projeto;
- coleção Postman e instruções de configuração do Firebase.

**Evidência adicional desejável, caso o professor a solicite:** print real da página inicial publicada, do catálogo de eventos e/ou da entrega em sala. Uma captura da página do GitHub foi enviada nesta conversa, mas **não está anexada ao portfólio**. Não foram criadas imagens fictícias nem atribuída uma nota de avaliação ao projeto.

## 9. Conclusão

O Itape + integra os principais conteúdos estudados em Programação Web: interface com React, rotas HTTP em Express, banco de dados, autenticação, controle de acesso, versionamento, testes e publicação. O projeto é apresentado aqui como **trabalho final coletivo**, preservando a autoria compartilhada e direcionando o leitor ao repositório da equipe para consultar o código completo.
