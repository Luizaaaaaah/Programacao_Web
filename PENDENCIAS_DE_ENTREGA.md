# Pendências de entrega — Programação Web

**Atualização da conferência:** 24/11/2026  
**Branch de trabalho:** [reorganizacao](https://github.com/Luizaaaaaah/Programacao_Web/tree/reorganizacao)

Este checklist reúne apenas ações que ainda dependem de execução real, acesso externo, confirmação da estudante ou capturas de tela. **Os relatórios das nove aulas estão organizados; isso não significa que todos os requisitos práticos tenham sido executados ou comprovados.**

## Prioridades para a conclusão

| Prioridade | Aula | Ação necessária | Situação atual |
|---|---|---|---|
| 1 | 05 — React | Conferir necessidade de evidências adicionais (commits e painel Vercel) e testes complementares | Cinco funcionalidades testadas na versão publicada; nove PNGs reais anexados e exibidos no relatório |
| 2 | 06 — Angular e Vue | Testar React, validar origem do template e obter demais prints exigidos | Quatro deploys `READY`; 26 prints reais confirmados no GitHub: sete do Vue básico, doze do Angular e sete da HoennDex (incluindo mobile em 390 × 844 px) |
| 3 | 08 — CRUD | Testar API e CRUD, revisar os PRs e publicar versão aprovada em produção; anexar prints | Render `live`; React corrigido em preview `READY`, porém produção ainda `ERROR` |
| 4 | 09 — ConectaAção | Confirmar entrega da atividade e acesso do professor ao site/código | Homepage, quiz com resultado Acolhedor Social, visual móvel e editor Lovable conferidos; seis prints anexados e exibidos no GitHub; repositório privado |
| 5 | 07 — PurpleMood | Anexar três prints reais preparados da API; verificar necessidade de testes POST/PUT/DELETE | Respostas atuais GET `/humores`, `/estatisticas` e `/frases` confirmadas visualmente; três PNGs preparados, ainda não enviados |
| 6 | 03 — Versionamento | Concluir validação prática e marcar checklist de testes | GitHub, tags e Vercel registrados com quatro capturas |
| 7 | 01 e 02 — Planejamento | Confirmar abertura dos links do Miro, Figma e Trello em conta de terceiro; validar sitemap proposto | Links e imagens disponíveis |
| 8 | 04 — CMS | Validar se o site Dev do Pantheon permanece acessível ao professor | WordPress, tema, plugins, homepage e quatro capturas registrados |

## O que já existe no GitHub

**Documentação acadêmica:** relatórios das [Aulas 01 a 09](atividades/README.md) e seus resumos. A pasta de cada atividade contém um README próprio.

**Coleção Postman pronta para importar:** [notas-crud.postman_collection.json](atividades/aula-08/postman/notas-crud.postman_collection.json). As quatro requisições existem no arquivo, mas os testes não foram executados aqui.

**Publicação registrada da Aula 03:** [OrganizaFácil](https://pwaula03versionamento.vercel.app/).

**Deploys `READY` encontrados na Vercel:** [Aula 05 React](https://exercicio-react-ecru.vercel.app), [Aula 06 Angular](https://exercicioangular.vercel.app), [Aula 06 Vue básico](https://exercicio-vue-fawn.vercel.app), [Aula 06 Vue HoennDex](https://vue-project-alpha-peach.vercel.app) e [Aula 09 ConectaAção](https://pixel-perfect-pixels-orcin.vercel.app). **Aula 08:** [prévia React `READY`](https://exercicioreact1-git-preparar-deploy-aula-08-luizaaaaaah.vercel.app) na branch de revisão; produção da main ainda está em `ERROR`. Status de deploy não equivale a teste de interface.

**Publicações adicionais identificadas na conta Render:** [PurpleMood — Aula 07](https://exercicio-express-bokp.onrender.com) e [API de notas — Aula 08](https://exercicio-express1.onrender.com). Os respectivos deploys históricos estão marcados como `live`; as respostas HTTP atuais ainda não foram verificadas.

**Ambiente de CMS:** [OrganizaFácil WordPress no Pantheon](https://dev-organizafacil-cms1.pantheonsite.io/) — Dev/Sandbox, sujeito às condições do provedor.

## Alterações prontas para revisão na Aula 08

- [PR #1 — API de notas: preparação Render](https://github.com/Luizaaaaaah/exercicio_express1/pull/1) — rascunho, não mesclado;
- [PR #1 — Front-end React: URL configurável](https://github.com/Luizaaaaaah/exercicio_react1/pull/1) — rascunho, não mesclado.

Os dois PRs devem ser revisados e testados antes de finalizar a integração. Os repositórios originais continuam com suas branches main preservadas.

## O que ainda exige participação da estudante

### Publicações

As conexões da Render e da Vercel estão autorizadas; os deploys e respectivos domínios foram consultados nas contas. Ainda dependem de validação o acesso público sem login, testes das interfaces, a integração CRUD de produção e, quando exigidas, as evidências capturadas no navegador. O vínculo da Aula 09 como trabalho efetivamente entregue ao professor ainda precisa ser confirmado.

### Capturas

Não foram criadas capturas fictícias. A pasta **prints da Aula 06** já contém 26 capturas reais: sete do Vue básico, doze do Angular e sete da HoennDex. Os nove prints reais da Aula 05 também foram confirmados na pasta `prints/` do GitHub e incluídos no relatório. Os seis prints reais do ConectaAção foram confirmados na pasta `prints/` da Aula 09 e incluídos no relatório. As demais evidências pendentes devem resultar da execução real dos respectivos projetos.

### Permissões

O repositório **pixel-perfect-pixels** está privado. O professor precisa de acesso autorizado ou de uma URL pública do site que permita conferir a entrega.

### Sincronização do computador

As alterações mais recentes foram realizadas diretamente na branch remota **reorganizacao**. Antes de continuar a editar o repositório principal no VS Code:

1. Salve todos os arquivos locais no editor.
2. Abra o terminal do repositório **Programacao_Web_Reorganizacao**.
3. Execute **git status**. Se houver alterações locais, não execute pull ainda: revise e salve-as em commit antes.
4. Se o status estiver limpo, execute **git pull --ff-only origin reorganizacao** para atualizar a cópia local.
5. Confirme com **git status**.

A branch **main** não foi modificada nesta rodada. A integração deve ocorrer somente após a revisão final das entregas.

## Critério para marcar uma atividade como concluída

Uma tarefa prática deve ser marcada como concluída somente quando os requisitos da aula e eventuais adaptações orientadas pelo professor estiverem documentados com evidências suficientes. Ter o código escrito não garante que a interface, os testes ou a publicação estejam funcionando.
