# TODO — Jerônimo

Lista de tarefas do projeto. Ver visão e formato em [`PLANO-JERONIMO.md`](PLANO-JERONIMO.md).

## Feito
- [x] Baixar manual original do D'Ooge (`fonte/latin-for-beginners.html`)
- [x] Traduzir Introdução + Parte I (pronúncia) + Lições I–II
- [x] Montar site Hugo + tema Hextra (`site/`), shortcode `lat`, CSS custom
- [x] Publicar no GitHub Pages (`eh-lucas/jeronimo`) com deploy automático
- [x] Definir formato do curso e fonte da Vulgata (`PLANO-JERONIMO.md`)
- [x] Traduzir as 30 primeiras lições do D'Ooge (base) → `traducao/licao-01..30.md`
- [ ] Revisar os ~24 flags ⚠️ deixados pelos agentes nas lições traduzidas

## Fase 3 — Fonte da Vulgata
- [ ] Baixar snapshot local da Vulgata Clementina para `fonte/vulgata/` (getBible v2 JSON)
- [ ] Gerar lista de frequência de lemas a partir do snapshot
- [ ] Definir núcleo de vocabulário de alta frequência (primeiras ~300 palavras)

## Fase 4 — Pronúncia eclesiástica
- [ ] Reescrever a Parte 0 (pronúncia eclesiástica) substituindo a clássica do D'Ooge
- [ ] Atualizar a seção de pronúncia no `REGRAS-TRADUCAO.md` (clássica → eclesiástica)
- [ ] Revisar exemplos de pronúncia para usar palavras da Vulgata

## Fase 5 — Novo formato (prova de conceito)
- [ ] Criar shortcode `lectio` (referência + texto + vocabulário + notas + tradução recolhível)
- [ ] Trazer as orações como primeiras leituras (Pater Noster, Ave Maria, Gloria, Credo)
- [ ] Converter Lições I–II ao formato Gramática → Vocabulário → Lectio → Exercícios
- [ ] Inserir 1 João como primeira leitura corrida

## Fase 6 — Lições (espinha D'Ooge + Vulgata)
- [ ] Construir tabela de mapeamento D'Ooge → versículos da Vulgata (lição a lição)
- [ ] Seguir as lições do D'Ooge (III em diante) já no novo formato
- [ ] Inserir marcos de leitura (João, Gênesis, Salmos) conforme a gramática permitir
- [ ] Manter glossário cumulativo do curso

## Decisões em aberto
- [ ] Manter os §§ do D'Ooge como referência ou renumerar como curso próprio?
- [ ] Quanto reordenar as lições do D'Ooge em função da leitura da Vulgata?
- [ ] Nível das notas: gramatical x devocional?
- [ ] Trilha de memorização (orações) separada das lições?

## Backlog / futuro
- [ ] Áudio da pronúncia eclesiástica
- [ ] Tooltip/glossário interativo para palavras já vistas
- [ ] Avaliar aposentar o `traducao/manual.html` (single-file) em favor do site Hugo
