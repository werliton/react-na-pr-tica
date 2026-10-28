# React na Prática

Apresentação interativa para o ensino de React, desenvolvida para a pós-graduação em Desenvolvimento Web do CEUMA e conduzida por **Werliton Silva**, Specialist Frontend e mentor de desenvolvimento web.

O material combina explicações, exemplos de código, demonstrações e quizzes para explorar desde componentes e estado local até comunicação com APIs e cache de dados.

## Visão geral

A aula está organizada em 21 slides, com navegação por menu lateral, botões e atalhos de teclado. Inclui notas para o instrutor e atividades que podem ser realizadas em um ambiente React separado, como um sandbox.

A apresentação é implementada em **HTML, CSS e JavaScript puro**. Os exemplos de React e JSX são exibidos como conteúdo didático; as interações simulam os conceitos no navegador, sem executar React.

## Conteúdo da aula

| Etapa | Temas abordados |
| --- | --- |
| Abertura | Apresentação do mentor e contextualização da aula. |
| Parte 1 — Fundamentos | Componentes, JSX, props, `useState`, re-renderização, snapshot de estado, `useEffect`, dependências e cleanup. |
| Parte 2 — Hooks e estado global | `useRef`, `useMemo`, hooks customizados, prop drilling e Context API com `createContext`, Provider e `useContext`. |
| Parte 3 — APIs, efeitos e cache | Exemplos de `fetch`, loading, erro e sucesso, race conditions, cleanup, cache, TTL e invalidação. Introdução conceitual a TanStack Query, SWR e RTK Query. |
| Fechamento | Quiz final e proposta de mini-projeto integrador. |

## Recursos interativos

- Edição de nome, cargo e cor com atualização da prévia e do exemplo de código de props.
- Comparação entre alterações de estado e de uma variável comum.
- Simulação do ciclo de vida de efeitos, com logs de execução e cleanup.
- Demonstrações de referências, memoização e reutilização de lógica com `useToggle`.
- Comparação visual entre prop drilling e Context, com atualização de consumidores.
- Requisições simuladas com controle de erro e tempos de resposta diferentes.
- Cache com indicação de HIT/MISS, TTL de 15 segundos e invalidação manual.
- Quizzes com feedback imediato e notas de apoio ao instrutor.
- Indicador de progresso e recuperação do último slide pelo `localStorage`, quando disponível.

As chamadas de API são simuladas com `Promise` e `setTimeout`. Não é necessário configurar um backend para utilizar as demonstrações.

## Como executar

### Abrir diretamente

Abra o arquivo [`index.html`](index.html) em um navegador moderno com JavaScript habilitado. Não há instalação de pacotes nem etapa de build.

É necessário acesso à internet para carregar o Tailwind CSS pelo CDN e as fontes do Google Fonts.

### Usar um servidor local

Se tiver Python 3 instalado, execute na pasta do projeto:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

Em seguida, acesse [http://localhost:8000](http://localhost:8000). Para encerrar o servidor, pressione `Ctrl + C` no terminal.

## Navegação

| Ação | Controle |
| --- | --- |
| Avançar um slide | `→` ou botão **Próximo** |
| Voltar um slide | `←` ou botão **Anterior** |
| Exibir ou ocultar notas do instrutor | `N` ou botão **Notas** |
| Exibir ou ocultar o menu lateral | `M` ou botão **Menu** |
| Ir a uma seção específica | Selecionar o slide no menu lateral |

Os atalhos ficam inativos enquanto o foco está em campos `input` ou `select`, permitindo interagir com as demonstrações. Em telas menores, o menu é recolhido após a seleção de um slide.

## Tecnologias e estrutura

| Tecnologia | Uso |
| --- | --- |
| HTML5 | Estrutura dos slides, formulários e exemplos de código. |
| Tailwind CSS 3.4.17 via CDN | Layout responsivo e estilos utilitários. |
| CSS incorporado | Controle de visibilidade, notas e animações de destaque. |
| JavaScript puro | Navegação, quizzes, simulações e persistência do slide. |
| Google Fonts | Fontes Inter e JetBrains Mono. |

```text
.
├── index.html   # Apresentação, estilos e lógica das demonstrações
└── readme.md    # Documentação do projeto
```

Para adaptar o material, edite as seções `section.sec` em `index.html`. O atributo `data-part` agrupa os slides por etapa, os títulos alimentam o menu lateral e os elementos com a classe `note` contêm as orientações ao instrutor. Os scripts ao final do arquivo controlam a navegação e as demonstrações.

## Mini-projeto proposto

Ao final da aula, a atividade sugerida é construir uma lista de usuários em um ambiente React, reunindo:

1. Componentes `UserList` e `UserCard` com props.
2. Campo de busca controlado por `useState`.
3. Busca de dados com loading, tratamento de erro e cleanup.
4. Tema claro/escuro compartilhado por Context.
5. Cache para reaproveitar usuários já consultados.
6. Como desafio adicional, substituição do fetch manual por TanStack Query.

O mini-projeto é uma proposta de exercício descrita nos slides e deve ser implementado separadamente.

## Mentor

**Werliton Silva** — Specialist Frontend · Mentor de Desenvolvimento Web

[Conectar no LinkedIn](https://www.linkedin.com/in/werliton-silva/)
