# Regras de tradução — *Latin for Beginners* (D'Ooge) → PT-BR

Este arquivo define as convenções que **toda** tradução do manual deve seguir, para
garantir consistência ao longo das 78 lições. Sempre consultar antes de traduzir uma
nova lição e atualizar quando surgir um caso novo.

Princípio geral:
> Trate o **latim como sagrado** (fidelidade total) e o **inglês como andaime**
> (adaptável, e a ser refeito sempre que o português não se comportar como o inglês).

---

## 1. Contraste com o inglês ≠ contraste com o português

O livro ensina latim **contrastando com o inglês**. Antes de traduzir cada
"*in English we…*", pergunte: **isso vale para o português ou não?**

> **Regra de fluxo (obrigatória):** sempre que um trecho de comparação com o inglês for
> mais delicado ou ambíguo — onde a adaptação para o português envolve julgamento —
> **perguntar ao usuário antes de decidir**, em vez de resolver sozinho. Não traduzir
> esses trechos "no chute".

- Quando o **português se comporta como o latim** (e não como o inglês), adaptar a
  moldura — às vezes invertendo o sentido, dizendo "assim como em português".
  - Ex.: queda do pronome sujeito (*luto*, não *eu luto*); marcação de pessoa/número
    no verbo; gênero gramatical. O inglês quase não tem; latim e português têm.
- Quando o **contraste continua válido** contra o português, mantê-lo.
  - Ex.: "o latim não tem artigo" — válido, pois o português tem `o`/`um`.
- Sinalizar a adaptação com uma nota quando o sentido do original mudar.

## 2. O latim é intocável

- **Preservar macrons e breves** (ā, ă) — são pedagógicos e fáceis de perder em
  cópia/encoding.
- **Nunca** alterar, "traduzir" ou modernizar palavras, formas ou paradigmas latinos.
- Conferir formas latinas suspeitas contra a gramática — o arquivo-fonte do Gutenberg
  pode ter **erros de OCR**.
- Manter as referências de seção (§) e a numeração do original.

## 3. Pronúncia: adaptar ao português, não ao inglês

- Substituir os exemplos ingleses por **equivalentes em português brasileiro**.
- Onde o português **não tem** o som equivalente, assinalar explicitamente.
- Alertar sobre **hábitos do PT-BR que corrompem o latim** (o livro não os menciona,
  pois só pensa no aluno americano):
  - `t`/`d` antes de `i`/`e` → **não** palatalizar: `ratiō` = "rá-ti-o", não "rá-tchi-o".
  - `s` intervocálico → **não** sonorizar em /z/: `rosa` com /s/.
  - `l` final de sílaba → **não** vocalizar em "u": `animal` com /l/.
  - vogais átonas → **não** reduzir (o `o` final latino é /o/, não /u/).

## 4. Cognatos e derivados

- O original lista derivados **ingleses** (`aqua` → *aquarium*). Trocar por cognatos
  **portugueses** (`aqua` → *aquário*; `filia` → *filha*; `lūna` → *lua*).
- Aproveitar a maior transparência do português, mas cuidar de **falsos amigos** e não
  forçar cognatos inexistentes.

## 5. Exercícios e referências culturais

- Exercícios de tradução **inglês→latim** viram **português→latim**; sinalizar a mudança.
- Reancorar no Brasil/Portugal as referências feitas para o aluno americano (conquista
  normanda, Shakespeare, "nossa língua mãe é o anglo-saxão" etc.).
- Citações bíblicas/literárias → usar versões em **português consagradas**
  (a formiga = Provérbios 6,6–8).
- Poesia (ex.: *Excelsior*): traduzir o sentido em prosa-verso ao lado do latim, mantendo
  o latim como está. Manter esse padrão em todos os textos literários.

## 6. Terminologia gramatical fixa

Usar **sempre** a nomenclatura abaixo, idêntica em todas as lições (evitar deriva de
termos). Acrescentar novos termos a esta tabela conforme aparecerem.

