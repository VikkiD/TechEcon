# Methods & Applications

Source for my Quarto blog on economics, econometrics, statistics, ML, and CS.

## One-time setup

1. Install [Quarto](https://quarto.org/docs/get-started/) (and R and/or Python
   for whichever engine your posts use).
2. Create a **public** GitHub repo named `TechEcon`. (On the free plan, Pages
   requires a public repo; the site is public either way.) This is a *project*
   site, so it will serve from a subpath: `https://USERNAME.github.io/TechEcon/`.
   Do **not** pick a license in GitHub's creation dialog — the license files are
   already in this repo (see License below).
3. Replace every `USERNAME` and `YOUR NAME` placeholder across `_quarto.yml`,
   `about.qmd`, `posts/_metadata.yml`, `LICENSE`, and `LICENSE-CONTENT.md`.
4. Push this folder to the `main` branch.

## Everyday workflow

Preview locally (live-reloads as you edit):

    quarto preview

When a post is ready, render + publish in one command:

    quarto publish gh-pages

That renders the whole site locally (running your code, baking in tables and
figures) and pushes the output to a separate `gh-pages` branch. In the repo's
Settings → Pages, set the source to the `gh-pages` branch once. Your `main`
branch stays clean source; the built HTML never clutters it.

## Adding a post

Create `posts/my-new-post/index.qmd` with front matter:

    ---
    title: "..."
    description: "..."
    date: 2026-01-23
    categories: [Economics, Method]
    ---

Categories are your tags. Keep to the fixed vocabulary so the filter stays
tidy: one **domain** (`Economics` or `Computer Science`) + one **mode**
(`Method` or `Applied`) per post. Casing matters — `Economics` and `economics`
would show up as two different categories.

## Résumé & how readers follow

- Drop your `resume.pdf` at the repo root. The `resources: "*.pdf"` line in
  `_quarto.yml` publishes it, and it's linked from the navbar ("Résumé") and the
  homepage "Start here" routing.
- No email list is set up (by design, for now). Readers follow via the **RSS
  feed** (`index.xml`, linked in the navbar) in any reader, or by plugging that
  feed into a reader-side service like Blogtrottr for email. Announce new posts
  on LinkedIn for full, spam-free control over timing.

## License

This repository is dual-licensed, because it contains two kinds of material:

- **Written content** (prose, essays, analysis, figures in the posts) —
  [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Reuse freely,
  including commercially, with attribution. See `LICENSE-CONTENT.md`.
- **Code** (code blocks, `theme.scss`, config, the scaffold) —
  [MIT](https://opensource.org/licenses/MIT). See `LICENSE`.

Do not use GitHub's built-in license picker — its only Creative Commons option
is **CC0** (public domain, *no* attribution required), which is not what you
want. The files above already set the correct licenses.
