# daewon88.github.io

Personal homepage of Daewon Chae — <https://daewon88.github.io>

A plain static site: no build step, no dependencies.

```
index.html               the whole page
assets/css/style.css     styles
assets/img/prof_pic.jpg  profile photo
assets/pdf/cv.pdf        CV
.nojekyll                tells GitHub Pages to serve files as-is
```

## Editing

Everything lives in `index.html`. Publications are grouped by year under
`#pub-list` → `.year-group`; news items are `<li>` entries in `.news`.

The Selected Work / Full Publications tabs filter that one list rather than
duplicating it: add the bare `data-selected` attribute to a publication's
`<li>` to have it appear under Selected Work. Year groups with no selected
entry hide themselves.
Colors, type scale and spacing are CSS custom properties at the top of
`assets/css/style.css`.

Typography uses San Francisco through the system font stack on Apple
platforms and falls back to Inter (loaded from Google Fonts) elsewhere.

## Preview locally

```sh
python3 -m http.server 8123
# then open http://localhost:8123
```

## Deploying

GitHub Pages serves the `main` branch at its root
(Settings → Pages → Source: *Deploy from a branch* → `main` / `/`).
Pushing to `main` publishes the site; there is no CI step.

The site was previously built from the [al-folio](https://github.com/alshedivat/al-folio)
Jekyll theme. That machinery was removed in favor of this static page — see the
git history before this commit to recover anything from it.
