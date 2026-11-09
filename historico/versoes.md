# Histórico de versões do repositório

**Repositório:** [Programacao_Web](https://github.com/Luizaaaaaah/Programacao_Web)  
**Branch principal:** main

## Estado encontrado antes da reorganização

A branch principal era main. O commit anterior observado tinha a mensagem “Add files via upload”, datado de 06/10/2026. Não foi localizada uma release publicada. As tags Git não foram confirmadas na consulta e, por isso, não são listadas como existentes.

## Registro de commits desta organização

| Data | Commit | Descrição |
|---|---|---|
| 09/11/2026 | [4aa92e0](https://github.com/Luizaaaaaah/Programacao_Web/commit/4aa92e02e57658b244e4bb47fa15ccdd5582abc5) | docs: organiza portfólio acadêmico das aulas 01 a 09 |
| 09/11/2026 | [5934e26](https://github.com/Luizaaaaaah/Programacao_Web/commit/5934e26dbc8deb48fb719d63c66c733f7413d0be) | docs: adiciona atalhos para documentos anteriores |

## Versões documentadas

| Tag | Descrição | Situação |
|---|---|---|
| v1.0.0 | Organização inicial do portfólio: índices, resumos, relatórios de atividades e histórico | Planejada; a tag ainda deve ser criada e publicada |

## Convenção SemVer

O padrão MAJOR.MINOR.PATCH foi apresentado na Aula 03:

- **MAJOR:** alteração estrutural incompatível.
- **MINOR:** inclusão de conteúdo ou funcionalidade sem quebrar a estrutura existente.
- **PATCH:** correção ou ajuste pontual.

## Como criar uma tag anotada

Após conferir as alterações, enviar os commits e confirmar que a branch está atualizada, executar dentro da pasta local:

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

