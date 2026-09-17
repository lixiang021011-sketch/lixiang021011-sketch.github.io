# portfolio-site

Single-page portfolio for job applications: systems, tools and verification.

Static site — one `index.html`, no build step, no dependencies. Images and the 30-page project manual live in `assets/`.

## Preview locally

```powershell
start index.html
```

Or, to preview exactly as it will be served:

```powershell
python -m http.server 8080
# then open http://127.0.0.1:8080/
```

## Publish with GitHub Pages

1. Create a new **public** repository named exactly `lixiang021011-sketch.github.io`
   (a user site: the URL becomes `https://lixiang021011-sketch.github.io/`).
2. In this folder:

```powershell
git remote add origin https://github.com/lixiang021011-sketch/lixiang021011-sketch.github.io.git
git branch -M main
git push -u origin main
```

3. Wait a minute, then open `https://lixiang021011-sketch.github.io/`.
   Pages publishes `main` / root automatically for a user site.

Alternative if you prefer a project site inside an existing repo: push this folder as `docs/` and enable
Pages for the `/docs` folder in the repository settings.

## What is on the page

- **Selected work** — FallenAngel, Game Forge, Bell Garden, StylesVN: the problem each answers, what exists today, and how it is checked.
- **How I work** — three habits: design claims get tested, production problems become tool problems, automation verifies state while people verify feel. Includes the standing statement about AI as the implementation layer.
- **Contact** — email, phone, GitHub.

## Files

| File | Notes |
| --- | --- |
| `index.html` | The whole site: content, layout and CSS inline. No JS, no fonts to download. |
| `assets/*.png` `assets/*.jpg` | Figures and screenshots, pre-optimised (max 1600px wide). |
| `assets/xiang-li-project-manual.pdf` | The 30-page project manual, linked from the page and the nav. |

## Keeping it current

When a project changes, update the matching block in `index.html` and, if a figure changed, replace the file in
`assets/` with the same name. The manual PDF is the long-form version — regenerate it from
`Desktop\作品展示手册\` and copy the new PDF over `assets/xiang-li-project-manual.pdf`.
