---
title: '使用 Astro 搭建个人博客'
description: '分享使用 Astro 框架搭建个人博客的经验和心得。'
pubDate: 2024-02-01
---

最近我使用 Astro 搭建了这个博客网站，这里记录一下整个过程。

## 为什么选择 Astro

Astro 是一个非常适合搭建内容驱动网站的框架，它有以下优势：

1. **零 JavaScript 默认**：生成纯静态 HTML，加载速度极快
2. **Markdown 支持**：原生支持 Markdown 写作，非常适合博客
3. **内容集合**：提供类型安全的内容管理方式
4. **灵活的部署**：可以部署到任何静态托管平台

## 项目结构

```
src/
├── content/blog/    # Markdown 博客文章
├── layouts/         # 页面布局模板
├── pages/           # 路由页面
├── components/      # 可复用组件
└── styles/          # 全局样式
```

## 添加新文章

只需要在 `src/content/blog/` 目录下创建新的 `.md` 文件即可。每篇文章需要包含 frontmatter：

```yaml
---
title: '文章标题'
description: '文章简介'
pubDate: 2024-01-01
---
```

非常简单方便！
