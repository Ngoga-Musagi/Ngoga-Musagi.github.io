# CLAUDE.md

Project memory for this repository. Read this first at the start of every session.
When you resolve a bug, make a non-obvious decision, or learn something that a
future session would otherwise have to rediscover, append it to the relevant log
section below so work never starts from nothing.

---

## What this is

The personal portfolio website for **Alexis Ngoga** — AI Engineer & Solution
Architect (Kigali, Rwanda). It is a **GitHub Pages user site**, served directly
from the `main` branch at **https://Ngoga-Musagi.github.io**.

- **Repo:** `git@github.com:Ngoga-Musagi/Ngoga-Musagi.github.io.git`
- **Hosting:** GitHub Pages (user site). Pushing to `main` deploys the site.
  There is no build step — the published file *is* `index.html`.
- **Owner:** Ngoga-Musagi (Alexis Ngoga)

## Structure

```
.
├── index.html                 # The entire site — single file, inline CSS, no JS, no framework
├── ngoga.jpg                  # Header profile photo (referenced as src="ngoga.jpg")
├── Alexis_Ngoga_resume.pdf    # Resume (not currently linked from index.html)
├── icons/
│   ├── bioscience-icon.png
│   ├── neo4j-icon.png
│   └── qiskit-icon.png        # Logos available for use (e.g. certifications/projects)
└── CLAUDE.md                  # This file
```

## How it's built

- **Single self-contained HTML file.** All styling is in one `<style>` block in
  `index.html`'s `<head>`. There is no external CSS, no JavaScript, no build
  tooling, no package manager, no CI. Edit `index.html` directly.
- **Academic CV layout** (à la Jon Barron's site): serif font (Georgia), centered
  ~880px column, blue links (`#1772d0`) that turn orange on hover (`#f09228`).
- **Content sections** (in order): Header → Bio → Education → Experience →
  Selected Projects → Skills → Certifications → Languages → Footer.
- **Experience and Projects** both reuse the `table.pubs` table style. Each row is
  a thumbnail cell (`td.thumb` with a `.pub-thumb` text badge like "EI", "RA") plus
  a content cell (`.title`, `.authors`, `.venue`, `.desc`, optional `.links`).
- **Responsive:** a `@media (max-width: 600px)` block stacks the header and table
  cells into single columns on mobile.

## Conventions

- Keep everything in `index.html` unless there's a strong reason to add files.
  Match the existing inline-CSS / no-JS style — don't introduce a framework.
- Use HTML entities (`&amp;`, `&nbsp;`, `&middot;`) as the existing markup does.
- Thumbnail badges are short text initials inside `.pub-thumb`. If using a real
  image instead, drop it in `icons/` and reference it relatively.
- The "Last updated" footer date is maintained by hand — update it when making
  meaningful content changes.
- Open external links with `target="_blank"`.

## Testing / preview

No build. To preview locally, open `index.html` in a browser, or serve the folder:
`python -m http.server` then visit `http://localhost:8000`. After pushing to
`main`, allow a minute or two for GitHub Pages to redeploy.

---

## Decisions log

Non-obvious choices made over time. Newest at the top.

- _(none yet)_

## Resolved issues log

When you fix a bug, record the symptom, the cause, and the fix here so it doesn't
get re-debugged later. Format: `YYYY-MM-DD — symptom → cause → fix`.

- _(none yet)_

## Open / known issues

- _(none yet)_
