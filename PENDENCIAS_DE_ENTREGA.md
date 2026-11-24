# Pendências de entrega — Programação Web

**Atualização da conferência:** 24/11/2026  
**Branch de trabalho:** [reorganizacao](https://github.com/Luizaaaaaah/Programacao_Web/tree/reorganizacao)

Este checklist reúne apenas ações que ainda dependem de execução real, acesso externo, confirmação da estudante ou capturas de tela. **Os relatórios das nove aulas estão organizados; isso não significa que todos os requisitos práticos tenham sido executados ou comprovados.**

## Prioridades para a conclusão

| Prioridade | Aula | Ação necessária | Situação atual |
|---|---|---|---|
| 1 | 05 — React | Executar o projeto, testar as cinco funcionalidades, publicar na Vercel e fazer os prints | Código analisado e README atualizado; URL e imagens ausentes |
| 2 | 06 — Angular e Vue | Testar os projetos, comprovar a origem do template e publicar os quatro deploys exigidos | React, Angular, Vue básico complementar e HoennDex possuem código; testes e deploys pendentes |
| 3 | 08 — CRUD | Testar e revisar os PRs da API e do React, integrar as alterações aprovadas, configurar o deploy, executar Postman e registrar prints | Código, coleção de testes e ajustes de deploy preparados em PRs de rascunho |
| 4 | 09 — ConectaAção | Confirmar que é a entrega da aula, disponibilizar site publicado e conferir acesso do professor | Código privado com quiz identificado; link público não confirmado |
| 5 | 07 — PurpleMood | Executar API, capturar rotas e confirmar se há publicação | Projeto alternativo validado pelo relato da orientação em sala; código documentado |
| 6 | 03 — Versionamento | Concluir validação prática e marcar checklist de testes | GitHub, tags e Vercel registrados com quatro capturas |
| 7 | 01 e 02 — Planejamento | Confirmar abertura dos links do Miro, Figma e Trello em conta de terceiro; validar sitemap proposto | Links e imagens disponíveis |
| 8 | 04 — CMS | Validar se o site Dev do Pantheon permanece acessível ao professor | WordPress, tema, plugins, homepage e quatro capturas registrados |

## O que já existe no GitHub

**Documentação acadêmica:** relatórios das [Aulas 01 a 09](atividades/README.md) e seus resumos. A pasta de cada atividade contém um README próprio.

**Coleção Postman pronta para importar:** [notas-crud.postman_collection.json](atividades/aula-08/postman/notas-crud.postman_collection.json). As quatro requisições existem no arquivo, mas os testes não foram executados aqui.

**Publicação já registrada:** [OrganizaFácil da Aula 03](https://pwaula03versionamento.vercel.app/).

**Ambiente de CMS:** [OrganizaFácil WordPress no Pantheon](https://dev-organizafacil-cms1.pantheonsite.io/) — Dev/Sandbox, sujeito às condições do provedor.

## Alterações prontas para revisão na Aula 08

- [PR #1 — API de notas: preparação Render](https://github.com/Luizaaaaaah/exercicio_express1/pull/1) — rascunho, não mesclado;
- [PR #1 — Front-end React: URL configurável](https://github.com/Luizaaaaaah/exercicio_react1/pull/1) — rascunho, não mesclado.

Os dois PRs devem ser revisados e testados antes de finalizar a integração. Os repositórios originais continuam com suas branches main preservadas.

## O que ainda exige participação da estudante

### Publicações

O acesso às contas da Vercel, Render e Lovable, a confirmação de URLs de produção e a execução de interfaces web ainda dependem de credenciais ou interações nas plataformas. Os URLs não podem ser deduzidos a partir do nome dos projetos.

### Capturas

Não foram criadas capturas fictícias. A pasta **prints** das Aulas 05 a 09 contém apenas arquivos de orientação; as imagens devem resultar da execução real dos respectivos projetos.

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
