---
layout: post
title: "Teste de Comparativo com 3 Produtos"
description: "Página temporária para validar a estrutura de comparativos com três produtos no Jekyll."
slug: teste-comparativo-3-produtos
category: comparativos
categories: [comparativos]
image: "/assets/images/posts/black-decker-bcd704c1.webp"
date: 2026-10-31
author: "Equipe de Análises"
---

{% include review-toc.html %}

**Aviso:** esta página é apenas um teste técnico. As informações não representam uma comparação real de produtos.

## Introdução

Este comparativo temporário serve para verificar se o site consegue apresentar três produtos diferentes utilizando o cadastro centralizado.

## Produto 1 — Black+Decker BCD704C1

Primeiro produto cadastrado no sistema. O objetivo é verificar a exibição do card correspondente.

{% include produto-card.html id="black_decker_bcd704c1" %}

## Produto 2 — Makita DHP482

Segundo produto cadastrado no sistema. O objetivo é verificar se o card utiliza os dados corretos, independentemente do primeiro produto.

{% include produto-card.html id="makita_dhp482" %}

## Produto 3 — Furadeira Teste 03

Terceiro produto, criado exclusivamente para validar a inclusão de novos produtos no catálogo YAML.

{% include produto-card.html id="furadeira_teste_03" %}

## Tabela Comparativa de Teste

| Produto | Cadastro | Finalidade |
|---|---|---|
| Black+Decker BCD704C1 | Existente | Testar card 1 |
| Makita DHP482 | Existente | Testar card 2 |
| Furadeira Teste 03 | Novo | Testar card 3 |

## Conclusão

Se os três cards aparecerem com os nomes correspondentes, o sumário funcionar e a página aparecer na listagem de comparativos, teremos validado a estrutura básica para três produtos.
