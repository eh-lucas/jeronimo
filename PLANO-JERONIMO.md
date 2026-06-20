# Plano do Jerônimo — curso de latim para ler a Vulgata

> Documento de planejamento. Define a visão, o formato e o roteiro do projeto.
> **Nada do conteúdo das lições foi alterado ainda** — isto é só o plano acordado.

## 1. Visão

O **Jerônimo** é um curso de latim cujo objetivo é **ensinar a ler a Bíblia em latim**.
Não é uma simples tradução do D'Ooge: usamos o *Latin for Beginners* (B. L. D'Ooge, 1911,
domínio público) como **espinha teórica/gramatical**, mas reorientamos tudo para a leitura da
**Vulgata**:

- os exemplos do D'Ooge são trocados por **versículos reais da Vulgata**;
- o vocabulário é o **vocabulário bíblico** (por frequência na Vulgata);
- **leituras da Vulgata** são intercaladas entre e dentro das lições;
- os **exercícios** passam a ser orientados à leitura bíblica;
- adotamos a **pronúncia eclesiástica** (não a clássica/restaurada do D'Ooge).

## 2. Decisões fechadas (2026-06-20)

| Tema | Decisão |
|---|---|
| Edição da Vulgata | **Vulgata Clementina** (domínio público) |
| Sequência de leituras | **Orações → 1 João** → Evangelho de João → Gênesis → Salmos |
| Formato da Lectio | **Latim + vocabulário/notas** (leitura ativa antes da tradução) |
| Pronúncia | **Eclesiástica** |

## 3. Fonte da Vulgata

- **Edição:** Vulgata Clementina (1592 / ed. Hetzenauer 1914), domínio público.
- **Texto-base digital:** Clementine Text Project (M. Tweedale, vulsearch.sourceforge.net).
- **Forma utilizável (testada):** API getBible v2, JSON por versículo, UTF-8 —
  `https://api.getbible.net/v2/vulgate/{livro}/{capitulo}.json`
  (ex.: `.../vulgate/43/1.json` = João 1).
- **Referência impressa PD:** sacredbible.org (Hetzenauer 1914).
- **A fazer:** baixar um **snapshot local** para `fonte/vulgata/` para não depender da API no
  build, e gerar dele as listas de frequência de vocabulário.

> Nova Vulgata (oficial atual) e Stuttgart (crítica) foram descartadas por terem copyright,
> o que impediria redistribuir o texto no site/repo.

## 4. Pronúncia eclesiástica (Parte 0)

Reescrever a "Parte I — Pronúncia" para a norma eclesiástica (romana). Principais diferenças
em relação à clássica que o D'Ooge ensina:

- **c** antes de e, i, ae, oe → /tʃ/ ("tch"): *caelum* = "tchélum".
- **g** antes de e, i → /dʒ/ ("dj"): *Genesis* = "djénesis".
- **gn** → /ɲ/ ("nh"): *agnus* = "ánhus".
- **ae, oe** → /e/: *caelum*, *poena*.
- **v** → /v/ (e não /w/ da clássica).
- **ti** + vogal → /tsi/: *gratia* = "grátsia" (exceto após s, t, x).
- **h** mudo; **th, ph, ch** = /t/, /f/, /k/.
- **sc** antes de e, i → /ʃ/ ("ch"): *descendit* = "deschéndit".
- Acentuação e quantidade silábica seguem as mesmas regras do D'Ooge.

> As regras de adaptação EN→PT-BR do `REGRAS-TRADUCAO.md` continuam valendo; a seção de
> pronúncia precisa ser **atualizada de clássica para eclesiástica** lá também.

## 5. Formato da lição

Cada lição passa a ter quatro blocos fixos:

1. **Gramática** — o ponto teórico do D'Ooge, adaptado ao português (espinha do curso).
2. **Vocabulário** — palavras da leitura + alta frequência na Vulgata. Substantivos com
   genitivo e gênero; verbos com a forma de citação; cognatos portugueses.
3. **Lectio** — passagem real da Vulgata que **usa a gramática da lição**, no formato
   "Latim + vocabulário/notas":
   - texto latino corrido com referência (ex.: *Io 1,1*);
   - lista de vocabulário novo logo abaixo;
   - notas gramaticais ligando o texto ao ponto da lição;
   - tradução de apoio em PT-BR (recolhível / ao fim), para a leitura ser ativa.
4. **Exercícios** — orientados à Bíblia: traduzir versículos, identificar formas/casos,
   completar lacunas com palavras da Vulgata, ler em voz alta (pronúncia eclesiástica).

**Leituras intercaladas** ("marcos de leitura") aparecem entre blocos de lições: textos
completos assim que a gramática acumulada permite (ex.: *Pater Noster* após o básico de
imperativo/vocativo; prólogo de João; Gênesis 1).

## 6. Sequência de leituras (corpus graduado)

1. **Orações** (curtas, memorizáveis, altíssima reutilização): *Pater Noster*, *Ave Maria*,
   *Gloria Patri*, *Credo*, *Signum Crucis*.
2. **1 Ioannis** — sintaxe simples e vocabulário muito repetitivo (clássico primeiro leitor).
3. **Evangelium secundum Ioannem** — prólogo + narrativa.
4. **Genesis** — narrativa do Antigo Testamento.
5. **Psalmi** — poesia/liturgia (etapa mais avançada).

## 7. Estratégia de vocabulário

- Gerar do snapshot da Vulgata uma **lista de frequência de lemas**. Um núcleo pequeno de
  palavras cobre a maior parte do texto bíblico — priorizar esse núcleo.
- Cada lição introduz vocabulário que **(a)** aparece na sua Lectio e **(b)** é de alta
  frequência, para o aluno reencontrá-lo logo.
- Manter um **glossário cumulativo** do curso.

## 8. Mapeamento D'Ooge → Vulgata (a detalhar)

Para cada lição do D'Ooge, escolher 1+ versículo(s) da Vulgata que exemplifiquem o ponto:
- 1ª declinação (-a/-ae) → nomes como *terra, aqua, gloria, gratia, vita*.
- 3ª pessoa do verbo (-t/-nt) → *amat, portat, vocat...* em versículos narrativos.
- (tabela completa a construir lição a lição, conforme avançarmos.)

## 9. Componentes técnicos (implementar depois)

- **Shortcode `lectio`** — bloco padronizado de passagem (referência + texto + vocabulário +
  notas + tradução recolhível).
- **Snapshot da Vulgata** em `fonte/vulgata/` (JSON Clementina).
- **Dados de vocabulário** (`site/data/`) gerados por frequência.
- Possível shortcode de **glossário/tooltip** para palavras já vistas.
- A pronúncia eclesiástica pode ganhar **áudio** no futuro (fora de escopo inicial).

## 10. Roteiro (fases)

1. **[feito]** Tradução-base do D'Ooge (intro + Parte I + Lições I–II) no site Hugo+Hextra.
2. **[este plano]** Definir formato e fonte da Vulgata. ✅
3. Baixar snapshot da Vulgata + gerar lista de frequência.
4. Reescrever a Parte 0 (pronúncia eclesiástica) e atualizar o `REGRAS-TRADUCAO.md`.
5. Criar o shortcode `lectio` e converter as Lições I–II ao novo formato (prova de conceito,
   com 1 João / orações como primeiras leituras).
6. Seguir lição a lição (D'Ooge como espinha), inserindo Lectiones e marcos de leitura.

## 11. Em aberto (decidir ao longo do caminho)

- Numeração: manter os §§ do D'Ooge como referência ou renumerar como curso próprio?
- Quanto adaptar a *ordem* das lições do D'Ooge à necessidade de leitura da Vulgata.
- Nível de detalhe das notas (gramatical x devocional).
- Se haverá trilha de memorização (orações) separada das lições.
