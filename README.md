# theveerakumar.github.io

> Deployment repository for [veerakumar.com](https://veerakumar.com) — the built files served by GitHub Pages.

The portfolio source code lives in [`github.com/theveerakumar/veerakumar.com`](https://github.com/theveerakumar/veerakumar.com) (Astro). This repo contains the compiled output.

## Structure

```
├── index.html          # Portfolio homepage (built from astro-portfolio)
├── 404.html            # Terminal-themed 404 page
├── favicon.png
├── robots.txt
├── CNAME               # Custom domain: veerakumar.com
├── .nojekyll           # Disables Jekyll processing on GitHub Pages
├── _astro/             # Built CSS/JS bundles
└── seaborn/            # Financial calculator app
```

## What's NOT Here

These sub-paths are served by their own repositories' GitHub Pages deployments, sharing the `veerakumar.com` custom domain:

| App | Path | Repo |
|-----|------|------|
| **Stockalysis** | `/stockalysis/` | `theveerakumar/stockalysis` |
| **StockVedic** | `/stockvedic/` | `theveerakumar/stockvedic` |
| **Seaborn** | `/seaborn/` | `theveerakumar/seaborn` |

## Deploy Flow

```
veerakumar.com (Astro source)
        ↓ npm run build
        ↓ dist/
        ↓ cp -r dist/*  theveerakumar.github.io/
        ↓ git push
    veerakumar.com (live)
```

Sub-apps (Stockalysis, StockVedic, Seaborn) deploy independently through their own CI/CD pipelines and auto-deploy on push.
