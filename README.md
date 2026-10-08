# EasyAz Landing Page

Landing page for **EasyAz.vn** — digital solutions provider:

- 📹 **Smart surveillance cameras** (Camera giám sát thông minh)
- ⏱️ **Timesheet** — automated time & attendance (chấm công tự động)

A dependency-free static site (HTML + CSS + vanilla JS) with a futuristic, light-blue tech look. Built to be hosted on **GitHub Pages** with the custom domain `easyaz.vn`.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Page markup and content |
| `styles.css` | Styling, layout, animations |
| `script.js` | Nav toggle, scroll reveal, footer year |
| `CNAME` | Custom domain for GitHub Pages (`easyaz.vn`) |
| `.nojekyll` | Tells GitHub Pages to skip Jekyll processing |

## Preview locally

No build step. Just open `index.html`, or serve the folder:

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Deploy on GitHub Pages

1. Push to `main` (repo: `easyazvn/landing-page`).
2. On GitHub: **Settings → Pages**.
3. **Source:** *Deploy from a branch* → Branch `main` / folder `/ (root)` → **Save**.
4. Under **Custom domain**, confirm `easyaz.vn` (the `CNAME` file sets this automatically).
5. Enable **Enforce HTTPS** once the certificate is issued (may take a few minutes).

## DNS configuration for `easyaz.vn`

At your domain registrar / DNS provider, point the domain at GitHub Pages:

**Apex domain (`easyaz.vn`)** — add four `A` records:

```
A   @   185.199.108.153
A   @   185.199.109.153
A   @   185.199.110.153
A   @   185.199.111.153
```

(Optionally add the matching `AAAA` records for IPv6:
`2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`.)

**`www` subdomain** — add a `CNAME` record:

```
CNAME   www   easyazvn.github.io
```

DNS changes can take up to 24–48h to propagate. GitHub will show a green check in **Settings → Pages** once the domain is verified.

## Editing content

- **Contact email:** search `tam.vo@easyaz.vn` in `index.html`.
- **Copy / sections:** all text lives in `index.html`.
- **Colors / theme:** edit the CSS variables at the top of `styles.css` (`--sky-*`, `--cyan`, `--grad`).
