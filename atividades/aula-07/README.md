# Atividade 07 — API de data e hora com Express

**Disciplina:** Programação Web  
**Professor:** Prof. Me. Deivison S. Takatu

## 1. Objetivo

Desenvolver uma API com Express que disponibilize uma rota de consulta de data e hora, publicar o back-end no Render e criar um front-end separado que consuma a API. A entrega deve manter API e interface em repositórios distintos.

## 2. O que foi solicitado

1. Criar uma API Express com rota para retornar data e hora.
2. Publicar o back-end no Render conectado ao GitHub.
3. Criar um front-end que consuma a API e apresente a data/hora.
4. Separar o back-end e o front-end em repositórios diferentes.
5. Documentar código, aplicação, painéis do Render e da Vercel, prints e links dos dois repositórios.

## 3. Projeto Express localizado

**Repositório:** [exercicio_express](https://github.com/Luizaaaaaah/exercicio_express)

O arquivo api.js foi conferido. Ele implementa uma API chamada PurpleMood, com recursos relacionados a registros de humor, incluindo rotas para listar, buscar, cadastrar, atualizar e excluir humores, além de estatísticas e frases motivacionais.

**Importante:** o código localizado é uma API funcional em Express, mas seu domínio de dados é humor — não foi identificada nele a rota de data e hora descrita no enunciado da Aula 07. Portanto, a existência desse repositório não comprova que a atividade específica esteja concluída.

O repositório contém uma pasta node_modules versionada. É recomendável remover dependências instaladas do controle de versão e criar um .gitignore apropriado no próprio projeto, após revisar as alterações localmente.

## 4. Front-end e publicação

Não foi localizado um repositório front-end que pudesse ser associado com segurança à API de data e hora desta aula. Também não foram confirmadas URLs de produção no Render e na Vercel.

| Entrega | Link / situação |
|---|---|
| API Express existente | [exercicio_express](https://github.com/Luizaaaaaah/exercicio_express) |
| Front-end data/hora | Não localizado |
| URL da API no Render | Não localizada |
| Site no Vercel | Não localizado |
| Prints de painéis e aplicação | Pendentes |

## 5. Estrutura recomendada para completar

- Rota da API documentada, com método HTTP e formato de resposta.
- Exemplo de resposta JSON com data e hora.
- Front-end mostrando a resposta da API.
- Variável de ambiente ou configuração clara para URL da API em produção.
- Teste do endpoint público e captura do painel Render.
- Front-end acessível em produção, testado em janela anônima.

## 6. Evidências a anexar

| Arquivo sugerido | O que deve mostrar |
|---|---|
| 01-rota-data-hora.png | Código da rota de data/hora |
| 02-api-local.png | Resposta JSON da API no ambiente local |
| 03-render-service.png | Serviço e status de deploy no Render |
| 04-api-publicada.png | Endpoint público respondendo |
| 05-frontend-data-hora.png | Interface que consome e apresenta a data/hora |
| 06-vercel-deploy.png | Deploy do front-end na Vercel |
| 07-repositorios-separados.png | Repositórios distintos para API e interface |

As capturas devem ser colocadas em [prints/](prints/README.md).

## 7. Situação desta documentação

- [x] Repositório com API Express localizado.
- [ ] Confirmar se existe uma versão da API específica para data/hora.
- [ ] Localizar o front-end correspondente.
- [ ] Confirmar Render e Vercel.
- [ ] Inserir prints e links públicos.

## 8. Nota de conferência

O repositório PurpleMood foi registrado como projeto Express encontrado, mas não foi classificado como implementação final do requisito de data/hora. Essa distinção evita atribuir uma entrega diferente à atividade solicitada.