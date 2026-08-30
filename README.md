# Archworks Industries website

A dependency-free static site for [archworksindustries.com](https://archworksindustries.com). GitHub Pages serves the files directly; there is no application server, build step, package manager, analytics, or third-party runtime.

## Preview locally

```powershell
cd D:\Github\Archworks-Industries-Website
python -m http.server 8080 --bind 127.0.0.1
```

Open [http://127.0.0.1:8080](http://127.0.0.1:8080), then press `Ctrl+C` to stop the preview.

## Site files

- `index.html` - Homepage structure and copy
- `styles.css` - Mobile-first layout and brand styling
- `404.html` - GitHub Pages not-found page
- `CNAME` - Custom domain
- `robots.txt`, `sitemap.xml`, and `site.webmanifest` - Search and browser metadata
- `assets/` - Favicons, social preview, and canonical brand artwork

## Brand assets

Production-ready SVG marks and outlined lockups live in `assets/brand/`.

The website uses:

- Jet: `#0B0B0B`
- Sand: `#E6E3DA`
- Sand Soft: `#C9C5BB`
- OD Green: `#4B4E47`
- Oxide Red: `#8B1E1E`

## Publish

The repository is configured for GitHub Pages from the root of the `main` branch. Push changes to `main` to republish. Keep `CNAME` unchanged unless the primary domain changes.
