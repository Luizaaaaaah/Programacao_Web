# Pendências de entrega — Programação Web

**Atualização da conferência:** 25/11/2026  
**Publicação final:** branch [main](https://github.com/Luizaaaaaah/Programacao_Web/tree/main) — reorganização integrada pelo [PR #1](https://github.com/Luizaaaaaah/Programacao_Web/pull/1). A branch [reorganizacao](https://github.com/Luizaaaaaah/Programacao_Web/tree/reorganizacao) permanece como histórico de desenvolvimento.

Este checklist reúne apenas ações que ainda dependem de execução real, acesso externo, confirmação da estudante ou capturas de tela. **Os relatórios das nove aulas estão organizados; isso não significa que todos os requisitos práticos tenham sido executados ou comprovados.**

## Prioridades para a conclusão

| Prioridade | Aula | Ação necessária | Situação atual |
|---|---|---|---|
| 1 | 05 — React | Conferir necessidade de evidências adicionais (commits e painel Vercel) e testes complementares | Cinco funcionalidades testadas na versão publicada; nove PNGs reais anexados e exibidos no relatório |
| 2 | 06 — Angular e Vue | Testar React, validar origem do template e obter demais prints exigidos | Quatro deploys `READY`; 26 prints reais confirmados no GitHub: sete do Vue básico, doze do Angular e sete da HoennDex (incluindo mobile em 390 × 844 px) |
| 3 | 08 — CRUD | Opcional: executar coleção Postman, repetir escrita na URL de produção e confirmar acesso pela conta do professor | API Render `live`, CRUD validado na prévia; produção React `READY` aberta e exibindo duas notas originais; 9 prints anexados |
| 4 | 09 — ConectaAção | Confirmar entrega da atividade e acesso do professor ao site/código | Homepage, quiz com resultado Acolhedor Social, visual móvel e editor Lovable conferidos; seis prints anexados e exibidos no GitHub; repositório privado |
| 5 | 07 — PurpleMood | Revisar necessidade de testes POST, PUT e DELETE e evidências extras | Três respostas GET reais (humores, estatísticas e frases) confirmadas; prints anexados e exibidos no relatório |
| 6 | 03 — Versionamento | Concluir validação prática e marcar checklist de testes | GitHub, tags e Vercel registrados com quatro capturas |
| 7 | 01 e 02 — Planejamento | Confirmar abertura dos links do Miro, Figma e Trello em conta de terceiro; validar sitemap proposto | Links e imagens disponíveis |
| 8 | 04 — CMS | Validar se o site Dev do Pantheon permanece acessível ao professor | WordPress, tema, plugins, homepage e quatro capturas registrados |

## Projeto final concluído em sala — Itape +

O **[Itape +](projeto-final/README.md)** foi registrado separadamente das nove aulas como **projeto final em equipe**, conforme confirmação da estudante. Seu repositório público é [RafaelRachidd/Itape-plus](https://github.com/RafaelRachidd/Itape-plus) e a [release v1.0.0](https://github.com/RafaelRachidd/Itape-plus/releases/tag/v1.0.0) é identificada como entrega final (23/11/2026). Os endereços de site Vercel e API Render estão declarados no README do projeto, mas não foram verificados independentemente nesta revisão do portfólio.

**Documentação já registrada:** escopo, equipe, tecnologias, arquitetura, recursos, versionamento e links de acesso. **Evidência adicional, se solicitada pelo professor:** prints reais do site funcionando e/ou confirmação formal da apresentação, sem inventar imagens ou nota.

## O que já existe no GitHub

**Documentação acadêmica:** relatórios das [Aulas 01 a 09](atividades/README.md) e seus resumos. A pasta de cada atividade contém um README próprio.

**Testes reais da Aula 08:** React + API Render validados em criar, listar, editar e excluir usando notas fictícias; nove capturas reais anexadas ao GitHub. A coleção Postman não foi executada neste fluxo.

**Coleção Postman pronta para importar:** [notas-crud.postman_collection.json](atividades/aula-08/postman/notas-crud.postman_collection.json). As quatro requisições existem no arquivo, mas os testes não foram executados aqui.

**Publicação registrada da Aula 03:** [OrganizaFácil](https://pwaula03versionamento.vercel.app/).

**Deploys `READY` encontrados na Vercel:** [Aula 05 React](https://exercicio-react-ecru.vercel.app), [Aula 06 Angular](https://exercicioangular.vercel.app), [Aula 06 Vue básico](https://exercicio-vue-fawn.vercel.app), [Aula 06 Vue HoennDex](https://vue-project-alpha-peach.vercel.app) e [Aula 09 ConectaAção](https://pixel-perfect-pixels-orcin.vercel.app). **Aula 08:** [produção React `READY`](https://exercicioreact1.vercel.app) no commit `18cf156`, após integração do PR #1 e configuração de `VITE_API_URL`. A [prévia React `READY`](https://exercicioreact1-git-preparar-deploy-aula-08-luizaaaaaah.vercel.app) foi validada com testes CRUD reais. A versão de produção foi aberta pela estudante sem tela de login e exibiu duas notas correspondentes à API; o CRUD de escrita havia sido validado na prévia.

**Publicações adicionais identificadas na conta Render:** [PurpleMood — Aula 07](https://exercicio-express-bokp.onrender.com) e [API de notas — Aula 08](https://exercicio-express1.onrender.com). Os serviços estão `live`; as rotas GET de PurpleMood e o CRUD da API de notas foram conferidos por capturas reais de navegador.

**Ambiente de CMS:** [OrganizaFácil WordPress no Pantheon](https://dev-organizafacil-cms1.pantheonsite.io/) — Dev/Sandbox, sujeito às condições do provedor.

## Alterações prontas para revisão na Aula 08

- [PR #1 — API de notas: preparação Render](https://github.com/Luizaaaaaah/exercicio_express1/pull/1) — integrado à `main` (commit `92d3584`);
- [PR #1 — Front-end React: URL configurável](https://github.com/Luizaaaaaah/exercicio_react1/pull/1) — integrado à `main` (commit `18cf156`).

Ambos os PRs foram revisados e integrados às respectivas branches `main`, e geraram publicações funcionais de API e interface.

## O que ainda exige participação da estudante

### Publicações

As conexões da Render e da Vercel estão autorizadas; os deploys e respectivos domínios foram consultados nas contas. A versão de produção do React foi aberta sem tela de login e exibiu as duas notas reais da API. O CRUD completo foi validado na prévia; a escrita em produção e o acesso a partir da conta do professor ainda dependem de verificação, se exigidos. O vínculo da Aula 09 como trabalho efetivamente entregue ao professor ainda precisa ser confirmado.

### Capturas

Não foram criadas capturas fictícias. A pasta **prints da Aula 06** já contém 26 capturas reais: sete do Vue básico, doze do Angular e sete da HoennDex. Os nove prints reais da Aula 05 também foram confirmados na pasta `prints/` do GitHub e incluídos no relatório. Os nove prints reais da Aula 08 estão anexados e vinculados ao relatório; a captura adicional da versão oficial foi enviada na conversa, ainda não no GitHub. Os seis prints reais do ConectaAção foram confirmados na pasta `prints/` da Aula 09 e incluídos no relatório. As demais evidências pendentes devem resultar da execução real dos respectivos projetos.

### Permissões

O repositório **pixel-perfect-pixels** está privado. O professor precisa de acesso autorizado ou de uma URL pública do site que permita conferir a entrega.

### Sincronização do computador

O portfólio já foi integrado à branch **main**. Para atualizar a cópia local no VS Code antes de novas alterações:

1. Salve todos os arquivos locais no editor.
2. Abra o terminal do repositório **Programacao_Web_Reorganizacao**.
3. Execute **git status**. Se houver alterações locais, não execute pull ainda: revise e salve-as em commit antes.
4. Com o status limpo, execute **git fetch origin**, depois **git switch main** e **git pull --ff-only origin main** para sincronizar a branch publicada. Não use `git push --force`.
5. Confirme com **git status**.

A integração final **já ocorreu**: [Pull Request #1 mesclado](https://github.com/Luizaaaaaah/Programacao_Web/pull/1), commit de merge [`66f2490`](https://github.com/Luizaaaaaah/Programacao_Web/commit/66f24907063b39954c7cb7902ec9dbbb61f24c42). **As pendências desta tabela são melhorias ou verificações complementares, não impedimentos para acessar o portfólio organizado.**

## Critério para marcar uma atividade como concluída

Uma tarefa prática deve ser marcada como concluída somente quando os requisitos da aula e eventuais adaptações orientadas pelo professor estiverem documentados com evidências suficientes. Ter o código escrito não garante que a interface, os testes ou a publicação estejam funcionando.
