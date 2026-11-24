# Atividade 09 — Website Builder com IA: ConectaAção

**Disciplina:** Programação Web  
**Professor:** Prof. Me. Deivison S. Takatu  
**Instituição:** Fatec Itapetininga

## 1. Objetivo

Utilizar uma ferramenta de criação de sites com recursos de inteligência artificial para produzir uma página personalizada, adicionar conteúdo, implementar ao menos uma interação e avaliar o resultado em diferentes tamanhos de tela.

## 2. Projeto identificado

**Nome mostrado no código:** ConectaAção  
**Ferramenta declarada:** Lovable  
**Repositório:** [pixel-perfect-pixels](https://github.com/Luizaaaaaah/pixel-perfect-pixels) — **privado**  
**Editor:** [Projeto no Lovable](https://lovable.dev/projects/827f8a9a-8919-4bbf-aa28-04b64bd48edd) — pode exigir autenticação.

O README do projeto afirma que ele foi criado com Lovable e que as alterações feitas no editor são sincronizadas com o repositório GitHub.

A finalidade do **ConectaAção** é apresentar diferentes causas de voluntariado e incentivar o visitante a encontrar formas de ajudar sua comunidade.

O projeto é compatível com os requisitos técnicos da Aula 09, embora seu vínculo como entrega final da disciplina ainda dependa de confirmação.

## 3. Estrutura da página

O arquivo principal [src/routes/index.tsx](https://github.com/Luizaaaaaah/pixel-perfect-pixels/blob/main/src/routes/index.tsx) contém:

| Seção | Conteúdo identificado |
|---|---|
| Início | Apresentação do projeto e botão para descobrir o perfil voluntário |
| Sobre | Explicação da proposta de incentivo ao voluntariado |
| Causas | Cartões com áreas de atuação voluntária |
| Como Ajudar | Exemplos de contribuições por tempo, habilidades, doações e divulgação |
| Quiz | Questionário interativo para identificar afinidade com causas |
| Rodapé | Identidade do projeto e navegação |

As causas apresentadas incluem educação, proteção animal, meio ambiente, apoio social a idosos, combate à fome e voluntariado digital.

## 4. Personalização visual

O código apresenta identidade visual própria:

- Cores semânticas **coral**, **amarelo-sol**, **azul-claro** e **azul-escuro**;
- Uso das fontes **Poppins** (destaques) e **Inter** (texto);
- Seções com espaçamento amplo e cartões arredondados;
- Imagem de destaque na área inicial;
- Botões de chamada para ação;
- Transições e movimentos leves em elementos visuais.

Essas escolhas estão declaradas no arquivo **src/styles.css**, que utiliza Tailwind CSS, variáveis de tema e estilos associados à interface.

## 5. Funcionalidade interativa — Quiz de voluntariado

O arquivo [src/components/Quiz.tsx](https://github.com/Luizaaaaaah/pixel-perfect-pixels/blob/main/src/components/Quiz.tsx) implementa um questionário com **seis perguntas**.

### Fluxo previsto

1. O usuário seleciona **Começar o Quiz**.
2. Responde seis perguntas com alternativas.
3. Visualiza o progresso e pode retornar à pergunta anterior.
4. As respostas contribuem para categorias de interesse.
5. Ao final, o sistema calcula um perfil e apresenta uma descrição e sugestões de ações.
6. O usuário pode refazer o quiz ou conhecer outras causas.

### Perfis previstos

| Perfil | Exemplos de ações exibidas |
|---|---|
| Educador Social | Reforço escolar e oficinas |
| Protetor Animal | Apoio a abrigos e campanhas de adoção |
| Agente Ambiental | Plantio, limpeza e reciclagem |
| Acolhedor Social | Apoio a idosos e campanhas solidárias |
| Voluntário Digital | Design, tecnologia e divulgação para organizações |

O cálculo contabiliza pontos atribuídos às alternativas e utiliza critérios de desempate definidos no código. As sugestões são orientativas, não avaliações profissionais.

## 6. Tecnologias observadas

O projeto inclui **React**, **TypeScript**, **TanStack Router**, **Tailwind CSS**, **Vite** e bibliotecas de interface definidas no **package.json**. O uso do Lovable como ferramenta de criação é declarado no README.

### Responsividade prevista no código

A interface utiliza classes responsivas como **md:**, **sm:** e **lg:** para alterar grades, espaçamentos, tipografia e navegação. Em telas menores, o cabeçalho prevê um botão que abre e fecha o menu mobile.

A presença dessas regras indica preocupação com responsividade. **Ainda não há capturas reais anexadas nem relatório de testes do layout em diferentes dispositivos.**

## 7. Como executar localmente

Com Node.js e NPM instalados:

~~~bash
npm install
npm run dev
~~~

O projeto também possui scripts para build e testes. Esta documentação foi elaborada por inspeção do código, sem afirmar que os comandos foram executados.

## 8. Acesso e publicação

| Recurso | Situação |
|---|---|
| Repositório de código | [pixel-perfect-pixels](https://github.com/Luizaaaaaah/pixel-perfect-pixels) — privado |
| Projeto no editor Lovable | [Abrir editor](https://lovable.dev/projects/827f8a9a-8919-4bbf-aa28-04b64bd48edd) — acesso pode exigir login |
| Página principal | Identificada no código como ConectaAção |
| Quiz de seis perguntas | Implementação localizada |
| Deploy Vercel | [pixel-perfect-pixels-orcin.vercel.app](https://pixel-perfect-pixels-orcin.vercel.app) — deploy de produção `READY` no painel; acesso por terceiros a validar |
| Testes de responsividade | Não documentados com evidências |

**Importante:** o professor não conseguirá acessar o conteúdo de um repositório privado sem receber permissão. A alternativa é disponibilizar acesso autorizado ou uma publicação pública da aplicação. Nenhuma alteração de privacidade foi realizada.

## 9. Evidências a anexar

Usar capturas reais na pasta [prints](prints/README.md):

| Nome | Conteúdo |
|---|---|
| 01-configuracao-lovable.png | Projeto aberto no Lovable |
| 02-identidade-visual.png | Estilos e personalização |
| 03-homepage.png | Página inicial ConectaAção |
| 04-quiz-pergunta.png | Pergunta do quiz |
| 05-quiz-resultado.png | Perfil calculado |
| 06-responsividade-mobile.png | Visualização em celular |
| 07-site-publicado.png | Endereço público, quando confirmado |

Não incluir dados de acesso nas capturas.

## 10. Situação da atividade

- [x] Repositório associado ao Lovable localizado.
- [x] Estrutura das seções identificada no código.
- [x] Identidade visual e tecnologias documentadas.
- [x] Quiz de seis perguntas e cinco perfis identificado.
- [ ] Confirmar que este foi o projeto entregue na Aula 09.
- [ ] Testar quiz e responsividade no navegador.
- [x] Confirmar deploy de produção `READY` e registrar domínio na Vercel.
- [ ] Validar acesso sem login e funcionalidade do quiz no navegador.
- [ ] Garantir ao professor acesso à entrega.
- [ ] Anexar prints reais.

## 11. Conclusão

O **ConectaAção** exemplifica a utilização de um Website Builder com IA para produzir uma página temática personalizada e uma experiência interativa.

A análise do código mostra as seções planejadas, a identidade visual, a navegação e o questionário de voluntariado. Um deploy de produção foi localizado como `READY` no painel da Vercel, mas a página e o quiz ainda precisam ser validados no navegador e o acesso ao código privado deve ser resolvido para a avaliação.
