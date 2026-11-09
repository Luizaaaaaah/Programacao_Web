# Aula 03 — Introdução ao versionamento e deploy

**Professor:** Prof. Me. Deivison S. Takatu  
**Disciplina:** Programação Web

## Visão geral

A aula apresentou o versionamento como prática para acompanhar a evolução de um projeto, trabalhar em equipe e recuperar alterações. Foram estudados Git, GitHub, SemVer, branches, merge, tags e deploy.

## Conteúdo estudado

### Versionamento e backup

O versionamento mantém o histórico das alterações e permite identificar quem mudou, quando e o que foi alterado. O backup guarda uma cópia de um estado em determinado momento. O versionamento favorece colaboração, rastreabilidade, reversão de alterações e auditoria.

### Versionamento semântico

O SemVer utiliza a estrutura MAJOR.MINOR.PATCH:

- **MAJOR:** alteração incompatível com versões anteriores.
- **MINOR:** inclusão de funcionalidade mantendo compatibilidade.
- **PATCH:** correção sem mudança incompatível.

Exemplo: 1.0.0 como versão estável inicial, 1.1.0 para uma funcionalidade compatível, 1.1.1 para uma correção e 2.0.0 para uma mudança incompatível.

### Git e GitHub

Git é o sistema de controle de versão executado localmente. GitHub hospeda repositórios remotos e permite compartilhar o código. A aula demonstrou a instalação, configuração do nome/e-mail, inicialização do repositório, commits e sincronização.

### Branches e merge

Branches isolam o desenvolvimento de novas funcionalidades e correções. A branch principal deve permanecer estável. O merge integra mudanças de uma branch em outra; conflitos podem ocorrer quando alterações incompatíveis atingem a mesma parte do código.

### Tags

Tags identificam pontos específicos do histórico, como versões estáveis. A apresentação diferenciou tags leves e anotadas e mostrou como listar, criar e enviar uma tag ao GitHub.

### Deploy

Deploy é a publicação de uma aplicação em um ambiente acessível aos usuários. Foram discutidos os ambientes de desenvolvimento, staging e produção, além da integração entre GitHub e Vercel para publicação automatizada.

## Atividade proposta

1. Criar um repositório com uma página HTML simples.
2. Versionar o código com Git e utilizar tags para marcar versões estáveis.
3. Personalizar o projeto e publicá-lo na Vercel, conectando o repositório do GitHub.
4. Documentar escolhas de design, personalizações, versionamento e deploy, incluindo prints e links do repositório e do site.

## Ferramentas e conceitos

Git, GitHub, branches, merge, tags, SemVer, Vercel, deploy e CI/CD.

## Síntese

O versionamento preserva o histórico técnico do projeto; o deploy torna o resultado acessível. O uso conjunto de Git, GitHub e Vercel cria um fluxo de desenvolvimento e publicação mais organizado.

**Próximo:** [Atividade 03](../atividades/aula-03/README.md) | [Índice das aulas](README.md)