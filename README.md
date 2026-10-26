# Personal academic website

A plain HTML and CSS site. There is no build step: GitHub Pages serves these files as they are.

## Files

| File | What it is |
|---|---|
| `index.html` | All the content: name, links, bio, papers |
| `style.css` | Fonts, colors and layout (light and dark mode) |
| `assets/photo.jpg` | Your headshot. Add a portrait image here (4:5 works best) and it replaces the initials automatically |
| `cv.pdf` | Your CV. The "CV" link under your name points here |
| `papers/` | PDFs and slides you want to link from the Research section |

## Editing

- **Add a paper:** in `index.html`, copy an `<article class="paper">` block and change the title, authors, abstract and links.
- **Change the link color:** edit `--link` in `style.css`. There's one value for light mode and one for dark mode.

To preview locally, run this, then open http://localhost:8000:

```bash
python3 -m http.server 8000
```

## Publishing on GitHub Pages

A user site has to live in a repository named exactly `<username>.github.io`, which here is `saatpanigrahi.github.io`.

```bash
git init -b main
git add .
git commit -m "Initial site"
gh repo create saatpanigrahi.github.io --public --source . --push
```

Then, on GitHub, open the repository's **Settings → Pages** and set the source to the `main` branch, `/ (root)` folder. The site goes live at https://saatpanigrahi.github.io within a minute or two.

To update it later:

```bash
git add . && git commit -m "Update site" && git push
```

### Custom domain (optional)

Buy a domain such as `yourname.com`. In **Settings → Pages → Custom domain**, enter it, then add the DNS records GitHub shows you at your domain registrar.
