# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

Relatório de pesquisa sobre a epistemologia de Kant e a visão computacional:
conhecimento como construção ativa, o *a priori* como "firmware" cognitivo,
predictive processing, vieses indutivos em redes neurais e exemplos adversariais.
Sumário das dez seções no [`README.md`](README.md).

## Natureza do repositório

**Repositório de pesquisa, só de dados e texto.** Não há código, build, testes
nem dependências — e não se deve adicionar nenhum sem pedido explícito.

```
README.md                       # índice e sumário do relatório
assets/fig1_isomorfismo.svg     # figura: isomorfismo estrutural
assets/fig2_linhagem.svg        # figura: linhagem intelectual
data/corpus_consolidado.csv     # corpus bibliográfico consolidado (76 obras)
data/auditoria_qualidade.json   # auditoria de qualidade do corpus
```

## Estado conhecido: dois artefatos prometidos e ausentes

O `README.md` anuncia dois arquivos que **nunca foram commitados** — o histórico
git tem apenas README, o CSV, o JSON e duas das três figuras:

1. `relatorio-kant-visao-computacional.md` — o relatório em si (~10.000 palavras,
   57 fontes). A sessão que criou o repositório se perdeu em tentativas de push
   de binários e terminou sem enviar o texto; ele pode existir apenas na máquina
   da autora.
2. `assets/` — a terceira figura, "panorama bibliométrico" (seção 8 do relatório).

Consequências práticas ao trabalhar aqui:

- **Não trate o README como inventário do que existe.** Confira no disco.
- A recuperação do relatório é uma tarefa de máquina local, descrita em
  `artigos/PROMPT-LOCAL.md` (Tarefa 1). Se não for recuperado, a alternativa
  registrada é reescrevê-lo a partir de `data/corpus_consolidado.csv`.
- Não apague nem reescreva o README para "corrigir" a promessa: ele é o registro
  do que o relatório deve conter, e o rastro de que falta.

## Relação com os repositórios irmãos

A auditoria transversal de artigos em `anavvanzin/artigos` varre este repositório
pelo glob `kant-visao-computacional/relatorio-*.md` (estágio "publicado"). O
prefixo `relatorio-` no nome do arquivo é o que o coloca na auditoria e na
compilação `tools/compilar.sh --todos` — preserve-o ao restaurar o texto.

## Convenções

- Idioma do conteúdo, dos commits e da comunicação: português.
- Citação: ABNT NBR 6023:2025 (PT) · Chicago (EN).
