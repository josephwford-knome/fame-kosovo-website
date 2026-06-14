# FAME — fame-kosovo.org

Public marketing site (brochureware) for **FAME — Future Albanian Minds Empowered**, with the interactive demo hosted at `/demo/`. Static HTML/CSS/JS — no build step, no dependencies.

## Files

```
index.html          The marketing site (everything inline — CSS + JS)
assets/
  fame_logo.jpg     Full brand lockup (hero)
  fame_eagle.png    Transparent eagle (nav, footer, watermark)
  favicon.png       Site icon
demo/
  index.html        Placeholder — replace with the real demo build
CNAME               Custom domain for GitHub Pages
```

## Deploy on GitHub Pages

1. Create a repository and add these files at the root (keep the folder structure).
2. Push to the `main` branch.
3. In the repo: **Settings → Pages**. Under **Build and deployment**, set **Source = Deploy from a branch**, branch **`main`**, folder **`/ (root)`**. Save.
4. The site publishes within a minute or two. The `CNAME` file points it at **fame-kosovo.org**.

## Point the domain at GitHub Pages

At your domain registrar's DNS settings for **fame-kosovo.org**:

**Apex (fame-kosovo.org)** — add four `A` records to GitHub's IPs:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**www (optional)** — add a `CNAME` record: `www` → `YOUR-USERNAME.github.io`

Then in **Settings → Pages**, confirm the custom domain shows `fame-kosovo.org` and tick **Enforce HTTPS** (available once the certificate provisions, usually within the hour).

## When the real demo is ready

The "Launch the demo" buttons link to `./demo/`. Two options:

- **Host on GitHub (recommended for one URL):** replace the contents of the `demo/` folder with your demo build. It goes live at `fame-kosovo.org/demo/`.
- **Point elsewhere (e.g. the Vercel app):** in `index.html`, change every `href="./demo/"` to the demo's URL. There are four — in the nav, the mobile nav button, the hero, and the demo band — plus the footer link.

## Things to confirm / customize

- **Domain spelling.** This package uses the hyphenated **fame-kosovo.org**. Your letter to Prof. Muçaj prints **famekosovo.org** (no hyphen) — a different domain. If you actually registered the no-hyphen version, run a find-and-replace from `fame-kosovo.org` to `famekosovo.org` in `index.html` and update `CNAME`.
- **Contact email.** Currently `jwford@knome.tech`. Swap for whatever inbox you want public.
- **Advisory / partner names are intentionally left off** the public page (the ACEs study and named advisors in your draft letter are not yet public). Add confirmed partners when you're ready.

---

*A project of Rowboats LLC. Built in Kosovo. Open to the world.*
