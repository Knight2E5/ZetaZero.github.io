# zetazero — portfolio site

A minimal, LaTeX-article-styled portfolio: two pages (Home, Math Notes),
one stylesheet, no build step.

## Files

```
index.html   Home page
notes.html   Math Notes listing (edit this to add new problem sets)
style.css    Shared styles
```

## Host on GitHub Pages

1. Create a new repository on GitHub, e.g. `zetazero.github.io` (for a
   user site at `https://<username>.github.io/`) or any name, e.g.
   `portfolio` (for a project site at `https://<username>.github.io/portfolio/`).
2. Push these three files to the repository root (the `main` branch).
3. In the repo, go to **Settings → Pages**, and under "Build and
   deployment" set **Source** to "Deploy from a branch", branch `main`,
   folder `/ (root)`. Save.
4. Wait a minute or two — GitHub will give you the live URL on that same
   Pages settings screen.

If you'd rather do it from the command line:

```bash
git init
git add index.html notes.html style.css README.md
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

Then enable Pages as in step 3.

## Adding a new note / problem collection

Open `notes.html` and duplicate one `<article class="entry">…</article>`
block (there's a comment right above the first one explaining exactly
what to change). Point `entry-links` at your actual PDF — the simplest
approach is to make a `notes/` folder in the repo, drop PDFs in there,
and link to e.g. `notes/abstract-algebra.pdf`.

## Customizing

- Colors, fonts, and spacing all live in `style.css` under the `:root`
  block at the top — change the hex values there to retheme everything.
- The "§" numbering in section headers and note entries is manual (kept
  as plain text) so you can renumber freely as entries are added or
  removed.
