# RustVault Copilot Instructions

## High-level architecture

- This repository is a content vault, not an application codebase. Read `COPILOT.md` before changing content; it is the main workflow specification for the repository.
- `raw/` contains the original source material. In practice that means Jekyll-style posts under `raw/_posts/` plus supporting images under `raw/assets/images/<year>/`.
- `wiki/` contains the Copilot-managed knowledge base derived from `raw/`. `wiki/index.md` is the table of contents for the vault, and `wiki/log.md` is the append-only change log.
- `.obsidian/` stores Obsidian vault metadata and editor state. Treat it as editor configuration, not part of the knowledge model.

## Key conventions

- Never edit files under `raw/`. Treat everything in that tree as immutable source input.
- Import work is source-driven: read the full raw document first, discuss the main takeaways with the user, then create or update wiki pages based on that source.
- Wiki changes are coordinated changes. When a wiki page changes, also update `wiki/index.md` and append a new entry to `wiki/log.md`.
- New wiki page filenames should be lowercase kebab-case, for example `makine-ogrenimi.md`.
- Wiki pages should follow the structure defined in `COPILOT.md`:

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

- Use Obsidian wikilinks (`[[sayfa-adı]]`) to connect related concepts across the wiki.
- Every factual claim in wiki content should cite its raw source using `(kaynak: dosyaadı.md)`. If two sources conflict, state the conflict explicitly. If a claim has no source, mark it as requiring verification.
- `wiki/log.md` is append-only.
- Repository content is written in Turkish; preserve that language in generated wiki pages and metadata unless the user asks for a different language.

## Repository-specific content patterns

- Raw posts consistently use YAML front matter with fields such as `layout`, `title`, `date`, `tags`, and `categories`.
- Raw posts often embed images by filename (for example `![rust_mini_00.png](rust_mini_00.png)`), while the corresponding assets live under `raw/assets/images/<year>/`.
- If asked to audit or lint the wiki, check for contradictions between pages, orphaned pages, concepts mentioned without their own page, claims that may be outdated relative to newer raw sources, and deviations from the required wiki page structure.
