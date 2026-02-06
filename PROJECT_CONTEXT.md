# Contexto do Projeto

## O que é
Blog pessoal do Daniel Rocha, feito com Hugo + tema Hextra, baseado no layout do Akita (akitaonrails.com).
Publicado no GitHub Pages.

## Repositório
- GitHub: `https://github.com/danielrochazz173-star/Blog-DanielRocha`
- Branch principal: `main`

## URL do site
- `https://danielrochazz173-star.github.io/Blog-DanielRocha/`

## Ferramentas e versões
- Hugo (build no CI): `0.155.2`
- Ruby: usado para gerar o índice (`scripts/generate_index.rb`)

## Estrutura do conteúdo
Posts seguem o padrão:
```
content/AAAA/MM/DD/slug/index.md
```
Exemplo:
```
content/2026/02/06/ola-mundo/index.md
```

## Criar post (manual)
1. Crie a pasta do post.
2. Edite o `index.md` com front matter + Markdown.
3. Rode o gerador do índice.
4. Commit e push.

Front matter:
```yaml
---
title: "Título do post"
date: 2026-02-06T10:00:00-03:00
draft: false
description: "Descrição curta"
tags: [tag1, tag2]
---
```

## Gerar índice (home)
A home é gerada automaticamente por:
```
./scripts/generate_index.rb
```

## Deploy (GitHub Pages)
- Workflow: `.github/workflows/pages.yaml`
- Build com Hugo (baseURL dinâmico do repo)
- Publicação via GitHub Actions

## Ajustes importantes já feitos
- `hugo.yaml` com `baseURL` correto para subpasta do Pages
- Atualização do Hugo no workflow para versão compatível com Hextra
- Remoção de `relativeURLs` e `canonifyURLs` (quebravam os assets)

## Como postar pelo celular
- App do GitHub
- Criar arquivo em `content/AAAA/MM/DD/slug/index.md`
- Commit

## Notas de rede (DNS)
Se `git push` falhar com `Could not resolve host: github.com`, ajustar DNS:
```
nmcli connection modify "Rocha 2.4" ipv4.dns "1.1.1.1 8.8.8.8" ipv4.ignore-auto-dns yes
nmcli connection down "Rocha 2.4"
nmcli connection up "Rocha 2.4"
```
Testar:
```
curl -I https://github.com
```
