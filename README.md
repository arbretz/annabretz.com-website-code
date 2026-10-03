# annabretz.com

Anna Bretz's resume site: a single-page static site — plain HTML and CSS, no build step. Hosted on Cloudflare Pages.

## Files

| File | Purpose |
|------|---------|
| `index.html` | All resume content. |
| `styles.css` | Styling (desert palette). Colors are defined at the top. |

## Preview locally

Just double-click `index.html` to open it in your browser.

## Deploy to Cloudflare

1. **Push to GitHub** — create a new repository, then upload these files to the root of it
   (GitHub web: *Add file → Upload files*, or with git:
   `git init && git add . && git commit -m "Initial site" && git branch -M main && git remote add origin https://github.com/<you>/<repo>.git && git push -u origin main`).
2. **Create the Pages project** — in the Cloudflare dashboard go to **Workers & Pages → Create → Pages → Connect to Git**, authorize GitHub, and pick the repository.
3. **Build settings** — Framework preset: **None**. Build command: *(leave empty)*. Build output directory: **`/`**. Click **Save and Deploy**. You'll get a `*.pages.dev` URL in about a minute.
4. **Attach your domain** — open the project → **Custom domains → Set up a custom domain**, enter `annabretz.com` (and optionally `www.annabretz.com`). If the domain's DNS is already on Cloudflare, the record is created automatically; HTTPS is issued within a few minutes.

Every push to `main` redeploys the site automatically.

> Note: Cloudflare occasionally reshuffles this dashboard. If "Create" lands you on the Workers flow, look for the **Pages** tab or a "Looking to deploy Pages?" link on that screen.
