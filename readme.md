# Abdelmalek Nouri — Portfolio

Multi-page static portfolio. No build step, no framework, no dependencies.
Just open `index.html` in a browser to preview locally.

## Structure

```
portfolio/
├── index.html              ← home page (hero, about, project grid, skills, contact)
├── styles.css              ← shared stylesheet for all pages
├── README.md               ← this file
├── resume.pdf              ← (add this — see below)
└── projects/
    ├── ltv.html            ← Passenger LTV Prediction
    ├── driver-value.html   ← Driver Value Segmentation (3-level model)
    ├── reactivation.html   ← Algeria Driver Reactivation A/B
    ├── okr.html            ← OKR Modelling Framework
    ├── medgames.html       ← Mediterranean Games Live Monitoring
    ├── churn.html          ← Customer Churn Prediction
    └── derm.html           ← Dermoscopic Lesion Segmentation
```

## Deploy in 5 minutes (free)

### Option 1 — GitHub Pages (recommended for a permanent URL)

1. Create a new public repository on GitHub called `portfolio` (or any name you prefer).
2. Upload the entire folder (`index.html`, `styles.css`, the `projects/` directory) to the repository root.
3. Go to **Settings → Pages → Source → Deploy from branch → main → /(root) → Save**.
4. Live within 1–2 minutes at `https://<your-username>.github.io/portfolio/`.

You can connect a custom domain later (e.g. `abdelmalek-nouri.com`) — Settings → Pages → Custom domain.

### Option 2 — Netlify (drag-and-drop)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag the entire portfolio folder onto the drop zone.
3. Netlify gives you a public URL instantly. Optionally connect a custom domain.

### Option 3 — Vercel

1. Go to [vercel.com/new](https://vercel.com/new).
2. Import a GitHub repo (or drag-and-drop the folder).
3. Deploy.

## Adding the resume PDF

The "Download resume" button on the home page links to `resume.pdf`. After deployment:

1. Export your DOCX resume to PDF.
2. Drop the PDF (named exactly `resume.pdf`) into the same folder as `index.html`.
3. Re-deploy — the button will work.

## Customizing

- **Hero text, About, Skills, Contact** → edit `index.html` directly. Every section has a clear comment marker (`<!-- Hero -->`, etc.).
- **Project pages** → each project is its own HTML file in `projects/`. Edit the file directly to update content.
- **Adding a new project** → copy any existing project HTML file (e.g. `projects/ltv.html`), rename it, edit the content, then add a new `<a class="project-card">` block to the grid in `index.html`.
- **Removing a project** → delete its HTML file in `projects/` and remove its card from the grid in `index.html`.
- **Color palette and typography** → all in `styles.css` at the top, in the `:root` block. Change `--accent` once and the whole site picks it up.

## Linking from your resume and LinkedIn

- **Resume header**: add the URL next to your LinkedIn (e.g., `abdelmalek-nouri.netlify.app`).
- **LinkedIn → Featured section**: paste the URL — LinkedIn will auto-generate a preview card.
- **LinkedIn → Contact info → Website field**: add the URL.
- **Email signature**: add a one-line link.

## Tech notes

- Pure HTML + CSS + a tiny bit of vanilla JavaScript on the home page (filter chips). Nothing else.
- Fonts: Fraunces (display) + Manrope (body) + JetBrains Mono (accents) — all loaded from Google Fonts CDN.
- All inline SVG diagrams are part of the HTML; they scale cleanly and print well.
- No tracking, no analytics, no cookies.
- Fully responsive (works on phone, tablet, desktop).
- Print-friendly (the nav and bottom nav links hide cleanly).
- Light theme, editorial aesthetic.
- ~30KB per page including styles. Loads instantly.

---

Built from scratch.
