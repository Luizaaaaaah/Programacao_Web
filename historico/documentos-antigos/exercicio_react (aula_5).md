# 🚀 Aula 05 — Introdução a Frameworks Front-end

> **Disciplina:** Desenvolvimento Web / Front-end  
> **Professor:** Prof. Me. Deivison S. Takatu  
> **Tema:** Introdução a Frameworks Front-end e React  
> **Atividade:** Aplicação React com múltiplas funcionalidades em uma única página

---

## 📚 Sumário

- [1. Resumo da aula](#1--resumo-da-aula)
- [2. Frameworks Front-end](#2--frameworks-front-end)
- [3. Framework x Biblioteca](#3--framework-x-biblioteca)
- [4. Por que utilizar frameworks](#4--por-que-utilizar-frameworks)
- [5. React](#5--react)
- [6. Conceitos fundamentais do React](#6--conceitos-fundamentais-do-react)
- [7. DOM e Virtual DOM](#7--dom-e-virtual-dom)
- [8. Node.js e NPM](#8--nodejs-e-npm)
- [9. Criação de um projeto React](#9--criação-de-um-projeto-react)
- [10. Estrutura do projeto](#10--estrutura-do-projeto)
- [11. Atividade prática](#11--atividade-prática)
- [12. Funcionalidades desenvolvidas](#12--funcionalidades-desenvolvidas)
- [13. Código da aplicação](#13--código-da-aplicação)
- [14. Estilização](#14--estilização)
- [15. Conceitos React utilizados no projeto](#15--conceitos-react-utilizados-no-projeto)
- [16. Etapas para entrega](#16--etapas-para-entrega)
- [17. Conclusão](#17--conclusão)

---

# 1. 📖 Resumo da aula

A aula apresentou uma introdução ao desenvolvimento **Front-end utilizando ferramentas modernas**, com foco em frameworks, bibliotecas JavaScript e principalmente no **React**.

Um framework front-end fornece ferramentas, padrões e uma estrutura que ajudam a organizar e acelerar o desenvolvimento de interfaces web. Entre as vantagens apresentadas estão maior produtividade, reutilização de componentes, manutenção facilitada, integração com APIs e organização do código.

Durante a aula, foi feita uma distinção importante entre **framework** e **biblioteca**. O material destaca que o React é tecnicamente uma **biblioteca JavaScript**, embora seja frequentemente chamado de framework.

A aula também abordou:

- Componentização;
- Programação reativa;
- Gerenciamento de estado;
- JSX;
- `useState`;
- `useEffect`;
- DOM e Virtual DOM;
- Node.js;
- NPM;
- `package.json`;
- Criação de projetos React;
- Estrutura de pastas;
- GitHub;
- Deploy no Vercel.

O conteúdo culminou em uma atividade prática na qual deveria ser criado um projeto React contendo cinco funcionalidades: **To-Do List, Contador de Cliques, Jogo da Velha, Calculadora e Buscador de CEP**.

---

# 2. 🧩 Frameworks Front-end

Um framework front-end é apresentado na aula como um conjunto de **ferramentas, bibliotecas e convenções** que padronizam o desenvolvimento de interfaces web.

A principal finalidade é oferecer uma estrutura que facilite a criação de aplicações maiores e mais complexas.

### Desenvolvimento tradicional

No desenvolvimento utilizando apenas JavaScript/HTML/CSS, é comum existir:

- Maior quantidade de código manual;
- Repetição;
- Maior dificuldade de manutenção;
- Manipulação manual da interface.

### Utilizando ferramentas modernas

Com frameworks e bibliotecas modernas, podemos trabalhar com:

- Componentes reutilizáveis;
- Gerenciamento de estado;
- Atualização eficiente da interface;
- Estrutura de código organizada;
- Integração facilitada com APIs.

---

# 3. ⚖️ Framework x Biblioteca

Essa é uma das diferenças importantes apresentadas na aula.

| Framework | Biblioteca |
|---|---|
| Controla o fluxo da aplicação | O desenvolvedor controla quando utilizá-la |
| Possui uma estrutura mais definida | É mais flexível |
| Pode impor padrões de desenvolvimento | Não necessariamente impõe uma estrutura |
| Exemplo: Angular | Exemplo: React |
| Exemplo: Vue, conforme apresentado no material | Exemplo: jQuery |

## 🔄 Inversão de controle

A diferença principal pode ser entendida pela ideia de **quem controla o fluxo**.

### Biblioteca

O desenvolvedor decide quando chamar determinada funcionalidade.

```text
Desenvolvedor
     ↓
 chama a biblioteca
     ↓
Biblioteca executa
```

### Framework

O framework possui maior controle sobre o fluxo da aplicação.

```text
Framework
     ↓
controla o fluxo
     ↓
executa componentes/funcionalidades
```

> **Importante:** o material da aula destaca explicitamente que o React não é tecnicamente um framework, mas uma biblioteca JavaScript para construção de interfaces.

---

# 4. 🚀 Por que utilizar frameworks?

Segundo o conteúdo apresentado, algumas vantagens são:

### ⚡ Produtividade

Evita que o desenvolvedor precise criar soluções do zero para problemas comuns.

### 🧱 Organização

A utilização de componentes permite dividir a aplicação em partes menores e mais fáceis de compreender.

### 🔧 Manutenção

Uma alteração em um componente pode ser realizada de forma mais isolada.

### 🌐 Comunidade

Tecnologias populares possuem documentação, plugins e soluções desenvolvidas pela comunidade.

### 📈 Escalabilidade

A organização por componentes e o gerenciamento de estado facilitam o crescimento da aplicação.

---

# 5. ⚛️ React

O React foi desenvolvido pelo Facebook em 2013 e tornou-se uma das ferramentas mais utilizadas para construção de interfaces web dinâmicas.

O React trabalha principalmente com:

- Componentes;
- JSX;
- Estado;
- Props;
- Hooks;
- Virtual DOM.

A aula destaca que é importante possuir conhecimento prévio de **HTML e JavaScript**, pois o React utiliza esses fundamentos para construir interfaces interativas.

## 🧱 Componentização

Uma aplicação React pode ser dividida em componentes independentes e reutilizáveis.

Por exemplo:

```text
Aplicação
│
├── Cabeçalho
│
├── Menu
│
├── To-Do List
│
├── Contador
│
├── Jogo da Velha
│
├── Calculadora
│
└── Buscador de CEP
```

No projeto desenvolvido nesta atividade, essas funcionalidades foram mantidas dentro do mesmo `App.js`, mas organizadas logicamente em diferentes partes.

---

# 6. 🪝 Conceitos fundamentais do React

## `useState`

O `useState` é utilizado para controlar o **estado de um componente funcional**.

Exemplo:

```jsx
import { useState } from 'react';

const [contador, setContador] = useState(0);
```

Nesse caso:

- `contador` guarda o valor atual;
- `setContador` altera o valor;
- `0` é o valor inicial.

Quando o estado é alterado, o React atualiza a interface.

### No projeto

O `useState` foi utilizado para controlar:

- Página atual;
- Lista de tarefas;
- Nova tarefa;
- Contador;
- Tabuleiro do jogo;
- Jogador atual;
- Valores da calculadora;
- Operação;
- Resultado;
- CEP;
- Resultado da busca;
- Mensagem de erro.

---

## `useEffect`

O material apresenta o `useEffect` como um Hook utilizado para lidar com **efeitos colaterais**, como chamadas de API.

Embora o projeto desenvolvido nesta atividade não tenha precisado de `useEffect`, o conceito é importante para aplicações React que precisam executar ações automaticamente em determinadas situações.

---

# 7. 🌳 DOM e Virtual DOM

## DOM

DOM significa **Document Object Model**.

Ele representa a estrutura da página HTML em forma de uma árvore de elementos.

Por meio do DOM, o JavaScript consegue modificar elementos da página.

Exemplo simplificado:

```text
HTML
│
└── body
    │
    ├── header
    │
    ├── main
    │   ├── h1
    │   └── button
    │
    └── footer
```

## Virtual DOM

O React utiliza o conceito de **Virtual DOM**.

De maneira simplificada:

```text
Alteração no estado
        ↓
Virtual DOM é atualizado
        ↓
React compara as mudanças
        ↓
Somente diferenças necessárias
são aplicadas ao DOM real
```

Isso ajuda a tornar as atualizações da interface mais eficientes.

---

# 8. 🟢 Node.js e NPM

## Node.js

O Node.js é um ambiente de execução JavaScript.

Na aula, ele é utilizado como parte do ambiente necessário para desenvolver aplicações React.

Uma forma de verificar a instalação é:

```bash
node --version
```

Se uma versão for exibida, o Node.js está disponível no sistema.

---

## 📦 NPM

NPM significa **Node Package Manager**.

Ele é utilizado para gerenciar pacotes e dependências JavaScript.

Entre suas funções estão:

- Instalar bibliotecas;
- Atualizar pacotes;
- Remover pacotes;
- Gerenciar dependências;
- Facilitar a colaboração entre desenvolvedores.

O arquivo:

```text
package.json
```

registra informações importantes sobre o projeto e suas dependências.

---

# 9. 🛠️ Criação de um projeto React

O material apresenta a criação de um projeto utilizando:

```bash
npx create-react-app meu-projeto-react
```

Depois:

```bash
cd meu-projeto-react
```

Para abrir no VS Code:

```bash
code .
```

E para iniciar o servidor de desenvolvimento:

```bash
npm start
```

### Fluxo completo

```bash
npx create-react-app meu-projeto-react
cd meu-projeto-react
code .
npm start
```

O `npx` permite executar o pacote utilizado para criar a aplicação.

---

# 10. 📁 Estrutura do projeto

Um projeto React possui diferentes arquivos e diretórios.

## `node_modules`

Armazena os pacotes instalados pelo NPM.

## `public`

Contém arquivos públicos da aplicação, como HTML e outros recursos.

## `src`

É onde ficam os principais arquivos React desenvolvidos pelo programador.

## `index.js`

É o ponto de entrada do React e realiza a renderização da aplicação no DOM.

## `App.js`

É o componente raiz da aplicação.

Neste projeto, toda a lógica das cinco funcionalidades foi colocada nesse arquivo.

## `App.css`

Contém os estilos utilizados pelo componente `App`.

## `index.css`

Pode conter estilos globais da aplicação.

## `package.json`

Contém informações do projeto e suas dependências.

## `package-lock.json`

Registra informações relacionadas às versões e à instalação das dependências.

## `.gitignore`

Define arquivos e diretórios que não devem ser enviados para o Git.

---

# 11. 🎯 Atividade prática

A atividade proposta na aula solicita a criação de um projeto React com um cabeçalho contendo as seguintes funcionalidades:

1. **To-Do List**
2. **Contador de Cliques**
3. **Jogo da Velha**
4. **Calculadora**
5. **Buscador de CEP**

Além disso, a atividade solicita:

- Utilizar Git;
- Realizar o commit no GitHub;
- Fazer o deploy no Vercel;
- Documentar os elementos criados;
- Explicar a escolha da estilização;
- Adicionar prints das telas;
- Informar os links do GitHub e Vercel.

---

# 12. 💻 Funcionalidades desenvolvidas

## 📝 12.1 To-Do List

A primeira funcionalidade permite cadastrar tarefas.

O usuário pode:

- Digitar uma tarefa;
- Adicionar a tarefa;
- Marcar a tarefa como concluída;
- Excluir a tarefa.

A lista é armazenada no estado do React.

### Conceitos utilizados

```jsx
useState()
map()
filter()
onChange
onClick
```

---

## 🖱️ 12.2 Contador de Cliques

O contador registra quantas vezes o usuário clicou.

Possui:

- Botão para adicionar um clique;
- Exibição do número atual;
- Botão para zerar.

Exemplo da lógica:

```jsx
setContador(contador + 1);
```

Para zerar:

```jsx
setContador(0);
```

---

## ❌ 12.3 Jogo da Velha

Foi criado um tabuleiro de 3 × 3.

O jogo alterna entre:

```text
X
O
X
O
...
```

O estado do tabuleiro é representado por um array:

```jsx
const [tabuleiro, setTabuleiro] = useState(
  Array(9).fill(null)
);
```

São verificadas oito possibilidades de vitória:

- 3 linhas;
- 3 colunas;
- 2 diagonais.

---

## 🧮 12.4 Calculadora

A calculadora permite realizar:

```text
Adição       +
Subtração    -
Multiplicação *
Divisão      /
```

A operação é escolhida através de um `<select>`.

A lógica utiliza `switch`:

```jsx
switch (operacao) {
  case '+':
    resultadoCalculo = numero1 + numero2;
    break;

  case '-':
    resultadoCalculo = numero1 - numero2;
    break;

  case '*':
    resultadoCalculo = numero1 * numero2;
    break;

  case '/':
    resultadoCalculo = numero1 / numero2;
    break;
}
```

Também foi adicionada uma verificação para impedir divisão por zero.

---

## 📍 12.5 Buscador de CEP

Essa funcionalidade consulta uma API externa.

O CEP informado é enviado para:

```text
https://viacep.com.br/ws/CEP/json/
```

A aplicação utiliza:

```jsx
fetch()
```

com:

```jsx
async/await
```

Os dados retornados são utilizados para apresentar:

- CEP;
- Logradouro;
- Bairro;
- Cidade;
- Estado.

### Fluxo

```text
Usuário digita CEP
        ↓
Aplicação valida o CEP
        ↓
fetch() realiza a requisição
        ↓
API retorna os dados
        ↓
React atualiza o estado
        ↓
Endereço aparece na tela
```

---

# 13. 🧑‍💻 Código da aplicação

Abaixo está o código utilizado para desenvolver a aplicação em um único arquivo `App.js`.

> O código é mantido como foi desenvolvido, sem alterar sua lógica.

```jsx
import { useState } from 'react';
import './App.css';

function App() {
  // Controla qual funcionalidade está sendo exibida
  const [pagina, setPagina] = useState('todo');

  // =========================
  // TO-DO LIST
  // =========================

  const [tarefas, setTarefas] = useState([]);
  const [novaTarefa, setNovaTarefa] = useState('');

  function adicionarTarefa() {
    if (novaTarefa.trim() === '') {
      return;
    }

    setTarefas([
      ...tarefas,
      {
        id: Date.now(),
        texto: novaTarefa,
        concluida: false
      }
    ]);

    setNovaTarefa('');
  }

  function concluirTarefa(id) {
    setTarefas(
      tarefas.map((tarefa) =>
        tarefa.id === id
          ? { ...tarefa, concluida: !tarefa.concluida }
          : tarefa
      )
    );
  }

  function removerTarefa(id) {
    setTarefas(tarefas.filter((tarefa) => tarefa.id !== id));
  }

  // =========================
  // CONTADOR
  // =========================

  const [contador, setContador] = useState(0);

  // =========================
  // JOGO DA VELHA
  // =========================

  const [tabuleiro, setTabuleiro] = useState(Array(9).fill(null));
  const [jogador, setJogador] = useState('X');

  function jogar(posicao) {
    if (tabuleiro[posicao] !== null || verificarVencedor(tabuleiro)) {
      return;
    }

    const novoTabuleiro = [...tabuleiro];
    novoTabuleiro[posicao] = jogador;

    setTabuleiro(novoTabuleiro);

    if (!verificarVencedor(novoTabuleiro)) {
      setJogador(jogador === 'X' ? 'O' : 'X');
    }
  }

  function verificarVencedor(tab) {
    const combinacoes = [
      [0, 1, 2],
      [3, 4, 5],
      [6, 7, 8],
      [0, 3, 6],
      [1, 4, 7],
      [2, 5, 8],
      [0, 4, 8],
      [2, 4, 6]
    ];

    for (let combinacao of combinacoes) {
      const [a, b, c] = combinacao;

      if (
        tab[a] &&
        tab[a] === tab[b] &&
        tab[a] === tab[c]
      ) {
        return tab[a];
      }
    }

    return null;
  }

  function reiniciarJogo() {
    setTabuleiro(Array(9).fill(null));
    setJogador('X');
  }

  const vencedor = verificarVencedor(tabuleiro);

  // =========================
  // CALCULADORA
  // =========================

  const [valor1, setValor1] = useState('');
  const [valor2, setValor2] = useState('');
  const [operacao, setOperacao] = useState('+');
  const [resultado, setResultado] = useState('');

  function calcular() {
    const numero1 = Number(valor1);
    const numero2 = Number(valor2);

    if (valor1 === '' || valor2 === '') {
      setResultado('Digite os dois valores.');
      return;
    }

    let resultadoCalculo;

    switch (operacao) {
      case '+':
        resultadoCalculo = numero1 + numero2;
        break;

      case '-':
        resultadoCalculo = numero1 - numero2;
        break;

      case '*':
        resultadoCalculo = numero1 * numero2;
        break;

      case '/':
        if (numero2 === 0) {
          setResultado('Não é possível dividir por zero.');
          return;
        }

        resultadoCalculo = numero1 / numero2;
        break;

      default:
        resultadoCalculo = 0;
    }

    setResultado(resultadoCalculo);
  }

  // =========================
  // BUSCADOR DE CEP
  // =========================

  const [cep, setCep] = useState('');
  const [endereco, setEndereco] = useState(null);
  const [erroCep, setErroCep] = useState('');

  async function buscarCep() {
    const cepLimpo = cep.replace(/\D/g, '');

    if (cepLimpo.length !== 8) {
      setErroCep('Digite um CEP válido com 8 números.');
      setEndereco(null);
      return;
    }

    try {
      setErroCep('');

      const resposta = await fetch(
        `https://viacep.com.br/ws/${cepLimpo}/json/`
      );

      const dados = await resposta.json();

      if (dados.erro) {
        setErroCep('CEP não encontrado.');
        setEndereco(null);
        return;
      }

      setEndereco(dados);
    } catch (erro) {
      setErroCep('Erro ao buscar o CEP.');
      setEndereco(null);
    }
  }

  // =========================
  // COMPONENTE PRINCIPAL
  // =========================

  return (
    <div className="App">

      {/* CABEÇALHO */}
      <header className="cabecalho">

        <div className="logo">
          <h1>React App</h1>
        </div>

        <nav>
          <button onClick={() => setPagina('todo')}>
            To-Do List
          </button>

          <button onClick={() => setPagina('contador')}>
            Contador de Cliques
          </button>

          <button onClick={() => setPagina('velha')}>
            Jogo da Velha
          </button>

          <button onClick={() => setPagina('calculadora')}>
            Calculadora
          </button>

          <button onClick={() => setPagina('cep')}>
            Buscador de CEP
          </button>
        </nav>

      </header>

      {/* CONTEÚDO */}
      <main className="conteudo">

        {/* =========================
            TO-DO LIST
        ========================= */}

        {pagina === 'todo' && (
          <section className="card">

            <h2>📝 To-Do List</h2>

            <div className="entrada-tarefa">

              <input
                type="text"
                placeholder="Digite uma tarefa..."
                value={novaTarefa}
                onChange={(e) => setNovaTarefa(e.target.value)}
                onKeyDown={(e) => {
                  if (e.key === 'Enter') {
                    adicionarTarefa();
                  }
                }}
              />

              <button onClick={adicionarTarefa}>
                Adicionar
              </button>

            </div>

            <ul className="lista-tarefas">

              {tarefas.map((tarefa) => (
                <li
                  key={tarefa.id}
                  className={tarefa.concluida ? 'concluida' : ''}
                >

                  <span
                    onClick={() => concluirTarefa(tarefa.id)}
                  >
                    {tarefa.texto}
                  </span>

                  <button
                    onClick={() => removerTarefa(tarefa.id)}
                  >
                    Excluir
                  </button>

                </li>
              ))}

            </ul>

            {tarefas.length === 0 && (
              <p>Nenhuma tarefa cadastrada.</p>
            )}

          </section>
        )}

        {/* =========================
            CONTADOR
        ========================= */}

        {pagina === 'contador' && (
          <section className="card">

            <h2>🖱️ Contador de Cliques</h2>

            <div className="contador">

              <p>Você clicou:</p>

              <strong>{contador}</strong>

              <p>vezes</p>

              <div>

                <button
                  onClick={() => setContador(contador + 1)}
                >
                  +1 Clique
                </button>

                <button
                  onClick={() => setContador(0)}
                >
                  Zerar
                </button>

              </div>

            </div>

          </section>
        )}

        {/* =========================
            JOGO DA VELHA
        ========================= */}

        {pagina === 'velha' && (
          <section className="card">

            <h2>❌ Jogo da Velha ⭕</h2>

            {vencedor ? (
              <h3>Vencedor: {vencedor}</h3>
            ) : (
              <h3>Jogador atual: {jogador}</h3>
            )}

            <div className="tabuleiro">

              {tabuleiro.map((valor, index) => (
                <button
                  key={index}
                  onClick={() => jogar(index)}
                  className="casa"
                >
                  {valor}
                </button>
              ))}

            </div>

            <button onClick={reiniciarJogo}>
              Reiniciar Jogo
            </button>

          </section>
        )}

        {/* =========================
            CALCULADORA
        ========================= */}

        {pagina === 'calculadora' && (
          <section className="card">

            <h2>🧮 Calculadora</h2>

            <div className="calculadora">

              <input
                type="number"
                placeholder="Primeiro número"
                value={valor1}
                onChange={(e) => setValor1(e.target.value)}
              />

              <select
                value={operacao}
                onChange={(e) => setOperacao(e.target.value)}
              >
                <option value="+">+</option>
                <option value="-">-</option>
                <option value="*">×</option>
                <option value="/">÷</option>
              </select>

              <input
                type="number"
                placeholder="Segundo número"
                value={valor2}
                onChange={(e) => setValor2(e.target.value)}
              />

              <button onClick={calcular}>
                Calcular
              </button>

            </div>

            {resultado !== '' && (
              <h3>Resultado: {resultado}</h3>
            )}

          </section>
        )}

        {/* =========================
            BUSCADOR DE CEP
        ========================= */}

        {pagina === 'cep' && (
          <section className="card">

            <h2>📍 Buscador de CEP</h2>

            <div className="buscador-cep">

              <input
                type="text"
                placeholder="Digite o CEP"
                value={cep}
                onChange={(e) => setCep(e.target.value)}
                maxLength="9"
              />

              <button onClick={buscarCep}>
                Buscar CEP
              </button>

            </div>

            {erroCep && (
              <p className="erro">
                {erroCep}
              </p>
            )}

            {endereco && (
              <div className="resultado-cep">

                <p>
                  <strong>CEP:</strong> {endereco.cep}
                </p>

                <p>
                  <strong>Logradouro:</strong> {endereco.logradouro}
                </p>

                <p>
                  <strong>Bairro:</strong> {endereco.bairro}
                </p>

                <p>
                  <strong>Cidade:</strong> {endereco.localidade}
                </p>

                <p>
                  <strong>Estado:</strong> {endereco.uf}
                </p>

              </div>
            )}

          </section>
        )}

      </main>

      {/* RODAPÉ */}
      <footer>
        <p>Projeto React - Atividade de Desenvolvimento Web</p>
      </footer>

    </div>
  );
}

export default App;
```

---

# 14. 🎨 Estilização

A aplicação recebeu uma estilização própria no arquivo `App.css`.

A proposta foi criar uma interface:

- Limpa;
- Moderna;
- Responsiva;
- Fácil de navegar;
- Com destaque para o conteúdo central.

## 🎨 Identidade visual

O cabeçalho utiliza uma aparência escura com destaque em azul, enquanto o conteúdo principal utiliza cartões brancos sobre um fundo claro.

### Estrutura visual

```text
┌──────────────────────────────────────────────────────┐
│                    REACT APP                         │
│                                                      │
│ To-Do │ Contador │ Jogo │ Calculadora │ CEP         │
└──────────────────────────────────────────────────────┘

                ┌────────────────────┐
                │                    │
                │   FUNCIONALIDADE   │
                │                    │
                │     conteúdo       │
                │                    │
                └────────────────────┘

┌──────────────────────────────────────────────────────┐
│       Projeto React - Atividade de Desenvolvimento   │
└──────────────────────────────────────────────────────┘
```

## Responsividade

Também foi utilizado `@media` para adaptar o cabeçalho e os controles para telas menores.

Exemplo:

```css
@media (max-width: 600px) {

  .cabecalho {
    padding: 20px;
  }

  nav {
    flex-direction: column;
    width: 100%;
  }

  nav button {
    width: 100%;
  }

  .card {
    padding: 25px 15px;
  }

  .entrada-tarefa,
  .buscador-cep {
    flex-direction: column;
  }

}
```

---

# 15. 🧠 Conceitos React utilizados no projeto

| Conceito | Aplicação no projeto |
|---|---|
| `useState` | Controle dos estados da aplicação |
| JSX | Estrutura da interface |
| Eventos | Interação com botões e campos |
| `onClick` | Botões do menu e funcionalidades |
| `onChange` | Campos de entrada |
| Renderização condicional | Troca das funcionalidades |
| `map()` | Exibição das tarefas e casas do jogo |
| `filter()` | Remoção de tarefas |
| Arrays | Armazenamento do tabuleiro e tarefas |
| `fetch()` | Consulta da API de CEP |
| `async/await` | Requisição assíncrona |
| `switch` | Operações da calculadora |
| CSS | Estilização da aplicação |
| Media Queries | Responsividade |

---

# 16. 📋 Etapas para entrega

A atividade proposta também solicita algumas etapas que devem ser realizadas para finalizar a entrega.

## 1️⃣ Criar o projeto

```bash
npx create-react-app meu-projeto-react
```

## 2️⃣ Desenvolver as funcionalidades

Implementar:

- [x] To-Do List
- [x] Contador de Cliques
- [x] Jogo da Velha
- [x] Calculadora
- [x] Buscador de CEP

## 3️⃣ Estilizar

Criar a identidade visual da aplicação e deixar a interface responsiva.

## 4️⃣ Testar

Verificar:

- [ ] Adicionar tarefas;
- [ ] Concluir tarefas;
- [ ] Excluir tarefas;
- [ ] Contador;
- [ ] Jogo da Velha;
- [ ] Operações matemáticas;
- [ ] Divisão por zero;
- [ ] Busca de CEP válido;
- [ ] CEP inexistente;
- [ ] Layout em diferentes tamanhos de tela.

## 5️⃣ Git e GitHub

A aula orienta realizar o commit e publicar o projeto no GitHub.

### Repositório

> 🔗 **GitHub:** `COLOCAR LINK DO REPOSITÓRIO AQUI`

## 6️⃣ Deploy no Vercel

A atividade também solicita publicar a aplicação no Vercel conectando o repositório do GitHub.

### Site

> 🌐 **Vercel:** `COLOCAR LINK DO SITE AQUI`

## 7️⃣ Documentação

A entrega deve conter:

- Descrição dos elementos criados;
- Explicação da estilização;
- Etapas realizadas;
- Prints das telas;
- Link do GitHub;
- Link do Vercel.

---

# 17. ✅ Conclusão

A atividade permitiu aplicar na prática os principais conceitos apresentados na introdução ao React.

Em uma única aplicação foram reunidas diferentes situações de interação com o usuário. O projeto utiliza **estado**, **eventos**, **renderização condicional**, **arrays**, **funções**, **requisições para API** e **estilização responsiva**.

A organização da aplicação também demonstra uma das principais vantagens das tecnologias modernas de desenvolvimento front-end: dividir a interface e sua lógica em partes que podem ser controladas e atualizadas de maneira eficiente.

O projeto desenvolvido funciona como uma pequena aplicação multifuncional, reunindo:

```text
             🚀 REACT APP
                  │
       ┌──────────┼──────────┐
       │          │          │
    To-Do     Contador     Jogo
       │          │          │
       └──────────┼──────────┘
                  │
          ┌───────┴───────┐
          │               │
     Calculadora      Buscador CEP
```

### 🎓 Principais aprendizados

> **React** → construção de interfaces por componentes e gerenciamento de estado.

> **useState** → armazenamento e atualização de informações da interface.

> **JSX** → combinação de estrutura semelhante ao HTML com JavaScript.

> **Eventos** → interação do usuário com a aplicação.

> **Fetch/API** → comunicação com serviços externos.

> **NPM/Node.js** → ambiente e gerenciamento de dependências para o projeto.

> **Git/GitHub/Vercel** → versionamento, publicação e disponibilização da aplicação.

---

## 📌 Referência principal

**TAKATU, Deivison S.** *Aula 05 — Introdução a Frameworks Front-end.* Material didático da disciplina.

> Material utilizado como base para este resumo e para a documentação da atividade.
