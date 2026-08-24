# Archworks Industries website

A lightweight, dependency-free one-page site for **archworksindustries.com**. It is built with plain HTML and CSS and is ready to publish directly from a GitHub Pages branch—no paid hosting, build process, package manager, or server required.

## Repository contents

```text
.
├── index.html                 Homepage
├── styles.css                 Responsive design and brand system
├── 404.html                   Branded not-found page
├── assets/
│   ├── favicon-32.png         Browser icon
│   ├── apple-touch-icon.png   Home-screen icon
│   ├── logo-mark-512.png      Large square logo mark
│   └── archworks-social.png   Link-preview card
├── CNAME                      GitHub Pages custom domain
├── .nojekyll                  Disables Jekyll processing
├── robots.txt                 Search crawler instructions
├── sitemap.xml                Search engine sitemap
├── site.webmanifest           Site/app metadata
└── README.md                  Setup instructions
```

## Preview locally

The site has no build step. You can open `index.html` directly in a browser. For the most accurate preview, serve the folder with any basic local web server.

For example, if Python is installed:

```powershell
python -m http.server 8080
```

Then visit `http://localhost:8080`.

## Publish with GitHub Pages

1. Create a public repository named `website` in the **Archworks-Industries** GitHub organization. GitHub Pages on the free organization plan requires the site repository to be public.
2. Upload or push every file in this folder to the repository's `main` branch.
3. Open the repository on GitHub and go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Select the `main` branch and the `/(root)` folder, then save.
6. Under **Custom domain**, enter `archworksindustries.com` and save.

GitHub may take a few minutes to publish the first version. The site will initially also be available at the organization's default Pages address.

GitHub's current official instructions: [Configuring a publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Point archworksindustries.com to GitHub Pages

Before changing DNS, add the custom domain in the repository's Pages settings as described above. Then create these records with the domain's DNS provider.

### Apex domain

| Type | Host | Value |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |

### www redirect

| Type | Host | Value |
|---|---|---|
| CNAME | `www` | `archworks-industries.github.io` |

Remove any conflicting parking or forwarding records for `@` or `www`. Do not use a wildcard DNS record.

DNS changes can take up to 24 hours to propagate. Once GitHub recognizes the domain and issues its certificate, return to **Settings → Pages** and enable **Enforce HTTPS**.

For the current DNS values and security guidance, see GitHub's official [custom-domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

## Recommended domain verification

To reduce the risk of a domain takeover, verify `archworksindustries.com` at the organization level:

1. Open the **Archworks-Industries** organization on GitHub.
2. Go to **Settings → Pages**.
3. Choose **Add a domain**.
4. Enter `archworksindustries.com`.
5. Add the TXT record GitHub provides to the domain's DNS and leave it in place.

See GitHub's [domain-verification instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages).

## Update the site

- Edit the copy in `index.html`.
- Edit colors, spacing, and layout in `styles.css`.
- Keep the `CNAME` file exactly as-is unless the primary domain changes.
- If the public contact address changes, update both `mailto:` links in `index.html`.
- Push changes to `main`; GitHub Pages will republish automatically.

## Brand system used

The page follows the established Archworks identity:

- Jet Black: `#0B0B0B`
- Gunmetal: `#2A2A2A`
- Sand: `#E6E3DA`
- OD Green: `#4B4E47`
- Oxide Red: `#8B1E1E`
- Geometric arch mark, wide 1970s industrial display typography, plain secondary type, and restrained technical-drawing details

No external fonts, scripts, trackers, cookies, or third-party assets are loaded.