| Inglês (original)      | Português (usar sempre)        |
|------------------------|--------------------------------|
| inflection             | flexão                         |
| declension             | declinação                     |
| conjugation            | conjugação                     |
| subject                | sujeito                        |
| predicate              | predicado                      |
| direct object          | objeto direto                  |
| transitive / intransitive | transitivo / intransitivo   |
| copula                 | cópula                         |
| verb / noun / pronoun  | verbo / substantivo / pronome  |
| personal endings       | terminações pessoais           |
| number (sing./plural)  | número (singular/plural)       |
| ultima / penult / antepenult | última / penúltima / antepenúltima |
| diphthong              | ditongo                        |
| quantity               | quantidade                     |
| long / short (vowel)   | longa / breve (vogal)          |
| enclitic               | enclítica                      |
| stem / ending          | radical / terminação           |

## 7. Alertas de revisão (⚠️)

Sempre que surgir **dúvida** sobre como traduzir ou adaptar um trecho — por menor
que seja —, inserir um alerta imediatamente abaixo do trecho problemático no arquivo
`traducao/licao-XX.md`, usando o formato:

```
> ⚠️ **[revisar — <tipo>]** Descrição objetiva do problema ou dúvida.
```

Tipos comuns de `<tipo>`:
- `comparação com inglês` — adaptação para o português é ambígua
- `referência cultural` — exemplo americano sem equivalente claro no Brasil
- `OCR / forma latina` — forma suspeita que pode ser erro do Gutenberg
- `terminologia` — termo gramatical sem equivalente direto confirmado

**Regras obrigatórias:**
- Os alertas existem **apenas** nos arquivos `traducao/` — nunca devem ir para o Hugo.
- O conteúdo definitivo só vai para o Hugo após revisão e resolução de todos os ⚠️.
- Não resolver o alerta sozinho quando o julgamento for subjetivo — deixar para revisão humana.

---

## 8. Ortografia e estilo

- **"breve" / "breves" sem acento** (vogal breve, sílaba breve). Nunca "bréve/bréves".
- Registro: didático, claro e atual — é um livro para iniciantes; evitar arcaísmos.
- Português brasileiro, ortografia do Acordo vigente.
- Manter macrons nas palavras latinas mesmo no corpo do texto português.

---

## 9. Convenções de estilo do site (Hugo + Hextra)

O conteúdo publicado vive em `site/` (Hugo + tema Hextra, submódulo em
`site/themes/hextra`). Estilos próprios ficam em **`site/assets/css/custom.css`**;
overrides de layout, em `site/layouts/`.

**Conteúdo das lições**
- Latim no corpo do texto: usar o shortcode `{{</* lat */>}}` (classe `.lat`,
  cor própria clara/dark via `--lat-cor`).
- Classes de apoio: `.glossa` (tradução sob o exemplo), `.deriv` (cognatos),
  `.sec` (número §), `.poema` (tabela bilíngue de poesia).
- Macrons/breves preservados também no corpo em português (ver §2).

**Identidade visual**
- **Fundo cor de papel de livro:** variável `--papel-bg` em `:root` (claro,
  `#f6f1e3`) e `.dark` (`#1a1813`), aplicada em `html body`. Todo novo tom de
  fundo deve ter par claro/dark — o tema dark é suportado e não pode quebrar.
- **Tamanho de fonte do leitor:** controle flutuante A−/A+ injetado pelo partial
  `site/layouts/partials/custom/head-end.html` (o Hextra inclui `custom/head-end`,
  não `custom/head`). O valor vai para `--content-font-size` e é aplicado a
  `.content p/li/blockquote/td/th`; títulos ficam intocados.

**Página inicial (`site/content/_index.md`)**
- Índice lição a lição, agrupado por parte, dentro de `.home-wrap`
  (centralizado, `max-width` 760px).
- Cards em grade de 2 colunas no desktop e 1 no mobile; o card "Ao estudante"
  fica isolado em `.home-card-single` (largura cheia, destacado).
- Cada parte abre com um `##` (margem superior + divisória fina).
- Ao publicar novas lições em `site/content/docs/...`, acrescentá-las também a
  este índice e ao `_index.md` da parte correspondente.

> O arquivo legado `traducao/manual.html` (single-file) está em vias de ser
> aposentado em favor do site Hugo (ver `TODO.md`); não receber conteúdo novo.
