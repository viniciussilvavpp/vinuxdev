# VinuxDev

Blog pessoal para documentar estudos, aprendizados e coisas que me interessam enquanto exploro o universo do desenvolvimento web com [AstroJS](https://astro.build).

![Astro](https://img.shields.io/badge/Astro-v7-ff5d01?logo=astro&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## Sobre

Este site é um espaço pessoal onde registro tudo o que aprendo. Aqui você pode encontrar posts sobre estudos, tutoriais, anotações de aulas e reflexões do dia a dia.

O tema utilizado é o [astro-theme-reimu](https://github.com/D-Sketon/astro-theme-reimu), adaptado e personalizado para atender às minhas necessidades.

---

## Funcionalidades

- Layout responsivo (desktop e mobile)
- Modo escuro / claro
- Suporte a MDX para posts
- Código com syntax highlighting (Expressive Code)
- Fórmulas matemáticas com KaTeX
- Diagramas com Mermaid
- Busca local (Fuse.js)
- Comentários (configurável — Valine, Waline, Giscus, entre outros)
- Animações de scroll (AOS)
- Efeitos visuais no mouse
- Preloader com animação
- RSS

---

## Stack

| Tecnologia | Função |
|---|---|
| [AstroJS](https://astro.build) | Framework principal |
| [React](https://react.dev) | Componentes interativos |
| [MDX](https://mdxjs.com) | Posts com componentes |
| [Stylus](https://stylus-lang.com) | Pré-processador CSS |
| [TypeScript](https://www.typescriptlang.org) | Tipagem estática |
| [pnpm](https://pnpm.io) | Gerenciador de pacotes |

---

## Início Rápido

### Pré-requisitos

- Node.js >= 22.12.0
- pnpm >= 9.6.0

### Instalação

```bash
# Clonar o repositório
git clone https://github.com/seu-usuario/astro-theme-reimu.git
cd astro-theme-reimu

# Instalar dependências
pnpm install

# Iniciar servidor de desenvolvimento
pnpm dev
```

### Comandos Disponíveis

```bash
pnpm dev        # Servidor de desenvolvimento
pnpm build      # Build para produção
pnpm preview    # Pré-visualizar build
pnpm lint       # Verificar código com ESLint
pnpm lint:fix   # Corrigir problemas automaticamente
```

---

## Estrutura do Projeto

```
/
├── public/                # Recursos estáticos
│   ├── fonts/             # Fontes locais
│   ├── images/            # Imagens do site
│   └── robots.txt
├── src/
│   ├── assets/            # Assets processados pelo Vite
│   ├── components/        # Componentes Astro/React
│   │   ├── partial/       # Componentes parciais (HeaderLink, Loader, etc.)
│   │   ├── sidebar/       # Sidebar e widgets
│   │   └── post/          # Componentes de posts
│   ├── content/           # Coleções de conteúdo
│   │   └── blog/          # Posts do blog (.mdx)
│   ├── layouts/           # Layouts de página
│   ├── languages/         # Arquivos de i18n
│   │   ├── pt-br.ts       # Português (Brasil)
│   │   └── en.ts          # Inglês
│   ├── pages/             # Rotas da aplicação
│   │   ├── about.mdx      # Página Sobre
│   │   ├── archives/      # Arquivo de posts
│   │   ├── blog/          # Página de blog
│   │   └── rss.xml.js     # Feed RSS
│   ├── styles/            # Estilos globais
│   │   ├── global.css     # CSS global e variáveis
│   │   └── base.stylus    # Estilos base
│   ├── utils/             # Funções utilitárias
│   └── config.ts          # Configuração do tema
├── astro.config.mjs       # Configuração do Astro
└── package.json
```

---

## Criando Posts

Crie um arquivo `.mdx` na pasta `src/content/blog/`:

```markdown
---
title: "Título do Post"
description: "Descrição breve do post"
pubDate: 2026-06-28
tags:
  - astro
  - estudo
categories:
  - desenvolvimento-web
---

Conteúdo do post aqui...
```

### Campos do Front Matter

| Campo | Obrigatório | Descrição |
|---|---|---|
| `title` | Sim | Título do post |
| `description` | Sim | Descrição para SEO |
| `pubDate` | Sim | Data de publicação |
| `updatedDate` | Não | Data de atualização |
| `cover` | Não | URL da imagem de capa |
| `tags` | Não | Lista de tags |
| `categories` | Não | Lista de categorias |
| `toc` | Não | Exibir sumário (padrão: `true`) |

---

## Configuração

Edite `src/config.ts` para personalizar o blog:

- **Informações do site**: título, subtítulo, descrição, autor
- **Menu**: links de navegação
- **Banner**: imagem do cabeçalho
- **Sidebar**: posição e widgets
- **Rodapé**: ano de início, contadores, ICP
- **Redes sociais**: links para perfis
- **Preloader**: habilitar/desabilitar e personalizar texto
- **Firework**: efeitos visuais no mouse

---

## Deploy

### GitHub Pages

1. Configure `astro.config.mjs`:

```javascript
export default defineConfig({
  site: "https://seu-usuario.github.io",
  base: "/nome-do-repo",
});
```

2. Faça push e configure GitHub Actions para deploy automático.

### Vercel / Netlify

Basta conectar o repositório GitHub — ambos detectam Astro automaticamente.

---

## Licença

MIT

---

Feito com 💜 enquanto aprendo AstroJS.
