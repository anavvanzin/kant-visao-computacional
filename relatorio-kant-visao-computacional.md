---
title: "Kant e a Visão Computacional: o conhecimento como construção ativa"
author: "Ana Vitória Vanzin Mendes"
lang: pt-BR
---

# Kant e a Visão Computacional: o conhecimento como construção ativa

**Relatório de pesquisa** — corpus bibliográfico de 76 obras (`data/corpus_consolidado.csv`),
nove campanhas de busca, período 1891–2026. Estrutura conforme o sumário do
`README.md`; qualidade do corpus documentada no Anexo A.

**Resumo:** Este relatório examina o paralelo estrutural entre a epistemologia
de Kant — o conhecimento como construção ativa do sujeito, condicionada por
formas a priori — e a visão computacional contemporânea. Reconstrói a linhagem
histórica que liga a filosofia crítica à engenharia (Helmholtz e a inferência
inconsciente; Marr e a teoria computacional da visão; as hierarquias
convolucionais do deep learning), mapeia o isomorfismo conceito a conceito,
organiza a literatura Kant–IA recente, analisa o processamento preditivo e a
visão ativa como kantismo naturalizado, delimita as rupturas da analogia
(Gibson, Dreyfus, apercepção, normatividade) e propõe a leitura do a priori
como *firmware*: estrutura gravada antes do uso — o *inductive bias* das
arquiteturas —, condicionante de todo uso e, no entanto, historicamente
regravável, cujos "bugs" são os exemplos adversariais. Fecha com panorama
bibliométrico do corpus e auditoria de qualidade dos dados.

**Palavras-chave:** Kant; visão computacional; epistemologia; a priori;
inferência inconsciente; David Marr; processamento preditivo; visão ativa;
viés indutivo; exemplos adversariais.

## Sumário

