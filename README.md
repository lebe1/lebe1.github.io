# lebe1.github.io

My personal portfolio at **[leonbeccard.com](https://leonbeccard.com/)**.

Plain static HTML and CSS — no Jekyll, no build step, no dependencies. What is in this
repository is exactly what gets served.


## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>. Paths are root-relative (`/assets/css/style.css`), and
because this is a *user* site served from the domain root rather than a project site under
a subpath, they resolve identically on localhost and on the live domain.

Don't open `index.html` as a `file://` URL — fonts and root-relative paths behave
differently under that scheme, so the page can look broken even when it's fine.

## Editing

Content lives directly in `index.html`. A project is one `<article class="project-card">`:
title, context line, description, optional `<ul class="project-tags">`, and a row of
`<a class="project-link">` buttons. Entries still needing copy use `<p class="project-todo">`,
which renders as visibly unfinished italic text instead of leaving a silent gap.

Fonts are self-hosted, so the page makes no third-party requests at all.

## Credit

Started from [chriskhanhtran/minimal-portfolio](https://github.com/chriskhanhtran/minimal-portfolio),
released into the public domain (see `LICENSE`). The Jekyll theme has since been removed
and the site rewritten as static HTML.
