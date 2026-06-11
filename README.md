# Personal academic website

A small, fast Jekyll site for an economist's homepage. No theme, no plugins —
GitHub Pages builds it as-is. You edit Markdown and YAML; GitHub rebuilds on push.

## What to edit

| File | What it controls |
|------|------------------|
| `_config.yml` | Your name, role, affiliation, email, and all profile links |
| `index.md` | Bio paragraphs and contact block |
| `_data/news.yml` | The "News" feed on the homepage |
| `_data/publications.yml` | The Research page (sorted newest-first automatically) |
| `cv.md` | Short text CV; drop your PDF at `assets/cv.pdf` |
| `assets/img/portrait.svg` | Replace with your photo (e.g. `portrait.jpg`, then update the path in `index.md`) |
| `assets/css/style.css` | Colours and type live in the `:root` block at the top |
| `CNAME` | Your custom domain (currently `www.flavienmoreau.com`) |

## Put it on GitHub Pages

1. Create a repo named **`<your-github-username>.github.io`** (this makes it serve at the root).
2. Upload these files (drag-and-drop in the browser, or `git push`).
3. Repo **Settings → Pages**: source = "Deploy from a branch", branch = `main`, folder = `/`.
4. In the same Pages screen, set the custom domain to `www.flavienmoreau.com` and tick **Enforce HTTPS** once it's available.

## Point your domain (DNS at Squarespace)

In your Squarespace domain dashboard → DNS settings:

- **CNAME**: host `www` → value `<your-github-username>.github.io`
- **A records**: host `@` → the four GitHub Pages IPs:
  `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`

Confirm the current IPs on GitHub's docs (search "GitHub Pages apex domain"); they're stable but worth verifying. DNS can take up to ~24h.

## Preview locally (optional)

Requires Ruby. Then:

```
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000.