1. [O núcleo kantiano: conhecimento como construção, não cópia](#1-o-núcleo-kantiano-conhecimento-como-construção-não-cópia)
2. [A ponte histórica: Helmholtz, Marr e o deep learning](#2-a-ponte-histórica-helmholtz-marr-e-o-deep-learning)
3. [Mapeamento conceitual item a item](#3-mapeamento-conceitual-item-a-item)
4. [A literatura Kant–IA contemporânea](#4-a-literatura-kantia-contemporânea)
5. [Predictive processing e visão ativa](#5-predictive-processing-e-visão-ativa)
6. [Onde a analogia se rompe](#6-onde-a-analogia-se-rompe)
7. [O a priori como firmware](#7-o-a-priori-como-firmware)
8. [Panorama bibliométrico](#8-panorama-bibliométrico)
9. [Síntese e avaliação final](#9-síntese-e-avaliação-final)
10. [Anexo A — auditoria de qualidade do corpus](#anexo-a--auditoria-de-qualidade-do-corpus)

---

## 1. O núcleo kantiano: conhecimento como construção, não cópia

A tese que organiza este relatório é a mais célebre da *Crítica da razão pura*:
o conhecimento não é cópia passiva de um mundo pronto, mas **construção ativa**
do sujeito, que impõe à matéria sensível formas que ele mesmo traz. "Pensamentos
sem conteúdo são vazios, intuições sem conceitos são cegas" (KANT, 2012, B 75):
a experiência só se constitui quando a receptividade da sensibilidade — cuja
forma são o espaço e o tempo — é trabalhada pela espontaneidade do entendimento,
cujas formas são as categorias. Entre um polo e outro opera a **síntese**: a
apreensão do múltiplo, sua reprodução na imaginação e seu reconhecimento no
conceito. É a chamada revolução copernicana — não é o conhecimento que se regula
pelos objetos, mas os objetos da experiência que se regulam pelas condições do
conhecer.

Convém precisar o que a revolução copernicana **não** diz, porque é aí que as
apropriações apressadas tropeçam. Ela não diz que o sujeito *cria* o mundo: a
matéria da sensação é dada, recebida, e permanece irredutível — o idealismo
kantiano é transcendental (sobre as formas), não material (sobre a
existência). Tampouco diz que as estruturas a priori são conteúdos inatos, um
estoque de ideias prontas: são **funções** — modos de operar sobre o dado, não
representações armazenadas. E não diz, por fim, que o conhecimento seja
arbitrário por ser construído: as formas são as mesmas para todo sujeito
racional, e é justamente essa universalidade que funda a objetividade dos
juízos sintéticos a priori — os juízos que ampliam o conhecimento (sintéticos)
sem depender da experiência (a priori), cuja possibilidade é a pergunta
motriz de toda a primeira Crítica. As três precisões terão tradução direta no
paralelo técnico: a rede não gera seus dados; seus vieses são funções
arquiteturais, não conteúdos; e a estrutura compartilhada é o que permite a
generalização — o análogo operacional da objetividade (seção 7).

Três peças desse aparato importam diretamente para o paralelo com a visão
computacional. Primeiro, o ***a priori***: espaço, tempo e categorias não vêm da
experiência, mas são condição de possibilidade dela — estruturas anteriores a
qualquer dado, que determinam **o que pode aparecer** como dado. Segundo, o
**esquematismo**: para que categorias puras se apliquem a intuições sensíveis, a
imaginação produz esquemas, procedimentos intermediários que traduzem conceito
em condição temporal-sensível. Terceiro, a **apercepção transcendental**: a
unidade do "eu penso" que deve poder acompanhar todas as minhas representações,
sem a qual síntese alguma teria um sujeito a quem pertencer.

A literatura que confronta esse aparato com sistemas artificiais de percepção
já é substancial. Schubbach (2021) usa a epistemologia kantiana para
caracterizar o tipo de justificação que os juízos de um sistema de *deep
learning* poderiam ter — o problema não é se a máquina "acerta", mas em que
sentido seu resultado é um **juízo**. Schlicht (2022) relê o desenvolvimento da
ciência cognitiva, do simbolismo ao conexionismo, sob a lente da teoria
kantiana da cognição, argumentando que as perguntas de Kant sobre as condições
da experiência estruturam, queira-se ou não, o programa da área. Vishwanath
(2005) examina o estatuto epistemológico da visão e nota a ironia histórica: as
teses que Kant rejeitou no realismo cartesiano e as que abraçou dividem até
hoje o campo da visão computacional. Na mesma chave, Stark e Choi (1996)
propõem reservar a distinção kantiana entre **sensação** e **percepção** para
interpretar o *scanpath* ocular como mecanismo epistemológico — a sequência de
fixações do olho como a síntese da apreensão tornada mensurável.

Há também um uso mais especulativo do repertório kantiano. Sloman (2008)
recorre à filosofia da matemática de Kant — o conhecimento matemático como
sintético a priori, descoberto "pensando do modo certo" — para perguntar o que
faltaria a "robôs jovens" para aprender matemática como crianças. Kaluža (2023)
contrasta o empirismo de Hume com a filosofia crítica de Kant no cenário da IA
e da economia da atenção, defendendo que a autonomia kantiana da mente nunca
foi tão desafiada. Hui (2026) rastreia o conceito de máquina no interior do
próprio Kant, lendo a filosofia crítica simultaneamente como antídoto contra a
máquina e como parcialmente maquínica. Pushkarsky (2025) sintetiza o valor
metodológico do gesto: aplicar a IA o método transcendental é perguntar pelas
condições a priori de possibilidade do próprio sistema — pergunta que a
engenharia responde, sem saber, toda vez que escolhe uma arquitetura.

O saldo da seção é uma formulação de trabalho: chamemos **construtivismo
perceptivo** a tese de que todo sistema que percebe — biológico ou artificial —
só extrai estrutura do estímulo porque já traz estrutura; o que varia entre os
sistemas é *qual* estrutura trazem e *de onde* ela vem. As seções seguintes
testam essa formulação: historicamente (seção 2), item a item (seção 3), na
literatura filosófica recente (seção 4), nos programas científicos que a
assumem (seção 5), nos pontos em que ela quebra (seção 6) e na sua tradução
técnica contemporânea (seção 7).

## 2. A ponte histórica: Helmholtz, Marr e o deep learning

O caminho de Kant à visão computacional não é um salto: passa por uma linhagem
identificável de cientistas da visão que naturalizaram, cada um a seu modo, a
tese construtivista (ver `assets/fig2_linhagem.svg`).

### 2.1 Helmholtz e a inferência inconsciente

Hermann von Helmholtz é o elo decisivo. No terceiro volume do *Handbuch der
physiologischen Optik*, ele formula a doutrina das **inferências inconscientes**
(*unbewusste Schlüsse*): a percepção não é registro, é conclusão — o sistema
visual infere, a partir de sensações fragmentárias e ambíguas, a causa externa
mais provável, por processos análogos à inferência lógica, porém automáticos,
irresistíveis e inacessíveis à introspecção (HELMHOLTZ, 1948). A tese foi
controversa desde o início: já em 1891, Hyslop discutia se "inferência
inconsciente" não seria uma contradição em termos, e se a teoria helmholtziana
da percepção espacial se sustentava (HYSLOP, 1891). Hamlyn (1977) retoma a
objeção conceitual — em que sentido um processo que o sujeito não pode nem
reconhecer como seu é uma *inferência*? — e Hacker (1995) disseca o quadro
conceitual da teoria, apontando que as inferências helmholtzianas são
"inefáveis": não podemos exprimi-las, apenas postulá-las.

A posição de Helmholtz na linhagem kantiana é, ela própria, disputada. Turner
(1977) documenta o Helmholtz **empirista**: contra o nativismo de Hering, ele
sustentava que a percepção de profundidade resulta de aprendizagem empírica, de
incontáveis inferências inconscientes acumuladas — um Kant sem a priori fixo,
por assim dizer, em que as formas da percepção são adquiridas. É precisamente
essa combinação — estrutura inferencial kantiana, conteúdo aprendido — que o
torna o ancestral comum das duas tradições contemporâneas: a bayesiana e a
conexionista.

Um segundo componente da teoria helmholtziana merece registro, porque
antecipa uma das teses mais duras da visão computacional: a **teoria dos
sinais**. Para Helmholtz, as sensações não são imagens das coisas, mas
*signos* delas — a qualidade sentida não precisa assemelhar-se à propriedade
que a causa, bastando que a correspondência seja regular e aprendível
(HELMHOLTZ, 1948). O rompimento com a epistemologia da cópia não poderia ser
mais explícito, e é exatamente o estatuto que o aprendizado de máquina
atribui às suas representações internas: um *feature map* não se parece com
o objeto; codifica-o de modo útil para a tarefa. Quando a seção 7 discutir
exemplos adversariais — casos em que o código da rede e o nosso divergem —,
será a teoria dos sinais levada à sua consequência incômoda: sistemas com
signos diferentes vivem em fenômenos diferentes. Westheimer (2008) pergunta diretamente "Helmholtz era
bayesiano?", lendo as inferências inconscientes como protótipo da inferência
estatística sobre hipóteses perceptivas; Barlow (1990) traduz a doutrina para a
psicofísica moderna — a inferência inconsciente como acesso automático a um
repositório de regularidades aprendidas, que é o que torna a percepção tão
eficaz para aprender; e Seth (2019) traça o arco completo, da inferência
inconsciente de Helmholtz à percepção preditiva contemporânea, passando pela
*beholder's share* da escola de Viena.

### 2.2 Marr e a teoria computacional da visão

Se Helmholtz naturalizou a inferência, David Marr formalizou a **construção**.
Em *Vision* (MARR, 2010), a percepção visual é analisada como processamento de
informação em três níveis — teoria computacional (que problema o sistema
resolve e por quê), representação e algoritmo, implementação física — e como
uma sequência de representações progressivamente mais estruturadas, do esboço
primário à representação tridimensional centrada no objeto. Já na conferência
de 1979 sobre reconhecimento de padrão e forma, Marr (1982) defendia que a
visão é a **construção de descrições simbólicas eficientes** a partir da
imagem, e que a escolha das representações é o aspecto central de qualquer
teoria da visão. A teoria da estereopsia desenvolvida com Poggio (MARR;
POGGIO, 1991) mostrou o programa em ato: derivar, de restrições físicas do
mundo (continuidade, unicidade da correspondência), o algoritmo que o sistema
visual *precisa* implementar.

A recepção filosófica do programa marriano é parte da nossa ponte. Kitcher
(1988) situa a teoria de Marr no desenvolvimento da visão computacional e
discute o que exatamente ela diz sobre quais características do ambiente o
sistema visual representa. Shagrir (2010) analisa o nível da "teoria
computacional" e mostra que ele carrega mais do que parece: o *porquê*
marriano amarra a computação às relações matemáticas do mundo representado.
Stevens (2012) revisita os três níveis e o peso da escolha de representações;
Hacker (2016) faz a crítica conceitual — o que Marr descreve seria teoria da
*visão de máquina*, um mapeamento de representação em representação, e não,
sem mais, teoria do ver humano. Warren (2012), a que voltaremos na seção 6,
pergunta se a teoria resolve o problema certo.

Vale explicitar por que os três níveis marrianos importam para a linhagem, e
não apenas para a história da área. O nível computacional é uma análise de
**tarefa e mundo**: a estereopsia é solúvel porque o mundo físico garante que
um ponto de superfície tem uma única posição num instante (unicidade) e que
superfícies variam suavemente (continuidade) — restrições que não estão nas
imagens, mas *sobre* elas, e que o par de olhos pode explorar porque o
problema já vem estruturado por elas (MARR; POGGIO, 1991). Shagrir (2010)
mostra que essa amarração do algoritmo às relações matemáticas do mundo é o
conteúdo próprio do "porquê" marriano; Stevens (2012) acrescenta que a escolha
de representações — o que cada estágio torna explícito — tem impacto profundo
sobre a computação correspondente. Traduzido: para Marr, ver é possível
porque o sistema *assume* um mundo com certa estrutura, e a teoria da visão é
a explicitação dessas suposições. É a forma lógica do argumento
transcendental, aplicada a um mecanismo.

O ponto para a nossa linhagem: Marr é um kantiano metodológico sem citar Kant.
Os três níveis são uma teoria das **condições de possibilidade** da percepção
visual — o nível computacional pergunta o que *tem de ser verdade* do mundo e
da tarefa para que a visão seja possível; as restrições (rigidez, continuidade)
funcionam como um a priori do domínio, pressuposto e não extraído da imagem.

### 2.3 Do neocognitron ao deep learning

A terceira arcada da ponte é técnica. As redes convolucionais profundas
herdaram de Marr a ideia de representações hierárquicas progressivas e de
Helmholtz o primado da aprendizagem — e as fundiram numa arquitetura em que a
hierarquia é a priori e o conteúdo é aprendido. Kavukcuoglu et al. (2010)
mostram a aprendizagem de **hierarquias de características convolucionais**
para reconhecimento visual; LeCun, Bengio e Hinton (2015) consagram a fórmula:
camadas sucessivas que compõem características simples em complexas, com a
convolução e o *pooling* embutindo na arquitetura as invariâncias esperadas do
mundo visual. A seção 7 examina em detalhe essa herança sob o nome técnico que
ela recebeu — *inductive bias* — e a seção 3, a seguir, organiza o paralelo
conceito a conceito.

## 3. Mapeamento conceitual item a item

A Tabela 1 organiza o isomorfismo estrutural entre o aparato kantiano e os
componentes de um sistema de visão computacional profundo (ver também
`assets/fig1_isomorfismo.svg`). O mapeamento é **estrutural, não semântico**:
afirma que os dois sistemas têm a mesma *forma* de solução para o mesmo
problema — extrair objetividade de estímulo subdeterminado —, não que redes
neurais "tenham" conceitos kantianos. Os limites do mapeamento são o objeto da
seção 6.

**Tabela 1 — Mapeamento conceitual Kant ↔ visão computacional**

| # | Kant | Visão computacional | Natureza do paralelo | Fontes de apoio |
|---|---|---|---|---|
| 1 | Formas puras da intuição (espaço, tempo) | Estrutura da grade de entrada; topologia convolucional; equivariância a translação | Condição estrutural anterior a qualquer dado | Benton et al. (2020); Bouchacourt et al. (2021) |
| 2 | Categorias do entendimento | Vieses indutivos arquiteturais; classes de hipóteses do modelo | Repertório finito que organiza todo input possível | Frisch et al. (2024); Grigorova e Komarov (2024) |
| 3 | Síntese da apreensão | Convolução + *pooling* local; agregação de características | Composição do múltiplo em unidades | Kavukcuoglu et al. (2010); Razzaghi, Abbasi e Bayat (2020) |
| 4 | Síntese da reprodução (imaginação) | Estados recorrentes; memória; *top-down feedback* | Retenção do passado na leitura do presente | Tani (1998); Nishimoto e Tani (2009) |
| 5 | Síntese do reconhecimento no conceito | Camadas finais de classificação; *softmax* sobre classes | Subsunção do particular sob o universal | Bilal et al. (2017); Yan et al. (2015) |
| 6 | Esquematismo | Representações intermediárias aprendidas; *feature maps* que medeiam pixel e classe | Procedimento-ponte entre sensível e conceitual | Zhang (2025); beim Graben (2024) |
| 7 | Juízo determinante | Inferência (*forward pass*) sobre exemplar dado | Aplicação de regra pronta a caso novo | Schubbach (2021) |
| 8 | Juízo reflexionante | Aprendizagem: busca da regra para o particular | Indução da regra a partir de casos | Schubbach (2021); beim Graben (2024) |
| 9 | Unidade da apercepção | **Sem análogo satisfatório** | Ponto de ruptura — ver seção 6 | Noller (2026); Shetty (2025) |
| 10 | Fenômeno vs. coisa em si | Espaço de representação vs. mundo; a rede só opera sobre o já-estruturado | Limite epistêmico compartilhado | Shetty (2025); Hohwy (2025) |

As linhas 1 e 3–5 formam o bloco em que o paralelo é mais literal. Na linha
1, a estrutura convolucional impõe ao dado exatamente o que as formas da
intuição impõem ao múltiplo sensível: uma organização espacial prévia — a
vizinhança de pixels *conta* como vizinhança porque a arquitetura a trata
assim, e a equivariância translacional (mover o objeto move a resposta, sem
alterá-la) é a homogeneidade do espaço tornada operação (BOUCHACOURT et al.,
2021). Nas linhas 3–5, a tríplice síntese kantiana encontra sua caricatura
funcional: a convolução com *pooling* apreende o múltiplo local em unidades
(apreensão); recorrência e realimentação retêm o processado para informar o
processamento seguinte (reprodução) — é o circuito que Tani (1998) e
Nishimoto e Tani (2009) exploram em robôs, com predição *top-down*
encontrando percepção *bottom-up*; e a camada de classificação subsume o
resultado sob uma classe (reconhecimento). As linhas 7–8, por sua vez,
importam a distinção da terceira Crítica que Schubbach (2021) mobiliza: a
*inferência* de um modelo treinado é juízo determinante (a regra está dada;
o caso é subsumido), o *treinamento* é juízo reflexionante (dado o particular,
busca-se a regra) — e a dificuldade kantiana de dar conta do reflexionante
sem pressupor o determinante reaparece, intacta, no problema da generalização.

Três linhas da tabela merecem glosa adicional. A linha 2 é o coração da analogia e seu
ponto mais discutido: Frisch et al. (2024) exploram, no quadro da IA
neuro-simbólica aplicada à visão computacional, a "faculdade de combinação" —
aprender conceitos sintéticos a priori aplicando estruturas inatas — como
programa de engenharia; Grigorova e Komarov (2024) chegam a tratar a
filosofia de Kant como "arquétipo" da IA, com as categorias do entendimento
como esquema de projeto. A linha 6 registra a leitura de Zhang (2025), para
quem os fenômenos de *insight* em sistemas de IA são o lugar natural de
aplicação dos conceitos a priori kantianos, e a de beim Graben (2024), que
constrói um análogo conexionista explícito de doutrina kantiana — no caso, a
harmonia das faculdades da terceira Crítica modelada em redes adversariais
generativas. A linha 9, por fim, é deliberadamente negativa: nenhuma obra do
corpus oferece um análogo técnico defensável da apercepção transcendental, e as
que tocam o tema (NOLLER, 2026; SHETTY, 2025) o fazem para marcar o limite.

## 4. A literatura Kant–IA contemporânea

O encontro entre Kant e a IA deixou de ser curiosidade para virar subcampo,
com marco editorial claro: o volume *Kant and Artificial Intelligence*,
publicado pela De Gruyter em 2022, do qual o corpus capta dois capítulos — Kim (2022), que
responde ao chamado de McCarthy por "ajuda filosófica" rastreando as origens
da IA de um ponto de vista kantiano, e Schlicht (2022), já discutido na seção
1. A Tabela 2 organiza a literatura do corpus por eixo temático.

**Tabela 2 — Literatura Kant–IA no corpus, por eixo**

| Eixo | Pergunta central | Obras do corpus (autor, ano) |
|---|---|---|
| Epistemológico | Que tipo de conhecimento/juízo um sistema de DL produz? | Schubbach (2021); Swanson (2016); Schlicht (2022); Vishwanath (2005); Stark e Choi (1996); Kaluža (2023) |
| Transcendental-técnico | O a priori pode ser implementado? Onde mora nas arquiteturas? | Zhang (2024, 2025); Frisch et al. (2024); beim Graben (2024); Pushkarsky (2025); Sloman (2008) |
| Histórico-conceitual | O que a IA deve (e faz) com o conceito kantiano de máquina/inteligência? | Kim (2022); Hui (2026); Grigorova e Komarov (2024) |
| Crítico-limitativo | O que falta, por princípio, à IA no quadro kantiano? | Noller (2026); Shetty (2025); Chaly (2025) |
| Ético | Agência moral, imperativo categórico e decisão algorítmica | Ulgen (2017); Manna e Nath (2021); Metlushko (2026) |

A tabela permite ler a sociologia do subcampo. O eixo epistemológico é o mais
antigo e o mais maduro — Stark e Choi (1996) e Vishwanath (2005) mostram que
a conversa entre Kant e a ciência da visão precede em décadas o boom do deep
learning, e Swanson (2016) é o artigo-ponte que a reacendeu, com o maior
impacto citacional do bloco filosófico do corpus. O eixo
transcendental-técnico é o mais jovem e o mais heterogêneo: reúne desde a
modelagem matemática séria (BEIM GRABEN, 2024) até programas ainda
especulativos (ZHANG, 2024, 2025), passando por trabalho de formação (FRISCH
et al., 2024) — sinal de campo em consolidação, onde os padrões de qualidade
ainda se negociam. O eixo crítico-limitativo, concentrado em 2025–2026,
sugere um movimento pendular: depois da onda de aproximações entusiasmadas,
a literatura passa a demarcar o que a analogia **não** cobre — Noller (2026)
e Shetty (2025) são, no fundo, a seção 6 deste relatório escrita por
kantianos de ofício.

O eixo **ético**, embora tangencial ao problema da percepção, confirma o
diagnóstico estrutural das outras linhas. Ulgen (2017) examina o que a ética
kantiana pode guiar na conduta de sistemas autônomos e híbridos
humano-máquina; Manna e Nath (2021) concluem que a agência moral kantiana
exige uma compreensão moral consciente que sistemas de IA não possuem;
Metlushko (2026) aplica o teste da fórmula da humanidade à decisão
algorítmica — tratar alguém como representante estatístico de uma categoria
demográfica é violação paradigmática. Note-se o padrão: os três chegam, pela
ética, ao mesmo ponto a que Noller (2026) e Shetty (2025) chegam pela
epistemologia — o que a IA não tem é a **espontaneidade unificada** do sujeito
kantiano, seja como apercepção (lado teórico), seja como autonomia (lado
prático). Chaly (2025) fecha o circuito discutindo o idealismo kantiano e a
dupla causalidade (natureza e liberdade) diante da IA.

No eixo transcendental-técnico, vale distinguir dois trabalhos de Zhang: o
working paper de 2024 propõe considerações ontológicas e epistemológicas
gerais sobre perspectivas kantianas a priori em IA (ZHANG, 2024), e o artigo
de 2025 localiza a discussão no fenômeno do *insight* (ZHANG, 2025). São
propostas programáticas, de baixo impacto citacional até aqui (ver seção 8),
mas indicam a direção do subcampo: sair do paralelo ilustrativo e perguntar,
em detalhe técnico, **onde** ficaria cada peça do aparato kantiano.

## 5. Predictive processing e visão ativa

Se há um programa científico contemporâneo que assume explicitamente a herança
Kant–Helmholtz, é o do **processamento preditivo** (*predictive processing*,
PP): a tese de que o cérebro é uma máquina de predição hierárquica, que gera
modelos do mundo de cima para baixo e usa o sinal sensorial apenas como erro de
predição a corrigir — percepção como inferência (CLARK, 2013), unificada no
princípio da energia livre (FRISTON, 2010).

A conexão kantiana do PP é hoje uma discussão filosófica por direito próprio, e
o corpus a capta em profundidade incomum. Swanson (2016) abriu a rubrica com
"The predictive processing paradigm has roots in Kant", mapeando as
correspondências: modelos generativos como formas da síntese, hierarquia
preditiva como hierarquia das faculdades. Beni (2018) corrige a genealogia:
as raízes kantianas do PP passam por Helmholtz — o PP brota das teorias
estatísticas da percepção como inferência inconsciente, não de Kant
diretamente. Zahavi (2018) complica de vez o quadro: se o PP leva a sério a
tese de que só temos acesso inferencial ao mundo externo, aproxima-se menos de
Kant que do neokantismo e do idealismo transcendental — com todos os ônus.
Hohwy (2025) morde a bala: o PP está comprometido com uma forma de idealismo
transcendental, e ele constrói a metafísica correspondente. Schlicht (2026)
chama esse movimento de "flerte" do PP com o idealismo transcendental e o
examina criticamente; Britten-Neish (2024) discute se a inferência ativa salva
o PP do "neoidealismo" — o risco de trancar o percebedor dentro do próprio
modelo; Christias (2024) propõe uma solução "naturalista-transcendental" para
o problema do acesso direto; e Laiho e Arstila (2026) fazem o trabalho
filológico: revisitam os elementos kantianos do PP e mostram que Kant fala,
sim, de inferência e antecipação — distinguindo o uso reprodutivo do uso
**antecipatório** da imaginação. Gouveia e Morujão (2026) estendem a discussão
à consciência: pode o "cérebro kantiano" — Bayes, codificação preditiva,
inferência ativa — explicá-la?

O mecanismo do PP merece um parágrafo técnico, porque é nele que mora o
kantismo. Num modelo generativo hierárquico, cada nível prediz a atividade do
nível inferior; o que sobe não é o sinal, é o **erro de predição** — a
diferença entre o previsto e o recebido —, ponderado pela **precisão**
estimada de cada fonte (quanto confiar no erro vs. no prior). Perceber, nesse
quadro, é convergir para a hipótese que minimiza erro em todos os níveis; o
princípio da energia livre generaliza o esquema para a ação: o organismo
também pode minimizar erro *mudando o mundo* para que ele confirme suas
predições (FRISTON, 2010; CLARK, 2013). A estrutura é kantiana em dois
pontos exatos: o estímulo jamais é lido "nu", mas sempre contra uma
expectativa estruturada (não há intuição sem conceito operando); e a
ponderação por precisão é uma teoria mecânica da *Spielraum* entre
receptividade e espontaneidade — quanto o dado pode contra o esperado. Laiho
e Arstila (2026) mostram que até o vocabulário antecipa: Kant distingue o uso
reprodutivo do uso antecipatório da imaginação, e é o segundo que o PP
implementa.

O segundo braço da seção é a **visão ativa**, e ele importa porque realiza o
outro lado da tese construtivista: se a percepção é construção, o percebedor
não pode ser espectador. Bajcsy, Aloimonos e Tsotsos (2018) revisitam o
programa da percepção ativa — um agente ativo escolhe *por que*, *o que* e
*como* sentir; a percepção é controle inteligente da aquisição de dados, não
recepção. A robótica desenvolvimental dá ao programa uma leitura
explicitamente construtivista, de linhagem piagetiana (o Kant naturalizado da
psicologia): Tani (1998) investiga a relação entre predição *top-down* e
percepção *bottom-up* num robô móvel, interpretando o "eu" a partir de
sistemas dinâmicos; Nishimoto e Tani (2009) mostram estruturas hierárquicas de
ação emergindo em aprendizagem neuro-robótica, em correspondência direta com a
visão construtivista de Piaget; Chaput (2004) constrói uma arquitetura
cognitiva construtivista para robôs autônomos robustos; Lewis e Luger (2000)
modelam a percepção robótica como interpretação ativa; Zaky et al. (2020)
aplicam percepção ativa à manipulação robótica com aprendizagem profunda.
Até na engenharia aplicada o vocabulário é o mesmo: Kuvich (2004) e Naillon
(1994) defendem que percepção não se separa de reconhecimento e decisão — em
análise de cenas por satélite ou navegação de robôs em campo. Schlemmer e
Vincze (2012) dão à área sua autorreflexão filosófica, formulando uma posição
de "racionalismo *cum* construtivismo" para a visão cognitiva situada — e
Schlemmer (2009), no trabalho que explicitamente convoca Kant, usa uma
ontologia para reunir o que Gibson e a tradição reconstrutivista separaram.

Um caso do corpus fecha o circuito entre os dois braços com quatro décadas de
antecedência: o *scanpath* de Stark e Choi (1996). A sequência de fixações
com que o olho varre uma cena não é aleatória nem ditada pelo estímulo — é um
percurso característico do observador, repetido no reconhecimento, que os
autores interpretam explicitamente em chave kantiana: a distinção entre
sensação (o que chega em cada fixação) e percepção (o que o percurso
constrói) torna-se operacional, e o *scanpath* funciona como a hipótese
perceptiva executada motoramente — "metafísica experimental", no título
provocador. É o PP avant la lettre (a predição guiando a amostragem) e a
visão ativa em escala ocular (a ação constituindo o percepto), unidos num
único paradigma experimental.

A convergência dos dois braços é o achado da seção: PP e visão ativa são o
mesmo kantismo naturalizado visto de dentro (a hierarquia generativa) e de
fora (o agente que age para perceber). O elo técnico entre ambos — a
**inferência ativa** — é exatamente o ponto em que Britten-Neish (2024) vê a
resposta ao neoidealismo: o agente que testa suas predições agindo não está
trancado no próprio modelo.

## 6. Onde a analogia se rompe

Uma analogia que não quebra em lugar nenhum não informa nada. A literatura do
corpus, complementada pelas fontes primárias das posições críticas, localiza
quatro pontos de ruptura.

**Primeira ruptura: Gibson e a recusa da construção.** A tradição ecológica
nega a premissa comum a Kant, Helmholtz, Marr e ao deep learning: a de que o
estímulo é pobre e precisa ser enriquecido por inferência ou representação.
Para Gibson (1979), o arranjo óptico ambiente, amostrado por um observador em
movimento, é rico o bastante para especificar diretamente as *affordances* do
ambiente — percepção é captação direta de informação, não construção. Warren
(2012) formula o confronto com precisão: Marr dá o "salto conceitual" de
supor que ver é formar uma descrição interna; Gibson pergunta se esse é o
problema certo a resolver. Se Gibson tem razão, o isomorfismo da Tabela 1
descreve dois sistemas que compartilham o mesmo erro — e a pobreza do estímulo,
que Kant e as CNNs resolvem com estrutura a priori, é artefato de laboratório
(imagens estáticas, tarefas passivas), não condição da percepção. A réplica
construtivista está na própria seção 5: a visão ativa incorpora o movimento do
observador *sem* abrir mão da representação — Schlemmer (2009) tenta
explicitamente a síntese das duas tradições.

A posição gibsoniana precisa ser tomada na sua força máxima para que a
ruptura apareça inteira. O conceito central é o de ***affordance***: o que o
ambiente *oferece* ao animal — superfícies que sustentam, aberturas que dão
passagem, objetos que se agarram — é propriedade relacional real do par
animal-ambiente, e é isso, não formas nem cores, o que a percepção capta
(GIBSON, 1979). Três consequências anti-kantianas seguem: a informação está
no arranjo óptico, não na cabeça (contra a síntese); a unidade de análise é o
sistema animal-ambiente, não o sujeito diante do dado (contra a própria
moldura sujeito/objeto); e o movimento não é acessório, é constitutivo — o
invariante só se revela na transformação do fluxo óptico. Note-se, porém, o
que a réplica construtivista pode conceder sem se render: que o estímulo do
observador *em movimento* é mais rico que o da retina estática. O que ela não
pode conceder é que riqueza dispense estrutura — captar invariantes no fluxo
exige um sistema sintonizado para *aqueles* invariantes, e a sintonia é o a
priori de volta, agora com roupagem ecológica. O debate Marr–Gibson (WARREN,
2012) é, nesse sentido, menos uma refutação que uma disputa sobre **onde**
mora a estrutura: no processamento ou na relação.

**Segunda ruptura: Dreyfus e o fundo não formalizável.** A crítica
fenomenológica de Dreyfus (1992) atinge a analogia por outro flanco: o que a
inteligência humana tem e o computador não tem não é um conjunto melhor de
regras a priori, mas um **fundo** de familiaridade corporal e situada que não é
regra nem representação — saber *como*, não saber *que*. Contra a leitura de
Kant que o aproxima de um sistema de regras, Dreyfus lembra que o próprio
esquematismo é o reconhecimento de que aplicar regra exige algo que não é
regra (sob pena de regresso infinito de regras para aplicar regras). A
literatura do corpus toca o tema pela banda fenomenológica: Zahavi (2018)
escreve desde Husserl, e Christias (2024) enfrenta o problema do acesso — mas
o corpus não contém nenhuma obra dedicada a Dreyfus, lacuna registrada no
Anexo A. O ponto sobrevive à lacuna: se o esquematismo é o que falta às
máquinas, ele é justamente a peça do aparato kantiano que a Tabela 1 mapeia
com menos segurança (linha 6 — representações intermediárias *aprendidas* são
esquemas só por cortesia).

**Terceira ruptura: a apercepção.** É o limite interno da analogia, visível
sem sair de Kant. A unidade transcendental da apercepção não é mais uma
estrutura entre estruturas: é a condição de que as sínteses sejam *de alguém*
— que as representações pertençam a uma consciência una que pode dizer "eu
penso". Nada na arquitetura de uma rede profunda desempenha esse papel; a
integração de informação num vetor de características não é atribuição a um
sujeito. Noller (2026) pergunta se os "conceitos" da IA não são conceitos
inautênticos, erros de categoria — e ancora a resposta na espontaneidade que a
apercepção pressupõe; Shetty (2025) marca que a IA opera inteiramente no
domínio fenomênico já estruturado por categorias *humanas* (dados, rótulos,
funções de perda): o sistema não constitui seu mundo, herda o nosso. Manna e
Nath (2021) chegam ao mesmo limite pela agência moral. Em termos da Tabela 1:
as linhas 1–8 têm análogos; a linha 9 não tem — e as linhas 1–8 só funcionam
no sistema kantiano *porque* a linha 9 as unifica.

**Quarta ruptura: a normatividade do juízo.** Um classificador erra
estatisticamente; um sujeito kantiano julga sob normas de que é responsável.
Schubbach (2021) mostra que mesmo a justificação dos resultados de deep
learning precisa ser de novo tipo — e Hacker (2016), pelo lado de Marr,
argumenta que descrever mapeamentos de representações não é ainda descrever o
*ver* de alguém. O deslizamento entre "o sistema detecta X" e "o sistema julga
que X" é o que a quarta ruptura proíbe.

O balanço da seção não é a demolição da analogia, mas sua delimitação: o
paralelo Kant–visão computacional é **estrutural nas sínteses e nos a priori**
(onde é fecundo e tecnicamente tradutível — seção 7) e **falha na
subjetividade** (apercepção, fundo prático, normatividade), exatamente onde a
filosofia crítica deixa de ser teoria do processamento e passa a ser teoria do
sujeito.

## 7. O *a priori* como firmware

A tradução técnica contemporânea do a priori kantiano tem nome na literatura
de aprendizagem de máquina: ***inductive bias*** — o conjunto de pressupostos
que um modelo traz *antes* dos dados e que determina o que ele pode aprender
deles. A metáfora que dá título à seção é informática: o a priori não é
*hardware* (fixo por natureza física) nem *software* (instalável por
experiência), mas **firmware** — estrutura gravada antes do uso, que condiciona
todo uso, e que, no entanto, tem história e pode ser regravada (pela evolução,
no caso biológico; pelo projetista, no artificial).

**Tabela 3 — O a priori como firmware: correspondências técnicas**

| Elemento kantiano | Firmware da rede | Evidência no corpus |
|---|---|---|
| Espaço como forma da intuição externa | Equivariância translacional da convolução; partilha de pesos | Bouchacourt et al. (2021); Habte et al. (2022) |
| Tempo como forma da intuição interna | Equivariância temporal; recorrência; janelas causais | Finzi (2023); Tani (1998) |
| Categorias (quantidade, qualidade, relação, modalidade) | Repertório arquitetural de composição: hierarquia, localidade, simetrias | Benton et al. (2020); Celledoni et al. (2021) |
| Esquematismo | *Feature maps* intermediários que traduzem estatística de pixels em estrutura de classe | Razzaghi, Abbasi e Bayat (2020); Cheng et al. (2018) |
| Antecipações da percepção | Priors do modelo generativo; predição hierárquica | Clark (2013); Friston (2010) |
| Limite do fenômeno | Fronteiras de generalização: o que o viés não cobre, o modelo não vê | Bachmann et al. (2023); Gruver (2025) |

Antes das evidências, o argumento de necessidade — porque ele é o teorema que
dá lastro à metáfora. Aprender é generalizar: concluir, de casos finitos, o
comportamento em casos não vistos. Mas qualquer conjunto finito de exemplos é
compatível com infinitas funções que divergem fora dele; sem restrição prévia
sobre o espaço de hipóteses, todas as extrapolações são equivalentes e
nenhuma aprendizagem é possível. Todo aprendiz que generaliza carrega,
portanto, um viés indutivo — a questão nunca é *se*, é *qual* e *quão*
adequado ao domínio (FINZI, 2023; GRUVER, 2025). Este é, em miniatura
técnica, o argumento transcendental kantiano: a experiência (aqui, a
generalização) é um fato; suas condições de possibilidade (aqui, o viés) são,
logo, necessárias. A pergunta kantiana "que formas tornam a experiência
possível?" vira a pergunta de engenharia "que vieses tornam a generalização
possível *neste* mundo?" — e a resposta da visão computacional (localidade,
hierarquia, equivariâncias) é uma hipótese empírica sobre a estrutura do
mundo visual.

A pesquisa técnica do corpus sustenta três teses sobre esse firmware.

**Primeira: o firmware é real e mensurável.** A linha de pesquisa sobre
equivariâncias trata as invariâncias esperadas do mundo (translação, rotação)
como pressuposto de projeto: Celledoni et al. (2021) constroem redes
equivariantes para problemas inversos de imagem, codificando na arquitetura o
conhecimento prévio sobre as simetrias do problema; Habte et al. (2022)
inventariam a equivariância/invariância dos filtros convolucionais; Finzi
(2023) desenvolve o quadro matemático para incorporar vieses indutivos como
distribuições a priori sobre funções. A hierarquia é o outro pressuposto
central: as CNNs assumem que o visual se compõe de partes locais em níveis —
e a literatura mostra o pressuposto funcionando, do rastreamento visual com
características hierárquicas (MA et al., 2015) à segmentação de fissuras
(LIU et al., 2019), da classificação hiperespectral (CHENG et al., 2018) à
detecção eficiente de objetos (LEE et al., 2016) e à agregação hierárquica de
vistas para características 3D (HAN et al., 2019). Bilal et al. (2017)
fornecem o resultado mais kantiano do lote: redes treinadas em grandes
taxonomias *aprendem* estrutura hierárquica de classes — os erros do modelo
respeitam a árvore semântica —, e arquiteturas que explicitam essa hierarquia
(YAN et al., 2015; ROY; PANDA; ROY, 2020) melhoram o desempenho. O firmware
hierárquico encontra eco no mundo.

**Segunda: o firmware pode migrar para os dados — até certo ponto.** Se as
formas podem ser aprendidas, o a priori kantiano vira a posteriori de espécie
ou de pré-treinamento — a posição helmholtziana-empirista redescoberta.
Benton et al. (2020) mostram que invariâncias podem ser *aprendidas dos dados*
de treinamento, parametrizando as simetrias e otimizando-as junto com os
pesos; Bouchacourt et al. (2021) verificam em dados naturais que a invariância
emerge das variações presentes nos dados quase tanto quanto do viés
arquitetural; Bachmann et al. (2023) levam a tese ao limite — MLPs sem viés
convolucional, em escala suficiente de computação, compensam a ausência do
prior; e Gruver (2025) examina o que resta do viés indutivo na era do
pré-treinamento em larga escala. A leitura kantiana desse debate: a
*localização* do a priori (arquitetura vs. dados vs. escala) é empírica e
está em disputa; a *necessidade* de algum a priori não está — mesmo o
"aprender invariâncias" de Benton et al. exige o espaço parametrizado de
invariâncias possíveis, dado de antemão.

**Terceira: os exemplos adversariais são bugs de firmware.** Perturbações
imperceptíveis a humanos mudam a classificação de uma rede com confiança
(SZEGEDY et al., 2014); a explicação clássica as atribui à linearidade
excessiva dos modelos em altas dimensões (GOODFELLOW; SHLENS; SZEGEDY, 2015).
Na gramática deste relatório: o mundo fenomênico da rede — o espaço de
representação estruturado pelo seu firmware — tem geometria diferente do
nosso; os exemplos adversariais habitam as dobras onde as duas estruturações
divergem. Eles são a demonstração empírica da tese kantiana de que o sistema
não vê "o mundo", vê o que suas formas constituem — e de que formas diferentes
constituem fenômenos diferentes a partir do mesmo estímulo. O "bug" não é
acidente de implementação: é a assinatura do a priori errado (ou, mais
exatamente, de um a priori *outro*).

## 8. Panorama bibliométrico

A figura `assets/fig3_panorama_bibliometrico.svg` resume a estrutura do corpus;
os números derivam de `data/corpus_consolidado.csv` após a correção estrutural
documentada no Anexo A.

O corpus tem **76 obras** em nove campanhas de busca, cobrindo 1891–2026. A
distribuição temporal é fortemente contemporânea — 52 obras (68%) de 2010 em
diante, 32 delas da década de 2020 —, com uma espinha histórica intencional:
Hyslop (1891) na recepção crítica de Helmholtz, a tradução de Helmholtz (1948),
os textos de Marr e sua recepção (1982–2012). Uma ressalva de dado: uma obra
de 2020 (ZAKY et al., 2020) consta na coluna de ano como "2003" por defeito de
extração (o prefixo do identificador arXiv foi tomado por ano); o painel A da
figura reflete a coluna como está.

A distribuição de citações segue a lei de potência típica de corpora
bibliográficos: mediana de 26 citações, quartil superior em 118, e cauda longa
dominada por *Vision* de Marr (31.047 citações na edição de 2010) e pela
teoria da estereopsia de Marr e Poggio (3.327). A assimetria é informativa: o
corpus combina um núcleo canônico consolidado (Marr, Helmholtz, percepção
ativa — as medianas mais altas por campanha estão em `r5a_marr` e
`r6a_helmholtz`) com uma frente filosófica jovem — as campanhas kantianas
(`r1`, `r2a`, `r2b`) e a de *predictive processing* (`r3a`) concentram obras
de 2018–2026 com citação ainda baixa, o que é esperado para um subcampo em
formação e recomenda cautela: nessas seções, o relatório descreve um debate em
andamento, não um consenso estabelecido.

Lido como instrumento — e não apenas como inventário —, o corpus tem um
desenho que vale explicitar. As nove campanhas triangulam o objeto por três
ângulos independentes: o filosófico (`r1`, `r2a`, `r2b`, `r3a`) pergunta o
que a filosofia diz da técnica; o histórico (`r5a`, `r6a`) reconstrói a
linhagem pela qual a tese construtivista chegou à engenharia; o técnico
(`r3b`, `r4a`, `r7a`) verifica se a engenharia, lida de dentro, exibe a
estrutura que a filosofia afirma. A força do argumento do relatório está
menos em qualquer obra individual do que nessa convergência: quando a
mediana de citações de `r5a_marr` (canônico consolidado) e os preprints de
2026 de `r3a_predictive` (fronteira em formação) apontam a mesma estrutura
— predição hierárquica estruturando percepção —, a tese ganha o tipo de
robustez que uma campanha só não daria. O custo do desenho também é
visível: triangulação larga significa profundidade rasa em cada vértice, e
é por isso que as seções analíticas apoiam as afirmações fortes sempre no
cruzamento de campanhas com as fontes primárias canônicas.

A cobertura por campanha é equilibrada (6 a 10 obras por tema), com as lacunas
já sinalizadas: a seção 6 depende de fontes primárias externas ao corpus
(Gibson, Dreyfus) e os exemplos adversariais da seção 7 idem (Szegedy,
Goodfellow) — oito complementos no total, listados como tais nas referências.

## 9. Síntese e avaliação final

O percurso do relatório sustenta quatro conclusões.

**1. O paralelo é estrutural e historicamente real.** Não se trata de
analogia decorativa: há uma linhagem documentável — Kant → Helmholtz → Marr →
deep learning — em que a tese do conhecimento como construção ativa foi
sucessivamente naturalizada (inferência inconsciente), formalizada (três
níveis, representações progressivas) e implementada (hierarquias
convolucionais com vieses indutivos). Cada elo da cadeia está representado no
corpus por fonte primária e por recepção crítica.

**2. A tradução técnica do a priori é o ponto fecundo.** O conceito de
*inductive bias* dá ao a priori kantiano um correlato operacional preciso —
estrutura anterior aos dados que condiciona o que se pode aprender deles — e
transforma questões transcendentais em questões experimentais: quanto do viés
pode migrar para os dados (BENTON et al., 2020; BACHMANN et al., 2023), o que
acontece nas fronteiras do viés (exemplos adversariais como "bugs de
firmware"), onde a hierarquia pressuposta encontra a estrutura do mundo
(BILAL et al., 2017). É aqui que o encontro Kant–visão computacional produz
pesquisa, e não apenas comentário.

**3. A analogia tem limite interno preciso.** Ela vale para o aparato das
sínteses e falha na subjetividade: apercepção, esquematismo como fundo
prático, normatividade do juízo (seção 6). A literatura crítica recente
(NOLLER, 2026; SHETTY, 2025) converge com a ética kantiana da IA (MANNA;
NATH, 2021) nesse diagnóstico — o que indica que o limite não é acidente de
formulação, mas fronteira real entre teoria do processamento e teoria do
sujeito.

**4. O debate vivo está no processamento preditivo.** A discussão sobre PP e
idealismo transcendental (ZAHAVI, 2018; HOHWY, 2025; SCHLICHT, 2026; LAIHO;
ARSTILA, 2026) é hoje o lugar onde a herança kantiana da ciência da percepção
é disputada com mais rigor — e a inferência ativa, ponto de convergência entre
PP e visão ativa (seção 5), é a aposta em circulação para conjurar o risco
idealista. Para a pesquisa futura, é a frente a acompanhar.

Cabe, por honestidade metodológica, registrar os limites deste relatório.
Primeiro, o corpus é de triagem (snippets do Google Scholar): a
profundidade com que cada obra é discutida aqui é limitada pelo que registro
bibliográfico e conhecimento estabelecido sustentam, e leituras integrais
poderão corrigir ênfases — as fichas de verificação estão no Anexo A.
Segundo, a frente filosófica do corpus é jovem (seção 8): parte do que este
relatório apresenta como "a literatura" é, na verdade, a primeira geração de
um debate, e o quadro pode mudar rápido. Terceiro, há lacunas deliberadas de
escopo: a discussão ética foi apenas tangenciada (Tabela 2), e a vertente
fenomenológica pós-Dreyfus (corporeidade, enativismo) ficou fora do corpus —
ambas são extensões naturais para uma segunda campanha de buscas.

Avaliação final: a metáfora do firmware — o a priori como estrutura gravada
antes do uso, condicionante e contudo historicamente regravável — sintetiza o
que o encontro entre Kant e a visão computacional tem de melhor a oferecer aos
dois lados. À filosofia, oferece um laboratório onde teses transcendentais
ganham consequências testáveis; à engenharia, um vocabulário para o que ela já
faz às cegas toda vez que escolhe uma arquitetura: decidir, antes de qualquer
dado, o que poderá contar como mundo.

## Anexo A — auditoria de qualidade do corpus

A auditoria completa está em [`data/AUDITORIA-CORPUS.md`](data/AUDITORIA-CORPUS.md)
(2026-09-04), que documenta: a correção de duas linhas com aspas não fechadas
no CSV (defeito que fazia parsers estritos lerem 73 registros em vez de 76 e
ocultava três obras, entre elas *Vision* de Marr); o confronto com a auditoria
automática anterior (`data/auditoria_qualidade.json`, mantida como artefato
histórico — acerta a contagem e o máximo de citações, mas seus escores de
consistência não detectavam o defeito de aspas, e seus "outliers" de ano e
citação são falsos positivos); e o perfil estatístico usado na seção 8.

Notas de verificação de fontes deste relatório:

- **Abstracts do corpus são snippets truncados** do Google Scholar (~190
  caracteres): serviram para triagem temática, nunca como fonte de conteúdo.
  Toda afirmação atribuída a uma obra foi limitada ao que o registro
  bibliográfico e o conhecimento estabelecido da obra sustentam.
- **Obras do corpus não citadas** neste relatório (constam do CSV e
  permanecem disponíveis para trabalho futuro): "Inductive Biases in Neural
  Networks" — material autopublicado, sem dados bibliográficos confiáveis,
  excluído por critério de fonte; "The pursuit of cyberism: ontology,
  epistemology, and ethics in the digital age" — tangencial ao escopo; "The
  engineering of vision from constructivism to virtual reality" — tese
  histórica de triagem.
- **Anos resolvidos na verificação**: Zhang (SSRN) = 2024; Zaky et al. = 2020
  (a coluna `year` do CSV traz "2003" por defeito de extração do identificador
  arXiv — documentado na auditoria).
- **Complementos externos ao corpus** (8 obras, todas canônicas, marcadas com
  asterisco nas referências): Kant (2012); Gibson (1979); Dreyfus (1992);
  Clark (2013); Friston (2010); Szegedy et al. (2014); Goodfellow, Shlens e
  Szegedy (2015); LeCun, Bengio e Hinton (2015). Foram adicionados porque as
  seções 5, 6 e 7 exigem as posições primárias que o corpus referencia mas
  não contém.

## Referências

Conforme ABNT NBR 6023:2025. Obras marcadas com * são complementos externos ao
corpus (ver Anexo A).

BACHMANN, G.; ANAGNOSTIDIS, S.; HOFMANN, T. Scaling MLPs: a tale of inductive bias. In: ADVANCES IN NEURAL INFORMATION PROCESSING SYSTEMS, 36., 2023. *Proceedings* […]. [S. l.]: NeurIPS, 2023. Disponível em: https://proceedings.neurips.cc/paper_files/paper/2023/hash/bf2a5ce85aea9ff40d9bf8b2c2561cae-Abstract-Conference.html. Acesso em: 4 set. 2026.

BAJCSY, R.; ALOIMONOS, Y.; TSOTSOS, J. K. Revisiting active perception. *Autonomous Robots*, v. 42, p. 177–196, 2018. Disponível em: https://link.springer.com/article/10.1007/s10514-017-9615-3. Acesso em: 4 set. 2026.

BARLOW, H. Conditions for versatile learning, Helmholtz's unconscious inference, and the task of perception. *Vision Research*, v. 30, n. 11, p. 1561–1571, 1990. Disponível em: https://www.sciencedirect.com/science/article/pii/004269899090144A. Acesso em: 4 set. 2026.

BEIM GRABEN, P. A neural network account of Kant's philosophical aesthetics. *Mind and Matter*, v. 22, n. 2, 2024. Disponível em: https://www.ingentaconnect.com/content/imp/mm/2024/00000022/00000002/art00005. Acesso em: 4 set. 2026.

BENI, M. D. Commentary: The predictive processing paradigm has roots in Kant. *Frontiers in Systems Neuroscience*, v. 11, art. 98, 2018. Disponível em: https://www.frontiersin.org/journals/systems-neuroscience/articles/10.3389/fnsys.2017.00098/full. Acesso em: 4 set. 2026.

BENTON, G. *et al.* Learning invariances in neural networks from training data. In: ADVANCES IN NEURAL INFORMATION PROCESSING SYSTEMS, 33., 2020. *Proceedings* […]. [S. l.]: NeurIPS, 2020. Disponível em: https://proceedings.neurips.cc/paper_files/paper/2020/hash/cc8090c4d2791cdd9cd2cb3c24296190-Abstract.html. Acesso em: 4 set. 2026.

BILAL, A. *et al.* Do convolutional neural networks learn class hierarchy? *IEEE Transactions on Visualization and Computer Graphics*, v. 24, n. 1, p. 152–162, 2017. Disponível em: https://ieeexplore.ieee.org/abstract/document/8017618/. Acesso em: 4 set. 2026.

BOUCHACOURT, D.; IBRAHIM, M.; MORCOS, A. Grounding inductive biases in natural images: invariance stems from variations in data. In: ADVANCES IN NEURAL INFORMATION PROCESSING SYSTEMS, 34., 2021. *Proceedings* […]. [S. l.]: NeurIPS, 2021. Disponível em: https://proceedings.neurips.cc/paper_files/paper/2021/hash/a2fe8c05877ec786290dd1450c3385cd-Abstract.html. Acesso em: 4 set. 2026.

BRITTEN-NEISH, G. Neuroidealism, perceptual acquaintance and the Kantian roots of predictive processing. *Synthese*, v. 204, 2024. Disponível em: https://link.springer.com/article/10.1007/s11229-024-04778-7. Acesso em: 4 set. 2026.

CELLEDONI, E. *et al.* Equivariant neural networks for inverse problems. *Inverse Problems*, v. 37, n. 8, 2021. Disponível em: https://iopscience.iop.org/article/10.1088/1361-6420/ac104f/meta. Acesso em: 4 set. 2026.

CHALY, V. Kantian idealism and AI. In: *Dialectic of Digital Enlightenment*. Cham: Springer, 2025. Disponível em: https://link.springer.com/chapter/10.1007/978-3-031-95469-6_2. Acesso em: 4 set. 2026.

CHAPUT, H. H. *The constructivist learning architecture*: a model of cognitive development for robust autonomous robots. 2004. Tese (Doutorado) — University of Texas at Austin, Austin, 2004. Disponível em: https://search.proquest.com/openview/c1d825abff9a1b4c1ac90d90c99c5d46/1. Acesso em: 4 set. 2026.

CHENG, G. *et al.* Exploring hierarchical convolutional features for hyperspectral image classification. *IEEE Transactions on Geoscience and Remote Sensing*, v. 56, n. 11, p. 6712–6722, 2018. Disponível em: https://ieeexplore.ieee.org/abstract/document/8393448/. Acesso em: 4 set. 2026.

CHRISTIAS, D. The problem of direct access in predictive processing models: a transcendental naturalist solution. *Phenomenology and the Cognitive Sciences*, 2024. Disponível em: https://link.springer.com/article/10.1007/s11097-024-10024-9. Acesso em: 4 set. 2026.

\* CLARK, A. Whatever next? Predictive brains, situated agents, and the future of cognitive science. *Behavioral and Brain Sciences*, v. 36, n. 3, p. 181–204, 2013.

\* DREYFUS, H. L. *What computers still can't do*: a critique of artificial reason. Cambridge, MA: MIT Press, 1992.

FINZI, M. *Understanding and incorporating mathematical inductive biases in neural networks*. 2023. Tese (Doutorado) — New York University, New York, 2023. Disponível em: https://search.proquest.com/openview/de08a4c306042b324b8032a068bcd355/1. Acesso em: 4 set. 2026.

FRISCH, I. A. *et al.* *Kantian and neurosymbolic artificial intelligence*: applications and insights in computer vision. Utrecht: Utrecht University, 2024. Disponível em: https://studenttheses.uu.nl/server/api/core/bitstreams/d828f991-60a2-4537-971f-64468fdf4dda/content. Acesso em: 4 set. 2026.

\* FRISTON, K. The free-energy principle: a unified brain theory? *Nature Reviews Neuroscience*, v. 11, n. 2, p. 127–138, 2010.

\* GIBSON, J. J. *The ecological approach to visual perception*. Boston: Houghton Mifflin, 1979.

\* GOODFELLOW, I. J.; SHLENS, J.; SZEGEDY, C. Explaining and harnessing adversarial examples. In: INTERNATIONAL CONFERENCE ON LEARNING REPRESENTATIONS, 3., 2015, San Diego. *Proceedings* […]. [S. l.: s. n.], 2015. arXiv:1412.6572.

GOUVEIA, S. S.; MORUJÃO, C. Can the Kantian brain explain consciousness? In: *Kant's Legacy for the 21st Century*. [S. l.: s. n.], 2026. Disponível em: https://books.google.com/books?id=lBvcEQAAQBAJ. Acesso em: 4 set. 2026.

GRIGOROVA, Y. V.; KOMAROV, S. V. Analyzing the problem of artificial intelligence through the prism of Immanuel Kant's philosophy. *Vestnik Permskogo Universiteta. Filosofiia. Psikhologiia. Sotsiologiia*, 2024. Disponível em: https://journal-vniispk.ru/2078-7898. Acesso em: 4 set. 2026.

GRUVER, N. *Understanding inductive bias in the era of large-scale pretraining with scientific data*. 2025. Tese (Doutorado) — New York University, New York, 2025. Disponível em: https://search.proquest.com/openview/088c09bb4896512b80bb14b8402b8663/1. Acesso em: 4 set. 2026.

HABTE, S. B. *et al.* Convolution filter equivariance/invariance in convolutional neural networks: a survey. In: PAN AFRICAN CONFERENCE ON ARTIFICIAL INTELLIGENCE, 2022. *Proceedings* […]. Cham: Springer, 2022. Disponível em: https://link.springer.com/chapter/10.1007/978-3-031-31327-1_11. Acesso em: 4 set. 2026.

HACKER, P. M. S. Helmholtz's theory of perception: an investigation into its conceptual framework. *International Studies in the Philosophy of Science*, v. 9, n. 3, p. 199–214, 1995. Disponível em: https://www.tandfonline.com/doi/pdf/10.1080/02698599508573519. Acesso em: 4 set. 2026.

HACKER, P. M. S. Seeing, representing and describing: an examination of David Marr's computational theory of vision. In: *Investigating Psychology*. London: Routledge, 2016. Disponível em: https://api.taylorfrancis.com/content/chapters/edit/download?identifierName=doi&identifierValue=10.4324/9781315463933-8&type=chapterpdf. Acesso em: 4 set. 2026.

HAMLYN, D. W. Unconscious inference and judgment in perception. In: *Images, Perception, and Knowledge*. Dordrecht: Springer, 1977. Disponível em: https://link.springer.com/content/pdf/10.1007/978-94-010-1193-8.pdf. Acesso em: 4 set. 2026.

HAN, Z. *et al.* 3D2SeqViews: aggregating sequential views for 3D global feature learning by CNN with hierarchical attention aggregation. *IEEE Transactions on Image Processing*, v. 28, n. 8, p. 3986–3999, 2019. Disponível em: https://ieeexplore.ieee.org/abstract/document/8666059/. Acesso em: 4 set. 2026.

HELMHOLTZ, H. von. Concerning the perceptions in general, 1867. In: DENNIS, W. (ed.). *Readings in the history of psychology*. New York: Appleton-Century-Crofts, 1948. Disponível em: https://psycnet.apa.org/record/2006-10213-027. Acesso em: 4 set. 2026.

HOHWY, J. A metaphysics for predictive processing. *Synthese*, v. 205, 2025. Disponível em: https://link.springer.com/article/10.1007/s11229-025-05169-2. Acesso em: 4 set. 2026.

HUI, Y. *Kant machine*: critical philosophy after AI. [S. l.: s. n.], 2026. Disponível em: https://books.google.com/books?id=lHS1EQAAQBAJ. Acesso em: 4 set. 2026.

HYSLOP, J. H. Helmholtz's theory of space-perception. *Mind*, v. 16, n. 61, p. 54–79, 1891. Disponível em: https://www.jstor.org/stable/2247192. Acesso em: 4 set. 2026.

\* KANT, I. *Crítica da razão pura*. Tradução de Fernando Costa Mattos. Petrópolis: Vozes, 2012.

KALUŽA, J. Hume's empiricism versus Kant's critical philosophy (in the times of artificial intelligence and the attention economy). *Információs Társadalom*, v. 23, n. 3, 2023. Disponível em: https://inftars.infonia.hu/pub/PUB_2023-Oct-09-20-15-06_74487.pdf. Acesso em: 4 set. 2026.

KAVUKCUOGLU, K. *et al.* Learning convolutional feature hierarchies for visual recognition. In: ADVANCES IN NEURAL INFORMATION PROCESSING SYSTEMS, 23., 2010. *Proceedings* […]. [S. l.]: NeurIPS, 2010. Disponível em: https://proceedings.neurips.cc/paper_files/paper/2010/hash/a01610228fe998f515a72dd730294d87-Abstract.html. Acesso em: 4 set. 2026.

KIM, H. Tracing the origins of artificial intelligence: a Kantian response to McCarthy's call for philosophical help. In: *Kant and Artificial Intelligence*. Berlin: De Gruyter, 2022. Disponível em: https://library.oapen.org/bitstream/handle/20.500.12657/57223/9783110706611.pdf. Acesso em: 4 set. 2026.

KITCHER, P. Marr's computational theory of vision. *Philosophy of Science*, v. 55, n. 1, p. 1–24, 1988. Disponível em: https://www.cambridge.org/core/journals/philosophy-of-science/article/marrs-computational-theory-of-vision/F952298186F6AB1481677812248A891B. Acesso em: 4 set. 2026.

KUVICH, G. Active vision and image/video understanding systems built upon network-symbolic models for perception-based navigation of mobile robots in real-world environments. In: *Mobile Robots XVII*. Bellingham: SPIE, 2004. Disponível em: https://www.spiedigitallibrary.org/conference-proceedings-of-spie/5609/0000/10.1117/12.577747.short. Acesso em: 4 set. 2026.

LAIHO, H.; ARSTILA, V. More than roots: revisiting Kantian elements in predictive processing. *Synthese*, 2026. Disponível em: https://link.springer.com/article/10.1007/s11229-026-05522-z. Acesso em: 4 set. 2026.

\* LECUN, Y.; BENGIO, Y.; HINTON, G. Deep learning. *Nature*, v. 521, p. 436–444, 2015.

LEE, B. *et al.* Efficient object detection using convolutional neural network-based hierarchical feature modeling. *Signal, Image and Video Processing*, v. 10, p. 1503–1510, 2016. Disponível em: https://link.springer.com/article/10.1007/s11760-016-0962-x. Acesso em: 4 set. 2026.

LEWIS, J. A.; LUGER, G. F. A constructivist model of robot perception and performance. In: ANNUAL MEETING OF THE COGNITIVE SCIENCE SOCIETY, 22., 2000. *Proceedings* […]. [S. l.: s. n.], 2000. Disponível em: https://escholarship.org/content/qt01m268s7/qt01m268s7.pdf. Acesso em: 4 set. 2026.

LIU, Y. *et al.* DeepCrack: a deep hierarchical feature learning architecture for crack segmentation. *Neurocomputing*, v. 338, p. 139–153, 2019. Disponível em: https://www.sciencedirect.com/science/article/pii/S0925231219300566. Acesso em: 4 set. 2026.

MA, C. *et al.* Hierarchical convolutional features for visual tracking. In: IEEE INTERNATIONAL CONFERENCE ON COMPUTER VISION, 2015, Santiago. *Proceedings* […]. [S. l.]: IEEE, 2015. p. 3074–3082. Disponível em: https://www.cv-foundation.org/openaccess/content_iccv_2015/html/Ma_Hierarchical_Convolutional_Features_ICCV_2015_paper.html. Acesso em: 4 set. 2026.

MANNA, R.; NATH, R. Kantian moral agency and the ethics of artificial intelligence. *Problemos*, v. 100, p. 139–151, 2021. Disponível em: https://www.ceeol.com/search/article-detail?id=1005362. Acesso em: 4 set. 2026.

MARR, D. Visual information processing: the structure and creation of visual representations. In: ALBRECHT, D. G. (ed.). *Recognition of Pattern and Form*. Berlin: Springer, 1982. (Lecture Notes in Biomathematics, 44). Disponível em: https://link.springer.com/chapter/10.1007/978-3-642-93199-4_4. Acesso em: 4 set. 2026.

MARR, D. *Vision*: a computational investigation into the human representation and processing of visual information. Cambridge, MA: MIT Press, 2010. Disponível em: https://direct.mit.edu/books/monograph/3299/. Acesso em: 4 set. 2026.

MARR, D.; POGGIO, T. A computational theory of human stereo vision. In: VAINA, L. M. (org.). *From the Retina to the Neocortex*: selected papers of David Marr. Boston: Birkhäuser, 1991. Disponível em: https://link.springer.com/chapter/10.1007/978-1-4684-6775-8_11. Acesso em: 4 set. 2026.

METLUSHKO, S. *Categorical imperative and the ethics of artificial intelligence*: a Kantian approach to algorithmic moral decision-making. [S. l.]: PhilArchive, 2026. Disponível em: https://philarchive.org/archive/METCIA-4. Acesso em: 4 set. 2026.

NAILLON, M. Active vision in satellite scene analysis. In: CONFERENCE ON ARTIFICIAL INTELLIGENCE, ROBOTICS, AND AUTOMATION FOR SPACE, 1994. *Proceedings* […]. [S. l.]: NASA, 1994. Disponível em: https://ntrs.nasa.gov/citations/19950017318. Acesso em: 4 set. 2026.

NISHIMOTO, R.; TANI, J. Development of hierarchical structures for actions and motor imagery: a constructivist view from synthetic neuro-robotics study. *Psychological Research*, v. 73, p. 545–558, 2009. Disponível em: https://link.springer.com/article/10.1007/s00426-009-0236-0. Acesso em: 4 set. 2026.

NOLLER, J. A Kantian critique of artificial intelligence. *Danish Yearbook of Philosophy*, 2026. Disponível em: https://brill.com/view/journals/dyp/aop/article-10.1163-24689300-bja10090/article-10.1163-24689300-bja10090.xml. Acesso em: 4 set. 2026.

PUSHKARSKY, A. G. The importance of Kant's philosophy of mind for contemporary research in artificial intelligence. *RUDN Journal of Philosophy*, 2025. Disponível em: https://journals.rudn.ru/philosophy/article/view/44928. Acesso em: 4 set. 2026.

RAZZAGHI, P.; ABBASI, K.; BAYAT, P. Learning spatial hierarchies of high-level features in deep neural network. *Journal of Visual Communication and Image Representation*, v. 70, 2020. Disponível em: https://www.sciencedirect.com/science/article/pii/S1047320320300675. Acesso em: 4 set. 2026.

ROY, D.; PANDA, P.; ROY, K. Tree-CNN: a hierarchical deep convolutional neural network for incremental learning. *Neural Networks*, v. 121, p. 148–160, 2020. Disponível em: https://www.sciencedirect.com/science/article/pii/S0893608019302710. Acesso em: 4 set. 2026.

SCHLEMMER, M. J. *Getting past passive vision*: on the use of an ontology for situated perception in robots. 2009. Tese (Doutorado) — Technische Universität Wien, Viena, 2009. Disponível em: https://repositum.tuwien.at/handle/20.500.12708/14734. Acesso em: 4 set. 2026.

SCHLEMMER, M. J.; VINCZE, M. Theoretic foundations of situating cognitive vision in robots and cognitive systems. *Journal of Experimental & Theoretical Artificial Intelligence*, v. 24, n. 1, 2012. Disponível em: https://www.tandfonline.com/doi/abs/10.1080/13623079.2011.588252. Acesso em: 4 set. 2026.

SCHLICHT, T. Minds, brains, and deep learning: the development of cognitive science through the lens of Kant's approach to cognition. In: *Kant and Artificial Intelligence*. Berlin: De Gruyter, 2022. Disponível em: https://library.oapen.org/bitstream/handle/20.500.12657/57223/9783110706611.pdf. Acesso em: 4 set. 2026.

SCHLICHT, T. Predictive processing's flirt with transcendental idealism. *Noûs*, 2026. Disponível em: https://onlinelibrary.wiley.com/doi/abs/10.1111/nous.12552. Acesso em: 4 set. 2026.

SCHUBBACH, A. Judging machines: philosophical aspects of deep learning. *Synthese*, v. 198, p. 1807–1827, 2021. Disponível em: https://link.springer.com/article/10.1007/s11229-019-02167-z. Acesso em: 4 set. 2026.

SETH, A. K. From unconscious inference to the beholder's share: predictive perception and human experience. *European Review*, v. 27, n. 3, p. 378–410, 2019. Disponível em: https://www.cambridge.org/core/journals/european-review/article/8FFFE6794CE680A8334474CC2F93C0FE. Acesso em: 4 set. 2026.

SHAGRIR, O. Marr on computational-level theories. *Philosophy of Science*, v. 77, n. 4, p. 477–500, 2010. Disponível em: https://www.cambridge.org/core/journals/philosophy-of-science/article/21C3C13FB31C51228AAD3D086E273990. Acesso em: 4 set. 2026.

SHETTY, R. Conscious limits: a Kantian perspective on the limits of human understanding and artificial intelligence. *Discover Artificial Intelligence*, v. 5, 2025. Disponível em: https://link.springer.com/article/10.1007/s44163-025-00221-z. Acesso em: 4 set. 2026.

SLOMAN, A. Kantian philosophy of mathematics and young robots. In: INTERNATIONAL CONFERENCE ON INTELLIGENT COMPUTER MATHEMATICS, 2008. *Proceedings* […]. Berlin: Springer, 2008. Disponível em: https://link.springer.com/chapter/10.1007/978-3-540-85110-3_45. Acesso em: 4 set. 2026.

STARK, L. W.; CHOI, Y. S. Experimental metaphysics: the scanpath as an epistemological mechanism. *Advances in Psychology*, v. 116, p. 3–69, 1996. Disponível em: https://www.sciencedirect.com/science/article/pii/S0166411596800690. Acesso em: 4 set. 2026.

STEVENS, K. A. The vision of David Marr. *Perception*, v. 41, n. 9, p. 1061–1072, 2012. Disponível em: https://journals.sagepub.com/doi/abs/10.1068/p7297. Acesso em: 4 set. 2026.

SWANSON, L. R. The predictive processing paradigm has roots in Kant. *Frontiers in Systems Neuroscience*, v. 10, art. 79, 2016. Disponível em: https://www.frontiersin.org/journals/systems-neuroscience/articles/10.3389/fnsys.2016.00079/full. Acesso em: 4 set. 2026.

\* SZEGEDY, C. *et al.* Intriguing properties of neural networks. In: INTERNATIONAL CONFERENCE ON LEARNING REPRESENTATIONS, 2., 2014, Banff. *Proceedings* […]. [S. l.: s. n.], 2014. arXiv:1312.6199.

TANI, J. An interpretation of the 'self' from the dynamical systems perspective: a constructivist approach. *Journal of Consciousness Studies*, v. 5, n. 5-6, p. 516–542, 1998. Disponível em: https://www.ingentaconnect.com/content/imp/jcs/1998/00000005/F0020005/880. Acesso em: 4 set. 2026.

TURNER, R. S. Hermann von Helmholtz and the empiricist vision. *Journal of the History of the Behavioral Sciences*, v. 13, n. 1, p. 48–58, 1977. Disponível em: https://onlinelibrary.wiley.com/doi/abs/10.1002/1520-6696(197701)13:1%3C48::AID-JHBS2300130106%3E3.0.CO;2-L. Acesso em: 4 set. 2026.

ULGEN, O. Kantian ethics in the age of artificial intelligence and robotics. *Questions of International Law*, v. 43, p. 59–83, 2017. Disponível em: http://www.open-access.bcu.ac.uk/5579/. Acesso em: 4 set. 2026.

VISHWANATH, D. The epistemological status of vision and its implications for design. *Axiomathes*, v. 15, p. 399–486, 2005. Disponível em: https://link.springer.com/article/10.1007/s10516-004-5445-y. Acesso em: 4 set. 2026.

WARREN, W. H. Does this computational theory solve the right problem? Marr, Gibson, and the goal of vision. *Perception*, v. 41, n. 9, p. 1053–1060, 2012. Disponível em: https://journals.sagepub.com/doi/abs/10.1068/p7327. Acesso em: 4 set. 2026.

WESTHEIMER, G. Was Helmholtz a Bayesian? *Perception*, v. 37, n. 5, p. 642–650, 2008. Disponível em: https://journals.sagepub.com/doi/abs/10.1068/p5973. Acesso em: 4 set. 2026.

YAN, Z. *et al.* HD-CNN: hierarchical deep convolutional neural networks for large scale visual recognition. In: IEEE INTERNATIONAL CONFERENCE ON COMPUTER VISION, 2015, Santiago. *Proceedings* […]. [S. l.]: IEEE, 2015. p. 2740–2748. Disponível em: https://www.cv-foundation.org/openaccess/content_iccv_2015/html/Yan_HD-CNN_Hierarchical_Deep_ICCV_2015_paper.html. Acesso em: 4 set. 2026.

ZAHAVI, D. Brain, mind, world: predictive coding, neo-Kantianism, and transcendental idealism. *Husserl Studies*, v. 34, p. 47–61, 2018. Disponível em: https://link.springer.com/article/10.1007/s10743-017-9218-z. Acesso em: 4 set. 2026.

ZAKY, Y. *et al.* Active perception and representation for robotic manipulation. *arXiv preprint*, arXiv:2003.06734, 2020. Disponível em: https://arxiv.org/abs/2003.06734. Acesso em: 4 set. 2026.

ZHANG, Z. *Kant's a priori philosophical perspectives on artificial intelligence*: ontological and epistemological considerations. [S. l.]: SSRN, 2024. Disponível em: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4913519. Acesso em: 4 set. 2026.

ZHANG, Z. The intersection of insight phenomenon in artificial intelligence and Kant's transcendental philosophy. In: INTERNATIONAL CONFERENCE ON ARTIFICIAL INTELLIGENCE AND COMPUTER ENGINEERING, 2025. *Proceedings* […]. [S. l.]: IEEE, 2025. Disponível em: https://ieeexplore.ieee.org/abstract/document/11189595/. Acesso em: 4 set. 2026.
