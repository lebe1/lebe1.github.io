# lebe1.github.io

My personal portfolio at **[leonbeccard.com](https://leonbeccard.com/)**.

Plain static HTML and CSS — no Jekyll, no build step, no dependencies. What is in this
repository is exactly what gets served.


## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000> 

## Editing

Content lives directly in `index.html`. A project is one `<article class="project-card">`:
title, context line, an optional `<img class="project-image">`, description, optional
`<ul class="project-tags">`, and a row of `<a class="project-link">` buttons. Cards with press
coverage add a `<div class="project-press">` holding a `<ul class="press-list">` of the same
buttons. Entries still needing copy use `<p class="project-todo">`, which renders as visibly
unfinished italic text instead of leaving a silent gap.

Every `<img>` carries its real `width` and `height` so nothing shifts while the page loads, and
descriptive `alt` text. Images are stored at roughly twice their display size (the CSS caps them
at 380px) and no larger.

Colours are CSS variables named by role (`--bg`, `--surface`, `--text`, `--accent`, …). A
`prefers-color-scheme: dark` block near the top of `style.css` redefines those values and nothing
else, so a new rule only needs to reference variables to work in both themes. Accent colours are
kept at 4.5:1 contrast or better against their background.

Fonts are self-hosted, so the page makes no third-party requests at all.

## Credit

Started from [chriskhanhtran/minimal-portfolio](https://github.com/chriskhanhtran/minimal-portfolio),
released into the public domain (see `LICENSE`). The Jekyll theme has since been removed
and the site rewritten as static HTML.
