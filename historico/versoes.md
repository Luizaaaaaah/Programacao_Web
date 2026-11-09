# Histórico de versões do repositório

**Repositório:** [Programacao_Web](https://github.com/Luizaaaaaah/Programacao_Web)  
**Branch principal:** main

## Estado anterior à reorganização

Na consulta ao repositório, foi observada uma branch principal main e um commit anterior com a mensagem “Add files via upload”, datado de 06/10/2026. Os READMEs de releases não apresentavam releases publicados. As tags Git não foram confirmadas nesta auditoria e, por isso, não são listadas como existentes.

## Versões documentadas

| Tag | Descrição | Situação |
|---|---|---|
| v1.0.0 | Organização inicial do portfólio: índices, resumos, relatórios de atividades e histórico | Planejada; publicar após revisar o commit no GitHub |

## Convenção SemVer

O padrão MAJOR.MINOR.PATCH foi apresentado na Aula 03:

- **MAJOR:** alteração estrutural incompatível.
- **MINOR:** inclusão de conteúdo ou funcionalidade sem quebrar a estrutura existente.
- **PATCH:** correção ou ajuste pontual.

## Como criar uma tag anotada

Após conferir as alterações, enviar o commit e confirmar que a branch está atualizada, executar dentro da pasta local:

~~~bash
git pull origin main
git status
git tag -a v1.0.0 -m "v1.0.0 - organização inicial do portfólio acadêmico"
git push origin v1.0.0
~~~

A tag só deve ser marcada como publicada depois de aparecer na aba **Tags** do GitHub. Esta documentação não cria nem presume uma tag.

## Convenção de commits

| Prefixo | Uso | Exemplo |
|---|---|---|
| docs | Documentação, README e capturas | docs: organiza os relatórios das aulas |
| feat | Nova funcionalidade de aplicação | feat: adiciona consulta de CEP |
| fix | Correção de erro | fix: corrige atualização de nota |
| refactor | Reorganização sem alterar o comportamento | refactor: separa interface e API |
| chore | Configuração e manutenção | chore: adiciona gitignore |

