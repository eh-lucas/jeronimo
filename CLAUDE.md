# CLAUDE.md

Guidance for AI assistants working in this repository.

## Project

**Jerônimo** — a faithful Brazilian-Portuguese translation of *Latin for
Beginners* (B. L. D'Ooge, 1911, public domain), published as a Hugo site.

- `traducao/` — translation drafts (`licao-01..50.md`), may carry `⚠️` review flags.
- `site/` — the published Hugo site (Hextra theme; custom CSS in
  `site/assets/css/custom.css`).
- `REGRAS-TRADUCAO.md` — translation and site-style conventions.
- `TODO.md` — task list.

## Commit conventions

- **Commit directly to `main`. Do not open pull requests.**
- **Split work into small, logically separate commits** — one concern per
  commit — so the history stays auditable.
- **Write commit messages in English**, following
  [Conventional Commits](https://www.conventionalcommits.org/):
  `type(scope): short summary` in the imperative mood.
  - Types used here: `feat`, `fix`, `style`, `docs`, `refactor`, `chore`.
  - Scope is optional; `site` is the common one (e.g. `fix(site): ...`).
- **Describe the *why*, not just the *what*** in the body. Explain the
  problem a change solves so a future reader understands the intent.
- Keep the subject line ≤ ~72 chars; wrap the body at ~72 columns.
- Only commit or push when the user asks.

## Notes

- Content/UI text is Brazilian Portuguese; code, commits, and these docs are English.
- Any new background/color must define both a light and a `.dark` value — the
  dark theme is supported and must not break.
