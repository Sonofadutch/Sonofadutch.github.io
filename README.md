# Portfolio

My work, shown as case studies rather than repositories. Static HTML and CSS, no
framework and no build step, served by GitHub Pages.

**Live:** https://sonofadutch.github.io

```
index.html          home — hero, work cards, how I work, about, contact
work/               one page per project
  _template.html    copy this to start a new one
css/site.css        the entire design system, one file
media/              captures and the link-preview image (see media/README.md)
```

## Why it looks like this

Most developer portfolios link straight to a repo and let the reader guess. A
client cannot read a repo, and a hiring manager will not. So each project gets a
page that answers, in order: what the problem was, what I decided and why, one
piece of real code, what went wrong, and what I would do differently.

Source stays private. Excerpts, a live link where there is one, and "available on
request" is enough — and it is what most working developers can show anyway, since
client work is usually under someone else's control.

## Working on it locally

No install, no dependencies. Open `index.html` in a browser, or serve it so that
the paths behave exactly as they will in production:

```powershell
cd C:\Users\projects\portfolio
python -m http.server 8000
```

Then http://localhost:8000. Ctrl+C to stop.

## Adding a project

1. `copy work\_template.html work\<slug>.html` and replace every `TODO`.
2. Record a capture into `media/<slug>.gif` — see `media/README.md`.
3. Copy one `<a class="card">` block in `index.html`, point it at the new page.
4. Fix the `.next` link at the bottom of the previous case study so the chain
   still runs.

That is the whole workflow. Deliberately — a portfolio that needs a build step is
a portfolio that stops getting updated.

## Publishing

Repo name must be **`Sonofadutch.github.io`** for the site to live at the root
domain. First time:

```powershell
cd C:\Users\projects\portfolio
git remote add origin https://github.com/Sonofadutch/Sonofadutch.github.io.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Source: Deploy from a branch → `main` / `root`**.
Live in about a minute. After that, every `git push` republishes.

`.nojekyll` is there so GitHub serves the files as-is instead of running them
through Jekyll.

## Before it goes public — checklist

- [x] LinkedIn URL in the footer of `index.html`, or delete that line
- [x] `media/og.png` exists (this is the image people see when you paste the link)
- [x] At least one real capture, not a placeholder
- [ ] Every claim on the site is true and every number is one you can back up
- [ ] No client name used without their say-so
- [ ] No live security issue described in enough detail to be followed
