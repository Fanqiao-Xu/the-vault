# The Vault

> A personal writing platform exploring the intersection of aesthetics, commercial thinking, and cultural analysis.

🔗 **Live site:** [fanqiao-xu.github.io/the-vault](https://fanqiao-xu.github.io/the-vault)

## What This Is

The Vault is an independently maintained English-language publication. Each piece takes a subject from architecture, design history, or brand strategy and examines the structure underneath — what makes something work, why it endures, and what it reveals about the people and economies around it.

Writing here sits somewhere between criticism and analysis. The references are Zumthor, Pallasmaa, Aalto, Heidegger. The questions are commercial as much as cultural.

## Selected Pieces

- **Bruder Klaus Field Chapel** — on Zumthor, material presence, and what it means to build something that resists explanation
- **Kering FY2024 Decline Analysis** — a data-driven examination of Gucci's revenue contraction and the structural limits of brand repositioning
- **Leaving Cardiff** — a personal essay on place, transition, and the architecture of departure

## Tech Stack

Pure HTML + CSS, no frameworks, no build step. Deployed via GitHub Pages.

## Project Structure

```
the-vault/
├── index.html              # Home page — article index
├── about.html              # About page
├── vault.css               # Global stylesheet
├── article.css             # Article page stylesheet
├── diary_bruderklaus.html  # Bruder Klaus Field Chapel
├── diary_cardiff.html      # Leaving Cardiff
├── diary_aalto.html        # Aalto House
├── insight_kering.html     # Kering FY2024 analysis
├── insight_lvmh.html       # LVMH analysis
└── assets/                 # Images (see optimization note below)
    ├── me.JPG
    ├── chapel_exterior.jpeg
    ├── chapel_interior.jpg
    ├── aalto_house_livingroom.JPG
    ├── aalto_house_outside.JPG
    ├── p1.jpeg
    ├── p2.jpg
    ├── p3.jpeg
    ├── p4.jpeg
    ├── door.JPG
    ├── glass.JPG
    ├── R0001550.JPG
    ├── shenyang_cafe.JPG
    ├── kering_chart.png
    └── lvmh_2025.jpg
```

## Image Optimization

> ⚠️ **Action needed:** Several images are 5–11MB. This bloats the repo and slows page load.

**Recommended steps:**
1. Move all images into `assets/` subfolder for cleaner structure
2. Compress all JPGs to <500KB (use [squoosh.app](https://squoosh.app) or `cwebp`)
3. Convert to WebP for 30–50% smaller file size with no quality loss
4. Update `<img src="...">` paths in HTML files

```bash
# Example: batch convert to WebP
for f in *.JPG *.jpg *.jpeg; do
  cwebp -q 80 "$f" -o "${f%.*}.webp"
done
```

## Deployment

This site is deployed via **GitHub Pages**:
1. Repo → Settings → Pages
2. Source: Deploy from branch → `main` → `/ (root)`
3. Site URL: `https://fanqiao-xu.github.io/the-vault`

## About

Written and maintained by **Fanqiao (Faye) Xu**.

## License

All written content © Fanqiao Xu. All rights reserved. Code (HTML/CSS) available under MIT License.
