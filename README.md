# Personal homepage — Xinyue Zhao

Static site. No build step. `index.html` is the whole page.

Type and neutral colors follow livemacroeval.github.io so the two sites read as a
set: Source Serif 4 for the name and paper titles, Libre Franklin for body text
and labels. Colour has two roles, as on that site: grey-blue `#2d6fa9` for links
and oxblood `#7a2e2e` for prose emphasis and status tags (`#8fb5dd` / `#d9a09a` in dark mode).

## Files
- `index.html` — the page (all CSS inline)
- `assets/Xinyue_Zhao_CV.pdf` — built from the Overleaf source
- `assets/photo.jpg` — headshot (440x440, cropped from `photo.jpeg`). If the file is
  absent the page silently omits the image.
- `cv-source/` — the Overleaf clone (git-ignored, not published)

## Preview locally
```
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy to GitHub Pages
```
git init -b main
git add .
git commit -m "Personal homepage"
git remote add origin https://github.com/<USERNAME>/<USERNAME>.github.io.git
git push -u origin main
```
Then Settings → Pages → Source: `Deploy from a branch`, branch `main`, folder `/ (root)`.
Live at `https://<USERNAME>.github.io` in about a minute.

## Refreshing the CV
```
cd cv-source && git pull && pdflatex main.tex && cp main.pdf ../assets/Xinyue_Zhao_CV.pdf
```

## Note on unpublished work
Only the EMNLP paper links out (arXiv + benchmark site). The two working papers list
titles and summaries only — no PDFs are hosted or linked.
