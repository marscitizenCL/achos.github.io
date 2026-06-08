# Achos — Website & Marketing

**For the Guardians of Sound**

This repository hosts the [achos.app](https://achos.app) website, built as a static GitHub Pages site.

---

## Structure

```
achos-site/
├── index.html              ← Landing page
├── privacy-policy.html     ← Privacy Policy (required for App Store)
├── support.html            ← Support page (required for App Store)
├── downloads/
│   ├── Achos_Technical_Manual_v1_0.pdf
│   └── Achos_Appendix_A_COFI_v4_final.pdf
├── assets/
│   └── images/             ← App screenshots (add before launch)
├── .nojekyll               ← Disables Jekyll processing
└── CNAME                   ← Custom domain (edit if using achos.app)
```

---

## GitHub Pages Setup

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Source: **Deploy from a branch → main → / (root)**
4. Site will be live at `https://[username].github.io/achos`

### Custom domain (optional)

To use `achos.app`:
1. Edit `CNAME` and replace the placeholder with `achos.app`
2. Add DNS records at your registrar:
   - `A` records pointing to GitHub Pages IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Or a `CNAME` record: `www` → `[username].github.io`

---

## Screenshots

Add app screenshots to `assets/images/` and update the placeholder `<div class="screen-body">` blocks in `index.html` with:

```html
<img src="assets/images/screenshot-main.png" alt="Achos main window" style="width:100%; display:block;">
```

Replace the three placeholder frames:
- **Hero** — main playback window
- **GRaiL feature card** — GRaiL narrative panel
- **Guardian's Path walkthrough** — Guardian's Path sequence

---

## Download links

PDFs are served directly from the `downloads/` folder:
- `downloads/Achos_Technical_Manual_v1_0.pdf`
- `downloads/Achos_Appendix_A_COFI_v4_final.pdf`

GitHub Pages serves them with correct `Content-Type`. The `download` attribute on `<a>` tags forces browser download rather than inline open.

---

## App Store URLs

Before launch, update the App Store button `href` in both `index.html` and `support.html`:

```html
<!-- Search for this and replace with the real App Store URL -->
href="https://apps.apple.com"
```

---

## Support email

Update `support@achos.app` in `support.html` and `privacy-policy.html` once the address is live.

---

**Developer:** Martín Gallardo Arenas · Santiago, Chile · 2026  
**Coding Agent:** Claude AI · Anthropic  
**Method:** Human-AI Co-Creation · COFI Framework
