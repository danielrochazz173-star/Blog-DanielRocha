# Blog do Daniel Rocha

Blog pessoal em Hugo + Hextra, com layout idêntico ao do Akita.

## Rodar local

```bash
hugo mod get
hugo server -p 1313
```

Abre http://localhost:1313

## Novo post

Crie a pasta e o `index.md`:

```bash
mkdir -p content/2026/02/06/meu-post
# edite content/2026/02/06/meu-post/index.md
```

Exemplo de front matter:

```yaml
---
title: "Título do post"
date: 2026-02-06T10:00:00-03:00
draft: false
description: "Descrição curta"
tags: [tag1, tag2]
---

Corpo em Markdown.
```

## Deploy

Push na branch `main` dispara o GitHub Actions e publica no Pages.

## Postar pelo celular

- App GitHub: editar/criar arquivos no repo, commit e push.
- Editor web do GitHub: também funciona no navegador do celular.
