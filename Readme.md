# DevPortfolio

Portefólio pessoal de programador, feito com **HTML, CSS e JavaScript puros** — sem frameworks nem passos de build. Apresenta quem sou, os meus projetos (com ligação ao GitHub), as minhas competências e um formulário de contacto.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

<!-- TODO: adiciona uma captura de ecrã em docs/preview.png e descomenta a linha abaixo -->
<!-- ![Pré-visualização do DevPortfolio](docs/preview.png) -->

**Demo:** <!-- TODO: https://o-teu-utilizador.github.io/devportfolio -->

## Funcionalidades

- Página inicial com apresentação e estado de disponibilidade
- Secção "O que faço" em formato editorial
- Projetos gerados a partir de dados, com **filtros por categoria** e links para o GitHub e demo
- Competências com barras animadas ao entrar no ecrã
- Formulário de contacto com validação (abre o cliente de email do visitante)
- Design **mobile-first**, responsivo, com menu móvel
- Tema escuro por defeito, com tema claro automático conforme o sistema
- Acessibilidade: HTML semântico, foco visível, alvos de toque ≥ 44px, `prefers-reduced-motion`

## Estrutura

```
devportfolio/
├── index.html   # página única: HTML, CSS e JS
└── README.md
```

## Como executar

Não precisa de instalação. Escolhe uma das opções:

```bash
# Opção 1: abrir diretamente
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows

# Opção 2: servidor local (requer Python 3)
python3 -m http.server 8000
# abre http://localhost:8000
```

## Personalização

Todo o conteúdo editável está no objeto `CONFIG`, no início do `<script>` de `index.html`:

| Campo | O que altera |
| --- | --- |
| `name` | O teu nome (título, iniciais, rodapé) |
| `email` | Destino do formulário de contacto |
| `github` / `linkedin` | Links na secção de contacto |
| `projects` | Lista de projetos: `title`, `desc`, `tags`, `type`, `repo`, `demo` |
| `skills` | Grupos de competências e nível (0–100) |

Exemplo de projeto:

```js
{
  title: "Lista de Tarefas",
  desc: "Aplicação de tarefas com filtros e edição.",
  tags: ["JavaScript", "HTML", "CSS"],
  type: "JavaScript",   // usado nos filtros
  repo: "https://github.com/o-teu-utilizador/lista-tarefas",
  demo: ""              // opcional
}
```

Para usar uma fotografia, substitui o bloco `.portrait` pela tag `<img>` comentada no HTML.

> Os projetos, o email e os links que vêm por defeito são **exemplos**. Substitui-os antes de publicar.

## Publicar no GitHub Pages

1. Garante que o ficheiro principal se chama `index.html` na raiz do repositório.
2. No GitHub, vai a **Settings → Pages**.
3. Em **Build and deployment**, escolhe **Deploy from a branch**, a branch `main` e a pasta `/ (root)`.
4. Guarda e aguarda um minuto; o endereço aparece no topo da página.

## Licença

Distribuído sob a licença MIT — vê o ficheiro `LICENSE` (cria-o se quiseres usar esta licença).
