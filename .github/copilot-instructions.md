# RustVault Copilot Instructions

## High-level architecture

This repository is a content vault, not an application codebase. `COPILOT.md` is the authoritative workflow specification — read it before changing any content.

- `raw/_posts/` — immutable source material (Jekyll-style blog posts). `raw/assets/images/<year>/` holds their images.
- `wiki/` — Copilot-managed knowledge base derived from `raw/`. Two kinds of pages coexist:
  - **Kavram sayfaları** (concept pages) — synthesize a theme across multiple sources (e.g., `sahiplik-ve-borclanma.md`)
  - **Kaynak özetleri** (source summaries) — one page per raw post, named after that post
- `wiki/index.md` — table of contents with three sections: *Kavram sayfaları*, *Kaynak özetleri*, *Öğrenme akışı*
- `wiki/log.md` — append-only change log
- `.obsidian/` — Obsidian vault config; treat as editor metadata, not part of the knowledge model

## Import workflow

When the user asks to import a raw source:

1. Read the full raw document
2. Discuss the key takeaways with the user **before writing anything**
3. Create a source summary page in `wiki/` named after the raw file
4. Create or update concept pages for each significant idea
5. Link related pages with Obsidian wikilinks (`[[sayfa-adı]]`)
6. Update `wiki/index.md` (add entries to the correct section with a one-line description)
7. Append a dated entry to `wiki/log.md`

A single source can touch 10–15 wiki pages; that is normal.

## Question-answering workflow

1. Read `wiki/index.md` first to locate relevant pages
2. Read those pages and synthesize an answer
3. Cite specific wiki pages in the response
4. If the answer is not in the wiki, say so explicitly
5. Offer to save a valuable answer as a new wiki page

## Audit / lint workflow

When asked to audit or lint the wiki, check for:

- Contradictions between pages
- Orphaned pages (no incoming wikilinks from other pages)
- Concepts mentioned in pages but without their own page
- Claims that may be outdated relative to newer raw sources
- Pages that deviate from the required page structure

Report findings as a numbered list with suggested fixes.

## Key conventions

- **Never edit files under `raw/`.** They are immutable source input.
- Wiki changes are coordinated: every change to a wiki page must also update `wiki/index.md` and append an entry to `wiki/log.md`.
- Wiki page filenames are lowercase kebab-case (e.g., `makine-ogrenimi.md`).
- All wiki content is written in Turkish unless the user requests otherwise.
- Every factual claim cites its raw source as `(kaynak: dosyaadı.md)`. If two sources conflict, state the conflict explicitly. If a claim has no source, mark it as requiring verification.
- Use Obsidian wikilinks (`[[sayfa-adı]]`) to connect related concepts.

## Wiki page structure

Every wiki page must follow this template exactly:

```markdown
# Sayfa Başlığı

**Özet**: Bu sayfayı açıklayan bir veya iki cümle.

**Kaynaklar**: Bu sayfanın dayandığı ham kaynak dosyaların listesi.

**Son güncelleme**: En son güncelleme tarihi.

---

## İlgili sayfalar

- [[ilgili-kavram-1]]
- [[ilgili-kavram-2]]
```

## Raw post patterns

- Raw posts use YAML front matter with fields: `layout`, `title`, `date`, `tags`, `categories`.
- Images are embedded by filename (e.g., `![rust_mini_00.png](rust_mini_00.png)`); the assets live under `raw/assets/images/<year>/`.
