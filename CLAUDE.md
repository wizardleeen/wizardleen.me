# Project Memory

## Project: 李洋的博客 (Li Yang's Blog)
- **Framework**: Astro v5 (static site generator)
- **Package manager**: pnpm (npm is too slow in this environment)
- **Domain**: wizardleen.me
- **Language**: All UI, comments, and content in Chinese (zh-CN)
- **Site title**: 李洋的博客

## Environment Notes
- There is a proxy `HTTPS_PROXY=http://localhost:8118` configured that routes through a US server — it is slow. Always `unset HTTPS_PROXY HTTP_PROXY https_proxy http_proxy` before running pnpm/network commands.
- No outbound access to GitHub (template fetching fails) — scaffold projects manually when needed.
- After `pnpm install`, run `pnpm approve-builds` if native packages (esbuild, sharp) need build scripts.

## Project Structure
```
src/
├── content/blog/        # Markdown 博客文章 (add .md files here for new posts)
├── content.config.ts    # 内容集合配置 (Astro v5 glob loader)
├── components/          # Header.astro, Footer.astro
├── layouts/             # BaseLayout.astro, BlogPost.astro
├── pages/               # index, about, blog/index, blog/[...slug]
└── styles/global.css    # 全局样式
```

## Blog Post Frontmatter
```yaml
---
title: '文章标题'
description: '文章简介'
pubDate: 2024-01-01
updatedDate: 2024-01-02  # 可选
---
```

## User Preferences
- Use Chinese for everything: UI text, code comments, CSS comments, blog content
- Keep things simple and minimal
