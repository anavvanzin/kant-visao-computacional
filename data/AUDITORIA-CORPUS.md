# Auditoria do corpus bibliográfico — `corpus_consolidado.csv`

**Data de referência:** 2026-09-04.
**Escopo:** perfil estrutural e estatístico do corpus consolidado (76 obras),
confronto com `auditoria_qualidade.json` e correção do único defeito
estrutural encontrado. Esta auditoria **não** avalia o mérito acadêmico das
obras — isso é papel da verificação de fontes do relatório.

## Inventário

| | |
|---|---|
| Obras | **76** (73 registros parseáveis antes da correção; 76 depois) |
| Colunas | 12 (`title`, `authors`, `year`, `citations`, `abstract`, `result_id`, `publication_info`, `pdf_links`, `url`, `total_results`, `search_time`, `busca`) |
| Período | 1891–2026 |
| Campanhas de busca | 9 (`r1`–`r7a`, coluna `busca`) |
| Duplicatas (título normalizado ou `result_id`) | nenhuma |
| Obras sem URL | nenhuma |

Proveniência: exportação de resultados do Google Scholar consolidada de nove
buscas temáticas. Consequência direta: **todos os 76 abstracts são snippets
truncados** (média de ~190 caracteres, com elipses "…") — servem para triagem
temática, **não** como fonte citável do conteúdo da obra. Qualquer afirmação
do relatório apoiada numa obra do corpus precisa de verificação na fonte
primária.

## Defeito estrutural encontrado e corrigido

**Duas linhas com aspas não fechadas** (linhas físicas 48 e 53, obras "Do
convolutional neural networks learn class hierarchy?" e "Exploring
hierarchical convolutional features for hyperspectral image classification").
Em ambas, o campo `publication_info` abria aspas que nunca fechavam, e a cauda
do registro (`pdf_links`, `url`, `total_results`, `search_time`, `busca`)
estava colada dentro delas, com a URL fundida ao `publication_info`:

```
…,"A Bilal, … - IEEE transactions on …, 2017 - ieeexplore.ieee.org/abstract/document/8017618/,unknown,unknown,r4a_cnn.csv
```

**Efeito:** um parser CSV estrito (módulo `csv` do Python, pandas etc.) entra
na aspa aberta e **engole os registros seguintes** para dentro do campo — o
corpus parseava com 73 registros, dois deles monstros de 21 e 15 campos, e
três obras íntegras (entre elas o *Vision* de Marr, a mais citada do corpus)
desapareciam da leitura. Ferramentas que contam linhas físicas não viam nada
de errado — por isso a auditoria antiga reportava 76 linhas com
`type_consistency: 100`.

**Correção aplicada (2 linhas, conteúdo preservado):** fechadas as aspas do
`publication_info` após o domínio (`… - ieeexplore.ieee.org"`), e a cauda
separada em campos próprios (`,[],https://ieeexplore.ieee.org/abstract/document/<id>/,unknown,unknown,r4a_cnn.csv`).
Nenhuma obra excluída, nenhum valor alterado além da separação mecânica;
`result_id` de todas as 76 obras confirmado antes/depois.

**Armadilha documentada para futuras sessões:** antes da correção, a leitura
via `csv.reader` sugeria "registros fundidos" faltando título — diagnóstico
falso. As obras estavam completas nas linhas seguintes do arquivo cru; o
defeito era só a aspa aberta. Ao investigar CSV suspeito aqui, confrontar
sempre o parse estrito com as linhas físicas antes de concluir perda de dado.

## Confronto com `auditoria_qualidade.json`

O JSON antigo (não regenerável nesta sessão; mantido como está) acerta e erra:

| Afirmação do JSON | Veredito |
|---|---|
| `rows: 76` | **Correto** — mas por contagem de linhas físicas; o parse estrito só via 73 até a correção. |
| `type_consistency: 100` | **Enganoso** — o defeito de aspas é exatamente um problema de consistência estrutural, invisível à checagem que foi feita. |
| `citations` máx. 31.047 | **Correto** (*Vision*, Marr). |
| `year` outliers (5; min 1891) | **Falso positivo** — 1891 é obra da campanha Helmholtz; a "anomalia" é a natureza histórica do corpus, não erro de dado. |
| `citations` outliers (12) | **Falso positivo** — skew de lei de potência é o esperado em corpus bibliográfico. |
| Colunas constantes `pdf_links`/`total_results`/`search_time` | **Correto** — as três não carregam informação (valores `[]`/`unknown` em 100% das linhas); manter apenas por fidelidade à exportação. |
| `year` faltante em 2 obras | **Correto** — "Kant's a Priori Philosophical Perspectives on Artificial Intelligence" (r2a) e "Inductive Biases in Neural Networks" (r7a). |

## Perfil estatístico

**Distribuição temporal** (76 obras; 2 sem ano):

| Década | 1890 | 1940 | 1970 | 1980 | 1990 | 2000 | 2010 | 2020 |
|---|---|---|---|---|---|---|---|---|
| Obras | 1 | 1 | 2 | 2 | 7 | 9 | 20 | 32 |

Corpus fortemente contemporâneo (68% de 2010 em diante), com espinha
histórica deliberada (Helmholtz → Marr).

**Citações** (assimetria de lei de potência, como esperado):
min 0 · p25 3 · **mediana 26** · p75 118 · p95 1.515 · máx **31.047**.
A mediana, não a média, é o número representativo. Top 5: *Vision* (Marr,
ed. 2010, 31.047), *A computational theory of human stereo vision* (Marr &
Poggio, 3.327), *Hierarchical convolutional features for visual tracking*
(2.277), *DeepCrack* (1.381), *Learning convolutional feature hierarchies*
(772).

## Cobertura por campanha × seções do relatório prometido

| Campanha | Obras | Seções do relatório (README) | Densidade |
|---|---|---|---|
| `r1_kant_cv` | 10 | §1 núcleo kantiano; §3 mapeamento conceitual | boa |
| `r2a_apriori_dl` | 6 | §4 literatura Kant–IA; §7 a priori como firmware | razoável |
| `r2b_categories_ai` | 8 | §3–§4 | boa |
| `r3a_predictive` | 8 | §5 predictive processing | boa |
| `r3b_active_vision` | 10 | §5 visão ativa | boa |
| `r4a_cnn` | 10 | §7 vieses indutivos/hierarquias em CNNs | boa |
| `r5a_marr` | 8 | §2 ponte histórica (Marr) | boa |
| `r6a_helmholtz` | 8 | §2 ponte histórica (Helmholtz) | boa |
| `r7a_inductive_bias` | 8 | §7 | boa |

**Lacunas de cobertura:**

1. **§6 ("onde a analogia se rompe")** é a seção mais desguarnecida: Gibson
   aparece em só 2 obras, fenomenologia em 2, e **Dreyfus e a apercepção
   kantiana não têm nenhuma obra dedicada**. A seção exigirá pesquisa
   complementar com fonte primária fora do corpus.
2. **Exemplos adversariais** ("bugs de firmware", prometidos na descrição do
   repositório) não têm campanha própria — verificar se `r7a` os cobre ao
   redigir; provável necessidade de complemento.
3. As **2 obras sem ano** precisam do ano resolvido na fonte primária antes de
   citação em ABNT.

## Recomendações

1. Relatório: citar obras do corpus somente após verificação primária
   (abstracts truncados não sustentam citação).
2. Anexo A do relatório: referenciar este documento e o JSON antigo, com as
   ressalvas da tabela de confronto acima.
3. Futuras exportações do Scholar: validar com parse CSV estrito no ato da
   consolidação (o defeito de aspas nasce na exportação).
